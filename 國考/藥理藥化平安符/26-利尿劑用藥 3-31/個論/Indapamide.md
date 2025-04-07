---
category: 利尿劑
tags:
  - 藥理藥化
  - Thiazide-like-Diuretics
  - Benzohydrazide
  - 利尿劑
created: 2025-03-31
updated: 2025-04-07 10:00
source:
  - 藥理藥化平安符
Abstract: 藥物個論
sr-due: 2025-04-10
sr-interval: 3
sr-ease: 250
---

#首刷 #review #GEN5


## 🔹 1. 基本資訊
- **藥名（Drug Name）**：Indapamide
- **分類（Category）**：Thiazide-like Diuretics、利尿劑、Benzohydrazide
- **MOA（Mechanism of Action）**：
?
> [!ERROR] 一句話MOA
> - 抑制腎小管遠曲曲小管中的 Na⁺/Cl⁻ 共輸體，減少鈉與氯的重吸收，產生利尿與降壓作用，同時具有血管擴張效果。 <!--SR:!2025-04-11,4,270-->


### 結構
![[Pasted image 20250331155906.png]]



## 🔹 2. Indapamide 相關字尾(2)
?
> [!tip] 口訣
> - -Inda =  Indoline 環
> - -pam- = 磺醯胺結構（–SO₂NH₂），該字尾在藥物命名中很有辨識度，苯二氮平類字尾多為這個，但如果在字在中間則是利尿劑的磺醯胺 <!--SR:!2025-04-11,4,270-->

## 🔹 3. 特色
#### 🧪 藥理（Pharmacology）
- 同時具有利尿及血管擴張作用


#### 🧬 藥化（Medicinal Chemistry）
- 含有 Indoline 環，就是部分還原的吲哚環(Indole)



#### ⚡副作用（Adverse Effects）

- 高血鈣（PTH促進 $Ca^{2+}$再吸收）、高尿酸血症、高血糖、高血脂、低血鈉 (該類副作用)


## 🔹 4. ADME（藥代動力學）
 - 不重要
## 🔹 5. 比較、連結

- [[Thiazide diuretics]]

##### 同類藥物(3)
?
- [[Chlorthalidone]]
- [[Quinethazone]]
- [[Xipamide]] <!--SR:!2025-04-08,1,230-->



```dataviewjs
// ---------- 標籤推薦區塊（以列表呈現） ----------

// 排除標籤（藥理藥化 + 當前 category）
const excludeTags = ["藥理藥化", dv.current().category];

// 擷取當前筆記的有效標籤（排除上面兩項）
const currentTags = dv.current().tags?.filter(t => !excludeTags.includes(t)) ?? [];

// 💡 顯示用標籤：dash 改為空格（預先處理好）
const displayTag = t => t.replace(/-/g, " ");
const displayTags = currentTags.map(displayTag);

// 抓出所有其他檔案（排除自己）
let allCandidates = dv.pages()
  .where(p => p.file?.path?.startsWith("國考/") && p.tags && p.file.name !== dv.current().file.name);

// 分類成符合多個標籤（multi）與單一標籤（single）
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

- Indapamide藥名拆字(2)::-Inda =  Indoline 環(部分還原的吲哚)，-pam- = 在字中為磺醯胺結構（–SO₂NH₂） <!--SR:!2025-04-11,4,270-->
- 所屬類別(3)::Thiazide-like Diuretics、利尿劑、Benzohydrazide <!--SR:!2025-04-11,4,270-->
- 最大特色::同時具有利尿及血管擴張作用 <!--SR:!2025-04-11,4,270-->

- hydrazide 的特性(4)::MAO 抑制劑的藥物骨架、抗結核藥 Isoniazid 的親戚、易被代謝氧化成肝毒性產物、Schiff base 的前驅物(Benzohydrazide 作為半穩定 Schiff 鹼類（hydrazones）) <!--SR:!2025-04-10,3,250-->