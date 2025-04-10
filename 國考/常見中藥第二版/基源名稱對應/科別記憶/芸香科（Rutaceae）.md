---
category: 中藥生藥學
tags:
  - 中藥科別
  - 芸香科
created: 2025-03-20
updated: 2025-04-10 09:35
source:
  - 常用中藥第二版
Abstract: 中藥詞卡
sr-due: 2025-05-05
sr-interval: 25
sr-ease: 250
---
#首刷 #review 
> **五種中藥材**
### 1.概念
- **芸香科（Rutaceae）** 是一類**富含芳香精油的木本或灌木植物**，包含許多具有**藥用、食用與香料價值**的種類，如 **枳實（Citrus aurantium）、黃柏（Phellodendron chinense）、花椒（Zanthoxylum bungeanum）**。  
- **主要藥用特性：**  
  - **理氣健脾**：如 **枳實（Citrus aurantium）**，含**黃酮類與香豆素**，可**行氣消食、化痰散結**，適用於脾胃氣滯、腹脹消化不良。  
  - **清熱燥濕**：如 **黃柏（Phellodendron chinense）**，富含**小檗鹼（Berberine）**，可**清熱解毒、瀉火燥濕**，常用於濕熱證、感染性疾病。  
  - **溫中散寒**：如 **花椒（Zanthoxylum bungeanum）**，含**揮發油與生物鹼**，能**溫中散寒、止痛驅寒**，適用於脾胃虛寒、寒性疼痛。  
  - **活血化瘀**：如 **吳茱萸（Evodia rutaecarpa）**，含**生物鹼類化合物**，可**溫肝散寒、降逆止嘔**，適用於寒性胃痛、噁心嘔吐。  

### 2.詞素拆解
- **Ruta-**（來自拉丁文 *ruta*，意為「芸香屬」）  
  - **Ruta**（芸香屬）：代表芸香科植物，如 **Ruta graveolens（芸香）**，以強烈芳香與藥用價值著稱。  
  - **Rue**（英語「芸香」）：直接來自拉丁文 *ruta*，用於指芸香植物。  
  - **命名原因：** 以 **芸香屬（Ruta）** 為代表命名，該屬植物具有芸香科典型的**芳香精油與藥用特性**。  

- **-aceae**（植物科名標準後綴）  

**完整結構：**
- **Rutaceae = *Ruta-*（芸香屬）+ *-aceae*（植物科後綴）**  
- **意義**：指與 **芸香屬（Ruta）** 相關的整個植物科，即「芸香科」，其成員通常具有**芳香揮發油、苦味生物鹼、藥用與食用價值**，並廣泛應用於**中藥、香料與園藝**。  

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

### 3.芸香科（Rutaceae） 相關知識點 + 閃卡區
- 芸香科，易與:: [[茜草科（Rubiaceae）]] 搞混，需分清楚
- 嚕他阿謝

  - **Rue**（英語「芸香」）：直接來自拉丁文 *ruta*，用於指芸香植物。  
  - **命名原因：** 以 **芸香屬（Ruta）** 為代表命名，該屬植物具有芸香科典型的**芳香精油與藥用特性**。  

