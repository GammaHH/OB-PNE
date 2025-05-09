---
category: 中藥生藥學
tags:
  - 中藥科別
  - 多孔菌科
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
>兩種中藥材
### 1.概念
- **多孔菌科（Polyporaceae）** 是一類**以木材為基質生長的大型腐生或共生真菌**，其子實體通常具有**多孔的孢子管結構**，而非傳統的菌褶。這類真菌在**藥用、森林分解與生態系統平衡**方面具有重要作用。代表屬種包括 **靈芝（Ganoderma spp.）、雲芝（Trametes versicolor）、松杉靈芝（Phellinus spp.）、茯苓（Wolfiporia extensa，部分分類歸入別科）**。  
- **主要藥用特性：**  
  - **補氣安神**：如 **靈芝（Ganoderma lucidum）**，富含**三萜類與多醣**，可**補氣安神、增強免疫**，適用於失眠、免疫力低下者。  
  - **抗腫瘤、調節免疫**：如 **雲芝（Trametes versicolor）**，含**雲芝多醣（PSK）**，可**增強免疫力、輔助癌症治療**，常用於腫瘤患者輔助治療。  
  - **抗炎清熱**：如 **松杉靈芝（Phellinus linteus）**，富含**黃酮類與多醣**，可**清熱解毒、抗炎**，適用於慢性炎症與肝病護理。  
  - **健脾利水**：如 **茯苓（Wolfiporia extensa）**，含**多醣與生物鹼**，可**健脾補中、利水滲濕**，適用於脾虛水腫、失眠健忘。 

### 2.詞素拆解
- **Polypor-**（來自希臘文 *πολύς* *πορος*，意為「多孔」）  
  - **Poly-**（多）：來自希臘文 *πολύς*（polýs），意為「多數的」。  
  - **Por-**（孔）：來自希臘文 *πορος*（poros），意為「孔、通道」。  
  - **Polypore**（多孔菌）：來自拉丁化的 *Polyporus*，指這類真菌的孢子管具有**多孔結構**，與一般菌褶不同。  
  - **命名原因：** 以 **多孔菌屬（Polyporus）** 為代表命名，該屬植物具有**多孔孢子管的形態特徵**。  

- **-aceae**（真菌科名標準後綴）  

**完整結構：**
- **Polyporaceae = *Polypor-*（多孔菌屬）+ *-aceae*（真菌科後綴）**  
- **意義**：指與 **多孔菌屬（Polyporus）** 相關的整個真菌科，即「多孔菌科」，其成員通常具有**木材腐生性、多孔孢子管、藥用與生態分解價值**，並廣泛應用於**中藥、功能性食品與森林生態系統**。  

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




### 3.多孔菌科（Polyporaceae） 相關知識點


