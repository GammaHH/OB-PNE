---
title: Romiplostim
category: 貧血治療劑
tags:
  - 藥理藥化
  - 貧血治療劑
  - TPO
  - 基因重組
created: 2025-03-01
updated: 2025-04-07 19:29
source:
  - 藥理藥化平安符
Abstract: 藥物個論
sr-due: 2025-05-07
sr-interval: 30
sr-ease: 270
---
#review 
## 🔹 1. 基本資訊
- **藥名（Drug Name）**：Romiplostim
- **分類（Category）**：貧血治療劑
- **MOA（Mechanism of Action）**：
?
> [!ERROR] 一句話MOA
> - 屬血小板生成素(Thrombopoietin, TPO) 致效劑，基因重組 <!--SR:!2025-03-28,4,270-->


## 🔹 2. 相關口訣(2)
?
> [!tip]- 口訣
> - plo 聯想到 platelets(血小板)
> - -stim 子尾 可能是某種**生成素**

## 🔹 3. 特色
#### 🧪 藥理（Pharmacology）

- SC給藥


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
- [[Eltrombopag]] <!--SR:!2025-03-29,2,230-->

##### 類似藥物(1) - 相關性比較高那種
?
- [[Oprelvekin]] <!--SR:!2025-03-29,2,230-->


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

- Romiplostim 藥名拆字(2) :: -plo 與 platelet（血小板）相關，-stim 表示具刺激或生成作用；整體為一種「刺激血小板生成的生物製劑」
- Romiplostim 所屬類別(2) :: 血小板生成素（TPO）致效劑，用於治療免疫性血小板低下（如 ITP）、貧血治療劑
- Romiplostim 特色(2) :: 類 TPO 作用劑，SC 施打，刺激骨髓產生血小板，為 recombinant fusion 蛋白
