---
title: Tranexamic acid
category: 止血劑
tags:
  - 藥理藥化
  - Antifibrinolytic-agent
  - 止血劑
created: 2025-02-26
updated: 2025-04-01 20:11
source:
  - 藥理藥化平安符
Abstract: 藥物個論
sr-due: 2025-04-16
sr-interval: 15
sr-ease: 250
---
#review 
## 🔹 1. 基本資訊
- **藥名（Drug Name）**：Tranexamic acid
- **分類（Category）**：Antifibrinolytic-agent、止血劑
- **MOA（Mechanism of Action）**：
?
> [!ERROR] 一句話MOA
> - 與==Thrombolytics-agent==相反，阻斷 Plasminogen > Plasmin，造成血栓形成，用於治療出血性疾病 <!--SR:!2025-04-04,3,250-->

### 結構
![[Pasted image 20250331214220.png]]


## 🔹 2. 相關字尾(3)
?
> [!tip]- 口訣
> - 字尾帶有 "acid"，與其分子結構及水溶性有關，這有助於其在血漿和體液中的溶解度增加，該類藥物都是酸類
> -  -trans 結構的異構物
> - -examic = 類似於 ε-aminocaproic acid 的命名風格，表示有 胺基 + 羧酸 結構 <!--SR:!2025-04-04,3,250-->

## 🔹 3. 特色
#### 🧪 藥理（Pharmacology）

- 可以治療::出血性疾病(特別強調)，因為他作用很強 <!--SR:!2025-04-04,3,250-->

#### 🧬 藥化（Medicinal Chemistry）

- 不知

#### ⚡副作用（Adverse Effects）
- 不知


## 🔹 4. ADME（藥代動力學）
 不重要
## 🔹 5. 比較、連結



##### 同類藥物(1)
?
- [[Aminocarprotic acid]] <!--SR:!2025-04-04,3,250-->



```dataviewjs
// ---------- 標籤推薦區塊（以列表呈現） ----------
const excludeTags = ["藥理學"];
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
````

## 🔹 6. 閃卡區
- Tranexamic acid 藥名拆字(2) :: tran- 表示 trans 立體異構結構；-examic 表示類似 ε-aminocaproic acid，具有胺基與羧酸官能基；acid 表示具酸性、提升水溶性 <!--SR:!2025-04-04,3,250-->
- Tranexamic acid 所屬類別(1) :: Antifibrinolytic agent（抗纖溶劑，止血劑） <!--SR:!2025-04-03,2,230-->
- Tranexamic acid 最大特色 :: 阻斷 plasminogen → plasmin，防止血塊溶解，可強力止血，用於出血性疾病 <!--SR:!2025-04-03,2,230-->
