---
category: 中藥生藥學
tags:
  - 中藥科別
  - 梧桐科
created: 2025-03-21
updated: 2025-04-07 19:41
source:
  - 常用中藥第二版
Abstract: 中藥詞卡
sr-due: 2025-05-07
sr-interval: 30
sr-ease: 290
---
#首刷 #review
### 1.概念
- **梧桐科（Malvaceae）** 是一類**主要由草本、灌木或喬木組成的雙子葉開花植物科**，許多成員具有**黏液質、黃酮與抗氧化物質**，廣泛應用於**中藥、食品、紡織與園藝**。現代分類中，**木槿、錦葵、棉花、可可樹、梧桐等植物**皆被歸為此科。代表植物包括 **錦葵（Malva sylvestris）、木槿（Hibiscus syriacus）、棉花（Gossypium spp.）、可可（Theobroma cacao）、梧桐（Firmiana simplex）**。  
- **主要藥用與經濟特性：**  
  - **潤肺止咳、清熱解毒**：如 **錦葵（Malva sylvestris）**，富含**黏液質與多酚類**，可**潤肺化痰、消炎止痛**，適用於咽喉腫痛、便秘。  
  - **活血通經、利水消腫**：如 **木槿（Hibiscus syriacus）**，含有**有機酸與花青素**，可**清熱利水、調經散瘀**，適用於月經不調與水腫。  
  - **保暖紡織與藥用副產物**：如 **棉花（Gossypium spp.）**，其棉籽油與棉根皮亦可入藥，具**活血作用**。  
  - **抗氧化、調節血壓**：如 **可可（Theobroma cacao）**，富含**可可多酚與黃烷醇類**，可**抗氧化、降血壓、提升心血管健康**。  
  - **宣肺止咳**：如 **梧桐（Firmiana simplex）**，其葉與樹皮傳統上用於**潤肺止咳、清熱解暑**，適用於暑熱咳嗽、喉嚨不適。

### 2.詞素拆解
- **Malv-**（來自拉丁文 *malva*，意為「錦葵」）  
  - **Malva**（錦葵屬）：代表梧桐科的模式屬，如 **Malva sylvestris（野錦葵）**，以其柔嫩葉片與潤腸、潤肺作用聞名。  
  - **Mallow**（英語「錦葵」）：來自拉丁詞 *malva*，指可藥用的草本植物。  
  - **命名原因：** 以 **錦葵屬（Malva）** 為代表命名，該屬植物具有**潤肺、清熱、可食可藥的特性**。  

- **-aceae**（植物科名標準後綴） 

**完整結構：**
- **Malvaceae = *Malv-*（錦葵屬）+ *-aceae*（植物科後綴）**  
- **意義**：指與 **錦葵屬（Malva）** 相關的整個植物科，即「梧桐科」，其成員通常具有**黏液質成分、潤肺止咳、抗氧化與經濟用途**，廣泛應用於**中藥、食品、紡織、園藝與保健領域**。  

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


### 3.梧桐科（Malvaceae） 相關知識點

- **Malv-**（來自拉丁文 *malva*，意為「錦葵」）  

- **Malva**（錦葵屬）：代表梧桐科的模式屬，如 **Malva sylvestris（野錦葵）**，以其柔嫩葉片與潤腸、潤肺作用聞名。  
- **Mallow**（英語「錦葵」）：來自拉丁詞 *malva*，指可藥用的草本植物。  *好旯他就是與棉花同科*
- **命名原因：** 以 **錦葵屬（Malva）** 為代表命名，該屬植物具有**潤肺、清熱、可食可藥的特性**。 <!--SR:!2025-04-10,3,270-->  



### 4.閃卡區


  
- **Malva**（錦葵屬）：代表XX科的模式屬，如 **Malva sylvestris（野錦葵）**，以其柔嫩葉片與潤腸、潤肺作用聞名。  
- **Mallow**（英語「錦葵」）：來自拉丁詞 *malva*，指可藥用的草本植物 > ***棉花屬於該科***
- **命名原因：** 以 **錦葵屬（Malva）** 為代表命名，該屬植物具有**潤肺、清熱、可食可藥的特性**。  
??
- **Malv-**（來自拉丁文 *malva*，意為「錦葵」）  、梧桐科（Malvaceae） <!--SR:!2025-04-11,4,290-->

