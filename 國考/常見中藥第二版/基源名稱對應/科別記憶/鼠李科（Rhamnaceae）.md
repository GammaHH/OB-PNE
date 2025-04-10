---
category: 中藥生藥學
tags:
  - 中藥科別
created: 2025-03-20
updated: 2025-04-07 19:37
source:
  - 常用中藥第二版
Abstract: 中藥詞卡
sr-due: 2025-05-01
sr-interval: 24
sr-ease: 250
---
#首刷 #review 
>一種中藥材
### 1.概念
- **鼠李科（Rhamnaceae）** 是一類**主要由灌木、喬木與藤本組成的雙子葉開花植物科**，其成員富含**生物鹼、黃酮與蒽醌類化合物**，廣泛應用於**中藥、食品、木材與染料**。代表植物包括 **鼠李（Rhamnus davurica）、酸棗（Ziziphus jujuba var. spinosa）、欖仁（Hovenia dulcis）、美鼠李（Rhamnus cathartica）、大青葉（Rhamnus utilis）**。  
- **主要藥用特性：**  
  - **安神養心**：如 **酸棗仁（Ziziphus jujuba var. spinosa）**，富含**皂苷與黃酮類**，可**寧心安神、補肝養血**，適用於失眠多夢、心悸。  
  - **清熱解毒**：如 **大青葉（Rhamnus utilis）**，含有**蒽醌類與黃酮類**，可**清熱解毒、抗菌抗病毒**，適用於感冒發熱、咽喉腫痛。  
  - **止渴醒酒**：如 **欖仁（Hovenia dulcis）**，富含**二氫楊梅素（Dihydromyricetin）**，可**解酒護肝、滋養胃陰**，適用於醉酒後不適、[[酒精]]性肝損傷。  
  - **潤腸通便**：如 **美鼠李（Rhamnus cathartica）**，含有**蒽醌類瀉劑成分**，可**潤腸通便、排毒養顏**，適用於習慣性便秘者。  

### 2.詞素拆解
- **Rhamn-**（來自希臘文 *ῥάμνος*（rhámnos），意為「鼠李」）  
  - **Rhamnus**（鼠李屬）：代表鼠李科的模式屬，如 **Rhamnus davurica（鼠李）**，其果實與樹皮可用於藥用與染色。  
  - **Rhamnin**（鼠李素）：一種從鼠李屬植物提取的黃酮類化合物，具抗氧化與抗炎作用。  
  - **命名原因：** 以 **鼠李屬（Rhamnus）** 為代表命名，該屬植物普遍具有**生物活性化合物與藥用價值**。  

- **-aceae**（植物科名標準後綴）  

**完整結構：**


- **Rhamnaceae = *Rhamn-*（鼠李屬）+ *-aceae*（植物科後綴）**  
- **意義**：指與 **鼠李屬（Rhamnus）** 相關的整個植物科，即「鼠李科」，其成員通常具有**鎮靜安神、清熱解毒、瀉下與保肝護肝的藥用價值**，並廣泛應用於**中藥、食品、保健品與木材染料行業**。  


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

### 3.鼠李科（Rhamnaceae） 相關知識點

- **Rhamn-**（來自希臘文 *ῥάμνος*（rhámnos），意為「==鼠李==」）  

- RHA 就是鼠李醣的縮寫



