---
category: 中藥生藥學
tags:
  - 中藥科別
  - 杜仲科
created: 2025-03-20
updated: 2025-04-07 10:15
source:
  - 常用中藥第二版
Abstract: 中藥詞卡
sr-due: 2025-04-15
sr-interval: 8
sr-ease: 210
---
#首刷 #review 
>一種中藥材
### 1.概念
- **杜仲科（Eucommiaceae）** 是**單屬科植物**，僅包含 **杜仲（Eucommia ulmoides）** 一種，為**中國特有的落葉喬木**，以**補腎強筋骨、降血壓、促進膠原蛋白合成**著稱，廣泛應用於**中藥、保健食品與橡膠工業**。  
- **主要藥用特性：**  
  - **補肝腎、強筋骨**：杜仲富含**杜仲苷（Eucommioside）、綠原酸（Chlorogenic acid）與木脂素**，可**補腎壯陽、強筋健骨**，適用於腎虛腰膝酸軟、筋骨無力。  
  - **降血壓、保護心血管**：含有**多酚類與黃酮類**，可**降低血壓、抗氧化、促進血液循環**，適用於高血壓、心血管疾病的輔助治療。  
  - **安胎作用**：可**補腎固精、安胎**，適用於孕婦腎虛胎動不安、習慣性流產。  
  - **促進膠原蛋白合成**：杜仲膠為其特有成分，能**促進膠原蛋白增生、增強骨密度**，有助於骨質疏鬆的預防與治療。  

### 2.詞素拆解
- **Eucommi-**（來自希臘文 *εὖ*（eu）「良好」+ *κόμμι*（kommi）「樹膠」）  
  - **Eucommia**（杜仲屬）：代表杜仲科的唯一屬，如 **Eucommia ulmoides（杜仲）**，以其樹皮與葉含有大量橡膠物質而得名。  
  - **Eu-**（良好）：來自希臘文 *εὖ*（eu），意為「良好、優秀」，表示該植物的藥用價值。  
  - **Commi-**（樹膠）：來自希臘文 *κόμμι*（kommi），意為「樹膠、橡膠」，形容該植物含有獨特的彈性樹脂。  
  - **命名原因：** 以 **杜仲屬（Eucommia）** 為代表命名，強調其**獨特的膠質成分與藥用價值**。  

- **-aceae**（植物科名標準後綴） 

**完整結構：**
- **Eucommiaceae = *Eucommi-*（杜仲屬）+ *-aceae*（植物科後綴）**  
- **意義**：指與 **杜仲屬（Eucommia）** 相關的整個植物科，即「杜仲科」，其成員具有**補腎強筋骨、降血壓、促進膠原蛋白合成**的藥用價值，並廣泛應用於**中藥、保健品與橡膠工業**。  

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




### 3.杜仲科（Eucommiaceae） 相關知識點

- **Eu-**：來自希臘文 *εὖ*（eu），意為「==良好、優秀==」，表示該植物的藥用價值。 <!--SR:!2025-04-10,3,230-->  

- **Commi-**：來自希臘文 *κόμμι*（kommi），意為「==樹膠、橡膠==」，形容該植物含有獨特的彈性樹脂。 <!--SR:!2025-04-10,3,230-->

