---
category: 中藥生藥學
tags:
  - 中藥科別
  - 罌粟科
created: 2025-03-21
updated: 2025-04-09 13:42
source:
  - 常用中藥第二版
Abstract: 中藥詞卡
sr-due: 2025-05-09
sr-interval: 30
sr-ease: 290
---
#首刷 #review
> 一種中藥材
### 1.概念
- **罌粟科（Papaveraceae）** 是一類**主要由草本植物組成的雙子葉植物科**，分布於**溫帶與寒帶地區**，部分種類亦分布於亞熱帶。此科植物常具有**乳汁（乳液）、艷麗花朵與多種生物鹼成分**，特別以其**中樞神經作用與止痛藥用價值**聞名。  
- 代表植物包括：  
  - **罌粟（Papaver somniferum）**：提煉鴉片、嗎啡、可待因等  
  - **紫堇（Corydalis spp.）**：含多種異喹啉類生物鹼，具鎮痛、活血作用  
  - **血根草（Sanguinaria canadensis）**：具抗菌成分  

### 2.詞素拆解
- **Papaver-**  
  來自拉丁文 *papaver*，意為「罌粟」。  
  - 此詞可能與拉丁語 *pappa*（糊狀物）相關，源於罌粟乳汁具凝稠性，亦可能與安眠作用（令人「沉睡」）語義有關。  
  - *Papaver somniferum*：拉丁種名意為「帶來睡眠的罌粟」（*somnus* = 睡眠，*ferre* = 帶來）  

- **-aceae**  
  植物科名標準後綴，表示「某某科」。 

**完整結構：**
- **Papaveraceae** = *Papaver-*（罌粟屬）+ *-aceae*（植物科後綴）  
→ 指與 **罌粟屬（Papaver）** 相關的整個植物科，即「罌粟科」，其成員常具有**乳汁、鮮豔花色與豐富的生物鹼類成分**，廣泛應用於**中樞鎮痛、活血、抗菌與藥理研究**中，是重要的藥用植物科之一。  

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


### 3.罌粟科（Papaveraceae） 相關知識點

- **Papaver-**  
  來自拉丁文 *papaver*，意為「罌粟」。  
  - 此詞可能與拉丁語 *pappa*（糊狀物）相關，源於罌粟乳汁具凝稠性，亦可能與安眠作用（令人「沉睡」）語義有關。  
  - 睡神
  - puppy 是英文中的罌粟
  - *Papaver somniferum*：拉丁種名意為「帶來睡眠的罌粟」（*somnus* = 睡眠，*ferre* = 帶來）  


### 4.閃卡區



- 罌粟papaver、罌粟科（Papaveraceae）
??
  來自拉丁文 *papaver*，意為「罌粟」。  
  - 此詞可能與拉丁語 *pappa*（糊狀物）相關，源於罌粟乳汁具凝稠性，亦可能與安眠作用（令人「沉睡」）語義有關。 <!--SR:!2025-04-12,3,270!2025-04-12,3,270--> 

???
