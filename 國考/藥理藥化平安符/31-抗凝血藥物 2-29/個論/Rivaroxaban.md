---
title: Rivaroxaban
category: 直接Xa抑制劑
tags:
  - 藥理藥化
  - 直接Xa抑制劑
created: 2025-02-25
updated: 2025-04-09 21:08
source:
  - 藥理藥化平安符
Abstract: 藥物個論
sr-due: 2025-05-09
sr-interval: 30
sr-ease: 270
---
#GEN5 #review 
## 🔹 1. 基本資訊
- **藥名（Drug Name）**：Rivaroxaban
- **分類（Category）**：直接Xa抑制劑
- **MOA（Mechanism of Action）**：
?
> [!ERROR] 一句話MOA
> - 直接抑制Xa，阻斷共通[[凝血路徑]] <!--SR:!2025-04-19,10,270-->

???

### 結構
#需要結構

## 🔹 2. 相關口訣
?
> [!tip]- 口訣
> - 找字中含有 Xa-ban 的 <!--SR:!2025-04-19,10,270-->

???

## 🔹 3. 特色
### 🧪 藥理（Pharmacology）

- 解毒劑為:: Andexanet alfa <!--SR:!2025-04-13,4,290-->

### 🧬 藥化（Medicinal Chemistry）

- NOACs 代表藥物有(4):: [[Dabigatran]]、Rivaroxaban、Apixaban、Edoxaban <!--SR:!2025-04-13,4,290-->

### ⚡副作用（Adverse Effects）
- 不知


## 🔹 4. ADME（藥代動力學）
 - 不重要
## 🔹 5. 比較、連結

[[怠辦連結]]



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


- Rivaroxaban 藥名拆字(1):: -xaban（來自 "xa" 表示直接抑制Xa，"ban" 表示抑制作用） <!--SR:!2025-04-13,4,290-->
- Rivaroxaban 所屬類別(2):: 直接Xa抑制劑（Direct Xa Inhibitor）、NOAC（新型口服抗凝血劑） <!--SR:!2025-04-13,4,290-->
- Rivaroxaban 特色(3):: 直接**抑制Xa凝血因子**，阻斷共通凝血路徑，廣泛用於預防和治療深**靜脈血栓**，**解毒劑為 Andexanet alfa** <!--SR:!2025-04-13,4,290-->
