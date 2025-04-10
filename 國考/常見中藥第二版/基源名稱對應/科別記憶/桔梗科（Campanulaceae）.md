---
category: 中藥生藥學
tags:
  - 中藥科別
  - 桔梗科
created: 2025-03-20
updated: 2025-04-10 09:28
source:
  - 常用中藥第二版
Abstract: 中藥詞卡
sr-due: 2025-04-13
sr-interval: 3
sr-ease: 230
---
#首刷 #review 
### 1.概念
- **桔梗科（Campanulaceae）** 是一類**主要由草本植物和少數灌木組成的雙子葉植物**，在**藥用、觀賞植物與食用花卉**方面具有重要價值。常見的植物有 **桔梗（Platycodon grandiflorus）、風鈴草（Campanula spp.）**。  
- **主要藥用特性：**  
  - **止咳化痰**：如 **桔梗（Platycodon grandiflorus）**，含有**皂苷**，可**潤肺止咳、化痰**，適用於咳嗽、咳痰不暢等呼吸道疾病。  
  - **清熱解毒**：如 **桔梗根（Platycodon grandiflorus）**，含有**多糖與皂苷**，可**清熱解毒、利尿**，常用於上呼吸道感染、肺炎等治療。  
  - **抗菌消炎**：如 **風鈴草（Campanula spp.）**，含有**黃酮類化合物**，可**抗菌抗炎**，具有一定的藥用價值，適合用於治療炎症相關的疾病。  

### 2.詞素拆解
- **Campanul-**（來自拉丁文 *campanula*，意為「小鐘」）  
  - **Campanula**（風鈴草屬）：該屬植物具有鐘狀花，故得名。  
  - **Bell-shaped flowers**（鐘狀花）：描述了該科植物典型的花型形狀，如風鈴草的花形狀類似鐘，並且富有觀賞價值。  
  - **命名原因：** 以花形狀的特徵命名，這類植物的花型通常呈鐘形，適合用作園藝與藥用。  

- **-aceae**（植物科名標準後綴）

**完整結構：**
- **Campanulaceae = *Campanul-*（鐘形花）+ *-aceae*（植物科後綴）**  
- **意義**：指與 **風鈴草屬（Campanula）** 相關的植物科，即「桔梗科」，其成員通常具有**鐘形花、藥用成分與觀賞價值**，並廣泛應用於**中藥、園藝與觀賞植物領域**。

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

- **Campanul-**（來自拉丁文 *campanula*，意為「==小鐘==」） <!--SR:!2025-04-13,3,230-->  
