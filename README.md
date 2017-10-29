# used_car-Ebay-Kleinanzeigen-

**数据来源**
    数据来源于Kaggle网站的一个德国销售网（Ebay Kleinanzeigen）的二手车数据。百度了一下关于这个德国销售网站，发现都是德文，表示看不懂，，，
    数据网址：https://www.kaggle.com/orgesleka/used-cars-database

**代码及分析**
<pre><code>
import pandas as pd
used_car=pd.read_csv('E:/file_of_python/used_car(Ebay Kleinanzeigen)/used-cars-database/autos.csv',encoding='latin-1')
print(used_car.head())
</code></pre>
<pre><code>
           dateCrawled                            name  seller offerType  \  
0  2016-03-24 11:52:17                      Golf_3_1.6  privat   Angebot    
1  2016-03-24 10:58:45            A5_Sportback_2.7_Tdi  privat   Angebot     
2  2016-03-14 12:52:21  Jeep_Grand_Cherokee_"Overland"  privat   Angebot  
3  2016-03-17 16:54:04              GOLF_4_1_4__3TÜRER  privat   Angebot   
4  2016-03-31 17:25:20  Skoda_Fabia_1.4_TDI_PD_Classic  privat   Angebot   

  price abtest vehicleType  yearOfRegistration    gearbox  powerPS  model  \
0    480   test         NaN                1993    manuell        0   golf   
1  18300   test       coupe                2011    manuell      190    NaN   
2   9800   test         suv                2004  automatik      163  grand   
3   1500   test  kleinwagen                2001    manuell       75   golf   
4   3600   test  kleinwagen                2008    manuell       69  fabia   

   kilometer  monthOfRegistration fuelType       brand notRepairedDamage  \
0     150000                    0   benzin  volkswagen               NaN   
1     125000                    5   diesel        audi                ja   
2     125000                    8   diesel        jeep               NaN   
3     150000                    6   benzin  volkswagen              nein   
4      90000                    7   diesel       skoda              nein   

           dateCreated  nrOfPictures  postalCode             lastSeen  
0  2016-03-24 00:00:00             0       70435  2016-04-07 03:16:57  
1  2016-03-24 00:00:00             0       66954  2016-04-07 01:46:50  
2  2016-03-14 00:00:00             0       90480  2016-04-05 12:47:46  
3  2016-03-17 00:00:00             0       91074  2016-03-17 17:40:17  
4  2016-03-31 00:00:00             0       60437  2016-04-06 10:17:21  
</code></pre>
<pre><code>
print('数据的大小：{}'.format(used_car.shape))
数据的大小：(371528, 20)
</code></pre>

可以看到数据大约有371528行, 20列，数据的维度较大，而且，很多的字段名字还是德文，下一步将会对数据进行简单的清洗。

