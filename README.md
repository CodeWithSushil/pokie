# Pokie
Pokie 
```php

require __dir__."/vendor/autoload.php";

$promiseA = async(function () {
    sleep(2);
    
    return 'Task 1';
});
$promiseB = async(function(){
  sleep(2);
  return 'Task 2';
});

// just takes 2 seconds...
[$resA, $resB] = await([$promiseA, $promiseB]);

echo $resA; // Task 1
echo $resB; // Task 2

```

## Android (Termux)
if you are a `Android` user, its means you are geting error, so i am fixed that problem for you so follow this file changes in `vendor/pokio/src/Runtime/Fork
/IPC.php`:
```php
43 

117 $lib = PHP_OS_FAMILY === 'Darwin' ? 'libc.dylib' : 'libc.so'; // befour libc.so.6
```
