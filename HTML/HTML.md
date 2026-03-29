# Study with HTML + CSS + JavaScript, <br>written by 김기수, Published from gilbut

## HTML Basic Components
### 1. Tag
  - Form: \<TagName>
### 2. Attributions
  - Form: \<TagName AttrName="AttrValue">
### 3. Symtax  
- Content exists:
  - ex) \<title>My First Web Page!</title>  
    - \<title>: Open tag  
    - My First Web Page!: Content  
    - \</title>: Close tag  
    - \<title> ... \</title>: Element  
- Content NOT exists:
  - empty tag: \<br>
### 4. Comment
  - Form: \<!-- Comment Content -->

  
## HTML Basic Structure
'''html
\<!-- Use ! for writing the basic structure automatically -->
<!DOCTYPE html> <!-- DTD(Document Type Definition): Defines the document type and tells the browser which HTML standard to use -->
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My First Web Page!</title>
</head>
<body>
    <!-- 웹 페이지에 표시할 내용을 적습니다. -->
    <p>My First Web Page</p>
    <blockquote cite="https://ko.wikipedia.org/wiki/HTML">
        <p>하이퍼 텍스트 마크업 언어(Hyper Text Markup Language, HTML, 문화어: 초본문표식달기언어, 하이퍼본문표식달기언어)는 
            웹 페이지를 위한 지배적인 마크업 언어다.</p>
    </blockquote>
    <p>차세대웹기술지원센터의 데이터에 따르면 
        <q cite="https://www.koreahtml5.kr/front/stats/browser/browserUseStats.do">
        2021년 대한민국에서 가장 점유율이 높은 웹 브라우저는 구글의 그롬입니다.</q>
    </p>
    <p>세일 기간을 맞이하여 온라인 강의 수강권을 할인된 금액(정가<del>36,000원</del> <ins>20,000원</ins>에 판매합니다.</p>
    <p>공기의 원소 기호는 H<sub>2</sub>0</p>
    <p>4<sup>2</sup>은 16입니다.</p>
</body>
</html>
'''
