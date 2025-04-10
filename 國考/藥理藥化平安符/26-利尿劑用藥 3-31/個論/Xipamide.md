---
category: 利尿劑
tags:
  - 藥理藥化
  - 利尿劑
  - Thiazide-like-Diuretics
  - Salicylanilide
created: 2025-03-31
updated: 2025-04-09 13:02
source:
  - 藥理藥化平安符
Abstract: 藥物個論
sr-due: 2025-04-12
sr-interval: 3
sr-ease: 230
---

#review #GEN5
## 🔹 1. 基本資訊
- **藥名（Drug Name）**：Xipamide
- **分類（Category）**：利尿劑、Thiazide-like Diuretics、Salicylanilide
- **MOA（Mechanism of Action）**：
?
> [!ERROR] 一句話MOA
> - 抑制腎小管遠曲曲小管中的 Na⁺/Cl⁻ 共輸體，減少鈉與氯的重吸收，產生利尿與降壓作用，同時具有血管擴張效果。 <!--SR:!2025-04-12,3,250-->

???


### 結構
![[Pasted image 20250331161714.png]]
- Salicylanilide
![[Pasted image 20250409132054.png]]
- 醯替苯胺 （Anilides）
![[Pasted image 20250409132243.png]]


## 🔹 2. Xipamide 相關字尾(2)
?
> [!tip] 口訣
> - -pam- = sulfonamide（–SO₂NH₂），在字尾為巴比妥鹽類藥物
> - Xip- = 類似 salicyl 或商品名稱語感修飾 <!--SR:!2025-04-12,3,250-->

???

## 🔹 3. 特色
#### 🧪 藥理（Pharmacology）
- 不知


#### 🧬 藥化（Medicinal Chemistry）
- 結構特徵為 Salicylanilide



#### ⚡副作用（Adverse Effects）


- 高血鈣（PTH促進 $Ca^{2+}$再吸收）、高尿酸血症、高血糖、高血脂、低血鈉 (該類副作用)

## 🔹 4. ADME（藥代動力學）
 - 不重要
## 🔹 5. 比較、連結

- [[Thiazide diuretics]]

##### 同類藥物(3)
?
- [[Quinethazone]]
- [[Indapamide]]
- [[Chlorthalidone]] <!--SR:!2025-04-10,1,210-->

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

- Xipamide藥名拆字(2)::-pam- = sulfonamide（–SO₂NH₂），Xip- = 類似 salicyl 或商品名稱語感修飾 <!--SR:!2025-04-12,3,250-->
- 所屬類別(2'/f>1)::利尿劑、Thiazide-like Diuretics > Salicylanilide
- 最大特色::結構特徵為 Salicylanilide
