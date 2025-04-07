---
title: Argatroban
category: 抗凝血
tags:
  - 藥理藥化
  - 直接thrombin抑制劑
created: 2025-02-25
updated: 2025-04-01 20:11
source:
  - 藥理藥化平安符
Abstract: 藥物個論
sr-due: 2025-04-11
sr-interval: 11
sr-ease: 250
---
#review 
## 🔹 1. 基本資訊
- **藥名（Drug Name）**：Argatroban
- **分類（Category）**：直接thrombin抑制劑
- **MOA（Mechanism of Action）**：
?
> [!ERROR] 小貼士
> 直接抑制 凝血因子II 的活化 <!--SR:!2025-04-01,4,270-->



### 結構
![[Pasted image 20250331214110.png]]


## 🔹 2. 相關比較口訣
?
> [!tip]- 口訣
> - 字中有ba 對IIa 抑制
> - 同[[Dabigatran]]
> - -gatroban = 直接thrombin抑制劑 <!--SR:!2025-04-01,4,270-->

## 🔹 3. 特色
### 🧪 藥理（Pharmacology）

- 治療 HIT
- IV給藥 (因為治療HIT)

### 🧬 藥化（Medicinal Chemistry）
- 無


### ⚡副作用（Adverse Effects）
- 無


## 🔹 4. ADME（藥代動力學）
 無
 
## 🔹 5. 比較、連結
- [[肝素誘導血小板缺乏症(HIT)]]


-  也是直接作用劑(4) [因子II、因子Xa]
?
[[Rivaroxaban]]
[[Argatroban]]
[[Hirudin]]
[[Dabigatran]] <!--SR:!2025-04-03,3,263-->


- 可以治療/給藥方式::HIT ，IV給藥<!--SR:!2025-04-10,10,270-->



```dataviewjs
// ---------- 標籤推薦區塊（以列表呈現） ----------
const excludeTags = ["藥理學","<%- drugCategory %>"];
const currentTags = dv.current().tags?.filter(t => !excludeTags.includes(t)) ?? [];

let tagMatches = dv.pages()
  .where(p => p.tags && p.file.name !== dv.current().file.name)
  .filter(p => p.tags.some(tag => currentTags.includes(tag)));

let tagGroups = {};

for (let tag of currentTags) {
  tagGroups[tag] = tagMatches.filter(p => p.tags.includes(tag));
}

let totalMatched = Object.values(tagGroups).reduce((acc, pages) => acc + pages.length, 0);

if (totalMatched > 0) {
  dv.header(5, `相關藥物（共 ${totalMatched} 筆）`);
  for (let [tag, pages] of Object.entries(tagGroups)) {
    if (pages.length > 0) {
      dv.header(6, `▸ ${tag}（${pages.length}）`);
      dv.list(
        pages.map(p => p.file.link)
      );
    }
  }
} else {
  dv.header(5, "相關藥物（0）");
  dv.paragraph("沒有找到與本藥物具有相同標籤的其他筆記。");
}
```


## 🔹 6. 閃卡區