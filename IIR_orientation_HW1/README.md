# IIR新生訓練HW1
## 處理
1. plus_item_category.csv
- 刪除sales_train.csv的date欄位
- 利用sales_train.csv的item_id對照items.csv的item_id取出item_category_id塞進去sales_train.csv裡
- 產出表格plus_item_category.csv

|date_block_num|shop_id|item_id|item_category_id|item_price|  item_cnt_day|
| -------------- | ------- | ------- | --- | --- | --- |

2. GT.csv
- DataFrame(sales_train.csv).groupby(['date_block_num', 'shop_id', 'item_id'], as_index=False).item_cnt_day.sum()
- 利用SQL指令後結果的item_id對照items.csv的item_id取出item_category_id塞進去

|date_block_num|shop_id|item_id|item_category_id|item_cnt_month|
| -------------- | ------- | ------- | --- |---|

## 評分項目
1.分析圖表兩張 40%(一張20%) & 解釋圖表的涵義 30%
- DataFrame(GT.csv).groupby('item_category_id', as_index=False).item_cnt_month.mean()
- 每月平均賣出多少item對item種類的分布，明顯出現三個高峰

![](https://i.imgur.com/cQpvxx5.png)
---
- DataFrame(GT.csv).groupby('shop_id', as_index=False).item_cnt_month.mean()
- 每月平均賣出多少item對shop_id的分布

![](https://i.imgur.com/oCLDi6r.png)
---
- DataFrame(GT.csv).groupby('date_block_num', as_index=False).item_cnt_month.mean()
- 每月平均賣出多少item對date_block_num的分布

![](https://i.imgur.com/frCnBCi.png)
---
- DataFrame(GT.csv).groupby('item_id', as_index=False).item_cnt_month.mean()
- 每月平均賣出多少item對item_id的分布

![](https://i.imgur.com/8kGTHbS.png)

---
- DataFrame(plus_item_category.csv).groupby('item_price', as_index=False).item_cnt_day.mean()
- 每天平均賣出多少item對item_price的分布，在低價時候的平均賣出數量比高價多出許多

![](https://i.imgur.com/4vQDV0u.png)

2. 了解所使用的函數 30%

pd.read_csv: read csv檔進來，result type 是 dataframe

data.drop: 刪除dataframe某欄

filter: 能在dataframe中加入某些條件以產出所需

groupby: 以某欄作單位執行相加、平均等動作

append: 在list尾吧加一個元素

to_csv: 將dataframe轉csv匯出

plt.subplots():　創建畫布

plot: 畫圖

set: 設定一些圖的參數

grid(): 畫上網格

savefig: save image

plt.show(): show image
