---
title: Aspirin
category: 抗血小板凝集
tags:
  - 藥理藥化
  - 抗血小板凝集
  - COX抑制劑
  - NSAID
created: 2025-02-25
updated: 2025-04-08 09:27
source:
  - 藥理藥化平安符
Abstract: 藥物個論
sr-due: 2025-03-30
sr-interval: 3
sr-ease: 250
---
## 🔹 1. 基本資訊
- **藥名（Drug Name）**：Aspirin (ASA)
- **分類（Category）**：抗血小板凝集、COX 非選抑制劑、NSAID、水楊酸衍生物
- **MOA（Mechanism of Action）**：
?
> [!ERROR] 一句話MOA
> - **不可逆**非選抑制COX(==Serine==上乙醯化) ，其他均為可逆
- 水楊酸衍生物 考點為代謝方式 

### 結構
![[Pasted image 20250331131148.png]]


## 🔹 2. 相關比較口訣
?
> [!tip]- 口訣
> - A : Acetyl ; s : salicylic acid 

## 🔹 3. 特色
### 🧪 藥理（Pharmacology）
- 不可逆非選抑制COX(乙醯化) ，其他均為可逆
- 低劑量時::不可逆乙醯化 COX-1，**使 TXA₂ 生成減少**，抗血凝集 

### 🧬 藥化（Medicinal Chemistry）

- 代謝很重要(3[2+1])
?
	1. COOH接Gly(主要)、接 Glucuronide 次
	2. OH接 Glucuronide 


### ⚡副作用（Adverse Effects）

- 在幼兒容易引起::雷氏症候群(Reye's syn) 

## 🔹 4. ADME（藥代動力學）
- **代謝方式**：
	- COOH 接 Gly(主要)、 Glucuronate 次
	- OH接 Glucuronate
## 🔹 5. 比較、連結
- ASA 為 Acetylsalicylic acid 的縮寫
- 吲哚美辛([[Indomethacin]])會增加鋰鹽的再吸收，可能提升毒性風險；阿司匹林([[國考/藥理藥化平安符/42-NSAID 3-26/個論/Aspirin|Aspirin]]) 和 對乙酰氨基酚([[Acetaminophen]])則無此作用



##### 同類藥物(2)
?
- [[Triflusal]]
- [[Diflunisal]] 
1-A、2-DI、3-Tri  


```dataviewjs
// ---------- 標籤推薦區塊（以列表呈現） ----------
const excludeTags = ["藥理學"];
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
<!--SR:!2025-04-15,14,290-->