---
title: Erythropoietin
category: 貧血治療劑
tags:
  - 藥理藥化
  - 貧血治療劑
  - EPO
  - 重組蛋白
created: 2025-03-01
updated: 2025-04-10 09:09
source:
  - 藥理藥化平安符
Abstract: 藥物個論
sr-due: 2025-05-10
sr-interval: 30
sr-ease: 270
---
#GEN5 
## 🔹 1. 基本資訊
- **藥名（Drug Name）**：Erythropoietin
- **分類（Category）**：貧血治療劑、重組蛋白
- **MOA（Mechanism of Action）**：
?
> [!ERROR] 一句話MOA
> - 刺激骨髓中的 erythroid progenitors 增加紅血球產生
- 又稱 EPO <!--SR:!2025-04-14,4,290-->

???

## 🔹 2. 相關口訣(2)
?
> [!tip] 口訣
> - -thro = thrombin(凝血酶) 
> - -Ery = 紅 <!--SR:!2025-04-14,4,290-->

???

## 🔹 3. 特色
#### 🧪 藥理（Pharmacology）

- 由身體製造，又稱 EPO
- 用於 終末期腎病
###### 其他
> 講義
- 一種 34–39 kDa 的糖蛋白，是第一種被分離出來的人類造血生長因子。
- 內源性 EPO 主要由腎臟產生，在低氧環境下促進 紅血球生成（erythropoiesis）。
>藥理 期中重點
- 用於 **終末期腎病（End-stage renal disease, ESRD）** 引起的 貧血
- 活化 JAK/STAT 路徑

#### 🧬 藥化（Medicinal Chemistry）
- 無


#### ⚡副作用（Adverse Effects）
- 高血壓、血栓 因為造成滲透壓改變


## 🔹 4. ADME（藥代動力學）
 不重要
## 🔹 5. 比較、連結

[[貧血單元病症整理]]


```dataviewjs
// ---------- 標籤推薦區塊（以列表呈現） ----------

// 排除標籤（藥理藥化 + 當前 category）
const excludeTags = ["藥理藥化", dv.current().category];

// 擷取當前筆記的有效標籤（排除上面兩項）
const currentTags = dv.current().tags?.filter(t => !excludeTags.includes(t)) ?? [];

// 💡 顯示用標籤：dash 改為空格（預先處理好）
const displayTag = t => t.replace(/-/g, " ");
const displayTags = currentTags.map(displayTag);

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
let totalUnique = new Set([...multiMatch, ...singleMatch].map(p => p.file.path)).size;

dv.header(5, `相關藥物（共 ${totalUnique} 筆）`);

// 🟦 多標籤命中的區塊
if (multiMatch.length > 0) {
  dv.header(6, `▸ ${displayTags.join("、")}（${multiMatch.length}）`);
  dv.list(
    multiMatch.map(p => {
      const tagsToShow = p.tags
        .filter(t => !excludeTags.includes(t))
        .map(displayTag);
      return `${p.file.link}　${tagsToShow.join("、")}`;
    })
  );
}

// 🟩 單一標籤命中的區塊（依照該標籤分類）
for (let [tag, pages] of Object.entries(singleGroups)) {
  const display = displayTag(tag);
  dv.header(6, `▸ ${display}（${pages.length}）`);
  dv.list(
    pages.map(p => {
      const tagsToShow = p.tags
        .filter(t => !excludeTags.includes(t) && t !== tag)
        .map(displayTag);
      return `${p.file.link}　${tagsToShow.join("、")}`;
    })
  );
}

// 🔕 無結果時提醒
if (multiMatch.length === 0 && Object.keys(singleGroups).length === 0) {
  dv.paragraph("沒有找到與本藥物具有相同標籤的其他筆記。");
}

```



- Erythropoietin 藥名拆字(2):: Erythro-（來自 erythrocyte，紅血球）+ -poietin（表示生成素） <!--SR:!2025-04-14,4,290-->
- Erythropoietin 所屬類別(3):: *貧血治療劑*、重組藥物、紅血球生成素（TPO） <!--SR:!2025-04-13,3,270-->
- Erythropoietin 特色(3):: TPO，用於治療因終末期腎病（ESRD）引起的貧血，並能激活 JAK/STAT 路徑 <!--SR:!2025-04-13,3,270-->
