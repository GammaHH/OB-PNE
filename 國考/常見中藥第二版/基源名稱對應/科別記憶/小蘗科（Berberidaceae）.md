---
category: 中藥生藥學
tags:
  - 中藥科別
  - 小蘗科
created: 2025-03-20
updated: 2025-04-06 22:34
source:
  - 常用中藥第二版
Abstract: 中藥詞卡
sr-due: 2025-05-06
sr-interval: 30
sr-ease: 290
---
#首刷 #review 
>一種中藥材
### 1.概念
- **小蘗科（Berberidaceae）** 是一類**主要由灌木與草本植物組成的雙子葉開花植物科**，以**富含生物鹼、苦味成分與抗菌特性**著稱，廣泛應用於**中藥、保健品與園藝**。代表植物包括 **小蘗（Berberis spp.）、黃連（Coptis chinensis，部分分類仍歸於此科）、淫羊藿（Epimedium spp.）、八角蓮（Dysosma versipellis）**。  
- **主要藥用特性：**  
  - **清熱解毒**：如 **黃連（Coptis chinensis）**，富含**小檗鹼（Berberine）**，可**清熱燥濕、抗菌消炎**，適用於腸胃炎、痢疾與感染性疾病。  
  - **補腎壯陽**：如 **淫羊藿（Epimedium spp.）**，含有**淫羊藿苷（Icariin）**，可**補腎助陽、強筋壯骨**，適用於腎虛陽痿、筋骨衰弱。  
  - **活血化瘀**：如 **八角蓮（Dysosma versipellis）**，富含**鬼臼毒素（Podophyllotoxin）**，可**抗腫瘤、活血化瘀**，適用於腫瘤治療與血瘀體質者。  
  - **保肝利膽**：如 **小蘗（Berberis spp.）**，富含**小檗鹼與黃酮類**，可**促進膽汁分泌、保護肝臟**，適用於膽囊炎、黃疸型肝炎。

### 2.詞素拆解
- **Berberid-**（來自拉丁文 *berberis*，意為「小蘗」）  
  - **Berberis**（小蘗屬）：代表小蘗科的模式屬，如 **Berberis vulgaris（歐洲小蘗）**，以其富含小檗鹼而聞名。  
  - **Berberine**（小檗鹼）：來自 *Berberis*，指該屬植物中提取的主要生物鹼，具有強效的抗菌與抗炎作用。  
  - **命名原因：** 以 **小蘗屬（Berberis）** 為代表命名，該屬植物具有**抗菌消炎、藥用活性與苦味成分**。  

- **-aceae**（植物科名標準後綴）

**完整結構：**
- **Berberidaceae = *Berberid-*（小蘗屬）+ *-aceae*（植物科後綴）**  
- **意義**：指與 **小蘗屬（Berberis）** 相關的整個植物科，即「小蘗科」，其成員通常具有**生物鹼成分、清熱燥濕、抗菌消炎與補腎壯陽的藥用價值**，並廣泛應用於**中藥、保健品與園藝領域**。  

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



### 3.小蘗科（Berberidaceae） 相關知識點


