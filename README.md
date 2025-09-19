# php-samples

## Find a factorial of a number

```
<?php
function findFactorial($n) {
   $factorial= 1;
    for ($i=1; $i<=$n; $i++) {
        $factorial *= $i;
    }
    return $factorial;
}
echo findFactorial(6) . "\n"; // Output: 720
?>
```

## Reverse a string

```
<?php
function reverseString($string) {
    $reverseString = '';
    for ($i=strlen($string) - 1; $i>=0; $i--) {
        $reverseString .= $string[$i];
    }
    return $reverseString;
}

echo reverseString('Shailesh') . "\n"; // // Output: hseliahS
<?php
```

## Find prime numbers

```
<?php
function primesUpTo($n) {
    $primes = [];
    for ($i = 2; $i <= $n; $i++) {
        $isPrime = true;
        for ($j = 2; $j <= sqrt($i); $j++) {
            if ($i % $j == 0) {
                $isPrime = false;
                break;
            }
        }
        if ($isPrime) $primes[] = $i;
    }
    return $primes;
}

print_r(primesUpTo(10));
// Output:
Array
(
    [0] => 2
    [1] => 3
    [2] => 5
    [3] => 7
)
?>
```
