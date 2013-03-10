#func JSEscape(w io.Writer, b []byte)

##参数
- w io.Writer 	写入的Writer
- b []byte 		需要进行转义的内容

##功能说明
JSEscape用于将b转义后的JavaScript文本写入到w中.

##代码示例

	package main
	
	import (
		"bytes"
		"fmt"
		"html/template"
	)
	
	func main() {
	
		w := bytes.NewBufferString("")
	
		b := []byte("<script>alert('xss!')</script>")
	
		template.JSEscape(w, b)
	
		fmt.Println(w)
	
	}
	
输出:	
	`\x3Cscript\x3Ealert(\'xss!\')\x3C/script\x3E`
