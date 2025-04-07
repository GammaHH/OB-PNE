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
sr-due: 2025-04-26
sr-interval: 25
sr-ease: 250
---
#review #GEN5
## 🔹 1. 基本資訊
- **藥名（Drug Name）**：Naproxen
- **分類（Category）**：NSAID、芳香類丙酸類
- **MOA（Mechanism of Action）**：
?
> [!ERROR] 一句話MOA
> - 抑制COX-1與COX-2酵素，減少前列腺素（prostaglandins）合成，達到抗發炎、止痛及解熱作用。 <!--SR:!2025-04-05,4,270-->


### 結構
![[Pasted image 20250331131356.png]]



## 🔹 2. Naproxen 相關字尾
?
> [!tip] 口訣
> - -Nap = Naphthalene（萘環）
> - 同乙酸類，代謝動不到酸的環
> - -pro = 丙酸類
 <!--SR:!2025-04-04,3,250-->


## 🔹 3. 特色
#### 🧪 藥理（Pharmacology）
- 無

#### 🧬 藥化（Medicinal Chemistry）

- 唯一以 **S(+)** form 上市的藥物，具光學異構物活性差異

#### ⚡副作用（Adverse Effects）

- 不知


## 🔹 4. ADME（藥代動力學）
| 階段                   | 內容   |
| -------------------- | ---- |
| 吸收（Absorption）   | 未知   |
| 分布（Distribution） | 高結合率 |
| 代謝（Metabolism）   | 未知   |
| 排泄（Excretion）    | 未知   |
| 半衰期（Half-life）   | 未知   |
## 🔹 5. 比較、連結


##### 同類藥物(2)
?
- [[Ibuprofen]]
- [[Flurbiprofen]] <!--SR:!2025-04-05,4,270-->

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

- 特色：唯一以:: S(+) form 上市的藥物，具光學異構和手性中心 <!--SR:!2025-04-05,4,270-->

- Naproxen 藥名拆字(3) :: Napro- 表示為 naphthalene（萘環）衍生結構，-proxen（= pro + en）結尾表示含有丙酸（propionic acid）結構 <!--SR:!2025-04-04,3,250-->
- Naproxen 所屬類別 (2):: NSAID、芳香環丙酸類（Propionic acid 類） <!--SR:!2025-04-05,4,270-->
