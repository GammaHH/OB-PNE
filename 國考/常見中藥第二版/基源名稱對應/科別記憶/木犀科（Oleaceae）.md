---
category: 中藥生藥學
tags:
  - 中藥科別
  - 木犀科
created: 2025-03-20
updated: 2025-04-06 22:33
source:
  - 常用中藥第二版
Abstract: 中藥詞卡
sr-due: 2025-05-06
sr-interval: 30
sr-ease: 290
---
#首刷 #review 
>兩種藥材

### 1.概念
- **木犀科（Oleaceae）** 主要由**喬木、灌木和藤本植物**組成，許多成員富含**揮發油、黃酮類與皂苷**，在**藥用、食用與觀賞**領域具有重要價值。代表植物包括 **連翹（Forsythia suspensa）、女貞（Ligustrum lucidum）、木犀（Osmanthus fragrans）、橄欖（Olea europaea）**。  
- **主要藥用特性：**  
  - **清熱解毒**：如 **連翹（Forsythia suspensa）**，富含**連翹苷（Forsythiaside）與黃酮類**，可**清熱解毒、消腫散結**，適用於風熱感冒、癰腫瘡毒。  
  - **滋補肝腎**：如 **女貞子（Ligustrum lucidum）**，含有**三萜類與黃酮類**，可**補益肝腎、強筋壯骨**，適用於腎虛腰膝酸軟、頭髮早白。  
  - **芳香健脾**：如 **木犀（Osmanthus fragrans）**，其花含**揮發油與多酚類**，可**芳香開胃、溫中散寒**，適用於食慾不振、胃寒腹痛。  
  - **抗氧化與心血管保護**：如 **橄欖（Olea europaea）**，富含**橄欖多酚（Oleuropein）與單不飽和脂肪酸**，可**抗氧化、降血脂、保護心血管健康**，廣泛應用於食品與保健領域。  

### 2.詞素拆解
- **Ole-**（來自拉丁文 *olea*，意為「橄欖」）  
  - **Olea**（橄欖屬）：典型木犀科植物，如 **Olea europaea（歐洲橄欖）**，以其果實與油脂著稱。  
  - **Oil**（英語「油」）：與拉丁文 *olea* 有語源關聯，因橄欖是主要的食用油來源之一。  
  - **命名原因：** 以 **橄欖屬（Olea）** 為代表命名，該屬植物具有**豐富的油脂與藥用價值**。  

- **-aceae**（植物科名標準後綴）  

**完整結構：**
- **Oleaceae = *Ole-*（橄欖屬）+ *-aceae*（植物科後綴）**  
- **意義**：指與 **橄欖屬（Olea）** 相關的整個植物科，即「木犀科」，其成員通常具有**芳香揮發油、藥用與食用價值**，並廣泛應用於**中藥、食品、保健與園藝**。  

#### 📌 相關藥材連結


```dataviewjs
const excludeTags = ["中藥科別","中藥生藥學"];
const currentTags = dv.current().tags?.filter(t => !excludeTags.includes(t)) ?? [];

let tagMatches = dv.pages()
  .where(p => p.tags && p.file.name !== dv.current().file.name)
  .filter(p => p.tags.some(tag => currentTags.includes(tag)));

let tagGroups = {};
for (let tag of currentTags) {
  tagGroups[tag] = tagMatches.filter(p => p.tags.includes(tag));
}

let totalMatched = Object.values(tagGroups).reduce((acc, pages) => acc + pages.length, 0);

if (totalMatched > 0) {
  dv.header(5, `相關藥物（共 ${totalMatched} 筆）`);
  for (let [tag, pages] of Object.entries(tagGroups)) {
    if (pages.length > 0) {
      dv.header(6, `▸ ${tag}（${pages.length}）`);
      dv.list(
        pages.map(p => {
          const tagsToShow = p.tags?.filter(t => !excludeTags.includes(t) && t !== tag) ?? [];
          return `${p.file.link}　${tagsToShow.join("、")}`;
        })
      );
    }
  }
} else {
  dv.header(5, "相關藥物（0）");
  dv.paragraph("沒有找到與本藥材具有相同標籤的其他筆記。");
}
```



### 3.木犀科（Oleaceae） 相關知識點


