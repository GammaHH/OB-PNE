---
category: 中藥生藥學
tags:
  - 中藥科別
  - 紫草科
created: 2025-03-21
updated: 2025-04-08 09:27
source:
  - 常用中藥第二版
Abstract: 中藥詞卡
sr-due: 2025-05-07
sr-interval: 30
sr-ease: 290
---
#首刷 #review
### 1.概念
- **紫草科（Boraginaceae）** 是一類**主要由草本、灌木或少數木本組成的雙子葉植物科**，廣泛分布於**溫帶至熱帶地區，尤以地中海地區種類最豐富**。  
- 本科植物常具**粗毛莖葉、螺旋狀聚繖花序、五裂花冠**，部分根部或莖含有**紫色色素與萜類、生物鹼等藥用成分**。  
- 代表藥用植物包括：  
  - **紫草（Lithospermum erythrorhizon）**：入藥部位為根，含**紫草素**，具清熱解毒、涼血活血功效  
  - **琉璃苣（Borago officinalis）**：歐洲常用草藥，有抗發炎、利尿、調節荷爾蒙等作用  
  - **勿忘我（Myosotis spp.）**：主要作觀賞植物  

### 2.詞素拆解
- **Boragin-**  
  來自模式屬 *Borago*（琉璃苣），拉丁化自阿拉伯語 *abu ʿaraq*，意為「出汗之父」，古人認為其具有**發汗與興奮作用**。  
  - *Borago officinalis*：為古歐洲常用草藥，具有利尿與鎮靜效果  
  - 詞根 *Bora-* 在語源學上也可能與「毛茸茸」相關，形容其莖葉上密布粗毛  

- **-aceae**  
  植物科名標準後綴，表示某某植物家族  

**完整結構：**
- **Boraginaceae** = *Boragin-*（來自琉璃苣屬 *Borago*，可能意為「出汗、粗毛植物」）+ *-aceae*（植物科後綴）  
→ 指與 **Borago 屬** 相關的整個植物科，即「紫草科」。其成員常具有**粗毛莖葉、紫紅色根部色素與藥用成分**，在**中藥（紫草）與歐洲草藥（琉璃苣）** 中均有應用，具清熱解毒、抗炎與荷爾蒙調節等多重價值。  


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



### 3.紫草科（Boraginaceae） 相關知識點

- **Boraginaceae** = *Boragin-*（來自琉璃苣屬 *Borago*，可能意為「出汗、粗毛植物」）+ *-aceae*（植物科後綴）  


### 4.閃卡區


- 紫草科:::（Boraginaceae）


- **Boragin-**  紫草、紫草科（Boraginaceae）
??
  來自模式屬 *Borago*（琉璃苣），拉丁化自阿拉伯語 *abu ʿaraq*，意為「==出汗之父==」，古人認為其具有**發汗與興奮作用**。 <!--SR:!2025-04-08,1,250-->