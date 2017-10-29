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
    整个的数据清洗包括可视化都是用的python（我用的Jupyter NoteBook），文件为：used_car.ipynb    
    
 **结论：**  
     *1、* SUV的价格最贵，并且卖的数量并不多；跑车、敞篷车的价格也比较贵；轿车、公共汽车、旅行车价位适中；小轿车和轿车不仅卖的多，还便宜。  
     *2、* 在eBay网站上的车辆中的数量关系是：轿车>小型轿车>旅行车>敞篷车>跑车>SUV>其它。  
     *3、* 大部分的车马力较为集中（100Ps至220Ps）,除了小型轿车的马力普遍较小（80PS左右）。  
     *4、* 大部分车辆的变速器类型还是手动的，尤其是小型轿车的变速器绝大多数是手动的，而SUV的手动变速器和自动变速器的汽车数量基本持平，这也SUV比其他类型的车要贵一些的一个原因。
     *5、* 混合型燃料的汽车的价格较高，柴油型、电动型汽车紧随其次，而汽油型、液化石油气型、压缩天然气型的汽车价格基本持平。
     *6、* 不论是什么车型，没有维修过的车占据了绝大多数，而维修过的车所占比例很小。
     *7、* eBay网站上的车辆一半以上在不到一周的时间就可以卖出去，绝大多数的车20天就能卖掉，而几乎所有的车40天就可以卖出去了。  
     *8、* eBay网站上的车很多比较陈旧，在10年~17年的居多。  
     *9、* 从图像可以看出，销售天数越大，价格越高；车龄(年)越大，价格越低。  
     *10、* 大众汽车以绝对性的优势占领eBay网站的销售冠军，销售量前十的是汽车的商标：大众>宝马>奔驰>欧宝>奥迪>福特>雷诺>标致>菲亚特>西特。  
     

