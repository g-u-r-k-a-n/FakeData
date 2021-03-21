# FakeData
This is a simple fake data :test_tube: generator script for SQL Server.

## Overview

While creating this db, my main purpose was to measure performance :rocket: by creating large datasets with non-real datas. For example, I was creating ten million rows of customer tables and trying to create different scenarios to avoid incorrect indexing or expensive execution plans. You can find max value for table rows at the end of the script. All the data  is completely imaginary and creates randomly:ferris_wheel:. You should replace them :thought_balloon: with your own data because I created the data of content with my native language.

## ER Diagram 

I made the normalisation but also combined other foreign keys to the address table for consistency. You can remove them depend on your cases.:construction:

![ER_Diagram](https://i.stack.imgur.com/Wi3eu.png)

## Some queries

```t-sql
select top 10 *  from [FakeData].[dbo].[Person]
```

|Id |FirstName|	LastName   | AddressId |       BirthDate	   |Gender|         Email				 |	PhoneNumberId |
|---|---------|------------|-----------|-----------------------|------|------------------------------|----------------|
|1  |Vedat	  |ISLAKCAN	   |8962       |1984-06-28 00:00:00.000| 1	  |vedat.islakcan@yandex.com	 |    1687 		  |
|2  |Bedirhan |GÜÇER	   |1343       |1962-08-20 00:00:00.000| 1	  |bedirhan.gucer@gmail.com		 |    2781 		  |
|3  |Şenay	  |KİNNA	   |1861       |1964-06-02 00:00:00.000| 0	  |senay.kinna@gmail.com		 |    1720 		  |
|4  |İpek	  |ÖZKARAKULAK |6748       |1990-06-04 00:00:00.000| 0	  |ipek.ozkarakulak@gmail.com	 |    7644 		  |
|5  |Evren	  |YURTKULU    |6893       |1962-09-15 00:00:00.000| 1	  |evren.yurtkulu@yandex.com	 |    5729 		  |
|6  |Bahar	  |ÇARLIK	   |3665       |1985-07-30 00:00:00.000| 0	  |bahar.carlik@yandex.com		 |    1384 		  |
|7  |Berivan  |ARSLANTUNÇ  |2717       |1956-11-07 00:00:00.000| 0	  |berivan.arslantunc@gmail.com	 |    5535 		  |
|8  |Baran	  |KEREY	   |2778       |1971-09-04 00:00:00.000| 1	  |baran.kerey@hotmail.com		 |    2459 		  |
|9  |Alparslan|BALALAN	   |9507       |1964-09-09 00:00:00.000| 1	  |alparslan.balalan@hotmail.com |    7529 		  |
|10 |Selda	  |BATTALLAR   |854	       |1998-12-22 00:00:00.000| 0	  |selda.battallar@hotmail.com	 |    9036 		  |

``` t-sql
select top 10 * from [FakeData].[dbo].[PersonInfo]/*view*/ order by 1
```

|CustomerId |Gender |     Person        |		Email   				            |   Phone	  |                        Address                         |        
|-----------|-------|-------------------|-------------------------------|-----------|--------------------------------------------------------|
|1          |Bay    |Vedat ISLAKCAN	    | vedat.islakcan@yandex.com   	|212-3217885|Gürler Mah. Cerrah Saliha Sok. Tepebaşı-Taksim/İstanbul |		  
|2          |Bay    |Bedirhan GÜÇER	    | bedirhan.gucer@gmail.com   	  |212-4422231|Zeytinlik Mah. Ezgi Sok. Zeytinlik-Bakırköy/İstanbul 	 |	  
|3          |Bayan  |Şenay KİNNA	      | senay.kinna@gmail.com   		  |286-5517987|Gazi Mustafa Kemal Mah. 18 Mart Sok. Merkez/Çanakkale	 | 
|4          |Bayan  |İpek ÖZKARAKULAK   | ipek.ozkarakulak@gmail.com   	|216-1341683|Atatürk Mah. Gaziler Cad. Cumhuriyet-Üsküdar/İstanbul	 |	  
|5          |Bay    |Evren YURTKULU     | evren.yurtkulu@yandex.com   	|366-8634023|İnalı Mah. Emin Ongan Sok. Bingöl-Merkez/Kastamonu		   | 
|6          |Bayan  |Bahar ÇARLIK	      | bahar.carlik@yandex.com   	  |242-7247251|Yeşilyurt Mah. Saygılı Sok. Yeşilköy-Kemer/Antalya		   | 
|7          |Bayan  |Berivan ARSLANTUNÇ | berivan.arslantunc@gmail.com  |282-1333247|Esenler Mah. Sıran Söğüt Sok. Marmaracık-Ergene/Tekirdağ|		  
|8          |Bay    |Baran KEREY	      | baran.kerey@hotmail.com   	  |388-1820943|Bahçelievler Mah. Yunus Emre Cad. Bilecik-Merkez/Niğde	 | 
|9          |Bay    |Alparslan BALALAN  | alparslan.balalan@hotmail.com |438-2241223|Dize Mah. Bulvar Cad. Yüksekova-Yüksekova/Hakkari	     |
|10         |Bayan  |Selda BATTALLAR    | selda.battallar@hotmail.com 	|222-8547251|Adahisar Mah Yunus Emre Cad. Dinek-Odunpazarı/Eskişehir |

#### Resources that were used
[List of most popular given names](https://en.wikipedia.org/wiki/List_of_most_popular_given_names):link:<br>
[Lists of most common surnames](https://en.wikipedia.org/wiki/Lists_of_most_common_surnames):link:<br>
[Streets in Turkey](https://tr.wikipedia.org/wiki/Kategori:Türkiye%27deki_cadde_ve_sokaklar):link:<br>
[Turkey plate codes](https://tr.wikipedia.org/wiki/Türkiye_il_plaka_kodları):link:<br>
[You can create your own large db with Ömer Faruk ÇOLAKOĞLU](https://youtu.be/1Z1W3ty01c4):link:
