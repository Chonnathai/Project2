1. Background

Even though the economic situation has not yet recovered as expected from the COVID situation. But consumer demand for housing still exists, whether buying or renting. As many business sectors have returned to normal operations, many people have started looking for a place to live close to their workplace. Bangkok is still the most popular province that receives interest in purchasing real estate, followed by metropolitan areas and tourist provinces.


2. Problem statement

As a real estate agent, How can we know the buying/selling prices in the market to set prices competitive with competitors in Bangkok and metropolitan areas to make more profit for company?

3. data dictionary

|Feature|Type|Dataset|Description|
|---|---|---|---|
|province|string|train.json, test.json|province name: this dataset only includes Bangkok,Samut Prakan and Nonthaburi|
|district|string|train.json, test.json|district name|
|subdistrict|string|train.json, test.json|subdtistrict name|
|property_type|string|train.json, test.json|type of the house: Condo, Townhouse or Detached House |
|bedrooms|int|train.json, test.json|the number of bedrooms|
|baths|int|train.json, test.json|the number of baths|
|floor_area|int|train.json, test.json|total area of inside floor [㎡]|
|latitude|float|train.json, test.json|latitude of the house|
|longitude|float|train.json, test.json|longitude of the house|
|nearby_stations|int|train.json, test.json|the number of nearby stations (within 1km)|
|nearby_supermarkets|int|train.json, test.json|the number of nearby supermarkets|
|nearby_shops|int|train.json, test.json|the number of nearby shops|
|year_built|int|train.json, test.json|year built|
|price|float|train.json|[TARGET VALUE] selling price|

4. brief summary of your analysis

- From the 'Missing Values by Column' bar chart, we could found a numbers of columns coataining a huge missing values which we display a bar chart for percentage of missing values in each columns so you could see that there are 7 columns with visibe blue bars. So we decided to use the rest of useful columns which have less missing values in other 14 columns. They have been considered that  they are important factors that affect the customer's choice of buying real estate.
- From the 'Distribution of Price' histogram chart, we could found the price range of most properties in Bangkok, Nonthaburi, and Samut Prakan are in the field of 1.5 million to 4 million baht.
- From the ' Price by Property Type' box plot, in Bangkok, Nonthaburi and Samut Prakan Detached, house prices have the highest average price, followed by condos and townhouses.
- From the 'Distribution of distrcts' bar chart,  in Bangkok, Nonthaburi and Samut Prakan Detached, Mueang Nonthaburi District _(Nonthaburi) has the highest number of house sale announcements, followed by Mueang Samut Prakan District (Samut Prakan) and Huai Khwang District (Bangkok).
- From the 'Correlation matrix' heat map, we could found correlation between columns showing high correlation coefficient pairwises such as Bed room/Bath, Floor area/Bed room and Floor area/Bath.v
- From the 'Correlation with price/price_log' heat map, we could found the columns that are most relevant to price are as follows: Floor area, Bath and Nearby shop.
- From the 'Comparison of Predicted and Actual values' scatter plot showing the selected model could predicted values as similar as actual values or it has positive linear relationship as a straight line sloping upwards when plotted on graph.



5. Conclusion

- The type of property likely has a significant impact on the price. 
- Detached houses have higher prices compared to condos and townhouses. 
- District, province, subdistrict, latitude and longitude can significantly affect the price. 
- Properties in specific districts or provinces may be more expensive due to their desirability. 
- The presence of nearby amenities such as supermarkets, and nearby stations (MRT, BTS) can impact prices. 
- Properties located closer to public transportation (BTS, MRT) may command higher prices. 
- Properties with more bedrooms and bathrooms, larger floor areas, and newer constructions may have higher prices.

6. Recommendation

- Identify the most popular property types in the area and focus on marketing and sales efforts for those types.
- Analyze which districts, provinces, and subdistricts have the highest demand. Focus on opportunities to make more  profits from those areas.
- For some customers who have a limited budget to purchase real estate. We can use data on real estate prices in each area to make recommendations so we could rapidly specific area to match with limited budget.

7. Limitation

- During the data cleaning, If there is a separation of property type column between condos and detached houses + townhouses as there is unequal data containing between them in floor level and floor area. Then, use KNN technique to fill in the missing data in each column to make the model prediction more accurate.
