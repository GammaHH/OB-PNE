---
category: NSAID
tags:
  - 藥理藥化
  - NSAID
  - 芳香環乙酸類
  - 前驅藥
created: 2025-03-26
updated: 2025-04-09 15:14
source:
  - 藥理藥化平安符
Abstract: 藥物個論
sr-due: 2025-04-29
sr-interval: 20
sr-ease: 250
---
#段考 #review 
## 🔹 1. 基本資訊
- **藥名（Drug Name）**：Sulindac
- **分類（Category）**：NSAID、芳香環乙酸類(Arylacetic Acid)
- **MOA（Mechanism of Action）**：
?
> [!ERROR] 小貼士
> 
> - 前驅藥，經肝臟酵素轉換為硫化物分泌至膽汁， 再從腸道吸收
> - 作用於 COX-1 和 COX-2 → ↓PG 生成 <!--SR:!2025-04-14,13,270-->

???

### 結構
![[Pasted image 20250331131444.png]]


## 🔹 2. Sulindac 相關字尾(2)
?
> [!tip] 口訣
> - -dac = double (carbon) acid
> - 該類藥物**代謝動不到乙酸**所在的芳香基團
> - -inda = 結構具有 indane 環
> - Sul = sulfide form 有活性<!--SR:!2025-04-11,2,254-->

???



## 🔹 3. 特色
#### 🧪 藥理（Pharmacology）

- 無


#### 🧬 藥化（Medicinal Chemistry）


- 一種**前藥**，但 Sulfide form 有活性
- 結構具有 indane 環
###### 其他
- 一種前驅藥，經肝臟酵素轉換為硫化物分泌至膽汁， 再從腸道吸收 → 有助於維持血中濃度，並具有↓GI 的副作⽤ 
#### ⚡副作用（Adverse Effects）

- 無


## 🔹 4. ADME（藥代動力學）
 - 氧化成 Sulfone 無活性
 - 代謝成 Sulfide form 有活性
## 🔹 5. 比較、連結

- [[NSAID前藥列表]]

##### 同類藥物(3) 
?
- [[Diclofenac]]
- [[Tolmetin]]
- [[Nabumetone]] <!--SR:!2025-04-29,20,250-->

???

##### 類似藥物(1) - 相關性比較高那種
?
- [[Indomethacin]] - 結構為 indole（吲哚）環 <!--SR:!2025-04-15,14,290-->

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
- Sulindac 藥名拆字(3):: Sul-（來自 sulfone 形式）+ -indac（結構中具有 indane 環） + dac => double (carbon) acid 芳香環乙酸類 <!--SR:!2025-04-12,3,253-->
- 所屬類別(2):: NSAID／芳香環乙酸類（Arylacetic Acid） <!--SR:!2025-04-12,3,253-->
- 最大特色:: 具有前驅藥性質，代謝後硫化物形式（Sulfide）才有活性；與其他 NSAID 相比，具有較低的胃腸道副作用，具有較長的代謝過程 <!--SR:!2025-04-12,3,253-->


- 一種前藥，但:: Sulfide form 才有活性，氧化成 Sulfone 無活性 <!--SR:!2025-04-15,14,290-->

- Sulfide結構
?
![[Pasted image 20250326085841.png]] <!--SR:!2025-04-15,14,290-->

???

- Sulfone結構
?
![[Pasted image 20250326085919.png]] <!--SR:!2025-04-15,14,290-->

???


- 結構具有:: indane 環，不同於[[Indomethacin]] <!--SR:!2025-04-14,13,270-->

- Sulindac 的代謝方式(2方向)
?
![[Pasted image 20241127182507.png]] <!--SR:!2025-04-15,14,290-->

???