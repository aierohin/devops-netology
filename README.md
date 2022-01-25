# Домашнее задание к занятию "7.5. Основы golang"  
  
## Обязательные задания 

Задание 3.1  

```
package main

import "fmt"

func main() {
	var input float64
	input = 5
	output := input * 0.3048

	fmt.Println(output)
}
```
Задание 3.2  

```
package main

import "fmt"

func main() {
	x := []int{48, 96, 86, 68, 57, 82, 63, 70, 37, 34, 83, 27, 19, 97, 9, 17}
	min := x[0]
	for _, v := range x {
		if v < min {
			min = v
		}
	}
	fmt.Println(min)
}
```

Задание 3.3  

```
package main

import "fmt"

func main() {
	for i := 1; i <= 100; i++ {
		if i%3 == 0 {
			fmt.Println(i)
		}

	}

}
```
