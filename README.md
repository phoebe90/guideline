# Guideline

本份指南會使用到 [RFC 2119][] 的關鍵字，以下列出原文與中文的對照：

| 原文 | 中文 |
|:--------:|:------:|
| MUST | **必須** |
| MUST NOT | **禁止** |
| SHOULD | **建議** |
| SHOULD NOT | **不建議** |
| MAY | **可以** |

如果有要表達 RFC 2119 文件裡的意思時，將會使用**粗體**表示。

## 通用指南

1. 開發流程／模式
2. [Source Repository](/source-repository/README.md) - Git 相關規範：commit message、flow
3. [Documentation](/documentation.md)
4. [Code Review](/code-review.md) - 如何進行 Code Review
5. [Integration](/integration/README.md) - 如何整合，包括如何測試
6. Delivery - 如何交付可用的軟體
7. Deployment - 如何佈署
8. Report - 報告包括什麼

## 實作指南

* Web server
* [API](/implement/api.md)
* Worker
* [Library](/implement/library.md)

## 語言指南

### 共同指南

* Build tools

### 語言細節

* [PHP](/language/php/README.md)
* [Java](/language/java/README.md)
* [JavaScript](/language/javascript/README.md)
* [CSS](/language/css/README.md)

## 如何協作

如有興趣共同編輯此文件，可以參考[這份文件](/CONTRIBUTING.md)。

[RFC 2119]: http://www.ietf.org/rfc/rfc2119.txt
