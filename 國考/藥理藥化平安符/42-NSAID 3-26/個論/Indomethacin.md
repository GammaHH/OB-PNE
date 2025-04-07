---
category: NSAID
tags:
  - 藥理藥化
  - NSAID
  - 芳香環乙酸類
created: 2025-03-26
updated: 2025-04-01 20:12
source:
  - 藥理藥化平安符
Abstract: 藥物個論
sr-due: 2025-04-13
sr-interval: 12
sr-ease: 250
---
#GEN4 #review 

## 🔹 1. 基本資訊
- **藥名（Drug Name）**：Indomethacin
- **分類（Category）**：NSAID、芳香環乙酸類
- **MOA（Mechanism of Action）**：
?
> [!ERROR] 一句話MOA
> - 抑制COX-1與COX-2酵素，減少前列腺素（prostaglandins）合成，達到抗發炎、止痛及解熱作用。 <!--SR:!2025-04-15,14,290-->

### 結構
![[Pasted image 20250331131247.png]]



## 🔹 2. Indomethacin 相關字尾/口訣
?
> [!tip] 口訣
> - ethacin 可以看出是 乙酸類 >> NSAID的芳香環乙酸類
> - indo- 表 indole 環
> - -meth 表示結構上有 methoxy
> - 該類藥物**代謝動不到乙酸**所在的芳香基團 <!--SR:!2025-04-14,13,270-->


## 🔹 3. 特色
#### 🧪 藥理（Pharmacology）

- 治療新生兒動脈閉鎖不全 PDA
- Alprostadil / Indomethacin, [[Ibuprofen]] 治勃起功能障礙



#### 🧬 藥化（Medicinal Chemistry）

- 代謝方式稱為三角代謝
###### 其他
- 具有indole 環


#### ⚡副作用（Adverse Effects）

- 無


## 🔹 4. ADME（藥代動力學）
 - 醯胺水解
 - COOH加上 Glucuronide 
 - C5脫甲基

## 🔹 5. 比較、連結
###### 三上段考的東西
- 吲哚美辛([[Indomethacin]])會**增加鋰鹽的再吸收**，可能提升毒性風險；阿司匹林([[國考/藥理藥化平安符/42-NSAID 3-26/個論/Aspirin|Aspirin]]) 和 對乙酰氨基酚則無此作用

##### 同類藥物(3)
?
- [[Diclofenac]]
- [[Tolmetin]]
- [[Nabumetone]] <!--SR:!2025-04-05,4,275-->


##### 類似藥物(1)
?
- [[Sulindac]] - 核心為 indane 不是 indole <!--SR:!2025-04-03,2,250-->


```dataviewjs
// ---------- 標籤推薦區塊（以列表呈現） ----------
const excludeTags = ["藥理學","NSAID"];
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
        pages.map(p => p.file.link)
      );
    }
  }
} else {
  dv.header(5, "相關藥物（0）");
  dv.paragraph("沒有找到與本藥物具有相同標籤的其他筆記。");
}
````

## 🔹 6. 閃卡區

- 代謝方式(3)
?
	 - 醯胺水解
	 - COOH加上 Glucuronide 
	 - C5脫甲基 <!--SR:!2025-04-03,2,250-->

- 該要用於治療(1)::新生兒動脈閉鎖不全 PDA <!--SR:!2025-04-15,14,290-->
- 結構具有::indole 環，和 [[Sulindac]] 不同 <!--SR:!2025-04-15,14,290-->

- 特殊治療::勃起功能障礙 Alprostadil / Indomethacin, [[Ibuprofen]] <!--SR:!2025-04-14,13,270-->

- Indomethacin 藥名拆字(3) :: indo- 表 indole 環，-meth 表示結構上有 methoxy，-ethacin 表示屬於乙酸類 NSAID <!--SR:!2025-04-05,4,275-->
- Indomethacin 所屬類別(2) :: NSAID、芳香環乙酸類 <!--SR:!2025-04-04,3,255-->
