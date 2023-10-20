# https://redis.io/
## How to run in command line:
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
to check:
```
127.0.0.1:6379>quit
Admin@DESKTOP-V6V9F0T MINGW64 /
$redis-cli
127.0.0.1:6379>get k1
"Mariia"
```
to check if the object exists:
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
