---
category: 中藥生藥學
tags:
  - 中藥科別
  - 旋花科
created: 2025-03-20
updated: 2025-04-10 09:31
source:
  - 常用中藥第二版
Abstract: 中藥詞卡
sr-due: 2025-04-21
sr-interval: 14
sr-ease: 230
---
#首刷 #review 
>一種中藥材
### 1.概念
- **旋花科（Convolvulaceae）** 是一類**主要由草本植物與攀緣灌木組成的雙子葉植物**，其植物通常具有**藤蔓性質**，並以**旋轉狀的花形**而得名。這個科別包含了**一些藥用植物與觀賞植物**，常見的植物有 **牽牛花（Ipomoea spp.）、番薯（Ipomoea batatas）**。  
- **主要藥用特性：**  
  - **通便與解毒**：如 **牽牛花（Ipomoea spp.）**，其種子含有**生物鹼**，可**潤腸通便、清熱解毒**，適用於便秘、腸道不適等。  
  - **強心與利尿**：如 **番薯（Ipomoea batatas）**，富含**皂苷和多糖**，可**強化心臟功能、改善水腫與利尿**。  
  - **止痛與抗炎**：如 **牽牛花的葉與根**，含有**黃酮類化合物**，具有一定的**抗炎與鎮痛作用**，可用於緩解風濕性關節炎等症狀。  

### 2.詞素拆解
- **Convolvul-**（來自拉丁文 *convolvulus*，意為「盤繞」或「旋轉」）  
  - **Convolvulus**（旋花屬）：該屬植物的特徵是花朵和藤蔓常呈現盤繞生長狀態，具有攀爬性。  
  - **Twisting vines**（盤繞藤蔓）：該科的植物常有圓形或螺旋狀的藤本結構，能夠攀附其他植物或支撐物生長。  
  - **命名原因：** 以植物的藤本性質與旋轉狀的花型命名，該科的植物特徵通常是具備**旋轉花形與藤本生長**。

- **-aceae**（植物科名標準後綴）

**完整結構：**
- **Convolvulaceae = *Convolvul-*（盤繞、旋轉） + *-aceae*（植物科後綴）**  
- **意義**：指與 **旋花屬（Convolvulus）** 相關的植物科，即「旋花科」，其成員具有**旋轉的花型與藤蔓生長特徵**，廣泛應用於**藥用、觀賞與食物來源**（如番薯）等領域。

#### 📌 相關藥材連結

- [[菟絲子]]

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

### 3.璇花科（Nyssaceae） 相關知識點
- **Nyss-**（來自希臘文 *Nýssa*，指地名）  
  - **Nyssa**（璇花屬）：代表璇花科的模式屬，如 **Nyssa sinensis（璇花樹）**，分布於中國與東南亞。  
  - **命名原因：** 可能源於古希臘傳說中的地名 *Nýssa*，或受神話影響命名。  


- **璇花科（Nyssaceae）** 曾被視為獨立科別，但在最新的**APG植物分類系統**中，通常被歸入**山茱萸科（Cornaceae）**。
