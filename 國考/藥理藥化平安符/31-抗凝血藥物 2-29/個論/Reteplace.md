---
title: Reteplace
category: 溶血栓
tags:
  - 藥理藥化
  - Thrombolytics-agent
  - 重組蛋白
  - 溶血栓
created: 2025-02-26
updated: 2025-04-10 08:47
source:
  - 藥理藥化平安符
Abstract: 藥物個論
sr-due: 2025-05-09
sr-interval: 30
sr-ease: 270
---
#review 
## 🔹 1. 基本資訊
- **藥名（Drug Name）**：Reteplace
- **分類（Category）**：Thrombolytics-agent、抗凝血劑、r-tPA
- **MOA（Mechanism of Action）**：
?
> [!ERROR] 一句話MOA
> - 促進 Plasminogen > Plasmin，溶解血栓 <!--SR:!2025-04-13,4,290-->

???


## 🔹 2. 相關口訣(2)
?
> [!tip]- 口訣
> - -place 即為rRNA的 Thrombolytics-agent
> - -ase 大蛋白藥物 <!--SR:!2025-04-13,4,290-->

???

## 🔹 3. 特色
#### 🧪 藥理（Pharmacology）

- 無

#### 🧬 藥化（Medicinal Chemistry）


#### ⚡副作用（Adverse Effects）
- 不知


## 🔹 4. ADME（藥代動力學）

- 在體內半衰期較同類長(14~18 min)
## 🔹 5. 比較、連結
###### Thrombolytics-agent半衰期比較
[[Alteplase]] < [[Reteplace]]

##### 同類藥物(1)
?
- [[Streptokinase]]

##### 類似藥物(1) - 相關性比較高那種
?
- [[Alteplase]]


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


- Reteplace 藥名拆字(2):: Retep-（來自 recombinant tissue plasminogen activator，r-tPA）+ -place（蛋白相關的藥物結尾） <!--SR:!2025-04-12,3,270-->
- 所屬類別(2):: 溶栓劑（Thrombolytics-agent）／抗凝血劑 <!--SR:!2025-04-13,4,290-->
- 特色(2):: 用於急性心肌梗塞和肺栓塞等情況的溶栓，作用機制是促進 Plasminogen 轉化為 Plasmin (**動脈溶栓**)，具有較長的半衰期（14-18 分鐘），相比其他同類藥物，如 Alteplase，效果持久 <!--SR:!2025-04-13,4,290-->
