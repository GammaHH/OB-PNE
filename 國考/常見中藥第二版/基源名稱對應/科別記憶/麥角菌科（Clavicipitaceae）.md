---
category: 中藥生藥學
tags:
  - 中藥科別
  - 麥角菌科
created: 2025-03-20
updated: 2025-04-07 11:36
source:
  - 常用中藥第二版
Abstract: 中藥詞卡
sr-due: 2025-04-18
sr-interval: 11
sr-ease: 230
---
#首刷 #review 
>一種藥材
### 1.概念
- **麥角菌科（Clavicipitaceae）** 是一類**主要由寄生性與共生性真菌組成的子囊菌門（Ascomycota）真菌科**，其中許多成員寄生於**昆蟲、植物（特別是禾本科植物）或其他真菌**，並具有**多種生物活性化合物**，被廣泛應用於**中藥、藥理研究與農業**。代表屬種包括 **麥角菌屬（Claviceps）、蟲草菌屬（Cordyceps，部分分類仍歸於此科）、擬蟲草菌屬（Metarhizium）**。  
- **主要藥用特性：**  
  - **血管收縮、治療偏頭痛**：如 **麥角菌（Claviceps purpurea）**，富含**麥角鹼（Ergot alkaloids）**，可**收縮血管、降低偏頭痛發作**，但過量使用會導致麥角中毒（ergotism）。  
  - **補肺益腎、抗疲勞**：如 **蟲草（Cordyceps sinensis，現分類為 Ophiocordyceps sinensis）**，含有**蟲草素（Cordycepin）與多醣**，可**補肺益腎、增強免疫**，適用於氣虛勞損。  
  - **抗菌抗病毒**：如 **擬蟲草（Metarhizium spp.）**，可產生**多種抗菌化合物**，應用於生物農藥與抗菌劑的開發。  
  - **神經調節、治療帕金森病**：某些麥角鹼類衍生物，如**溴隱亭（Bromocriptine）**，可**模擬多巴胺作用、用於帕金森病治療**。  

### 2.詞素拆解
- **Clavicipit-**（來自拉丁文 *clava*「棒狀」+ *caput*「頭」）  
  - **Claviceps**（麥角菌屬）：代表麥角菌科的模式屬，如 **Claviceps purpurea（黑麥角菌）**，其子實體呈現棒狀結構。  
  - **Clavi-**（棒狀）：來自拉丁文 *clava*，指某些麥角菌的孢子體或菌體呈棒狀。  
  - **Capit-**（頭部）：來自拉丁文 *caput*，形容子囊孢子產生部位的結構。  
  - **命名原因：** 麥角菌的子實體呈**棒狀結構**，因此以 *Claviceps* 命名。  

- **-aceae**（真菌科名標準後綴）  

**完整結構：**
- **Clavicipitaceae = *Clavicipit-*（麥角菌屬）+ *-aceae*（真菌科後綴）**  
- **意義**：指與 **麥角菌屬（Claviceps）** 相關的整個真菌科，即「麥角菌科」，其成員通常具有**寄生性、產生多種生物活性化合物、藥用與農業價值**，並廣泛應用於**中藥、藥理研究與生物農藥**。  

#### 📌 相關藥材連結

- [[冬蟲夏草]]


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



### 3.麥角菌科（Clavicipitaceae） 相關知識點

- **Clavicipit-**（來自拉丁文 *clava*「==棒狀==」+ *caput*「==頭==」）  ，即麥角菌的形態特徵



