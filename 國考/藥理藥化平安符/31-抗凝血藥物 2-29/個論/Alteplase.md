---
title: Alteplase
category: 溶血栓
tags:
  - 藥理藥化
  - Thrombolytics-agent
  - 溶血栓
  - 蛋白藥物
created: 2025-02-26
updated: 2025-04-10 08:54
source:
  - 藥理藥化平安符
Abstract: 藥物個論
sr-due: 2025-05-10
sr-interval: 30
sr-ease: 310
---
#review #GEN5 

## 🔹 1. 基本資訊
- **藥名（Drug Name）**：Alteplase (t-PA)
- **分類（Category）**： 抗凝血劑、Thrombolytics-agent
- **MOA（Mechanism of Action）**：
?
> [!ERROR] 一句話MOA
> - 促進 Plasminogen > Plasmin，溶解血栓，又稱為 t-PA <!--SR:!2025-04-26,16,310-->

???


## 🔹 2. 相關口訣(3)
?
> [!tip] 口訣
> - -place 即為rRNA的 Thrombolytics-agent 
> - -ase、-in 同時也是蛋白藥物的意思
> - **蛋白質均較少作為 inhibitor** <!--SR:!2025-04-23,13,290-->

???

## 🔹 3. 特色
#### 🧪 藥理（Pharmacology）

- 又稱為 t-PA 為體內可產生大分子蛋白

#### 🧬 藥化（Medicinal Chemistry）

- 在體內相比同類==半衰期最短==，因為他是自體產生的 <!--SR:!2025-04-13,3,250-->
???
#### ⚡副作用（Adverse Effects）
- 不知

???


## 🔹 4. ADME（藥代動力學）
 不重要
## 🔹 5. 比較、連結

###### Thrombolytics-agent半衰期比較
[[Alteplase]] < [[Reteplace]]

##### 藥劑學
- **Alteplase (Activase)**
    - 冷凍乾燥粉末，無菌注射用水（不含防腐劑）為稀釋劑，需臨用時製備。


##### 類似藥物(1) - 相關性比較高那種
?
- [[Reteplace]] <!--SR:!2025-04-14,4,280-->

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

- Alteplase 藥名拆字(1):: -plase（來自 "plasminogen" 轉化為 "plasmin" 的過程，表示溶解血栓的作用） <!--SR:!2025-04-14,4,280-->
- Alteplase 所屬類別(2):: 溶栓劑（Thrombolytics-agent）、抗凝血劑 <!--SR:!2025-04-14,4,280-->
- Alteplase 特色(3):: 為重組型 **t-PA**，促進 Plasminogen 轉化為 Plasmin，用於急性心肌梗塞、肺栓塞(靜脈)等**血栓**疾病，**半衰期較短**（相較同類藥物） <!--SR:!2025-04-14,4,280-->
