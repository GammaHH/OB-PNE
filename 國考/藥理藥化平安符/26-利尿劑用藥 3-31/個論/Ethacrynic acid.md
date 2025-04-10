---
category: 利尿劑
tags:
  - 藥理藥化
  - Loop-diuretics
  - Phenoxyacetic-acid
created: 2025-03-30
updated: 2025-04-09 23:01
source:
  - 藥理藥化平安符
Abstract: 藥物個論
sr-due: 2025-04-12
sr-interval: 3
sr-ease: 250
---

#首刷 #review #GEN4


## 🔹 1. 基本資訊
- **藥名（Drug Name）**：Ethacrynic acid
- **分類（Category）**：Loop diuretics、Phenoxyacetic acid
- **MOA（Mechanism of Action）**：
?
> [!ERROR] 一句話MOA
> - 抑制腎臟粗上行支的 Na⁺/K⁺/2Cl⁻ cotransporter（NKCC2），使 Na⁺、Cl⁻、K⁺ 重吸收減少，進而造成水分與電解質大量排出，並降低管腔正電位導致 Ca²⁺、Mg²⁺ 排出增加。
> - 耳毒性為 LOOP 共通副作用，但它**最易造成耳毒性**
> - 可與含 SH 基之酵素產生共價結合 <!--SR:!2025-04-13,4,270-->

???


### 結構
#需要結構



## 🔹 2. Ethacrynic acid 相關字尾
?
> [!tip] 口訣
> - ethyl + acrylic acid(丙烯酸)
> - -eth = 可以是接在丙烯酸末端乙基，也可以是乙酸根支鏈 <!--SR:!2025-04-13,4,270-->

???


## 🔹 3. 特色
#### 🧪 藥理（Pharmacology）
- 非磺胺類藥物（不會產生過敏反應）


#### 🧬 藥化（Medicinal Chemistry）
- 可與含 SH 基之酵素產生共價結合
- 氯的位置是在 2,3-上（hard）



#### ⚡副作用（Adverse Effects）

- 最易造成耳毒性


## 🔹 4. ADME（藥代動力學）
 - 不重要
## 🔹 5. 比較、連結

- [[Loop Diuretics]] - 最易造成耳毒性

##### 同類藥物(3)
?
- [[Torsemide]]
- [[Bumetanide]]
- [[Furosemide]] <!--SR:!2025-04-13,4,270-->

???

##### 同類藥物()
?
- <!--SR:!2025-04-13,4,270--> 

???

##### 類似藥物() - 相關性比較高那種
?
- <!--SR:!2025-04-13,4,270--> 

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

## 🔹 6. 閃卡區

- Ethacrynic acid藥名拆字():: -acrylic acid(丙烯酸)、-eth = 可以是接在丙烯酸末端乙基，也可以是乙酸根支鏈 <!--SR:!2025-04-13,4,270-->
- 所屬類別(2)::Loop diuretics、Phenoxyacetic acid <!--SR:!2025-04-13,4,270-->
- 必記特色(2)::LOOP中最易造成耳毒性、非磺胺類藥物（不會產生過敏反應） <!--SR:!2025-04-13,4,270-->

