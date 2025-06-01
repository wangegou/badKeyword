# badKeyword

一个用于敏感词匹配的 Go 语言库，基于 Aho-Corasick 算法实现高效关键词检测。

---

#### 目前收录敏感词数量：45822 个

## 安装

使用 Go Modules，直接通过以下命令安装指定版本：

```bash
go get github.com/wangegou/badKeyword@v1.0.0
```

## 示例

```
package main

import (
	"time"

	badKeywords "github.com/wangegou/badKeyword"
)
func main() {
	text := "待检测字符串"
	if badKeywords.Check_Keywords(text ) {
		// println("文本包含敏感词！")
	} else {
		// println("文本不包含敏感词。")
	}

}
```

功能特点

- 高效的 Aho-Corasick 多模式匹配算法
- 支持数万关键词规模，自动分组匹配提升性能
- 简单易用的接口，快速集成到项目中
- 可扩展自定义关键词库

使用建议

- 根据业务需求合理维护关键词库，定期更新
- 大规模关键词建议分批加载，提升匹配效率
- 如果匹配性能瓶颈明显，可结合布隆过滤器做预过滤

贡献指南
欢迎提交 Issues 和 Pull Requests，帮助完善项目。

许可证
本项目采用 MIT 许可证，详见 LICENSE 文件。

联系方式
如有问题或建议，请在 GitHub 仓库提交 Issue，或联系项目维护者。

---
