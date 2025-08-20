---
description: Generate Mermaid diagram
allowed-tools: Bash, Read, Grep, LS
---

$ARGUMENTS

為以上提到的內容產生 Mermaid 圖（有關聯則畫在一起、無關聯則分開），用 .md 檔儲存在目前專案的根目錄。

接著使用以下指令驗證 Mermaid 語法正確：

`npx -p @mermaid-js/mermaid-cli mmdc -i mermaid.md -o test.md`

`test.md` 僅供語法驗證使用，最終可以刪除。
