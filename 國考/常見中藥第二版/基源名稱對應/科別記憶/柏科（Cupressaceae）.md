---
category: 中藥生藥學
tags:
  - 中藥科別
  - 柏科
created: 2025-03-20
updated: 2025-04-07 10:18
source:
  - 常用中藥第二版
Abstract: 中藥詞卡
sr-due: 2025-04-16
sr-interval: 9
sr-ease: 210
---
#首刷 #review 
>兩種中藥材
### 1.概念
- **柏科（Cupressaceae）** 主要為**常綠喬木或灌木**，廣泛分布於全球溫帶地區，許多種類**富含揮發油與抗菌成分**，具有**藥用、園藝與木材價值**，如 **側柏（Platycladus orientalis）、圓柏（Juniperus spp.）、紅杉（Sequoia sempervirens）**。  
- **主要藥用特性：**  
  - **清熱止血**：如 **側柏葉（Platycladus orientalis）**，富含**黃酮類與單寧**，可**涼血止血、化痰止咳**，適用於咳血、吐血、衄血等出血症狀。  
  - **溫腎壯陽**：如 **圓柏（Juniperus communis）**，含**揮發油與生物鹼**，可**利尿消腫、溫腎補陽**，適用於腎虛水腫、風濕關節痛。  
  - **安神助眠**：如 **紅杉（Sequoia sempervirens）**，其木材與葉片的芳香精油可用於**舒緩壓力、改善失眠**，常見於芳香療法。  
  - **抗菌消炎**：如 **柏樹類（Cupressus spp.）**，富含**抗氧化成分與抗菌活性化合物**，能有效**抑制細菌與真菌感染**，常用於藥物與天然保健品。  

### 2.詞素拆解
- **Cupress-**（來自拉丁文 *cupressus*，意為「柏樹」）  
  - **Cupressus**（柏屬）：典型柏科植物，如 **Cupressus sempervirens（地中海柏）**，以其**防風耐旱、木材堅硬耐久**聞名。  
  - **Cypress**（英語「柏樹」）：直接來自拉丁文 *cupressus*，經古法語 *cipres* 演變而來。  
  - **命名原因：** 以 **柏屬（Cupressus）** 為代表命名，該屬植物具有柏科典型的**芳香精油與木材耐久特性**。  

- **-aceae**（植物科名標準後綴）  

**完整結構：**
- **Cupressaceae = *Cupress-*（柏屬）+ *-aceae*（植物科後綴）**  
- **意義**：指與 **柏屬（Cupressus）** 相關的整個植物科，即「柏科」，其成員通常具有**芳香精油、抗菌成分、藥用與木材價值**，並廣泛應用於**中藥、建築木材、香氛與保健**。  

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


### 3.柏科（Cupressaceae） 相關知識點

-  **Cypress**（英語「==柏樹==」）：直接來自拉丁文 *cupressus*，經古法語 *cipres* 演變而來。 <!--SR:!2025-04-10,3,230-->  


