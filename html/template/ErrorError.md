#func (e *Error) Error() string

##功能说明
用于返回错误的详细说明

##源码示例

	func (e *Error) Error() string {
		if e.Line != 0 {
			return fmt.Sprintf("html/template:%s:%d: %s", e.Name, e.Line, e.Description)
		} else if e.Name != "" {
			return fmt.Sprintf("html/template:%s: %s", e.Name, e.Description)
		}
		return "html/template: " + e.Description
	}
	