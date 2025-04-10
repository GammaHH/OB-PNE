---
category: 利尿劑
tags:
  - 藥理藥化
  - 保鉀型利尿劑
  - 常考
  - 拮抗醛固酮受體
created: 2025-03-31
updated: 2025-04-09 09:47
source:
  - 藥理藥化平安符
Abstract: 藥物個論
sr-due: 2025-04-13
sr-interval: 4
sr-ease: 270
---

#首刷 #review #GEN5


## 🔹 1. 基本資訊
- **藥名（Drug Name）**：Spironolactone
- **分類（Category）**：保鉀型利尿劑
- **MOA（Mechanism of Action）**：
?
> [!ERROR] 一句話MOA
> - 拮抗腎臟集合管中醛固酮受體（MR），**減少 Aldosterone 分泌**>>Conn’s syndrome ，抑制 Na⁺ 重吸收與 K⁺ 排出，達到利尿與保鉀作用，常用於高血壓、水腫與心衰。
> - **有 steroid 骨架且具荷爾蒙受體作用**（如抗雄性或雌激素樣作用，這裡抗MR），所以有特殊副作用(男性女乳症) <!--SR:!2025-04-13,4,270-->

???


### 結構
![[Pasted image 20250331162939.png]]



## 🔹 2. Spironolactone 相關字尾/口訣
?
> [!tip] 口訣
> - -Spir = Spiral / steroid 類固醇骨架（steroid-like），具四環結構
> 	- S act = 7-acetyl 、lact = 17-lactone
> 	
> - -lactone = 含內酯環的化合物，與醛固酮結構相似，競爭性結合醛固酮受體 <!--SR:!2025-04-13,4,270-->

???

## 🔹 3. 特色
#### 🧪 藥理（Pharmacology）

- 用於肝硬化、水腫、**Conn’s syndrome**(腎上腺生產過量醛固酮)

#### 🧬 藥化（Medicinal Chemistry）
-  C7有SCOCH₃ 增加口服活性 > 所以脫去 C7後仍有活性
- γ-Lactone (C17位) 是活性基



#### ⚡副作用（Adverse Effects）

- 男性女乳症


## 🔹 3. ADME（藥代動力學）
| 階段               | 內容                             |
| ---------------- | ------------------------------ |
| 吸收（Absorption）   | 未知                             |
| 分布（Distribution） | 未知                             |
| 代謝（Metabolism）   | 脫去 C7-SCOCH₃ → 活性代謝物 Canrenone |
| 排泄（Excretion）    | 未知                             |
| 半衰期（Half-life）   | 未知                             |
## 🔹 5. 比較、連結

- [[保鉀型利尿劑]]


##### 同類藥物(2)
?
- [[Triamterene]]
- [[Amiloride]] <!--SR:!2025-04-13,4,270-->

???

##### 類似藥物(1) - 相關性比較高那種
?
- [[Eplerenone]] - 骨架一樣 <!--SR:!2025-04-13,4,270-->

???


```dataviewjs
// ---------- 標籤推薦區塊（以列表呈現） ----------

// 排除標籤（藥理藥化 + 當前 category）
const excludeTags = ["藥理藥化", dv.current().category];

// 擷取當前筆記的有效標籤（排除上面兩項）
const currentTags = dv.current().tags?.filter(t => !excludeTags.includes(t)) ?? [];

// 💡 顯示用標籤：dash 改為空格（預先處理好）
const displayTag = t => t.replace(/-/g, " ");
const displayTags = currentTags.map(displayTag);

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
let totalUnique = new Set([...multiMatch, ...singleMatch].map(p => p.file.path)).size;

dv.header(5, `相關藥物（共 ${totalUnique} 筆）`);

// 🟦 多標籤命中的區塊
if (multiMatch.length > 0) {
  dv.header(6, `▸ ${displayTags.join("、")}（${multiMatch.length}）`);
  dv.list(
    multiMatch.map(p => {
      const tagsToShow = p.tags
        .filter(t => !excludeTags.includes(t))
        .map(displayTag);
      return `${p.file.link}　${tagsToShow.join("、")}`;
    })
  );
}

// 🟩 單一標籤命中的區塊（依照該標籤分類）
for (let [tag, pages] of Object.entries(singleGroups)) {
  const display = displayTag(tag);
  dv.header(6, `▸ ${display}（${pages.length}）`);
  dv.list(
    pages.map(p => {
      const tagsToShow = p.tags
        .filter(t => !excludeTags.includes(t) && t !== tag)
        .map(displayTag);
      return `${p.file.link}　${tagsToShow.join("、")}`;
    })
  );
}

// 🔕 無結果時提醒
if (multiMatch.length === 0 && Object.keys(singleGroups).length === 0) {
  dv.paragraph("沒有找到與本藥物具有相同標籤的其他筆記。");
}

```


## 🔹 6. 閃卡區

- Spironolactone藥名拆字(2)::S act = 7-acetyl 增強活性、lact = 17-lactone 活性基團 <!--SR:!2025-04-13,4,270-->
- 所屬類別(2)::保鉀型利尿劑、拮抗醛固酮受體<!--SR:!2025-04-12,3,250-->
- 最大特色副作用::男性女乳症 <!--SR:!2025-04-13,4,270-->
- 活性代謝物::脫去 C7-SCOCH₃ → 活性代謝物 Canrenone，**做成 Prodrug 可以增加口服活性** <!--SR:!2025-04-13,4,270-->


Canrenone 為 Spironolactone 的活性代謝物，請問他長怎樣?(附上Spironolactone)
![[Pasted image 20250331163814.png]]
?
![[Pasted image 20250331163838.png]]

???