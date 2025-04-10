---
category: 中藥生藥學
tags:
  - 中藥科別
  - 蠶蛾科
created: 2025-03-20
updated: 2025-04-10 09:26
source:
  - 常用中藥第二版
Abstract: 中藥詞卡
sr-due: 2025-04-11
sr-interval: 2
sr-ease: 230
---
#首刷 #review 
> 一種中藥材
### 1.概念
- **蠶蛾科（Bombycidae）** 是**鱗翅目（Lepidoptera）中的一類昆蟲科**，以**桑葉為食的幼蟲（蠶）與經濟價值**著稱，主要用於**蠶絲生產、科學研究與中藥**。代表物種包括 **家蠶（Bombyx mori）、野蠶（Bombyx mandarina）、白尾蠶（Theophila religiosa）**。  
- **主要經濟與藥用特性：**  
  - **蠶絲生產**：如 **家蠶（Bombyx mori）**，幼蟲吐絲可用於**製作高品質蠶絲**，應用於紡織業與醫學材料（如可吸收縫線）。  
  - **中藥應用**：如 **僵蠶（白殭蠶，Bombyx batryticatus）**，指被**白殭菌感染的蠶蛹**，含有**蛋白酶與多種生物活性物質**，可**祛風止痙、化痰散結**，適用於中風癱瘓、頑固性咳嗽。  
  - **抗菌抗炎**：蠶蛾科昆蟲體內富含**蠶素（Sericin）與抗菌肽**，可**促進傷口癒合、抗氧化與抑菌**，應用於生物醫學。  
  - **營養與保健**：蠶蛹富含**蛋白質、不飽和脂肪酸與微量元素**，在部分地區被用作**高蛋白食品**，具有增強免疫力的潛力。  

### 2.詞素拆解
- **Bombyc-**（來自拉丁文 *bombyx*，意為「蠶、絲」）  
  - **Bombyx**（蠶屬）：代表蠶蛾科的模式屬，如 **Bombyx mori（家蠶）**，該物種是**蠶絲生產的主要來源**。  
  - **Bombycine**（與蠶有關的）：指與蠶或蠶絲有關的特性，例如「蠶絲蛋白」（Bombycine protein）。  
  - **命名原因：** 以 **蠶屬（Bombyx）** 為代表命名，強調該科昆蟲的**吐絲能力與經濟價值**。  

- **-idae**（動物科名標準後綴） 

**完整結構：**
- **Bombycidae = *Bombyc-*（蠶屬）+ *-idae*（動物科後綴）**  
- **意義**：指與 **蠶屬（Bombyx）** 相關的整個動物科，即「蠶蛾科」，其成員通常具有**吐絲能力、飼養於桑葉、經濟與藥用價值**，並廣泛應用於**紡織業、中藥、保健食品與生物科技**。

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



- [[白僵蠶]]

### 3.蠶蛾科（Bombycidae） 相關知識點




