#func JSEscapeString(s string) string

##参数
- s string 需要进行转义的字符串

##返回
- string 转义后的字符串

##功能说明
JSEscapeString返回s转义后的JS文本.

##代码示例

	package main
	
	import (
		"fmt"
		"html/template"
	)
	
	func main() {
	
		s := "<script>alert('xss!')</script>"
	
		fmt.Println(template.JSEscapeString(s))
	
	}
	
输出:	
	`\x3Cscript\x3Ealert(\'xss!\')\x3C/script\x3E`
