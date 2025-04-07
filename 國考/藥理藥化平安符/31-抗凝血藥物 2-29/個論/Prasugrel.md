---
category: 抗血小板凝集
tags:
  - 藥理藥化
  - 抗血小板凝集
  - 不可逆P2Y12拮抗劑
created: 2025-03-31
updated: 2025-04-06 21:31
source:
  - 藥理藥化平安符
Abstract: 藥物個論
sr-due: 2025-04-15
sr-interval: 9
sr-ease: 230
---

#首刷 #review #GEN5


## 🔹 1. 基本資訊
- **藥名（Drug Name）**：Prasugrel
- **分類（Category）**：抗血小板凝集、不可逆P2Y12拮抗劑
- **MOA（Mechanism of Action）**：
?
> [!ERROR] 一句話MOA
> - 為 thienopyridine 類前驅藥，活化後不可逆抑制血小板的 ADP（P2Y₁₂）受體，抑制血小板聚集，防止動脈血栓形成。 <!--SR:!2025-04-09,3,250-->


### 結構
![[Pasted image 20250331215039.png]]



## 🔹 2. Prasugrel 相關字尾(2)
?
> [!tip] 口訣
> - -grel > **不**可逆 + prodrug
> - -Prasu = 可能源於結構中 thienopyridine，su = sulfor , Pr = pyridine <!--SR:!2025-04-08,2,230--> 

- thienopyridine = thiophene + pyridine
## 🔹 3. 特色
#### 🧪 藥理（Pharmacology）
- 半衰期為同類藥物中最長


#### 🧬 藥化（Medicinal Chemistry）
- 結構似 [[Ticagrelor]] 含有 Thienopyridine



#### ⚡副作用（Adverse Effects）

- 不知


## 🔹 4. ADME（藥代動力學）
 - 不重要
## 🔹 5. 比較、連結

- [[怠辦連結]]

##### 同類藥物(1)
?
- [[Ticagrelor]] <!--SR:!2025-04-09,3,250-->

##### 類似藥物(2) - 相關性比較高那種
?
- [[Clopidogrel]]
- [[Ticlopidine]] <!--SR:!2025-04-09,3,250-->





```dataviewjs
// ---------- 標籤推薦區塊（以列表呈現） ----------
const excludeTags = ["藥理藥化"];
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
  dv.header(5, "類似藥物（0）");
  dv.paragraph("沒有找到與本藥物具有相同標籤的其他筆記。");
}

```




## 🔹 6. 閃卡區

- Prasugrel藥名拆字(2)::-grel > **不**可逆 + prodrug、-Prasu =  thienopyridine <!--SR:!2025-04-08,2,230-->
- 所屬類別(2)::抗血小板凝集、不可逆P2Y12拮抗劑 <!--SR:!2025-04-08,2,230-->
- 最大特色::同類藥物中**半衰期最長** <!--SR:!2025-04-09,3,250-->
