---
category: 中藥生藥學
tags:
  - 中藥科別
  - 十字花科
created: 2025-03-20
updated: 2025-04-06 21:26
source:
  - 常用中藥第二版
Abstract: 中藥詞卡
sr-due: 2025-04-23
sr-interval: 17
sr-ease: 270
---
#首刷 #review 
> 兩種藥材
### 1.概念

- **十字花科（Brassicaceae）** 是一類**主要由草本植物組成的雙子葉開花植物科**，以**富含芥子油苷（Glucosinolates）與辛辣風味**著稱，廣泛應用於**藥用、食用與農業**。代表植物包括 **白芥（Brassica alba）、大蒜芥（Alliaria petiolata）、芥菜（Brassica juncea）、蘿蔔（Raphanus sativus）、油菜（Brassica napus）**。  
- **主要藥用特性：**  
  - **行氣散結**：如 **芥菜（Brassica juncea）**，富含**芥子油苷與揮發油**，可**行氣散結、祛痰止咳**，適用於風寒咳嗽、痰濕阻滯。  
  - **解毒消腫**：如 **蘿蔔（Raphanus sativus）**，含有**硫代葡萄糖苷與維生素C**，可**清熱解毒、促進消化**，適用於食積脹滿、咳嗽痰多。  
  - **溫中散寒**：如 **白芥（Brassica alba）**，富含**揮發油與芥子鹼**，可**溫中散寒、通絡止痛**，適用於寒性腹痛、關節痹痛。  
  - **降脂護肝**：如 **油菜（Brassica napus）**，其種子含**亞麻酸與植物甾醇**，可**降低膽固醇、保護心血管**，常用於食用油與保健食品。

### 2.詞素拆解
- **Brassic-**（來自拉丁文 *brassica*，意為「甘藍、芥菜」）  
  - **Brassica**（甘藍屬）：代表十字花科的模式屬，如 **Brassica oleracea（甘藍）**，其變種包括捲心菜、花椰菜與羽衣甘藍。  
  - **命名原因：** 以 **甘藍屬（Brassica）** 為代表命名，該屬植物具有**典型的十字形花冠與芥子油苷含量**。  

- **-aceae**（植物科名標準後綴）  

**完整結構：**
- **Brassicaceae = *Brassic-*（甘藍屬）+ *-aceae*（植物科後綴）**  
- **意義**：指與 **甘藍屬（Brassica）** 相關的整個植物科，即「十字花科」，其成員通常具有**辛辣味、抗氧化物質、食用與藥用價值**，並廣泛應用於**中藥、食品、農業與保健領域**。  

#### 📌 相關藥材連結



```dataviewjs
// ---------- 標籤推薦區塊（以列表呈現） ----------
const excludeTags = ["中藥科別"];
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
        pages.map(p => p.file.link)
      );
    }
  }
} else {
  dv.header(5, "相關藥物（0）");
  dv.paragraph("沒有找到與本藥物具有相同標籤的其他筆記。");
}
````

### 3.十字花科（Brassicaceae） 相關知識點



