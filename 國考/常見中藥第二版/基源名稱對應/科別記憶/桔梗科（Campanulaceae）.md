---
category: 中藥生藥學
tags:
  - 中藥科別
created: 2025-03-20
updated: 2025-04-06 22:29
source:
  - 常用中藥第二版
Abstract: 中藥詞卡
sr-due: 2025-04-09
sr-interval: 3
sr-ease: 250
---
#首刷 #review 
### 1.概念
- **柏科（Cupressaceae）** 是一類**主要由常綠喬木與灌木組成的裸子植物**，在**藥用、建材與芳香精油**方面具有重要價值，包含 **側柏（Platycladus orientalis）、檜木（Chamaecyparis spp.）、紅杉（Sequoia spp.）**。  
- **主要藥用特性：**  
  - **收斂止血**：如 **側柏葉（Platycladus orientalis）**，富含**黃酮與單寧**，可**涼血止血、化痰止咳**，適用於咯血、便血與脫髮治療。  
  - **鎮靜安神**：如 **柏子仁（Biota orientalis，今為 Platycladus orientalis）**，含**脂肪油與黃酮類**，可**養心安神、潤腸通便**，適用於心悸失眠與腸燥便秘。  
  - **抗菌消炎**：如 **檜木（Chamaecyparis spp.）**，富含**萜類化合物**，可**抗菌抗炎、驅蟲防腐**，常用於香薰精油與木材防腐。  
  - **活血通絡**：如 **紅杉（Sequoia sempervirens）**，含有**強效抗氧化物**，可**促進血液循環、減緩衰老**，部分應用於保健品與中藥材。 

### 2.詞素拆解
- **Cupress-**（來自拉丁文 *cupressus*，意為「柏樹」）  
  - **Cupressus**（柏屬）：典型柏科植物，如 **Cupressus sempervirens（地中海柏）**，常見於公園與墓園。  
  - **Cypress**（英語「柏樹」）：直接來自拉丁詞 *cupressus*，指柏樹類植物，尤其是地中海柏與美國柏類。  
  - **命名原因：** 以 **柏屬（Cupressus）** 為代表命名，該屬植物具有**耐寒、芳香精油與建材價值**。  

- **-aceae**（植物科名標準後綴）  

**完整結構：**
- **Cupressaceae = *Cupress-*（柏樹屬）+ *-aceae*（植物科後綴）**  
- **意義**：指與 **柏屬（Cupressus）** 相關的整個植物科，即「柏科」，其成員通常具有**芳香精油、藥用成分、建築木材與園藝價值**，並廣泛應用於**中藥、香薰、木材與保健領域**。  

#### 📌 相關藥材連結




```dataviewjs
const excludeTags = ["中藥科別","中藥生藥學"];
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
        pages.map(p => {
          const tagsToShow = p.tags?.filter(t => !excludeTags.includes(t) && t !== tag) ?? [];
          return `${p.file.link}　${tagsToShow.join("、")}`;
        })
      );
    }
  }
} else {
  dv.header(5, "相關藥物（0）");
  dv.paragraph("沒有找到與本藥材具有相同標籤的其他筆記。");
}
```


### 3.桔梗科（Campanulaceae） 相關知識點


