---
category: 中藥生藥學
tags:
  - 中藥科別
  - 桑科
created: 2025-03-20
updated: 2025-04-07 10:14
source:
  - 常用中藥第二版
Abstract: 中藥詞卡
sr-due: 2025-04-14
sr-interval: 7
sr-ease: 210
---
#首刷 #review 
> 三種中藥材
### 1.概念
- **桑科（Moraceae）** 是一類**主要為喬木、灌木或藤本植物**的開花植物，包含許多**藥用、食用與工業價值**的種類，如 **桑樹（Morus alba）、無花果（Ficus carica）、構樹（Broussonetia papyrifera）**。  
- **主要藥用特性：**  
  - **補肝腎、益氣血**：如 **桑椹（Morus alba）**，富含**花青素與黃酮類**，可**滋陰補血、養肝腎**，適用於血虛、目暗、腎虛腰膝酸軟。  
  - **清肺潤燥**：如 **桑葉（Morus alba）**，含有**黃酮與生物鹼**，可**清肺潤燥、平抑肝陽**，適用於肺熱咳嗽、頭暈目眩。  
  - **消腫利尿**：如 **構樹皮（Broussonetia papyrifera）**，可**清熱利尿、消腫散結**，適用於水腫、小便不利。  
  - **健脾消食**：如 **無花果（Ficus carica）**，富含**多酚類與可溶性纖維**，可**健脾開胃、助消化**，適用於脾胃虛弱、消化不良。  

### 2.詞素拆解
- **Mora-**（來自拉丁文 *morus*，意為「桑樹」）  
  - **Morus**（桑屬）：代表桑科的模式屬，如 **Morus alba（白桑）**，以其葉可餵養蠶，果實可食或入藥。  
  - **Mulberry**（英語「桑樹」）：來自拉丁文 *morus*，經古英語 *morberie* 演變而來。  
  - **命名原因：** 以 **桑屬（Morus）** 為代表命名，該屬植物為桑科的典型成員，具有**藥用與養蠶經濟價值**。  

- **-aceae**（植物科名標準後綴）  

**完整結構：**
- **Moraceae = *Mora-*（桑屬）+ *-aceae*（植物科後綴）**  
- **意義**：指與 **桑屬（Morus）** 相關的整個植物科，即「桑科」，其成員通常具有**乳汁分泌組織、特殊花序（隱頭花序或穗狀花序）、藥用與經濟價值**，並廣泛應用於**中藥、食品與造紙業**。 

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




### 3.桑科（Moraceae） 相關知識點

- **Mora-**（來自拉丁文 *morus*，意為「==桑樹==」） <!--SR:!2025-04-10,3,230-->  

- **Morus**（桑屬）：代表桑科的模式屬，如 **Morus alba（白桑）**，以其葉可餵養蠶，果實可食或入藥。  
- **Mulberry**（英語「桑樹」）：來自拉丁文 *morus*，經古英語 *morberie* 演變而來。  




