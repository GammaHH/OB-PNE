---
category: 利尿劑
tags:
  - 藥理藥化
  - 保鉀型利尿劑
  - Pyrazine
created: 2025-03-31
updated: 2025-04-10 09:40
source:
  - 藥理藥化平安符
Abstract: 藥物個論
sr-due: 2025-04-13
sr-interval: 3
sr-ease: 251
---

#首刷 #review #GEN5


## 🔹 1. 基本資訊
- **藥名（Drug Name）**：Amiloride
- **分類（Category）**：保鉀型利尿劑
- **MOA（Mechanism of Action）**：
?
> [!ERROR] 一句話MOA
> - 抑制腎臟遠曲小管與集合管的 ENaC（上皮鈉通道），減少鈉再吸收、促進水分排出，同時保留鉀離子，達到輕度利尿與保鉀效果。 <!--SR:!2025-04-14,4,272-->

???


### 結構
![[Pasted image 20250331165552.png]]
- Pyrazine
![[Pasted image 20250331165531.png]]


## 🔹 2. Amiloride 相關字尾(2[1>2/1])
?
> [!tip] 口訣
> - Ami- = amino / amidino，可聯想成胺基與  guanidino（胍基），高度鹼性
> - -ide = 可以聯想到具有胺基的相關藥物，通常具有**鹼性特性**。​常經過**第一相代謝** <!--SR:!2025-04-14,4,272-->

???

## 🔹 3. 特色
#### 🧪 藥理（Pharmacology）
- 用於 Liddle's syndrome (保鉀有整理)
- 噴霧劑可治療 cystic fibrosis (參考)
- **治療腎因性尿崩症**


#### 🧬 藥化（Medicinal Chemistry）
- 強鹼性 Guanidino 基
- Pyrazine 骨架



#### ⚡副作用（Adverse Effects）

- 不知


## 🔹 4. ADME（藥代動力學）
 - 不重要
## 🔹 5. 比較、連結

- [[保鉀型利尿劑]]

##### 同類藥物(3)
?
- [[Triamterene]]
- [[Eplerenone]]
- [[Spironolactone]] <!--SR:!2025-04-23,13,270-->

???


```dataviewjs
// ---------- 標籤推薦區塊（以列表呈現） ----------
const excludeTags = ["藥理藥化", dv.current().category];
const currentTags = dv.current().tags?.filter(t => !excludeTags.includes(t)) ?? [];

let tagMatches = dv.pages()
  .where(p => p.tags && p.file.name !== dv.current().file.name)
  .filter(p => p.tags.some(tag => currentTags.includes(tag)));

let tagGroups = {};

for (let tag of currentTags) {
  tagGroups[tag] = tagMatches.filter(p => p.tags.includes(tag));
}

let totalMatched = Object.values(tagGroups).reduce((acc, pages) => acc + pages.length, 0);

if (totalMatched > 0) {
  dv.header(5, `相關藥物（共 ${totalMatched} 筆）`);
  for (let [tag, pages] of Object.entries(tagGroups)) {
    if (pages.length > 0) {
      dv.header(6, `▸ ${tag}（${pages.length}）`);
		 dv.list(
		  pages.map(p => {
		    const tagsToShow = p.tags?.filter(t => !excludeTags.includes(t) && t !== tag) ?? [];
		    return `${p.file.link}　${tagsToShow.join("、")}`;
		  })
      );
    }
  }
} else {
  dv.header(5, "相關藥物（0）");
  dv.paragraph("沒有找到與本藥物具有相同標籤的其他筆記。");
}

```


## 🔹 6. 閃卡區

- Amiloride藥名拆字(2)::Ami- = amino / amidino，可聯想成胺基與  guanidino（胍基），高度鹼性、-ide = 可以聯想到具有胺基的相關藥物，通常具有**鹼性特性**。​常經過第一相代謝 <!--SR:!2025-04-26,16,290-->
- 所屬類別(1)::保鉀型利尿劑 <!--SR:!2025-04-14,4,272-->
- 最大特色::**有強鹼性 Guanidino 基**(重點) <!--SR:!2025-04-14,4,272-->
- 骨架特色::Pyrazine 骨架 <!--SR:!2025-04-14,4,272-->
- 可以治療/特色(4)::Liddle's syndrome (保鉀有整理)、**噴霧劑**可治療 cystic fibrosis (參考)、可用於鋰鹽導致的尿崩症、**腎因性尿崩症** <!--SR:!2025-04-14,4,272-->
