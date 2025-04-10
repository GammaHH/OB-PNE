---
category: 利尿劑
tags:
  - 藥理藥化
  - 利尿劑
  - Phthalimidine
  - Thiazide-like-Diuretics
created: 2025-03-31
updated: 2025-04-10 09:10
source:
  - 藥理藥化平安符
Abstract: 藥物個論
sr-due: 2025-04-22
sr-interval: 12
sr-ease: 270
---

#首刷 #review #GEN5


## 🔹 1. 基本資訊
- **藥名（Drug Name）**：Chlorthalidone
- **分類（Category）**：利尿劑、Phthalimidine、Thiazide-like Diuretics
- **MOA（Mechanism of Action）**：
?
> [!ERROR] 一句話MOA
> - 抑制腎小管遠曲曲小管中的 Na⁺/Cl⁻ 共輸體，減少鈉與氯的重吸收，產生利尿與降壓作用，同時具有血管擴張效果。 <!--SR:!2025-04-11,4,270-->

???


### 結構
![[Pasted image 20250331161136.png]]
- **phthalimidine** 
![[Pasted image 20250410091807.png]]

## 🔹 2. Chlorthalidone 相關字尾(3)
?
> [!tip] 口訣
> - -thali = 結構特徵：Phthalimidine
> - -Chlor = Cl 取代
> - -idone = 可能表示酮基或內酰胺結構 <!--SR:!2025-04-11,4,270-->

???


## 🔹 3. 特色
#### 🧪 藥理（Pharmacology）

- 不知


#### 🧬 藥化（Medicinal Chemistry）
- 結構特徵：Phthalimidine



#### ⚡副作用（Adverse Effects）

- 高血鈣（PTH促進 $Ca^{2+}$再吸收）、高尿酸血症、高血糖、高血脂、低血鈉 (該類副作用)


## 🔹 4. ADME（藥代動力學）
 - 不重要
## 🔹 5. 比較、連結

- [[Thiazide diuretics]]

##### 同類藥物(3)
?
- [[Quinethazone]]
- [[Indapamide]]
- [[Xipamide]] <!--SR:!2025-04-11,4,270-->

???

###### 藥劑學
> 藥物與隱形眼鏡的交互作用

- Primidone (普利米酮)、Hydrochlorothiazide (氫氯噻嗪)、Chlorthalidone (氯噻酮)：可能引起眼部或眼瞼水腫。
- Rifampin (利福平)：**淚液可能染成橙色**。
- Ribavirin (利巴韋林)：可能導致**鏡片模糊**。
- Salicylates (水楊酸鹽類)：可能引發眼睛發炎。
- Acetazolamide (乙酰唑胺)：可能**改變屈光度**。

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

- Chlorthalidone藥名拆字(3)::-thali = Phthalimidine (特徵)、thai，-Chlor = Cl 取代，-idone = 酮基或內酰胺結構 <!--SR:!2025-04-16,6,250-->
- 所屬類別(3)::利尿劑、Phthalimidine、Thiazide-like Diuretics <!--SR:!2025-04-13,3,250-->
- 結構特徵::Ph**thali**midine <!--SR:!2025-04-13,3,250-->

###### 107-2
73.下列何項利尿劑具有phthalimidine結構，且可開環形成benzophenone衍生物？
(A) metolazone
(B) indapamide
(C) chlorthalidone
(D) quinethazone
?
答案：C <!--SR:!2025-04-13,3,268-->

???