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

## Find even numbers from array 

```
<?php

$arr = [1, 2, 3, 4, 5, 6, 7,8 , 9];

$even = array_filter($arr, fn($n) => $n % 2 == 0);
print_r($even);

// Output
/*
(
    [1] => 2
    [3] => 4
    [5] => 6
    [7] => 8
)
*/
?>
```

## Find HCF of two numbers

```
<?php
// Recursive function to calculate HCF
function findHCF($a, $b) {
    if ($b == 0) {
        return $a;
    }
    return findHCF($b, $a % $b);
}

// Example usage
$num1 = 56;
$num2 = 98;

$hcf = findHCF($num1, $num2);

echo "The HCF of $num1 and $num2 is: $hcf";
?>
// Output The HCF of 56 and 98 is: 14
```

### Euclidean alogorithm

```
<?php
// Function to calculate HCF using Euclidean algorithm
function findHCF($a, $b) {
    while ($b != 0) {
        $temp = $b;
        $b = $a % $b;
        $a = $temp;
    }
    return $a;
}

// Example usage
$num1 = 56;
$num2 = 98;

$hcf = findHCF($num1, $num2);

echo "The HCF of $num1 and $num2 is: $hcf";
?>
```


