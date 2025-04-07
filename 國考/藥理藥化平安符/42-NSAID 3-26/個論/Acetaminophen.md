---
category: NSAID
tags:
  - 藥理藥化
  - NSAID
created: 2025-03-26
updated: 2025-04-06 20:12
source:
  - 藥理藥化平安符
Abstract: 藥物個論
sr-due: 2025-05-06
sr-interval: 30
sr-ease: 290
---
#GEN5 #review 
## 🔹 1. 基本資訊
- **藥名（Drug Name）**：Acetaminophen (APAP)
- **分類（Category）**：NSAID
- **MOA（Mechanism of Action）**：
?
> [!ERROR] 一句話MOA
> - 抑制中樞神經系統內的 COX 活性，減少前列腺素合成，產生解熱與止痛作用，但抗發炎效果極弱。 <!--SR:!2025-04-20,14,290-->


### 結構
![[Pasted image 20250331131117.png]]



## 🔹 2. Acetaminophen 相關字尾/口訣(4)
?
> [!tip] 口訣
> - -ace = Acetyl(乙醯基)
> - -amino = 胺基（–NH₂）
> - [[-phen]] = Phenyl(苯基)，絕對不能看成 酚基
> - -ol / -en（美式名稱語尾） = 羥基（–OH），語尾變化較非正式，en也可能毫無意義 <!--SR:!2025-04-20,14,290-->


## 🔹 3. 特色
#### 🧪 藥理（Pharmacology）


- **無抗發炎**作用

#### 🧬 藥化（Medicinal Chemistry）

- 大人和小孩的代謝物不同，小孩 O-sulfate ；大人 O-glucuronide
- 氧化形成 NAPQI，**代謝酶CYP2E1和[[酒精]]相同**
- 解毒劑，運用上面的SH 基團行 Conjugation 
	- Glutathione(GSH)
	- N-acetylcysteine(NAC) 

#### ⚡副作用（Adverse Effects）

- 不知


## 🔹 4. ADME（藥代動力學）
 - 不重要
## 🔹 5. 比較、連結

```dataviewjs
// ---------- 標籤推薦區塊（以列表呈現） ----------
const excludeTags = ["藥理藥化","NSAID"];
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

##### 類似藥物(1僅相似)
?
- [[國考/藥理藥化平安符/31-抗凝血藥物 2-29/個論/Aspirin|Aspirin]] - ASA <!--SR:!2025-04-20,14,290-->

## 🔹 6. 閃卡區

- 小孩代謝物:: O-sulfate <!--SR:!2025-04-20,14,290-->
- 大人代謝物:: O-glucuronide <!--SR:!2025-04-20,14,290-->
- 毒性代謝物(PhaseII, by)::  NAPQI(N-acetyl-p-benzoquinone imine) by CYP2E1 (和酒精相同) <!--SR:!2025-04-20,14,290-->
- 使用的代謝酶::和[[酒精]]相同(CYP2E1) <!--SR:!2025-04-20,14,290-->
- 相關解毒劑(2)::Glutathione(GSH)、N-acetylcysteine(NAC) 的SH Conjugation <!--SR:!2025-04-20,14,290-->
- 身為NSAID的特色::無抗發炎作用 <!--SR:!2025-04-20,14,290-->


- Acetaminophen 藥名拆字:: Acetaminophen = Acetyl（-ace）+ Amino（-amino）+ Phenyl（-phen）+ 羥基語尾（-en/-ol）
- 所屬類別(2):: 非典型NSAID（實際不具抗發炎效果）／解熱鎮痛劑（Antipyretic/Analgesic）
