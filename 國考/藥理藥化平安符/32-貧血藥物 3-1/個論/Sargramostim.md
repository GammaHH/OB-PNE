---
title: Sargramostim
category: 貧血治療劑
tags:
  - 藥理藥化
  - 貧血治療劑
  - GM-CSF
created: 2025-03-01
updated: 2025-04-09 15:33
source:
  - 藥理藥化平安符
Abstract: 藥物個論
sr-due: 2025-05-09
sr-interval: 30
sr-ease: 290
---
#review 

## 🔹 1. 基本資訊
- **藥名（Drug Name）**：Sargramostim
- **分類（Category）**：貧血治療劑、GM-CSF
- **MOA（Mechanism of Action）**：
?
> [!ERROR] 一句話MOA
> - 即白血球生長激素 <!--SR:!2025-04-13,4,282--> 

???

## 🔹 2. 相關口訣/字尾(3)
?
> [!tip]- 口訣
> - -stim 子尾 可能是某種**生成素**
> - 字頭音譯"傻瓜"，可以聯想到 GM(Game manager) 都是傻瓜！ 
> - -gramo-（來自 granulocyte，表示粒細胞） <!--SR:!2025-04-13,4,282-->

???

## 🔹 3. 特色
#### 🧪 藥理（Pharmacology）


- 屬於 Granulocyte-macrophage colony-stimulating factor(GM-CSF)

#### 🧬 藥化（Medicinal Chemistry）
- 不知


#### ⚡副作用（Adverse Effects）
- 不知


## 🔹 4. ADME（藥代動力學）
 不重要
## 🔹 5. 比較、連結

[[貧血單元病症整理]]


##### 藥劑學
- **GM-CSF**：可稀釋於 0.9% NaCl 注射液中（用於靜脈輸注），濃度低時需事先添加 ==0.1% **白蛋白**==至生理鹽水中。 <!--SR:!2025-04-23,14,290-->

???

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

- Sargramostim藥名拆字(2)::-gramo-（來自 granulocyte，表示粒細胞）+ -stim（表示刺激、生成素） <!--SR:!2025-04-13,4,282-->
- Sargramostim所屬類別(2)::白血球生長激素（GM-CSF，Granulocyte-macrophage colony-stimulating factor）、貧血治療劑 <!--SR:!2025-04-13,4,282-->
