---
title: Ticlopidine
category: 抗血小板凝集
tags:
  - 藥理藥化
  - 不可逆P2Y12拮抗劑
created: 2025-02-25
updated: 2025-04-07 10:38
source:
  - 藥理藥化平安符
Abstract: 藥物個論
sr-due: 2025-04-27
sr-interval: 20
sr-ease: 250
---
#review 

## 🔹 1. 基本資訊
- **藥名（Drug Name）**：Ticlopidine
- **分類（Category）**：不可逆P2Y12拮抗劑
- **MOA（Mechanism of Action）**：
?
> [!ERROR] 一句話MOA
> - 不可逆的抑制血小板上的 ADP 接受器 <!--SR:!2025-04-18,11,270-->

### 結構
![[Pasted image 20250328085609.png]]


## 🔹 2. 相關藥名解析(2)
?
> [!tip] 口訣
> - -clo = 可能來自 chlorine + piperidine 的縮合，即具有 Cl 取代
> - -pidine = 明顯的 N 雜環（pyridine 類結構） <!--SR:!2025-04-18,11,270-->

## 🔹 3. 特色
### 🧪 藥理（Pharmacology）
- 就是MOA


### 🧬 藥化（Medicinal Chemistry）

- 該類藥物均有結構骨架為:: Thienopyridine ，硫雜環看不出來，這是不可逆 P2Y12 藥物所共通 <!--SR:!2025-04-18,11,270-->

### ⚡副作用（Adverse Effects） - 知道就好 (2)
?
- 較多AEs，比較老的藥
- 顆粒型白血球缺乏症
- 再生不良性貧血 <!--SR:!2025-04-18,11,270-->


## 🔹 4. ADME（藥代動力學）
 不重要
## 🔹 5. 比較、連結

##### 同類藥物(2)
?
- 具有共通結構 Thienopyridine
- [[Prasugrel]]
- [[Ticagrelor]] - 可逆的P2Y12拮抗劑 <!--SR:!2025-04-09,2,250-->

##### 類似藥物(1) - 相關性比較高那種
?
- [[Clopidogrel]] <!--SR:!2025-04-18,11,270-->




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

- Ticlopidine 藥名拆字:: Ticlopidine = -clo-（可能與 Cl 取代基有關）+ -pidine（pyridine 類含氮雜環結構） <!--SR:!2025-04-11,4,274-->
- 所屬類別(2)::不可逆 P2Y12 抑制劑（Thienopyridine 類抗血小板藥物） <!--SR:!2025-04-08,1,234-->
- 最大特色::具 Thienopyridine 結構，作用不可逆，為早期 P2Y12 抑制劑之一，但副作用較多（如顆粒性白血球缺乏與再生不良性貧血），已多被 Clopidogrel 或更新藥物取代 <!--SR:!2025-04-11,4,274-->


