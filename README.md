```go
package main

import "fmt"

func isPrime(n int) bool {
	if n <= 1 {
		return false
	}
	for i := 2; i*i <= n; i++ {
		if n%i == 0 {
			return false
		}
	}
	return true
}

func main() {
	primeCount := 0
	num := 2

	for primeCount < 10 {
		if isPrime(num) {
			fmt.Printf("%d ", num)
			primeCount++
		}
		num++
	}
}
```
