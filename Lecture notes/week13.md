# Recap

## 各學年資料合併

  - [主程式](./week12.md#範例程式合併多年)  
  - [支援程式merge.R](https://github.com/tpemartin/112-2-R-EE/blob/main/Lecture%20notes/merge.R)
  
> 進行stack data前要先移除有問題的109學年資料：
> ```r
> # 移除109 -----
>
> merged_data_list[["109"]] <- NULL
> ```


# 資料說明

## 整體描述

有多少欄位？有多少筆資料？

## 欄位說明

有多少缺失值？ 佔多少比例？  

### 連續型

全距，平均數，極大值，極小值。
四分位數，中位數。

### 間斷資料

#### 類別型

當類別少於 10 個時，列出：
各類別的數量。  
各類別的比例。  
當類別大於與等於 10 個時，只列出各類別的數量。

#### 純文字


## AI prompt設計

針對data frame進行資料描述遵守以下規則：
1. 先整體描述資料有多少欄位，多少筆資料。再進行逐欄描述。
2. 針對每一個欄位，先描述有多少缺失值，佔多少比例。  
3. 若欄位為連續型，則需描述全距，平均數，極大值，極小值，四分位數，中位數。  
4. 若欄位為間斷資料，先判斷是否低於10類，若低於10類，則需描述各類別的數量，各類別的比例。當類別大於與等於 10 個時，只列出各類別的數量。 
資料描述的各別結果請存在一個list裡並各別給予適當的元素名稱。