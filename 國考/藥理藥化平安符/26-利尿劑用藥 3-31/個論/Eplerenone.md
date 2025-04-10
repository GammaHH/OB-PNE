---
category: 利尿劑
tags:
  - 藥理藥化
  - 保鉀型利尿劑
created: 2025-03-31
updated: 2025-04-10 07:37
source:
  - 藥理藥化平安符
Abstract: 藥物個論
sr-due: 2025-04-13
sr-interval: 3
sr-ease: 250
---

#首刷 #review #GEN5


## 🔹 1. 基本資訊
- **藥名（Drug Name）**：Eplerenone
- **分類（Category）**：保鉀型利尿劑
- **MOA（Mechanism of Action）**：
?
> [!ERROR] 一句話MOA
> - 拮抗醛固酮受體，抑制腎臟集合管中 Na⁺ 重吸收與 K⁺ 排出，達到保鉀與降壓效果，且具有**較高選擇性**與較少荷爾蒙副作用。 <!--SR:!2025-04-14,4,270-->

???


### 結構
![[Pasted image 20250331164545.png]]



## 🔹 2. Eplerenone 相關字尾(3)
?
> [!tip] 口訣
> - -Eple + -one= 可以想為「epoxy + spironolactone」混合詞根，從 spironolactone 衍生而來，並加上 epoxy 環修飾，提升選擇性
> - -ren- = "renal"（腎）或 "receptor"
> - -one = steroid-like 並含酮基特徵 <!--SR:!2025-04-14,4,270-->

???

## 🔹 3. 特色
#### 🧪 藥理（Pharmacology）
- 不知


#### 🧬 藥化（Medicinal Chemistry）
-  9,11位 epoxide



#### ⚡副作用（Adverse Effects）

- 相較 [[Spironolactone]]，**較不會導致男性女乳症副作用**


## 🔹 4. ADME（藥代動力學）
 - 不重要
## 🔹 5. 比較、連結

- [[保鉀型利尿劑]]

##### 同類藥物(2)
?
- [[Amiloride]]
- [[Triamterene]] <!--SR:!2025-04-14,4,270-->

???

##### 類似藥物(1) - 相關性比較高那種
?
- [[Spironolactone]] - 具有 steroid 骨架 <!--SR:!2025-04-14,4,270-->

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

- Eplerenone藥名拆字(3)::-Eple + -one = 可以想為「epoxy + spironolactone」混合詞根、-ren- = "renal"（腎）或 "receptor"、-one = steroid-like 並含酮基特徵 <!--SR:!2025-04-14,4,270-->
- 所屬類別(1)::保鉀型利尿劑 <!--SR:!2025-04-14,4,270-->
- 最大特色::相較 spironolactone，**較不會導致男性女乳症副作用** <!--SR:!2025-04-14,4,270-->
- 結構特殊點::9,11位 epoxide <!--SR:!2025-04-11,1,230-->
