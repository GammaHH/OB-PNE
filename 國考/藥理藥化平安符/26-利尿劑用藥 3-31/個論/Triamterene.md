---
category: 保鉀型利尿劑
tags:
  - 藥理藥化
  - 保鉀型利尿劑
created: 2025-03-31
updated: 2025-04-06 21:34
source:
  - 藥理藥化平安符
Abstract: 藥物個論
sr-due: 2025-04-16
sr-interval: 10
sr-ease: 230
---

#首刷 #review #GEN5


## 🔹 1. 基本資訊
- **藥名（Drug Name）**：Triamterene
- **分類（Category）**：[[保鉀型利尿劑]]
- **MOA（Mechanism of Action）**：
?
> [!ERROR] 一句話MOA
> - 抑制腎臟遠曲小管與集合管上的 ENaC（上皮鈉通道），減少 Na⁺ 再吸收並保留 K⁺，達到利尿與保鉀效果。 <!--SR:!2025-04-20,14,290-->


### 結構
![[Pasted image 20250331165007.png]]
-  pteridine (蝶碇)
![[Pasted image 20250331164754.png]]



## 🔹 2. Triamterene 相關字尾(2)
?
> [!tip] 口訣
> - Tri-am-	= 三個胺基
> - -terene	= pteridine（蝶啶），分子骨架來源 <!--SR:!2025-04-19,13,270-->

## 🔹 3. 特色
#### 🧪 藥理（Pharmacology）
- 不知 (代謝物具利尿活性?)


#### 🧬 藥化（Medicinal Chemistry）
- 代謝物具利尿活性 (4'-hydroxytriamterene)
-  有三個胺基，類 pteridine 衍生
- 學名： 2,4,7-triamino-6-phenylpteridine



#### ⚡副作用（Adverse Effects）

- 不知


## 🔹 4. ADME（藥代動力學）
 - 不重要
## 🔹 5. 比較、連結

- [[保鉀型利尿劑]]

##### 同類藥物(3)
?
- [[Spironolactone]]
- [[Eplerenone]]
- [[Amiloride]] <!--SR:!2025-04-08,2,250-->


```dataviewjs
// ---------- 標籤推薦區塊（以列表呈現） ----------
const excludeTags = ["藥理藥化","<%- drugCategory %>"];
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

- Triamterene藥名拆字(2)::Tri-am- = 三個胺基、-terene = pteridine（蝶啶） <!--SR:!2025-04-19,13,270-->
- 所屬類別(1)::保鉀型利尿劑 <!--SR:!2025-04-19,13,270-->
- 最大特色::代謝物4'-hydroxytriamterene 仍具活性 <!--SR:!2025-04-07,1,210-->

- 三胺基位置
?
2,4,7-(6-phenylpteridine)
![[Pasted image 20250331165007.png]] <!--SR:!2025-04-09,3,250-->

