---
category: NSAID
tags:
  - 藥理藥化
  - NSAID
  - Oxicam
created: 2025-03-26
updated: 2025-04-01 20:12
source:
  - 藥理藥化平安符
Abstract: 藥物個論
sr-due: 2025-04-11
sr-interval: 10
sr-ease: 250
---
#首刷 #review #GEN5

## 🔹 1. 基本資訊
- **藥名（Drug Name）**：Piroxicam
- **分類（Category）**：NSAID、Oxicam(Enolcarboxamides)
- **MOA（Mechanism of Action）**：
?
> [!ERROR] 一句話MOA
> - 非選擇性抑制COX-1與COX-2，抑制前列腺素合成，達到**長效的抗發炎、鎮痛與解熱作用**。 <!--SR:!2025-04-15,14,290-->


### 結構
![[Pasted image 20250331131426.png]]



## 🔹 2. Piroxicam 相關字尾/口訣
?
> [!tip] 口訣
> - -Pir = Pyridine
> - -oxicam = oxicam 類藥物>>均有 Benzothiazine，通常半衰期很長、效價強 <!--SR:!2025-04-14,13,270-->


## 🔹 3. 特色
#### 🧪 藥理（Pharmacology）

- NSAID中抗發炎最強最長者

#### 🧬 藥化（Medicinal Chemistry）
- Enolcarboxamides 結構為
?
烯醇烯胺，烯(Enol)、carbox(Carbonyl group)、carboxamide(羧酸胺)
- [[Meloxicam]]
![[Pasted image 20250401122834.png]] <!--SR:!2025-04-04,3,251-->

- 均有 Benzothiazine，通常半衰期很長、效價強



#### ⚡副作用（Adverse Effects）

- 不知


## 🔹 4. ADME（藥代動力學）
| 階段               | 內容                                                |
| ---------------- | ------------------------------------------------- |
| 吸收（Absorption）   | 未知                                                |
| 分布（Distribution） | 未知                                                |
| 代謝（Metabolism）   | **CYP2C9** pyridine 對位接 OH<br>次要代謝物為糖精(Saccharin) |
| 排泄（Excretion）    | 未知                                                |
| 半衰期（Half-life）   | 未知                                                |
## 🔹 5. 比較、連結



##### 類似藥物(1)
?
- [[Meloxicam]] - 多了一個 Thiazole 
```dataviewjs
// ---------- 標籤推薦區塊（以列表呈現） ----------
const excludeTags = ["藥理學","NSAID"];
const currentTags = dv.current().tags?.filter(t => !excludeTags.includes(t)) ?? []; <!--SR:!2025-04-04,3,250-->

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

- 該藥的主要代謝物和次要代謝物為何::CYP2C9 pyridine 對位接 OH、次要代謝物為糖精(Saccharin) <!--SR:!2025-04-02,1,210-->
- -oxicam結構均有
?
- Benzothiazine 
![[imgsrv.png]] <!--SR:!2025-04-05,4,271-->

- Piroxicam 藥名拆字(2) :: Pir 表 pyridine 結構；-oxicam 表 oxicam 類（含benzothiazine 骨架） <!--SR:!2025-04-05,4,271-->
- Piroxicam 所屬類別(3) :: NSAID、Oxicam 類、Enolcarboxamide 結構藥物 <!--SR:!2025-04-05,4,271-->
- Piroxicam 最大特色 ::為長效型 NSAID 中抗發炎**作用最強且半衰期最長**者 <!--SR:!2025-04-05,4,271-->

