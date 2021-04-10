# Go-CapMonster

Go-CapMonster is a Go wrapper used to interact with the [CapMonster](https://capmonster.cloud/en/) API.

Example usage:

```
package main

import (
    "fmt"
    "github.com/mattia-git/go-capmonster"
)

func main() {
    c := &capmonster.Client{APIKey: "your-key-goes-here"}

    key, err := c.SendRecaptcha(
        "http://http.myjino.ru/recaptcha/test-get.php", // url that has the recaptcha
        "6Lc_aCMTAAAAABx7u2W0WPXnVbI_v6ZdbM6rYf16", // the recaptcha key
    )
	if err != nil {
        fmt.Println(err)
	}else{
        fmt.Println(key)
    }    
}

```