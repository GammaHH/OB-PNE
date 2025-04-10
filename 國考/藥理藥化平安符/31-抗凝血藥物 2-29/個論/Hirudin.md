---
title: Hirudin
category: 抗凝血
tags:
  - 藥理藥化
  - DTIs
created: 2025-02-25
updated: 2025-04-10 08:56
source:
  - 藥理藥化平安符
Abstract: 藥物個論
sr-due: 2025-04-25
sr-interval: 15
sr-ease: 271
---
#review #GEN5 
## 🔹 1. 基本資訊
- **藥名（Drug Name）**：Hirudin
- **分類（Category）**：DTIs
- **MOA（Mechanism of Action）**：
?
> [!ERROR] 一句話MOA
> - 直接抑制 thrombin <!--SR:!2025-04-08,11,270-->

???

???

## 🔹 2. 相關口訣
> [!tip] 口訣
> - -ase、-in （常見的蛋白質名詞後綴）

???

## 🔹 3. 特色
### 🧪 藥理（Pharmacology）

- 又稱為==水蛭素==
- 治療[[肝素誘導血小板缺乏症(HIT)]] <!--SR:!2025-04-08,11,270-->
???
### 🧬 藥化（Medicinal Chemistry）
- 無

### ⚡副作用（Adverse Effects）
- 不知


## 🔹 4. ADME（藥代動力學）
 不重要
## 🔹 5. 比較、連結
- [[水蛭科（Hirudinidae）]]

##### 藥劑學

- **抗凝血藥（Lepirudin）**：
    
    - 一種由酵母細胞重組產生的水蛭素（recombinant hirudin）。
    - 監測方法：使用部分凝血活酶時間（aPTT）來測試其抗凝活性。

##### 同類藥物(2)
?
- [[Argatroban]]
- [[Dabigatran]]

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

- Hirudin藥名拆字(2)::Hirud-（來自水蛭科學名 Hirudinidae）+ -in（常見的蛋白質名詞後綴）
- Hirudin所屬類別(1)::直接凝血酶抑制劑（Direct Thrombin Inhibitor, DTI）
- Hirudin 可以治療::由肝素誘導的血小板減少症（HIT）
