---
category: 中藥生藥學
tags:
  - 中藥科別
  - 石竹科
created: 2025-03-21
updated: 2025-04-09 13:44
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
- **石竹科（Caryophyllaceae）** 是一類**主要由一年生或多年生草本植物組成的雙子葉植物科**，廣泛分布於**溫帶地區的原野、山坡與草地**。其花多為**對稱性強、花瓣深裂如「剪刀狀」**，葉對生、莖節膨大，具有典型辨識特徵。  
- 常見植物如 **石竹（Dianthus spp.）、麥藍菜（Silene spp.）、翹搖草（Stellaria spp.）** 等，其中 **繁縷（Stellaria media）** 可作中藥，有**清熱解毒、涼血止血**之功。

### 2.詞素拆解
- **Caryophyll-**  
  來自希臘文 *karyon*（κάρυον，意為「核、種子」）+ *phyllon*（φύλλον，意為「葉」）  
  - **karyo-**：核（指植物的種子或果實形狀）  
  - **-phyll**：葉，可能與某些屬種具**對生葉、葉形明顯**有關  
  - 此詞也與丁香屬 *Caryophyllus*（現歸入 *Syzygium*）有語源重疊，但石竹科命名主要來自石竹屬植物的形態學特徵（花形、葉形）  

- **-aceae**  
  植物科名標準後綴，表示某某植物家族  

**完整結構：**
- **Caryophyllaceae** = *Caryophyll-*（石竹屬）+ *-aceae*（植物科後綴）  
→ 指與 **石竹屬（Caryophyllus 或 Dianthus）** 相關的整個植物科，即「石竹科」。該科植物具有**對生葉、節膨大、深裂花瓣**等外形特徵，部分種類具有**藥用或觀賞價值**，常見於園藝與草藥應用中。

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


### 3.石竹科（Caryophyllaceae） 相關知識點

- **Caryophyll-**  
  來自希臘文 *karyon*（κάρυον，意為「核、種子」）+ *phyllon*（φύλλον，意為「葉」）  
  - **karyo-**：核（指植物的種子或果實形狀）  
  - **-phyll**：葉，可能與某些屬種具**對生葉、葉形明顯**有關  
  - 此詞也與丁香屬 *Caryophyllus*（現歸入 *Syzygium*）有語源重疊，但石竹科命名主要來自石竹屬植物的形態學特徵（花形、葉形）  


### 4.閃卡區


- **Caryophyll-**  、石竹科（Caryophyllaceae）詞源
??
  來自希臘文 *karyon*（κάρυον，意為「核、種子」）+ *phyllon*（φύλλον，意為「葉」） <!--SR:!2025-04-17,8,230!2025-04-23,14,255-->  

???

- 來自希臘文 *karyon*::（κάρυον，意為「核、種子」） <!--SR:!2025-04-23,14,250-->

- *phyllon*::（φύλλον，意為「葉」） folium <!--SR:!2025-04-11,2,190-->