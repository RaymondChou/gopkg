#func JSEscaper(args ...interface{}) string

##参数
- args 多个输入参数

##返回
- string 转义后的字符串

##功能说明
JSEscaper 返回多个参数一起转义后的字符串

##代码示例

	package main
	
	import (
		"fmt"
		"html/template"
	)
	
	func main() {
	
		a := "<script>alert('xss!')</script>"
	
		b := "<h1>Raymond</h1>"
	
		c := "<h2>Chou</h2>"
	
		fmt.Println(template.JSEscaper(a, b, c))
	
	}
	
输出:	
`\x3Cscript\x3Ealert(\'xss!\')\x3C/script\x3E\x3Ch1\x3ERaymond\x3C/h1\x3E\x3Ch2\x3EChou\x3C/h2\x3E`
