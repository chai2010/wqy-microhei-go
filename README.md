- *赞助 BTC: 1Cbd6oGAUUyBi7X7MaR4np4nTmQZXVgkCW*
- *赞助 ETH: 0x623A3C3a72186A6336C79b18Ac1eD36e1c71A8a6*
- *Go语言付费QQ群: 1055927514*

----

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
