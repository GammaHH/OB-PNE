---
title: Warfarin
category: 抗凝血
tags:
  - 藥理藥化
  - 口服抗凝血劑
created: 2025-02-25
updated: 2025-04-01 20:11
source:
  - 藥理藥化平安符
Abstract: 藥物個論
sr-due: 2025-04-15
sr-interval: 15
sr-ease: 290
---
#首刷 #review #GEN5
## 🔹 1. 基本資訊
- **藥名（Drug Name）**：Warfarin
- **分類（Category）**：口服抗凝血劑
- **MOA（Mechanism of Action）**：
?
> [!ERROR] 一句話MOA
> - 阻斷 K還原酶，使凝血因子7、9、10、2；蛋白C、S > 造成表皮壞死
> 


## 🔹 2. 相關比較口訣
?
> [!tip]- 口訣
> - war > 像是嬰兒哭聲，因此==分泌乳汁的孕婦==可以使用
> - -farin = coumarin 類衍生物


## 🔹 3. 特色
### 🧪 藥理（Pharmacology）
- 使用之後 VII 因子降低最快(外源性抑制的最上游)
- 解毒劑為 Vit.K1 (因為他抑制Vit. K 的再回收活化)
- 僅在體內有效
- INR 用來監測外生性[[凝血路徑]]
###### 其他
- 用於 預防金屬瓣膜病患血栓栓塞 
### 🧬 藥化（Medicinal Chemistry）

- 結構中的 OH基團可以形成烯醇，製成鹽類製劑
- S form 比較強
- 2-OH 為活性代謝物

### ⚡副作用（Adverse Effects）
- 表皮壞死
- 致畸胎，孕婦不能用，但分泌乳汁的可以



## 🔹 4. ADME（藥代動力學）
| 階段                   | 內容                    |
| -------------------- | --------------------- |
| 吸收（Absorption）   | 未知                    |
| 分布（Distribution） | 未知                    |
| 代謝（Metabolism）   | CYP2C9 為S form 主要代謝方式 |
| 排泄（Excretion）    | 未知                    |
| 半衰期（Half-life）   | 未知                    |
## 🔹 4. 比較、連結
[[Warfarin 和 Heparin的比較]]



##### 同類藥物(3)
?
- [[Dabigatran]]
- [[Phenindione、Anisindione]]


```dataviewjs
// ---------- 標籤推薦區塊（以列表呈現） ----------
const excludeTags = ["藥理學","<%- drugCategory %>"];
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
```



## 🔹 5. 閃卡區
- 解毒劑為:: Vit.K1 (因為他抑制Vit. K 的再回收活化)
- 使用之後 ==VII== 因子降低最快(外源性抑制的最上游)
- 結構中的 OH基團::可以形成烯醇，製成鹽類製劑

- ==S== form 比較強

- 活性代謝物為::2-OH 

- (藥名)藥名拆字()::- war 分泌乳汁的孕婦可以使用、-farin = coumarin 類衍生物
