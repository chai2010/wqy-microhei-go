# Go语言文泉驿微米黑字体

```go
package main

import (
	"fmt"
	"log"
	"net/http"

	"github.com/chai2010/wqy-microhei-go"
)

func main() {
	http.HandleFunc("/", func(w http.ResponseWriter, r *http.Request) {
		fmt.Fprint(w, wqy_microhei.Version)
	})
	http.HandleFunc("/data", func(w http.ResponseWriter, r *http.Request) {
		fmt.Fprint(w, wqy_microhei.FontData)
	})

	log.Fatal(http.ListenAndServe(":8080", nil))
}
```
