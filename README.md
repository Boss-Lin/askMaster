### Table1: User
| Id 	|Name |
| ------------- | ------------- |
| user_1| Obi-Wan	|
| user_2| Darth Vader	|
| user_3| Darth Maul |

> ### 問題
> 1. 假如資料庫設計我不使用“AUTO_INCREMENT”，程式碼要如何達到自動編號？
> 2. JDBC要怎麼達到客製化ID的效果(ex: user_數字)？

### Table2: Group
| Id	| Ref_Id |group|
| ------------- | -----|-------- |
| 1	| user_1	| Jedi|
| 2	| user_2 	|Sith|
| 3	| user_3 	|Sith|

### Table3: Force
| Id	| Ref_Id |	The Force|
| ------------- | ----|--------- |
| 1	| 1 	| bright side|
| 2	| 2 	|dark side|
| 3	| 3 	|dark side|

## 說明
**每一個table的Ref_Id都是對應上一個table的Id。**

# 我要新增資料
> 	以下為我要新增的資料
```
{
  "Name": "Luke Skywalker",
  "Group": "Jedi",
  "Force": "bright side"
}
```

> ### 問題
> 3. 假設前端jsp畫面設計3個form和1個button，按下去一起送出表單，那要怎麼同時新增這3個table的資料？  

我卡在Ref_Id這裡，前面table如果沒有送出成功後面table就爆了。  
