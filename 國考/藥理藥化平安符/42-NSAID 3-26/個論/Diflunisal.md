---
category: NSAID
tags:
  - 藥理藥化
  - NSAID
  - 水楊酸衍生物
created: 2025-03-26
updated: 2025-04-07 11:06
source:
  - 藥理藥化平安符
Abstract: 藥物個論
sr-due: 2025-04-29
sr-interval: 22
sr-ease: 250
---
#GEN5 #review 
## 🔹 1. 基本資訊
- **藥名（Drug Name）**：Diflunisal
- **分類（Category）**：NSAID、水楊酸衍生物
- **MOA（Mechanism of Action）**：
?
> [!ERROR] 一句話MOA
> - 可逆非選抑制COX <!--SR:!2025-04-22,15,290-->

### 結構
![[Pasted image 20250331131220.png]]


## 🔹 2. Diflunisal 相關字尾(3)
?
> [!tip] 口訣
> - -iflusal/-iflunisal 有點不太重要，水楊酸衍生物
> - Di-, flu = 兩個間位F
> - -sal = salicylic acid
> - 補 -ni- 為音節詞，無義 <!--SR:!2025-04-18,11,270-->

## 🔹 3. 特色
#### 🧪 藥理（Pharmacology）

- 水楊酸衍生物特色：(4)
?
	- 低劑量抑制尿酸排泄(**鹼性藥物**)，痛風禁用
	- 預防心肌梗塞(高劑量，每日)
	- 氣喘禁用
	- 雷氏症候群，小兒不能用(意識不清) <!--SR:!2025-04-08,1,234-->


#### 🧬 藥化（Medicinal Chemistry）
- 不知



#### ⚡副作用（Adverse Effects）

- 抑制尿酸排泄(低劑量)
- **氣喘禁用**


## 🔹 4. ADME（藥代動力學）
 - 不重要
## 🔹 5. 比較、連結


##### 同類藥物(2)
?
- [[國考/藥理藥化平安符/42-NSAID 3-26/個論/Aspirin|Aspirin]]
- [[Triflusal]]
1-A、2-DI、3-Tri <!--SR:!2025-04-22,15,290-->

##### 類似藥物(1) - 相關性比較高那種
?
- [[Triflusal]] <!--SR:!2025-04-22,15,290-->



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



## 🔹 6. 閃卡區

- Di-, flu 表示::兩個F(間位) <!--SR:!2025-04-18,11,270-->

- Diflunisal 藥名拆字(3)::Diflunisal = Di-（兩個）+ flu-（氟取代）+ -ni-（音節詞，無意義）+ -sal（salicylic acid 衍生物） <!--SR:!2025-04-10,3,254-->
- 所屬類別(2):: NSAID／水楊酸衍生物（salicylate derivative） <!--SR:!2025-04-11,4,274-->
- 特色(3)::具 salicylate 結構但非 acetylated，可抑制 COX 並具止痛、解熱與抗發炎作用，但低劑量反而會抑制尿酸排泄，不適用於痛風，小孩使用有雷氏症候群風險 <!--SR:!2025-04-11,4,274-->

