# https://redis.io/
## How to run Redis in command line:
```
Admin@DESKTOP-V6V9F0T MINGW64 /
$ redis-cli
127.0.0.1:6379>
```
6379 - Default port
## How to close Redis
```
127.0.0.1:6379>quit
Admin@DESKTOP-V6V9F0T MINGW64 /
$
```
### Redis is a Key-Value storage. 
It is neccessary to input "key" and "value". For example there is a login flow. Tokens of users will be stored in Redis.  And we must check how is implemented the mechanizm of deleting or updating of token burning counter. As a testers we must understand what to do to check how tokens are putting in database, they exist there or not, how long it will live unting it will be burned. If we update user request will token burning counter also be updated or not.
### Creating object
+ k1 - name of the object
+ "Mariia" is the value of the object
```
127.0.0.1:6379>set k1 "Mariia"
OK
127.0.0.1:6379>
```
### Show the content of object
```
127.0.0.1:6379>get k1
"Mariia"
127.0.0.1:6379>
```
To check:
```
127.0.0.1:6379>quit
Admin@DESKTOP-V6V9F0T MINGW64 /
$redis-cli
127.0.0.1:6379>get k1
"Mariia"
```
### To check if the object exists:
```
127.0.0.1:6379>exists k1
(integer) 1
```
"1" means "exists"
```
127.0.0.1:6379>exists kk1
(integer) 0
```
"0" means "not exists"

If we ask to show not existing object we will have "nil":
```
127.0.0.1:6379>get kk1
(nil)
```
### To delete all from database:
```
127.0.0.1:6379>flushall
OK
```
### Assigning lifetime to object:
Inputing the value and lifetime to object:

!!!Inputing some value: all values will be of  string type!!!

`ex` - lifetime in seconds, `px` - lifetime in milliseconds
```
127.0.0.1:6379>set k1 222 ex 60
OK
127.0.0.1:6379>
```
To see left time for the object we use `ttl` - time to live - command
```
127.0.0.1:6379>ttl k1
(integer) 51
127.0.0.1:6379>
```
!!! positive integer for `ttl` command means the object exists for example
```
127.0.0.1:6379>ttl k1
(integer) 51
127.0.0.1:6379>
```
negative integer for `ttl` command means the object doesn't exist in the database for example
```
127.0.0.1:6379>ttl k1
(integer) -2
127.0.0.1:6379>
```
To update existing burning counter for the existing object (real mechanizm of updating login token when user is away from the app and then come back and try to login after 10 minutes for example):
```
127.0.0.1:6379>setex k1 120 333
OK
127.0.0.1:6379>ttl k1
(integer) 116
127.0.0.1:6379>
```
first digit is lifetime , second digit is the value.
Time of expiring of the object:
```
127.0.0.1:6379>expire k1 120 xx
(integer)1
127.0.0.1:6379>ttl k1
(integer) 118
```
!!! "xx" is added when the timer for the object is already exists. (or you can left without "xx")
If the timer for the object was not added then to add it you do:
```
127.0.0.1:6379>set k1 222
OK
127.0.0.1:6379>expire k2 180 nx
(integer) 1
127.0.0.1:6379>ttl k2
(integer) 175
127.0.0.1:6379>
```
As a tester you need to check if the token exists ( command `exists`) and its lifetime (`ttl`) and how it is expiring.
### How large data is stored in Redis Database





