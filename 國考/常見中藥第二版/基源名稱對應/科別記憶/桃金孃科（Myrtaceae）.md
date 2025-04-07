---
category: 中藥生藥學
tags:
  - 中藥科別
created: 2025-03-20
updated: 2025-04-06 22:30
source:
  - 常用中藥第二版
Abstract: 中藥詞卡
sr-due: 2025-04-09
sr-interval: 3
sr-ease: 250
---
#首刷 #review 
### 1.概念
- **桃金孃科（Myrtaceae）** 是一類**主要由喬木或灌木組成的雙子葉開花植物科**，以**芳香精油、抗菌特性與藥用價值**聞名，廣泛應用於**中藥、香精香料、保健食品與園藝**。代表植物包括 **蒲桃（Syzygium samarangense）、番石榴（Psidium guajava）、尤加利（Eucalyptus spp.）、丁香（Syzygium aromaticum）、桃金孃（Myrtus communis）**。  
- **主要藥用特性：**  
  - **抗菌抗炎**：如 **丁香（Syzygium aromaticum）**，富含**丁香酚（Eugenol）**，可**抗菌消炎、鎮痛止咳**，適用於牙痛、消化不良與呼吸道感染。  
  - **收斂止瀉**：如 **番石榴（Psidium guajava）**，其葉富含**單寧與黃酮類**，可**收斂止瀉、降血糖**，適用於腸胃不適與糖尿病輔助治療。  
  - **清熱解毒**：如 **尤加利（Eucalyptus spp.）**，含有**尤加利醇（Eucalyptol）**，可**化痰止咳、清熱抗炎**，適用於感冒與鼻塞。  
  - **強心活血**：如 **桃金孃（Myrtus communis）**，富含**芳香精油與黃酮**，可**強心活血、促進消化**，適用於心血管保健與消化系統調理。

### 2.詞素拆解
- **Myrt-**（來自希臘文 *μύρτος*（mýrtos）「桃金孃」）  
  - **Myrtus**（桃金孃屬）：代表桃金孃科的模式屬，如 **Myrtus communis（桃金孃）**，以其芳香葉片與藥用價值聞名。  
  - **Myrtle**（桃金孃）：來自拉丁詞 *myrtus*，進一步轉化為英語 *myrtle*，象徵純潔與勝利。  
  - **命名原因：** 以 **桃金孃屬（Myrtus）** 為代表命名，該屬植物普遍具有**芳香精油與藥用價值**。  

- **-aceae**（植物科名標準後綴）  

**完整結構：**
- **Myrtaceae = *Myrt-*（桃金孃屬）+ *-aceae*（植物科後綴）**  
- **意義**：指與 **桃金孃屬（Myrtus）** 相關的整個植物科，即「桃金孃科」，其成員通常具有**芳香精油、抗菌消炎、藥用與經濟價值**，並廣泛應用於**中藥、食品、香精香料與園藝**。  

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


### 3.桃金孃科（Myrtaceae） 相關知識點


