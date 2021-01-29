### Step 2. Extract the ODBC JSON Query

/!\ Very important: Tableau only accept the generic Driver ODBC JSON and a custom query to declare and use DataSource.
We'll need to generate and convert the ODBC JSON JDataSource created in Step 1 into a query interpretable by Tableau

##### 1. In the ODBC Datasource (Zappysys), go to Preview sheet

![dataviz_init_3](imgs/dataviz_init_3.png "")

##### 2. Then “Query Builder”

![dataviz_init_4](imgs/dataviz_init_4.png "")

##### 3. Extend the new window and select all the checkbox

![dataviz_init_5](imgs/dataviz_init_5.png "")

##### 4. Go to “Filter Options” and extend the window if necessary

![dataviz_init_6](imgs/dataviz_init_6.png "")

##### 5. Select Filter

![dataviz_init_7](imgs/dataviz_init_7.png "")

##### 6. Select the “data” row, and validate

![dataviz_init_8](imgs/dataviz_init_8.png "")

##### 7. Select and copy the query in the bottom of the screen – Late you’ll need to paste it in Tableau

![dataviz_init_9](imgs/dataviz_init_9.png "")

Here is the query (Example) to copy

```
SELECT * FROM $
WITH(
	 Src='http://[AZURE ENDPOINT].westeurope.cloudapp.azure.com/parameter/[PARTNER CODE]/site/_search'
	,Filter='$.data[*]'
	,RequestData='{"matching":"*","fetch": ["*"]}'
	,RequestContentTypeCode='ApplicationJson'
	,Header='cache-control: no-cache || Accept: */* || Content-Type: application/json'
	,RequestMethod='POST'
)
```

---