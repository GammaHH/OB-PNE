---
category: 中藥生藥學
tags:
  - 中藥科別
  - 車前科
created: 2025-03-21
updated: 2025-04-10 09:29
source:
  - 常用中藥第二版
Abstract: 中藥詞卡
sr-due: 2025-04-12
sr-interval: 16
sr-ease: 290
---
#首刷 #review
>一種中藥材
### 1.概念
- **車前科（Plantaginaceae）** 是一類**多年生草本為主的雙子葉植物科**，傳統上分類簡單，但在**APG(被子植物親緣關係小組)現代分類系統中已大幅擴展**，納入許多原屬[[玄參科（Scrophulariaceae）]]的植物。其成員廣泛分布，常見於路邊、草地、濕地等地，具備**藥用、園藝與生態價值**。  
- 代表藥用植物如 **車前草（Plantago asiatica）**，具**清熱利尿、化痰止咳**之效，其他如 **筋骨草（Scoparia dulcis）** 等也具藥用潛力。 

### 2.詞素拆解
- **Plantagin-**  
  來自拉丁文 *plantago*，原指「車前草」  
  - *Planta*（腳掌）+ *-ago*（表示某類物）→ 因葉形扁平如足掌而得名  
  - **Plantago**：車前屬，是車前科的模式屬，如 *Plantago asiatica*（車前草）  
  - 與英文 *plantain*（車前草）同源  

- **-aceae**  
  植物科名標準後綴，表示「某某科」  

**完整結構：**
- *Stemonaceae = **Stemon**-（百部屬）+ -**aceae**（植物科後綴）* → 指與百部屬（Stemona）相關的整個植物科，即「百部科」，其成員多為地下具塊根的草本植物，富含生物鹼與具藥用價值，廣泛應用於止咳與殺蟲等領域。

#### 📌 相關藥材連結

```dataviewjs
const excludeTags = ["中藥科別","中藥生藥學"];
const currentTags = dv.current().tags?.filter(t => !excludeTags.includes(t)) ?? [];

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
let multiPaths = new Set(multiMatch.map(p => p.file.path));
let totalUnique = new Set([...multiMatch, ...singleMatch].map(p => p.file.path)).size;

dv.header(5, `相關藥物（共 ${totalUnique} 筆）`);

if (multiMatch.length > 0) {
  dv.header(6, `▸ ${currentTags.join("、")}（${multiMatch.length}）`);
  dv.list(
    multiMatch.map(p => {
      const tagsToShow = p.tags.filter(t => !excludeTags.includes(t));
      return `${p.file.link}　${tagsToShow.join("、")}`;
    })
  );
}

// 顯示單一標籤命中分類後的筆記
for (let [tag, pages] of Object.entries(singleGroups)) {
  dv.header(6, `▸ ${tag}（${pages.length}）`);
  dv.list(
    pages.map(p => {
      const tagsToShow = p.tags.filter(t => !excludeTags.includes(t) && t !== tag);
      return `${p.file.link}　${tagsToShow.join("、")}`;
    })
  );
}
if (multiMatch.length === 0 && Object.keys(singleGroups).length === 0) {

  dv.paragraph("沒有找到與本藥材具有相同標籤的其他筆記。");
}

```

### 3.車前科（Plantaginaceae） 相關知識點

- **Plantagin-**  
  來自拉丁文 *plantago*，原指「車前草」  
  - *Planta*（腳掌）+ *-ago*（表示某類物）→ 因葉形扁平如足掌而得名  


### 4.閃卡區


- **Plantagin-**  
  來自拉丁文 *plantago*，原指「==車前草==」  
  - *Planta*（腳掌）+ *-ago*（表示某類物）→ 因葉形扁平如足掌而得名  