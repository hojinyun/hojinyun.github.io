---
title:  "Phone Comparison Website"
categories: [Project]
---
### [Phone Comparison Website Proejct Github](https://github.com/hojinyun/Phone_Comparison_Website)

### Website Goal:

This website lets the users two phones through search engine and compares them for the user. Unlike other websites where they list out features of two phones, our website tells the user what is different by how much and also gives advice to the user.

이 사이트는 유저가 핸드폰 두개를 고르면 그 핸드폰을 비교한 뒤 특정 스펙이 얼만큼 차이나는지 가르쳐 주는 사이트다. 여타 사이트와는 다르게 두 핸드폰의 정보를 나열 해주는 것은 기본이며 차이점을 쉽게 설명 해주며 조언까지 해주는 사이트이다.

### Design:

Our website collects phone datas form "Danawa," and use search engine to let user choose two phones they want to compare. After user chooses two phones, we give advice by comparing two numerical values of phones features and give comparison and analytical advice.

이 사이트는 다나와를 통해 핸드폰 정보를 얻으면 검색 엔진을 이용하여 유저가 비교를 원하는 핸드폰을 검색 시 보여주고 고르게 한다. 유저가 핸드폰을 고르고 난 후에 두 핸드폰의 스펙을 비교하여 유저에게 조언을 해준다.

### Problems:

다나와 같은 사이트는 동적 페이지라서 HTML 태그 구조를 파악하기 어렵다. 따라서, Beautifulsoup, requests 뿐만 아니라 selenium도 사용해야 파악이 가능하다.

🧐Selenium을 사용하면 느리다는 단점이 있다.

개발자 도구에서 요소랑 소스가 다르면 동적 웹사이트인지 바로 확인 가능

똑같은 핸드폰 거를 수 있도록 구현하기

## Data:

### Functions:

Main.py: creates the overall website

Scrapper.py: extract information form website

- extract_phone:
    - input:
        1. html: gets the tags of phones
    - function: extract the phone information from the html tags
    - return: return dictionary of phones different informations
- extract_phones:
    - input:
        1. last_page: gets total pages, but there are too many phones, so only recent 10 pages 
        2. url: for links of different pages
    - function: use extract_phone function to get data from different pages and put them into phones array
    - return: phones array

export.py: turn information into .csv file

## Website:

### Search Engine:

Need a search engine to access the data

### Comparison Page :

Need to load user chosen phone data

## Web Framework:

### Flask:

- Micro Framework
- Designed for one application
- Does not have 🧐ORM(Object Relational Mapping)
- Easier to add new features

### Django:

- Full-stack Framework
- Designed for multiple application
- Has ORM
- Complex to add new features

🧐 When communicating with database one has to use the query, this query differs by every database(MySQL, Oracle ... etc) and ORM is a function  that helps us use python instead of query

### Port Forwarding:

Tried port forwarding to access website from other device that is not local. Coding did not need any change, but only need to change the setting of the router. Had to set the internal and external port number range for the router.