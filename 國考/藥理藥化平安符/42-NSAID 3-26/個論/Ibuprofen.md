---
category: NSAID
tags:
  - 藥理藥化
  - NSAID
  - 芳香環丙酸類
created: 2025-03-26
updated: 2025-04-01 20:12
source:
  - 藥理藥化平安符
Abstract: 藥物個論
sr-due: 2025-04-13
sr-interval: 12
sr-ease: 250
---
#首刷 #review #GEN5

## 🔹 1. 基本資訊
- **藥名（Drug Name）**：Ibuprofen
- **分類（Category）**：NSAID、芳香環丙酸類(Propionic acid)
- **MOA（Mechanism of Action）**：
?
> [!ERROR] 一句話MOA
> - 抑制COX-1與COX-2酵素，減少前列腺素（prostaglandins）合成，達到抗發炎、止痛及解熱作用。 <!--SR:!2025-04-05,4,270-->

### 結構
![[Pasted image 20250327225304.png]]
- 紅圈為 $\omega$-1 位置


## 🔹 2. Ibuprofen 相關字尾(3)
?
> [!tip] 口訣
> - pro = 丙酸 ，同乙酸類，代謝動不到酸的環
> - fen = 有苯環
> - -Ibu 可以聯想成 兩碳後的 $\omega$-1 代謝 (I=1) <!--SR:!2025-04-04,3,250-->

## 🔹 3. 特色
#### 🧪 藥理（Pharmacology）

- $\omega$-1 代謝

##### 其他
- 對幼兒最安全

#### 🧬 藥化（Medicinal Chemistry）

- 具有一個手性中心

#### ⚡副作用（Adverse Effects）

- 不知


## 🔹 4. ADME（藥代動力學）
| 階段                   | 內容            |
| -------------------- | ------------- |
| **吸收（Absorption）**   | 未知            |
| **分布（Distribution）** | 未知            |
| **代謝（Metabolism）**   | $\omega$-1 代謝 |
| **排泄（Excretion）**    | 未知            |
| **半衰期（Half-life）**   | 未知            |
## 🔹 5. 比較、連結


##### 同類藥物(2)
?
- [[Naproxen]]
- [[Flurbiprofen]] <!--SR:!2025-04-02,1,230-->

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

- $\omega$-1 代謝 的本質是什麼?
?
- 在支鏈末端倒數一個碳上加上 水溶性基團
![[Pasted image 20250326101520.png]] <!--SR:!2025-04-05,4,270-->



- Ibuprofen 藥名拆字(2) :: ibu 可聯想成 I = 1，表示進行 ω-1 位點代謝；pro = 丙酸類結構，fen = 具有苯環而非苯環取代基 <!--SR:!2025-04-04,3,250-->
- Ibuprofen 所屬類別(2) :: NSAID、芳香環丙酸類（Propionic acid 類） <!--SR:!2025-04-05,4,270-->
- Ibuprofen 最大特色 :: 對幼兒最安全 <!--SR:!2025-04-05,4,270-->


- 主要代謝為:: ω-1 羥化（位於 isobutyl 末端的倒數第二碳），因此具有一個手性中心