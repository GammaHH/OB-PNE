---
title: Eltrombopag
category: 貧血治療劑
tags:
  - 藥理藥化
  - 貧血治療劑
  - TPO
created: 2025-03-01
updated: 2025-04-07 10:32
source:
  - 藥理藥化平安符
Abstract: 藥物個論
sr-due: 2025-05-02
sr-interval: 25
sr-ease: 250
---
#review 

## 🔹 1. 基本資訊
- **藥名（Drug Name）**：Eltrombopag
- **分類（Category）**：貧血治療劑、TPO
- **MOA（Mechanism of Action）**：
?
> [!ERROR] 一句話MOA
>- 屬血小板生成素(Thrombopoietin, TPO) 致效劑 <!--SR:!2025-04-18,11,270-->

## 🔹 2. 相關口訣
?
> [!tip]- 口訣
> - -trom- 對應血小板生成素(thrombopoietin)TPO 
> - -pag（小分子致效劑結尾常見字根） <!--SR:!2025-04-18,11,270-->

## 🔹 3. 特色
#### 🧪 藥理（Pharmacology）
- PO給藥


#### 🧬 藥化（Medicinal Chemistry）
- 不知



#### ⚡副作用（Adverse Effects）
- 不知


## 🔹 4. ADME（藥代動力學）
 不重要
## 🔹 5. 比較、連結

[[貧血單元病症整理]]

##### 同類藥物(1)
?
- [[Romiplostim]] <!--SR:!2025-04-22,15,290-->

##### 類似藥物(1) - 相關性比較高那種
?
- [[Oprelvekin]] <!--SR:!2025-04-08,1,210-->


```dataviewjs
// ---------- 標籤推薦區塊（以列表呈現） ----------
const excludeTags = ["藥理藥化", dv.current().category];
const currentTags = dv.current().tags?.filter(t => !excludeTags.includes(t)) ?? [];

let allCandidates = dv.pages()
  .where(p => p.file?.path?.startsWith("國考/") && p.tags && p.file.name !== dv.current().file.name);


// 先分出 multi 和 single
let multiMatch = [];
let singleMatch = [];

for (let p of allCandidates) {
  const matchCount = currentTags.reduce((acc, tag) => acc + (p.tags.includes(tag) ? 1 : 0), 0);
  if (matchCount >= 2) {
    multiMatch.push(p);
  } else if (matchCount === 1) {
    singleMatch.push(p);
  }
}

// 建立 singleMatch 的分類 group
let singleGroups = {};
for (let p of singleMatch) {
  let matchedTag = currentTags.find(tag => p.tags.includes(tag));
  if (matchedTag) {
    if (!singleGroups[matchedTag]) singleGroups[matchedTag] = [];
    singleGroups[matchedTag].push(p);
  }
}

// 合併總筆數（無重複）
let multiPaths = new Set(multiMatch.map(p => p.file.path));
let totalUnique = new Set([...multiMatch, ...singleMatch].map(p => p.file.path)).size;

dv.header(5, `相關藥物（共 ${totalUnique} 筆）`);

if (multiMatch.length > 0) {
  dv.header(6, `▸ ${currentTags.join("、")}（${multiMatch.length}）`);
  dv.list(
    multiMatch.map(p => {
      const tagsToShow = p.tags.filter(t => !excludeTags.includes(t));
      return `${p.file.link}　${tagsToShow.join("、")}`;
    })
  );
}

// 顯示單一標籤命中分類後的筆記
for (let [tag, pages] of Object.entries(singleGroups)) {
  dv.header(6, `▸ ${tag}（${pages.length}）`);
  dv.list(
    pages.map(p => {
      const tagsToShow = p.tags.filter(t => !excludeTags.includes(t) && t !== tag);
      return `${p.file.link}　${tagsToShow.join("、")}`;
    })
  );
}
if (multiMatch.length === 0 && Object.keys(singleGroups).length === 0) {
  dv.paragraph("沒有找到與本藥物具有相同標籤的其他筆記。");
}


```


-  Eltrombopag藥名拆字(2):: Eltrombopag = -tromb-（對應 TPO，血小板生成）+ -pag（小分子致效劑結尾常見字根） <!--SR:!2025-04-11,4,270-->
- 所屬類別(2)::血小板生成促進劑（Thrombopoietin receptor agonist, TPO-RA）、貧血治療劑、TPO <!--SR:!2025-04-10,3,250-->
- 最大特色::為口服小分子 TPO 受體致效劑，可刺激血小板生成，適用於慢性免疫性血小板低下症（ITP）或某些貧血狀況 <!--SR:!2025-04-10,3,250-->

