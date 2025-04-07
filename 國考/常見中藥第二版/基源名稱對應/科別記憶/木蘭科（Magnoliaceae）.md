---
category: 中藥生藥學
tags:
  - 中藥科別
  - 木蘭科
created: 2025-03-20
updated: 2025-04-06 22:30
source:
  - 常用中藥第二版
Abstract: 中藥詞卡
sr-due: 2025-05-06
sr-interval: 30
sr-ease: 290
---
#首刷 #review 
### 1.概念
- **木蘭科（Magnoliaceae）** 是一類**主要為喬木或灌木的開花植物**，以**芳香精油與強韌木質**著稱，包含許多**藥用、觀賞與木材價值**的種類，如 **厚朴（Magnolia officinalis）、辛夷（Magnolia biondii）、玉蘭（Magnolia denudata）**。  
- **主要藥用特性：**  
  - **行氣燥濕**：如 **厚朴（Magnolia officinalis）**，含**木蘭酚（Magnolol）與厚朴酚（Honokiol）**，可**行氣燥濕、消脹止痛**，適用於消化不良、腹脹便秘。  
  - **宣肺通鼻**：如 **[[辛夷]]（Magnolia biondii）**，富含**揮發油與黃酮類**，可**宣肺通鼻、祛風散寒**，常用於鼻炎、鼻塞流涕。  
  - **養顏潤肺**：如 **玉蘭（Magnolia denudata）**，含**芳香揮發油**，可**清熱解毒、潤肺止咳**，適用於咽乾口渴、咳嗽少痰。  
  - **鎮靜安神**：木蘭類植物中的**厚朴酚（Honokiol）** 具有**中樞神經抑制作用**，可**緩解焦慮與失眠**。  

### 2.詞素拆解
- **Magnolia-**（來自法語 *Magnolia*，以植物學家 Pierre Magnol 命名）  
  - **Magnolia**（木蘭屬）：代表木蘭科的模式屬，如 **Magnolia officinalis（厚朴）**，以其藥用與芳香精油著稱。  
  - **命名原因：** 為紀念 **法國植物學家 Pierre Magnol（1638–1715）**，他對植物分類學作出了重大貢獻。  

- **-aceae**（植物科名標準後綴）  

**完整結構：**
- **Magnoliaceae = *Magnolia-*（木蘭屬）+ *-aceae*（植物科後綴）**  
- **意義**：指與 **木蘭屬（Magnolia）** 相關的整個植物科，即「木蘭科」，其成員通常具有**芳香精油、強韌木質、藥用與觀賞價值**，並廣泛應用於**中藥、香料與園藝**。 

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




### 3.木蘭科（Magnoliaceae） 相關知識點



### 4.木蘭科（Magnoliaceae） 相關詞
#### (1) 植物學相關詞-參考




#### (2) 藥用植物相關詞

