#type Error

##类型说明

Error类型用于描述模板转义过程中发生的错误

##示例代码

	type Error struct {
	    // ErrorCode 描述一种错误
	    ErrorCode ErrorCode
	    // Name 是在其中遇到错误模板的名称
	    Name string
	    // Line 是模板中发生错误的行号
	    Line int
	    // Description 是错误的详细说明
	    Description string
	}