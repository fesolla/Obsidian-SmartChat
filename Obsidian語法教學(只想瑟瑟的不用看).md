**一、標題 (Headings)**

使用 `#` 符號來定義標題，`#` 的數量決定標題的層級。

```markdown
# 一級標題
## 二級標題
### 三級標題
#### 四級標題
##### 五級標題
###### 六級標題
```

**二、文字樣式 (Text Styles)**

- **粗體 (Bold)**：使用 `**文字**` 或 `__文字__`
    
    ```markdown
    **這是粗體文字**
    __這也是粗體文字__
    ```
    
- **斜體 (Italic)**：使用 `*文字*` 或 `_文字_`
    
    ```markdown
    *這是斜體文字*
    _這也是斜體文字_
    ```
    
- **粗斜體 (Bold and Italic)**：使用 `***文字***` 或 `___文字___`
    
    ```markdown
    ***這是粗斜體文字***
    ___這也是粗斜體文字___
    ```
    
- **刪除線 (Strikethrough)**：使用 `~~文字~~`
    
    ```markdown
    ~~這是刪除線文字~~
    ```
    
- **高亮 (Highlight)**：使用 `==文字==` (Obsidian 特有)
    
    ```markdown
    ==這是高亮文字==
    ```
    
- **行內程式碼 (Inline Code)**：使用 `` `文字` ``
    
    ```markdown
    `這是行內程式碼`
    ```
    

**三、列表 (Lists)**

- **無序列表 (Unordered List)**：使用 `*`、`-` 或 `+`
    
    ```markdown
    * 項目一
    * 項目二
    * 項目三
    
    - 項目一
    - 項目二
    - 項目三
    
    + 項目一
    + 項目二
    + 項目三
    ```
    
- **有序列表 (Ordered List)**：使用數字和 `.`
    
    ```markdown
    1. 項目一
    2. 項目二
    3. 項目三
    ```
    
- **巢狀列表 (Nested List)**：在子列表前加入空格或 Tab
    
    ```markdown
    * 項目一
        * 子項目一
        * 子項目二
    * 項目二
        1. 子項目 1
        2. 子項目 2
    ```
    

**四、連結 (Links)**

- **行內連結 (Inline Link)**：`[連結文字](連結網址)`
    
    ```markdown
    [Google](https://www.google.com)
    ```
    
- **參考連結 (Reference Link)**：
    
    ```markdown
    [連結文字][連結標籤]
    
    [連結標籤]: 連結網址 "連結標題 (可選)"
    ```
    
    例如：
    
    ```markdown
    [Google][google_link]
    
    [google_link]: https://www.google.com "Google 搜尋引擎"
    ```
    
- **內部連結 (Internal Link)**：`[[筆記標題]]` 或 `[[筆記標題#標題]]` (Obsidian 特有)
    
    ```markdown
    [[我的筆記]]
    [[我的筆記#章節標題]]
    ```
    
    - `[[筆記標題]]`：連結到名為 "我的筆記" 的筆記。
    - `[[筆記標題#章節標題]]`：連結到 "我的筆記" 筆記中的 "章節標題" 標題。
- **連結別名 (Link Alias)**：`[[筆記標題|顯示文字]]` (Obsidian 特有)
    
    ```markdown
    [[我的筆記|點擊這裡查看我的筆記]]
    ```
    

**五、圖片 (Images)**

- **行內圖片 (Inline Image)**：`![圖片替代文字](圖片網址)` 或 `![圖片替代文字](圖片路徑)`
    
    ```markdown
    ![Obsidian Logo](https://obsidian.md/images/obsidian-logo-text.png)
    ![本地圖片](images/my_image.jpg)
    ```
    

**六、引用 (Blockquotes)**

使用 `>` 符號。

```markdown
> 這是一段引用文字。
> 可以有多行。
```

**七、程式碼區塊 (Code Blocks)**

使用三個反引號 ````` 包圍程式碼。可以指定程式語言來啟用語法高亮。

````markdown
```javascript
function helloWorld() {
  console.log("Hello, world!");
}
````

````

**八、水平線 (Horizontal Rule)**

使用三個或以上的 `*`、`-` 或 `_`。
```markdown
---
***
___
````

**九、表格 (Tables)**

```markdown
| Header 1 | Header 2 | Header 3 |
| -------- | -------- | -------- |
| Cell 1   | Cell 2   | Cell 3   |
| Cell 4   | Cell 5   | Cell 6   |
```

- `|` 分隔欄位。
- `--------` 定義標題列。 `:` 可以用來對齊文字：
    - `---:` 右對齊
    - `:---` 左對齊
    - `:---:` 居中對齊

**十、任務列表 (Task Lists)**

使用 `[ ]` 或 `[x]` 表示未完成或已完成的任務。

```markdown
- [ ] 未完成的任務
- [x] 已完成的任務
```

**十一、註腳 (Footnotes)**

```markdown
這是一段文字[^1]。

[^1]: 這是註腳的內容。
```

**十二、數學公式 (Math)**

使用 `$` 或 `$$` 包圍 LaTeX 語法。

- **行內公式 (Inline Math)**：`$E=mc^2$`
- **區塊公式 (Block Math)**：
    
    ```markdown
    $$
    \int_0^\infty e^{-x^2} dx = \frac{\sqrt{\pi}}{2}
    $$
    ```
    

**十三、YAML Front Matter (Obsidian 特有)**

在筆記的開頭使用三個 `---` 包圍 YAML 格式的元數據。可以用於定義標籤、別名等。

```yaml
---
tags: [note, example]
aliases: [範例筆記, 示範]
---

這是筆記的內容。
```

**十四、呼叫方塊 (Callouts) (Obsidian 特有)**

使用 `> [!type] title` 建立呼叫方塊，`type` 可以是 `note`、`tip`、`warning`、`danger`、`info`、`success`、`question`、`failure`、`bug`、`example`、`quote`。

```markdown
> [!NOTE]
> 這是一個提示框。
> 裡面可以包含多行文字。
```

**十五、嵌入筆記 (Embedding Notes) (Obsidian 特有)**

使用 `![[筆記標題]]` 或 `![[筆記標題#標題]]` 將其他筆記嵌入到當前筆記中。

```markdown
![[我的筆記]]
![[我的筆記#章節標題]]
```

**十六、標籤 (Tags) (Obsidian 特有)**

使用 `#標籤名稱` 來添加標籤。

```markdown
這是一個 #範例筆記，包含 #Obsidian 和 #Markdown 標籤。
```