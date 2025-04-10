---
title: Filgrastim
category: 貧血治療劑
tags:
  - 藥理藥化
  - 貧血治療劑
  - G-CSF
  - 重組蛋白
created: 2025-03-01
updated: 2025-04-09 12:59
source:
  - 藥理藥化平安符
Abstract: 藥物個論
sr-due: 2025-04-16
sr-interval: 7
sr-ease: 250
---
#review

## 🔹 1. 基本資訊
- **藥名（Drug Name）**：Filgrastim
- **分類（Category）**：貧血治療劑、重組蛋白
- **MOA（Mechanism of Action）**：
?
> [!ERROR] 一句話MOA
> - 即**G-CSF**白血球生長激素 <!--SR:!2025-03-31,3,250-->

## 🔹 2. 相關字尾/口訣(2)
?
> [!tip]- 口訣
> - -stim 子尾 可能是某種生成素 
> - -Filg 會讓人想到抗血栓類，但他其實不是 <!--SR:!2025-04-08,11,270-->

## 🔹 3. 特色
#### 🧪 藥理（Pharmacology）

- 為白血球生長激素

#### 🧬 藥化（Medicinal Chemistry）
- 不知


#### ⚡副作用（Adverse Effects）
- 不知


## 🔹 4. ADME（藥代動力學）
 - 不重要
## 🔹 5. 比較、連結

[[貧血單元病症整理]]

##### 藥劑學
- **PEG 化 G-CSF**：在 **Filgrastim** 的 N 末端添加 20kDa 的單甲氧基聚乙二醇（PEG），以延長其半衰期。
- **GM-CSF**：可稀釋於 0.9% NaCl 注射液中（用於靜脈輸注），濃度低時需事先添加 0.1% **白蛋白**至生理鹽水中。

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

- Filgrastim 藥名拆字(2):: Fil-（音譯字根，並無明確語源，讓人想到抗血栓類，但他其實不是）+ -grastim（來自 "granulocyte stimulating factor" 白血球生成素的縮寫）
- 所屬類別(2):: 白血球生長激素（G-CSF）/貧血治療劑
- 最大特色:: 主要用於刺激白血球生成，用於治療由化療引起的白血球減少症，並且是 G-CSF 的重組形式

