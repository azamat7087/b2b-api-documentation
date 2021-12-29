# Documentation for b2b API

This is a API documentation for business to business application. 

1) Clients API - API where we can get all the information about counterparties and log in as a member of the company

   ```
   http://domen.kz/clients/
   ```

2)  Smart Docs API -  API where we can generate smart documents 

   ```
   http://domen.kz/smart_docs/
   ```

## Clients API

 1. Sections [Retrieve, List] - sections of companies 

    ```
    http://127.0.0.1:8000/clients/sections/
    ```

    Response:
    
    ```json
    {
        "count": 18,
        "next": null,
        "previous": null,
        "results": [
            {
                "id": "1d0173d1",
                "section": "B2B-услуги"
            },
            {
                "id": "60328fea",
                "section": "Автосервис"
            },
            {
                "id": "7a59bd88",
                "section": "Автотовары"
            },
            {
                "id": "39420ef2",
                "section": "Власть"
            },
         ...
    ```



2. Sub_Sections [Retrieve, List] - sub_sections of companies

```
 http://127.0.0.1:8000/clients/sub_sections/
```

Response:

```json
{
    "count": 98,
    "next": "http://127.0.0.1:8000/clients/sub_sections/?page=2",
    "previous": null,
    "results": [
        {
            "id": "b5f3de50",
            "sub_section": "Кондитерские изделия",
            "section": "Продукты"
        },
        {
            "id": "a75de1e9",
            "sub_section": "Бытовые",
            "section": "Услуги"
        },
        {
            "id": "4ec25c01",
            "sub_section": "Религия",
            "section": "Остальное"
        },
        ...
```



3. Currencies [Retrieve] - exchange rate

```
 http://127.0.0.1:8000/clients/currencies/
```

Response:

```json
{
    "CNY_sale": "68.50",
    "CNY_buy": "67.10",
    "CNY_difference": "0.0",
    "USD_sale": "434.90",
    "USD_buy": "433.50",
    "USD_difference": "0.0",
    "RUB_sale": "5.96",
    "RUB_buy": "5.91",
    "RUB_difference": "0.0",
    "EUR_sale": "493.30",
    "EUR_buy": "491.30",
    "EUR_difference": "0.0"
}
        ...
```

4. Rubrics [Retrieve, List] - rubrics of companies

```
 http://127.0.0.1:8000/clients/rubrics/
```

Response:

```json
{
    "count": 1050,
    "next": "http://127.0.0.1:8000/clients/rubrics/?page=2",
    "previous": null,
    "results": [
        {
            "id": "13b185cd",
            "rubric": "Оценка собственности",
            "sub_section": "Юридические услуги"
        },
        {
            "id": "c0626209",
            "rubric": "Детекторы лжи",
            "sub_section": "Безопасность"
        },
        {
            "id": "c8e28946",
            "rubric": "Полиграфические услуги",
            "sub_section": "Полиграфии"
        },
        {
            "id": "cbb47668",
            "rubric": "IP-телефония",
            "sub_section": "Ещё"
        },
        ...
```



5. News [Retrieve] - latest news

```
 http://127.0.0.1:8000/clients/news/
```

Response:

```json
{
    "title": "Итоги года СПК Алматы: инвестиционное развитие, программа реновации, поддержка бизнеса",
    "image": "https://static.forbes.kz/img/articles/c0d0022bd99ed15905b5f2d6d03fff83-120x80.JPG",
    "link": "https://forbes.kz//process/businessmen/itogi_goda_spk_almatyi_investitsionnoe_razvitie_programma_renovatsii_podderjka_biznesa/",
    "source": "Forbes.kz"
}
        ...
```



6. Regions [Retrieve, List] - company regions

```
 http://127.0.0.1:8000/clients/regions/
```

Response:

```json
{
    "count": 1,
    "next": null,
    "previous": null,
    "results": [
        {
            "id": "a0dcf27d",
            "region": "Алматинская область"
        }
    ]
}
```



7. Localities [Retrieve, List] - company localities

```
 http://127.0.0.1:8000/clients/localities/
```

Response:	

```json
{
    "count": 5,
    "next": null,
    "previous": null,
    "results": [
        {
            "id": "61f787ba",
            "locality": "Алматы"
        },
        {
            "id": "4c790198",
            "locality": "Каскелен"
        },
        {
            "id": "c065db74",
            "locality": "Капшагай"
        },
        {
            "id": "496ad561",
            "locality": "Талгар"
        },
        {
            "id": "39c6583d",
            "locality": "с. Коянкус"
        }
    ]
}
```



8. Districts [Retrieve, List] - company districts

```
 http://127.0.0.1:8000/clients/districts/
```

Response:	

```json
{
    "count": 154,
    "next": "http://127.0.0.1:8000/clients/districts/?page=2",
    "previous": null,
    "results": [
        {
            "id": "5d80f29c",
            "district": "Н?р Алатау м-н"
        },
        {
            "id": "652665f5",
            "district": "11-й микрорайон"
        },
        {
            "id": "740634ba",
            "district": "Алгабас"
        },
        {
            "id": "6c4d0fc8",
            "district": "3-й микрорайон"
        },
        {
            "id": "3f2e9588",
            "district": "Казахфильм"
        },
      ...
```





9. Types [Retrieve, List] - company types

```
 http://127.0.0.1:8000/clients/types/
```

Response:	

```json
{
    "count": 1762,
    "next": "http://127.0.0.1:8000/clients/types/?page=2",
    "previous": null,
    "results": [
        {
            "id": "94442d36",
            "type": "таможенно-брокерская компания"
        },
        {
            "id": "f24429e2",
            "type": "таможенный брокер"
        },
        {
            "id": "226c0b78",
            "type": "брокерская компания"
        },
        {
            "id": "55c1f053",
            "type": "таможенный представитель"
        },
        {
            "id": "ae7535a0",
            "type": "компания"
        },
      ...
```



10. KRP names [Retrieve, List] - krp names

```
 http://127.0.0.1:8000/clients/krp_names/
```

Response:	

```json
{
    "count": 14,
    "next": null,
    "previous": null,
    "results": [
        {
            "id": "cf58cd9c",
            "krp_name": "Малые предприятия (6 - 10)"
        },
        {
            "id": "f7eb0441",
            "krp_name": "Малые предприятия (<= 5)"
        },
        {
            "id": "db895838",
            "krp_name": "Малые предприятия (11-15)"
        },
        {
            "id": "671f0f99",
            "krp_name": "Малые предприятия (21-30)"
        },
        {
            "id": "a1ace52c",
            "krp_name": "Малые предприятия (16-20)"
        },
 
      ...
```



11. KRP names [Retrieve, List] - krp names

```
 http://127.0.0.1:8000/clients/krp_names/
```

Response:	

```json
{
    "count": 14,
    "next": null,
    "previous": null,
    "results": [
        {
            "id": "cf58cd9c",
            "krp_name": "Малые предприятия (6 - 10)"
        },
        {
            "id": "f7eb0441",
            "krp_name": "Малые предприятия (<= 5)"
        },
        {
            "id": "db895838",
            "krp_name": "Малые предприятия (11-15)"
        },
        {
            "id": "671f0f99",
            "krp_name": "Малые предприятия (21-30)"
        },
        {
            "id": "a1ace52c",
            "krp_name": "Малые предприятия (16-20)"
        },

      ...
```



12. Emails [Retrieve, List] - email with client data

```
 http://127.0.0.1:8000/clients/krp_names/
```

Response:	

```json
{
    "count": 7970,
    "next": "http://127.0.0.1:8000/clients/emails/?page=2",
    "previous": null,
    "results": [
        {
            "id": "5a4e2ebe",
            "email": "orient_logist@mail.ru",
            "clients_bin": "120240004698",
            "company_id": "e0b63605",
            "company_name": "ТОО \"ORIENT LOGIST GROUP\"",
            "alternative_name": "ТОО \"ORIENT LOGIST GROUP\""
        },
        {
            "id": "3be55f87",
            "email": "customsrep@mail.ru",
            "clients_bin": "110940008664",
            "company_id": "b9e72c72",
            "company_name": "ТОО \"SBA TRADE GROUP\"",
            "alternative_name": "ТОО \"SBA TRADE GROUP\""
        },
        {
            "id": "d569531f",
            "email": "center-logistic@mail.ru",
            "clients_bin": "070540011550",
            "company_id": "46c982e4",
            "company_name": "ТОО \"CENTER ВЭД LOGISTIC\"",
            "alternative_name": "ТОО \"CENTER ВЭД LOGISTIC\""
        },
      ...
```





13. Phone numbers [Retrieve, List] - phone numbers with client data (AUTH ONLY)

```
 http://127.0.0.1:8000/clients/phone_numbers/
```

Response:	

```json
{
    "count": 17980,
    "next": "http://127.0.0.1:8000/clients/phone_numbers/?page=2",
    "previous": null,
    "results": [
        {
            "id": "fce64670",
            "phone_number": "+7(727)382-15-31",
            "client": "ТОО \"ORIENT LOGIST GROUP\""
        },
        {
            "id": "aab12be1",
            "phone_number": "+7(777)683-30-03",
            "client": "ТОО \"АЛМАТИНСКОЕ ЮРИДИЧЕСКОЕ АГЕНТСТВО\""
        },
        {
            "id": "acc2399e",
            "phone_number": "+7(701)725-36-93",
            "client": "ТОО \"ORIENT LOGIST GROUP\""
        },
        {
            "id": "24f72c0b",
            "phone_number": "+7(702)870-97-83",
            "client": "ТОО \"ЮРИДИЧЕСКАЯ КОМПАНИЯ \"СТРАХОВАЯ ПОМОЩЬ\""
        },
        {
            "id": "a6c74b64",
            "phone_number": "+7(727)382-16-86",
            "client": "ТОО \"SBA TRADE GROUP\""
        },
      ...
```







14. Clients [Retrieve, List] - all clients data (AUTH ONLY)

```
 http://127.0.0.1:8000/clients/clients/
```

Response:	

```json
{
    "count": 9532,
    "next": "http://127.0.0.1:8000/clients/clients/?page=2",
    "previous": null,
    "results": [
        {
            "director": "СПЕТЬ ВИТАЛИЙ АЛЕКСАНДРОВИЧ",
            "bin": "180540034205",
            "company_name": "ТОО \"DELUXE TRADE COMPANY\"",
            "alternative_name": "ТОО \"DELUXE TRADE COMPANY\"",
            "company_name_ex": "Deluxe Trade Сompany",
            "company_name_search": "deluxe trade сompany",
            "registration_date": "2018-05-28T00:00:00+06:00",
            "oked": "46690",
            "description": "Оптовая торговля прочими машинами и оборудованием",
            "secondary_oked": null,
            "krp_code": "105",
            "kato": "751910000",
            "address": "Г.АЛМАТЫ, ТУРКСИБСКИЙ РАЙОН, МИКРОРАЙОН ҚАЙРАТ, 181",
            "index_ex": "50010",
            "address_ex": "?амар с?лу, 23",
            "comment_to_adress_ex": null,
            "subway_or_bus_ex": "Максимова",
            "web_site_ex": "http://dtc.kz",
            "vk_ex": null,
            "twitter_ex": null,
            "facebook_ex": null,
            "instagram_ex": null,
            "seal_image": null,
            "updated": "2021-10-08T11:49:59.482374+06:00",
            "krp_name": "f7eb0441",
            "region_ex": "a0dcf27d",
            "locality_ex": "61f787ba",
            "district_ex": "6f83244c"
        },
        {
            "director": "ТЛЕУБАЕВ САБЫР МАМАНОВИЧ",
            "bin": "120240004698",
            "company_name": "ТОО \"ORIENT LOGIST GROUP\"",
            "alternative_name": "ТОО \"ORIENT LOGIST GROUP\"",
            "company_name_ex": "ORIENT LOGIST GROUP",
            "company_name_search": "orient logist group",
            "registration_date": "2012-02-07T00:00:00+06:00",
            "oked": "52299",
            "description": "Прочая транспортно-экспедиционная деятельность",
            "secondary_oked": null,
            "krp_code": "110",
            "kato": "751510000",
            "address": "Г.АЛМАТЫ, ЖЕТЫСУСКИЙ РАЙОН, ПРОСПЕКТ СУЮНБАЯ, 12, кв 15",
            "index_ex": "50016",
            "address_ex": "Суюнбая проспект, 12",
            "comment_to_adress_ex": "1 этаж, 15 офис",
            "subway_or_bus_ex": "Райымбек батыра",
            "web_site_ex": null,
            "vk_ex": null,
            "twitter_ex": null,
            "facebook_ex": null,
            "instagram_ex": null,
            "seal_image": null,
            "updated": "2021-10-08T11:34:27.320088+06:00",
            "krp_name": "cf58cd9c",
            "region_ex": "a0dcf27d",
            "locality_ex": "61f787ba",
            "district_ex": null
        },
      ...
```



15. Staff [Retrieve, List] - returns all users position (AUTH ONLY)

```
 http://127.0.0.1:8000/clients/staff/
```

Response:	

```json
{
    "count": 2,
    "next": null,
    "previous": null,
    "results": [
        {
            "user": "d9adf1d9",
            "role": "Директор",
            "phone_number": null
        },
        {
            "user": "bb9c7f5c",
            "role": "Работник",
            "phone_number": null
        }
    ]
}
      ...
```





16. Get User Company [Retrieve] - returns current user company and position in this company

```
 http://127.0.0.1:8000/clients/get_user_company/
```

Response:	

```json
{
    "user": {
        "user": "d9adf1d9",
        "role": "Директор",
        "phone_number": null
    },
    "company": {
        "director": "ИСАЕВА АСЕЛЬ ТОКТАРБЕКОВНА",
        "bin": "120440025390",
        "company_name": "ТОО \"ЕВРАЗИЯ ТРАНЗИТ СЕРВИС\"",
        "alternative_name": "ТОО \"ЕВРАЗИЯ ТРАНЗИТ СЕРВИС\"",
        "company_name_ex": "Евразия Транзит Сервис",
        "company_name_search": "евразия транзит сервис",
        "registration_date": "2012-04-28T00:00:00+06:00",
        "oked": "52299",
        "description": "Прочая транспортно-экспедиционная деятельность",
        "secondary_oked": null,
        "krp_code": "110",
        "kato": "751910000",
        "address": "Г.АЛМАТЫ, ТУРКСИБСКИЙ РАЙОН, УЛИЦА ЗАКАРПАТСКАЯ, 51",
        "index_ex": "50039",
        "address_ex": "Ахметова, 51Б",
        "comment_to_adress_ex": "4 этаж, 777 офис",
        "subway_or_bus_ex": "Ахметова (конечная)",
        "web_site_ex": null,
        "vk_ex": null,
        "twitter_ex": null,
        "facebook_ex": null,
        "instagram_ex": null,
        "seal_image": null,
        "updated": "2021-11-20T13:19:37.478796+06:00",
        "krp_name": "cf58cd9c",
        "region_ex": "a0dcf27d",
        "locality_ex": "61f787ba",
        "district_ex": null
    }
}
      ...
```



# Smart Doc

​	

**Relations of smart doc models**



![models_drw](/img/models_drw.png)







1. Works [Retrieve, List, Create] - the work done by the company

```
 http://127.0.0.1:8000/smart_doc/works/
```

Response:	

**GET:**

```json
{
    "count": 2,
    "next": null,
    "previous": null,
    "results": [
        {
            "id": "a095fbe6",
            "name": "Доставка посылки курьером",
            "description": "Не указано",
            "measure": "шт",
            "price": "21.00",
            "staff": "65b4e1b7"
        },
        {
            "id": "7002005a",
            "name": "Работа",
            "description": "Не указано",
            "measure": "шт",
            "price": "21.00",
            "staff": "65b4e1b7"
        }
    ]
}
      ...
```

**POST:**

```json
{
     
    "name": "Доставка посылки курьером",
    "description": "",
    "measure": "шт",
    "price": "21.00"
    
}
```





2. Actors [Retrieve, List, Create] - the custom actors for documents

```
 http://127.0.0.1:8000/smart_doc/actors/
```

Response:	

**GET:**

```json
{
    "count": 1,
    "next": null,
    "previous": null,
    "results": [
        {
            "id": "b0eff6b0",
            "full_name": "Азамат Боранбаев Кайратович",
            "role": "Работник"
        }
    ]
}
      ...
```

**POST:**

```json
 {
     "full_name": "Азамат Боранбаев Кайратович",
     "role": "Работник"
 }
```



3. Products [Retrieve, List, Create] - sell products

```
 http://127.0.0.1:8000/smart_doc/products/
```

Response:	

**GET:**

```json
{
    "count": 5,
    "next": null,
    "previous": null,
    "results": [
        {
            "id": "160dd17e",
            "name": "ASUS laptop 4gb",
            "description": "Новейший ноутбук от asus",
            "measure": "шт",
            "manufacturer": "ASUS",
            "image": null,
            "price": "1.00",
            "staff": "65b4e1b7"
        },
        {
            "id": "dd78f364",
            "name": "Продукт_3",
            "description": "Описание продукта 4",
            "measure": "шт",
            "manufacturer": "Компания",
            "image": null,
            "price": "1.00",
            "staff": "65b4e1b7"
        },
      ...
```



**POST:**

```json
{
    "name": "ASUS laptop 4gb",
    "description": "Новейший ноутбук от asus",
    "measure": "шт",
    "manufacturer": "ASUS",
    "image": null,
    "price": "1.00"
}
```





4. Beneficiares [Retrieve, List, Create] - beneficiar object for invoice for payment

```
 http://127.0.0.1:8000/smart_doc/beneficiaries/
```

Response:	

**GET:**

```json
{
    "count": 1,
    "next": null,
    "previous": null,
    "results": [
        {
            "id": "ffe11841",
            "beneficiary": "Азамат",
            "beneficiary_bank": "АО \"CAPITAL BANK KAZAKHSTAN”",
            "PIC": "KZ417812870193980012",
            "BIC": "TBKBKZKA",
            "KBe": "13",
            "Knp": "123",
            "staff": "65b4e1b7"
        }
    ]
}
```



**POST:**

```json
{
    "beneficiary": "Азамат1",
    "beneficiary_bank": "АО \"CAPITAL BANK KAZAKHSTAN”",
    "PIC": "KZ417812870193980012",
    "BIC": "TBKBKZKA",
    "KBe": "13",
    "Knp": "123"
}
```





5. Beneficiares [Retrieve, List, Create] - beneficiar object for invoice for payment

```
 http://127.0.0.1:8000/smart_doc/beneficiaries/
```

Response:	

**GET:**

```json
{
    "count": 1,
    "next": null,
    "previous": null,
    "results": [
        {
            "id": "ffe11841",
            "beneficiary": "Азамат",
            "beneficiary_bank": "АО \"CAPITAL BANK KAZAKHSTAN”",
            "PIC": "KZ417812870193980012",
            "BIC": "TBKBKZKA",
            "KBe": "13",
            "Knp": "123",
            "staff": "65b4e1b7"
        }
    ]
}
```



**POST:**

```json
{
    "beneficiary": "Азамат1",
    "beneficiary_bank": "АО \"CAPITAL BANK KAZAKHSTAN”",
    "PIC": "KZ417812870193980012",
    "BIC": "TBKBKZKA",
    "KBe": "13",
    "Knp": "123"
}
```































































