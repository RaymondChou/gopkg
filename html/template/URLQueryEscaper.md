#func URLQueryEscaper(args ...interface{}) string

##参数
- args 多个输入参数

##返回
- string 转义后的字符串

##功能说明
URLQueryEscaper 返回多个参数一起转义后的字符串

##代码示例

	package main
	
	import (
		"fmt"
		"html/template"
	)
	
	func main() {
	
		a := "http://"
	
		b := "www.github.com/"
	
		c := "RaymondChou/"
	
		fmt.Println(template.URLQueryEscaper(a, b, c))
	
	}
	
输出:	
`http%3A%2F%2Fwww.github.com%2FRaymondChou%2F`
