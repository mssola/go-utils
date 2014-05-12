
# Misc

This package contains random function that I did not where to put. By now
there's only the EnvOrElse function. This function is similar to Python's get
but this one deals with environment variables. An example:

~~~ go
package main

import (
	"fmt"

	"github.com/mssola/go-utils/misc"
)

func main() {
	home := misc.EnvOrElse("HOME", "/home/user")
	fmt.Printf("%v\n", home) // => /home/mssola
	home = misc.EnvOrElse("HOM", "/home/user")
	fmt.Printf("%v\n", home) // => /home/user
}
~~~
