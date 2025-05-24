# Pokie
Pokie 
```php
<?php

require __dir__."/vendor/autoload.php";

$t = microtime(true);

$promiseA = async(function () {
    sleep(1);
    
    return 'Task 1';
});
$promiseB = async(function(){
  sleep(1);
  return 'Task 2';
}); 

$promiseC = async(function () {
    sleep(1);
    
    return 'Task 3';
});
$promiseD = async(function () {
  sleep(1);
  return 'Task 4';
});

// just takes 2 seconds...
[$resA, $resB, $resC, $resD] = await([$promiseA, $promiseB, $promiseC, $promiseD]);

var_dump(microtime(true) - $t);

echo $resA; // Task 1
echo $resB; // Task 2
echo $resC; // Task 3
echo $resC; // Task 4

```
