# Competitive Programming in GO
Go is a powerful language. For my job preparation I am going to learn GO. And for me the best way to learn a language is to practice problem solving. There will be other important things left that's true. But those will not be that much hard to learn.

### Template and FastIO
```go
package main

import (
	"bufio"
	"fmt"
	"os"
)

func solve(in *bufio.Reader, out *bufio.Writer) {
}

func main() {
	in := bufio.NewReader(os.Stdin)
	out := bufio.NewWriter(os.Stdout)
	defer out.Flush()

	var tc int
	fmt.Scan(&tc)
	for t := 0; t < tc; t++ {
		solve(in, out)
	}
}

```

### Reading and Writing

#### Reading inputs
```go
var n,k int
fmt.Fscan(in, &n, &k)
```
#### Declaring variable length array and reading
```go
var ara []int = make([]int, n)
for i := 0; i < n; i++ {
    fmt.Fscan(in, &ara[i])
}
```
#### Output 
```go
res := 0
fmt.Fprintln(out, res)

```
### Sorting
Need to import package `sort`

#### sorting an array of int
```go
var ara []int = make([]int, n)
// populate arary
sort.Slice(a)
```

#### sorting an array of struct or by custom comparator
The custom comparator is weird :/ It uses index. So we can't use function reference like we use in C++. May be we can. But I haven't figured that part out yet. 
```go
type pair struct {
	first  int
	second int
}
var a []pair = make([]pair, n)
sort.Slice(a, func(i, j int) bool {
		return a[i].first > a[j].first
	})
```

### Strings
#### Basic syntaxes
```go
var s1 string = "abcde"
s2 := "abcde" # short form when initialized

len1 := len(s1) # length of string s1
```
#### Taking input
```go
var s string
fmt.Fscan(in,&s)
```
#### ords of character
```go
ord0 := int(s[0]-'a')

```

