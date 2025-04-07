---
category: 中藥生藥學
tags:
  - 中藥科別
  - 列當科
created: 2025-03-20
updated: 2025-04-07 10:05
source:
  - 常用中藥第二版
Abstract: 中藥詞卡
sr-due: 2025-04-15
sr-interval: 8
sr-ease: 210
---
#首刷 #review 
### 1.概念
- **列當科（Orobanchaceae）** 是一類**主要為寄生性或半寄生性的雙子葉開花植物科**，其中許多成員寄生於**其他植物的根部**，並具有**特殊的生理適應與藥用價值**。代表植物包括 **列當（Orobanche spp.）、[[肉蓯蓉]]（Cistanche deserticola）、鹽生[[肉蓯蓉]]（Cistanche tubulosa）、假馬先蒿（Pedicularis spp.）**。  
- **主要藥用特性：**  
  - **補腎壯陽**：如 **[[肉蓯蓉]]（Cistanche deserticola）**，富含**苯乙醇苷（Echinacoside）與皂苷類**，可**補腎助陽、潤腸通便**，適用於腎虛陽痿、腸燥便秘。  
  - **強筋健骨**：如 **鹽生[[肉蓯蓉]]（Cistanche tubulosa）**，含有**酚類化合物與多醣**，可**補肝腎、強壯筋骨**，適用於腰膝酸軟、筋骨無力。  
  - **活血祛瘀**：如 **列當（Orobanche spp.）**，富含**黃酮與生物鹼**，可**活血通絡、補益精血**，適用於氣血虛弱、疲勞乏力。  
  - **祛風除濕**：如 **假馬先蒿（Pedicularis spp.）**，含有**生物鹼與黃酮類**，可**祛風除濕、舒筋活絡**，適用於風濕關節痛、筋骨僵硬。 

### 2.詞素拆解
- **Orobranch-**（來自希臘文 *ὄροβος*（orobos）「野豌豆」+ *ἄγχω*（anchō）「扼殺」）  
  - **Orobanche**（列當屬）：代表列當科的模式屬，如 **Orobanche crenata（皺葉列當）**，其寄生於豆科植物根部。  
  - **Oro-**（野豌豆）：來自希臘文 *ὄροβος*（orobos），指某些列當科植物常寄生於豆科植物。  
  - **Branch-**（扼殺）：來自希臘文 *ἄγχω*（anchō），意為「扼殺、窒息」，形容該科植物的寄生特性。  
  - **命名原因：** 該科植物以**寄生性與吸收宿主養分**而得名，強調其對宿主植物的影響。  

- **-aceae**（植物科名標準後綴）  


**完整結構：**
- **Orobanchaceae = *Orobranch-*（列當屬）+ *-aceae*（植物科後綴）**  
- **意義**：指與 **列當屬（Orobanche）** 相關的整個植物科，即「列當科」，其成員通常具有**寄生性、補腎壯陽、強筋活血的藥用特性**，並廣泛應用於**中藥、保健品與生態研究**。  

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



### 3.列當科（Orobanchaceae） 相關知識點

- **Orobranch-**（來自希臘文 *ὄροβος*（orobos）「野豌豆」+ *ἄγχω*（anchō）「扼殺」）  
- **Branch-**（扼殺）：來自希臘文 *ἄγχω*（anchō），意為「扼殺、窒息」，形容該科植物的寄生特性。  
