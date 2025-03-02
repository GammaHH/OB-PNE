---
updated: 2025-02-25 22:57
---
## 📝 最近更新的筆記
```dataview
TABLE file.mtime AS "最後修改時間"
FROM ""
SORT file.mtime DESC
LIMIT 5

```



```dataviewjs
let notes = dv.pages('"工作日誌"') // 指定資料夾
    .where(p => p.file.tasks.some(t => !t.completed)) // 只選擇有未完成待辦事項的筆記
    .sort(p => p.file.mtime, "desc"); // 按修改時間排序

if (notes.length > 0) {
    let latestNote = notes[0]; // 取得最新的筆記
    dv.header(2, `📌 最新工作事項`); 
    
    // 顯示筆記的 [[]] 連結，點擊可編輯
    dv.paragraph(`🔗 [${latestNote.file.name}](${latestNote.file.path})`);
    
    // 嵌入筆記內容
    dv.paragraph(`![[${latestNote.file.name}]]`);
} else {
    dv.paragraph("📭 沒有找到含有未完成待辦事項的工作日誌");
}
```


## 🔍 搜尋資料庫
```dataviewjs
// **創建 UI 容器**
let container = dv.el("div", "");
container.style.marginBottom = "10px";

// **建立搜尋輸入框**
let input = document.createElement("input");
input.type = "text";
input.placeholder = "🔍 搜尋筆記標題...";
input.style = `
    width: 100%;
    max-width: 800px;
    padding: 8px;
    font-size: 16px;
    border: 1px solid var(--background-modifier-border);
    border-radius: 5px;
    background-color: var(--background-primary);
    color: var(--text-normal);
`;
container.appendChild(input);

// **讀取 Obsidian 內所有筆記，並取得唯一的「單層」資料夾名稱**
let allNotes = dv.pages();
let uniqueFolders = [...new Set(allNotes.map(n => n.file.folder.split("/")[0]))].filter(f => f);

// **建立範圍選擇（下拉選單）**
let folderSelect = document.createElement("select");
folderSelect.innerHTML = `<option value="">📂 全部範圍</option>`; // 預設顯示 "全部範圍"

// **填充下拉選單**
uniqueFolders.forEach(folder => {
    let option = document.createElement("option");
    option.value = folder;
    option.textContent = folder;
    folderSelect.appendChild(option);
});

folderSelect.style = "margin-left: 10px; padding: 5px;";
container.appendChild(folderSelect);

// **建立顯示搜尋結果的區塊**
let results = dv.el("div", "");
container.appendChild(results);

// **搜尋函式**
function performSearch() {
    let query = input.value.trim().toLowerCase();
    let selectedFolder = folderSelect.value; // 獲取選擇的資料夾範圍

    results.innerHTML = ""; // 清空舊的搜尋結果

    // **如果搜尋框為空，不顯示結果**
    if (query === "") return;

    // 根據選擇的範圍過濾筆記
    let filteredNotes = dv.pages(selectedFolder ? `"${selectedFolder}"` : "")
        .where(p => p.file.name.toLowerCase().includes(query));

    for (let note of filteredNotes) {
        let containerItem = document.createElement("div");
        containerItem.style = `
            border: 1px solid var(--background-modifier-border);
            padding: 8px;
            margin-bottom: 5px;
            border-radius: 5px;
            background-color: var(--background-secondary);
            color: var(--text-normal);
        `;

        let link = document.createElement("a");
        link.href = note.file.link;
        link.target = "_blank";
        link.style = "font-weight: bold; text-decoration: none; color: var(--text-accent);";
        link.textContent = note.file.name;

        let summary = document.createElement("p");
        summary.style = "color: var(--text-muted); font-size: 14px;";
        summary.textContent = note.Abstract ? "摘要：" + note.Abstract : "（無摘要）";

        containerItem.appendChild(link);
        containerItem.appendChild(summary);
        results.appendChild(containerItem);
    }
}

// **監聽搜尋框與範圍選擇變更**
input.addEventListener("input", performSearch);
folderSelect.addEventListener("change", performSearch);

```


