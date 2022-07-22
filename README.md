# Food_Insecurity_NYC

According to the US Department of Agriculture (USDA), food insecurity, is an economic and social condition in which people lack consistent access to enough food to sustain a healthy life¹.In this project, we study the food insecurity problem by looking at the listed prices of various food items across neighborhoods in NYC.

**Our hypothesis is that people living in areas with higher food insecurity problems would pay more for the same items compared to those in more secured areas**.
For the scope of work, we will only assess food products from KeyFoods supermarkets, one of the top 4 Supermarket Leaders in Metro New York (according Food Trade News 2021 report). In particular, we will use the following datasets:

### **`keyfood_products.csv`**

This CSV file contains the price information about 2 million food items listed on KeyFoods stores in NYC.

|store|department|upc|product|size|price|
|--|--|--|--|--|--|
102|bakery|102-28556000000|Store Prepared - Challah Egg|1 EA|\$4.99 each|
102|bakery|102-28781600000|Store Prepared - fw Cheesecake Plain 7 Inch|1 EA|\$27.99 each|
|...|...|...|...|...|...|

The details of the columns are as follows:

|Column|Description|
|--|--|
|**store** | The unique id of each store |
|**department**| The department (or aisle) that the food item belongs to. Possible values are:<br />`'bakery'`,`'beverages'`,`'breakfast'`,`'deli'`,`'frozen'`,`'international'`,<br/>`'meatandseafood'`,`'pantry'`,`'produce'`,`'refrigerated'`, and `'snacks'`|
|**upc**|The unique id for each item in a food store. It is often in the format of `SID-XXXXXXXXXX`,<br/> where `SID` is a store id if it's specific to a store, `UPC` if it's a general product, or `'KEY'` <br/> if it's a KeyFoodsproduct. If an item doesn't have any UPC code, this field will be `N/A`.|
|**product**|This is the listed name of the product|
|**size**|The unit that the product is being sold in|
|**price**|The price text of the product as shown on their websites. This is not a number but have<br/>been verified to start with the price mark`$XX.XX`. Note that for items without price<br/>information, this field could be listed as `Price not Available`|


### **`keyfood_nyc_stores.json`**

This JSON file contains information for all KeyFoods stores in NYC. There are a lot of details about each store, however, for this homework, we are only interested in the following fields:

|Field|Description|
|--|--|
|**name** | This is the unique id of each store, which could be crosswalk with the **store** field above |
|**communityDistrict**|The community district code that the store belongs to. It's simply a larger geographical<br/> unit comparing to a zip code. More information can be found [here](https://communityprofiles.planning.nyc.gov/).|
|**foodInsecurity**|A food insecurity score computed for the community district that the stores belong to.<br/> This value has the range of 0 to 1 with 0 being without any food insecurity rish, and 1 <br/> has the most food insecure risk.|

## Part A: Testing hypothesis with sample datasets
Task done with Spark RDD
## Part B: Testing the whole dataset
Task done with Spark Dataframe

