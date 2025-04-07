---
category: 中藥生藥學
tags:
  - 中藥科別
  - 棕櫚科
created: 2025-03-20
updated: 2025-04-07 10:11
source:
  - 常用中藥第二版
Abstract: 中藥詞卡
sr-due: 2025-04-16
sr-interval: 9
sr-ease: 210
---
#首刷 #review 
>兩種中藥材
### 1.概念
- **棕櫚科（Arecaceae）** 是一類**主要由喬木與灌木組成的單子葉開花植物科**，以**發達的樹幹、羽狀或掌狀葉、*豐富的油脂與纖維***著稱，廣泛應用於**食品、藥用、建築與園藝**。代表植物包括 **椰子（Cocos nucifera）、棕櫚（Areca catechu）、油棕（Elaeis guineensis）、蒲葵（Livistona chinensis）**。  
- **主要藥用特性：**  
  - **驅蟲消積**：如 **檳榔（Areca catechu）**，富含**檳榔鹼（Arecoline）**，可**驅蟲消積、行氣利水**，適用於腸道寄生蟲、消化不良。  
  - **滋補強壯**：如 **椰子（Cocos nucifera）**，其果實與椰子水富含**脂肪與電解質**，可**補充體力、增強免疫**，適用於營養不良、虛弱體質。  
  - **潤腸通便**：如 **油棕（Elaeis guineensis）**，其果實含有**豐富的棕櫚油**，可**滋潤腸道、促進排便**，適用於腸燥便秘。  
  - **清熱利尿**：如 **蒲葵（Livistona chinensis）**，富含**生物鹼與黃酮**，可**清熱利水、止血**，適用於尿道炎、血尿。

### 2.詞素拆解
- **Areca-**（來自馬來語 *areca*，意為「檳榔」）  
  - **Areca**（檳榔屬）：代表棕櫚科的模式屬，如 **Areca catechu（檳榔）**，以其果實具有興奮作用而聞名。  
  - **命名原因：** 檳榔在東南亞地區**廣泛種植與使用**，因此以該屬植物命名整個科。  

- **-aceae**（植物科名標準後綴） 

**完整結構：**
- **Arecaceae = *Areca-*（檳榔屬）+ *-aceae*（植物科後綴）**  
- **意義**：指與 **檳榔屬（Areca）** 相關的整個植物科，即「棕櫚科」，其成員通常具有**發達的幹部、堅韌的纖維、豐富的油脂與藥用價值**，並廣泛應用於**食品、藥用、建築與園藝領域**。  

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



### 3.棕櫚科（Arecaceae） 相關知識點


- **Areca-**（來自馬來語 *areca*，意為「==檳榔==」）  

- **棕櫚科（Arecaceae）** 是一類**主要由喬木與灌木組成的單子葉開花植物科**，以**發達的樹幹、羽狀或掌狀葉、*豐富的油脂與纖維***著稱
