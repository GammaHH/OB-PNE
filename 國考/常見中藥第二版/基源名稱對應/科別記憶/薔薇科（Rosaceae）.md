---
category: 中藥生藥學
tags:
  - 中藥科別
  - 薔薇科
created: 2025-03-20
updated: 2025-04-06 20:38
source:
  - 常用中藥第二版
Abstract: 中藥詞卡
sr-due: 2025-04-26
sr-interval: 20
sr-ease: 270
---
#首刷 #review 
> 五種藥材

### 1.概念
- **薔薇科（Rosaceae）** 是一類廣泛分布的**木本與草本植物**，包含許多**水果類、藥用與觀賞植物**，如 **玫瑰（Rosa spp.）、山楂（Crataegus pinnatifida）、桃（Prunus persica）、枇杷（Eriobotrya japonica）** 等。  
- **主要藥用特性：**  
  - **生津潤肺**：如 **枇杷葉（Eriobotrya japonica）**，含**三萜類化合物**，可**潤肺止咳、降氣化痰**，常用於呼吸道疾病。  
  - **活血化瘀**：如 **山楂（Crataegus pinnatifida）**，富含**黃酮類與有機酸**，能**促進血液循環、消食化積**，用於高血脂、消化不良。  
  - **補氣養血**：如 **桃仁（Prunus persica）**，含**苦杏仁苷**，具有**活血祛瘀、潤腸通便**之效。  
  - **收斂止瀉**：如 **覆盆子（Rubus idaeus）**，富含**鞣質與黃酮**，可**固精縮尿、補腎**，常用於腎虛遺精與尿頻。

### 2.詞素拆解
- **Rosa-**（來自拉丁文 *rosa*，意為「玫瑰、薔薇」）  
  - **Rose**（玫瑰）：直接來自拉丁詞 *rosa*，指薔薇屬植物。  
  - **Rosin**（松香）：雖然來自松樹，但因其氣味與某些薔薇科植物相似而得名。  
  - **Rosette**（葉叢、花冠狀構造）：來自 *rosa*，指類似玫瑰花形的結構。  
  - **命名原因：** 以 **薔薇屬（Rosa）** 為代表命名，該屬植物具有該科典型的**花朵形態與芳香特性**。  

- **-aceae**（植物科名標準後綴）  

**完整結構：**

- **Rosaceae = *Rosa-*（薔薇屬）+ *-aceae*（植物科後綴）**  
- **意義**：指與 **薔薇屬（Rosa）** 相關的整個植物科，即「薔薇科」，其成員通常具有**芳香花朵、多汁果實、藥用與營養價值**，並廣泛應用於**藥用、食用與園藝**。  
#### 📌 相關藥材連結



```dataviewjs
// ---------- 標籤推薦區塊（以列表呈現） ----------
const excludeTags = ["中藥科別"];
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


### 3.薔薇科（Rosaceae） 相關知識點




