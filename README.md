# HOMEWORK04-레이아웃

## 1. 과제 주제 설명
---

- 이번 과제의 제목은 My Home Page이며 '나만의 홈페이지'를 만든다면 어떤 요소들이 들어가면 좋을지 떠올려보며 작성하였다.

- My Home Page 상단은 home, Gallery, Login항목이 포함된 메뉴와 사진이 포함되어 있고 중간 부분과 하단은 사진, 일정, 일지, 저작권 표시 등이 포함되어 있다.



## 2. 주요 코드 설명
---
### Grid 사용하여 홈페이지의 전체적인 구조 설정
   ```html
   <style>
      .container{
         display: grid;
         grid-template-rows: 83px 300px 380px 450px 70px;
         grid-template-columns: repeat(3, 1fr);
         grid-template-areas:
               "header header header" 
               "header header header"
               "main main aside"
               "section section section"
               "footer footer footer";}
   </style>
   ```
   - .container는 body부분에서 전체 코드를 감싸고 있는 container라는 이름을 가진 클래스이다.

   - 이 container클래스를 grid로 설정하고 grid-template-rows/columns를 이용하여 5개의 행과 3개의 열로 구성된 그리드를 만들었다.

   - grid-template-areas를 통해 생성한 그리드의 각 영역에 header, main, aside, section, footer라는 이름을 지정하였다.


 ### body의 전체적 구조와 Grid 영역 지정

   ```html
   <body>
      <div class="container">
         <header>Header</header>
         <main>Main</main>
         <aside>Aside</aside>
         <section>Section</section>
         <footer>Footer</footer>
      <div>
   </body>
   ```   
   
   ```css
   <style>
      header{grid-area:header;}
      main{grid-area:main;}
      section{grid-area:section;}
      aside{grid-area:aside;}
      footer{grid-area:footer;}
   </style>
   ```
   - body에서 header, main, aside, section, footer 태그를 이용해 큰 틀을 정하였다.
   
   - 각 태그들(grid-item들)에 대해 grid-area속성을 이용하여 영역의 이름 지정하였다. (지정한 이름에 따라 배치됨)


 ### header 요소 구조
   ```html
   <header>
      <nav class="navbar">
         <ul class="navbar-menu">
            <li>Home</li>
                ...
         </ul>
      </nav>
      <div class="header-image"></div>
   </header>
   ```
   - header에서 nav태그와 div태그를 이용하여 각각 메뉴와 사진을 설정하였다.
   
   - 메뉴는 head 부분에서 Flex박스를 이용하여 만들었다.

### main, aside, section 요소 구조
   ```css
   main{display:flex;}

   section{display:flex;}
       
   aside{display:flex;}
   ```
   ```html
   <main>
      <div><img src="" height="200"></div>
      <div><p>Lorem</p></div>
   </main>

   <aside>
      <div><p>Lorem</p></div>
   </aside>

   <section>
      <div><p>Lorem</p></div>
      <div><p>Lorem</p></div>
   </section>
   ``` 
   - main, aside요소는 3열을 차지하고 section요소는 4열을 차지하는데 main, aside, section 모두 display속성을 flex로 설정하여 각각의 내부 자식 요소들을 쉽게 정렬하였다. 
   
### footer 요소 구조

```html
<footer>
   <div><p>Copyright &copy;2020. All Right Reserved.</p></div>  
</footer>
```
- footer요소는 저작권을 표시하는 공간으로 사용하였고 div태그를 이용하여 저작권 표시 문구를 썼다.



## 비교 및 고찰
---
- 본 과제를 통해 직접 홈페이지의 구조를 만들어봄으로써 레이아웃이 어떻게 설계되는지 더 잘 이해할 수 있었고, 실습 내용으로는 부족했던 grid와 flex에 대한 개념을 더 이해할 수 있었다.

- 설계 초반에는 어떤 것부터 시작해야 할지 감이 잡히지 않아 많이 헤매었지만 수업 자료를 복습하고 인터넷 검색을 해보면서 레이아웃에 대해 어느정도 이해할 수 있었고 끝까지 잘 마무리 할 수 있었다.

- 이번 과제를 수행하면서 4주차 때 배운 내용들 뿐 아니라 이전에 배웠던 태그들과 css속성들도 사용하게 되었는데 이로써 배웠던 내용들을 잊지 않고 더 오래 기억하고 잘 활용할 수 있게 되었다.

- 아직 flex 박스, Grid container의 속성과 flex item, Grid item의 속성들을 사용하는 것이 익숙하지 않고 여러 속성들의 개념이 혼동되는 것 같다. 앞으로 계속 복습하고 실습해보며 익숙해져야 할 필요가 있다.

- 세부적으로 각각 코드를 볼 때는 이해가 잘 되나, 전체적인 구조를 보는 것이 아직은 부족한 것 같다. 추가 자료들을 찾아보며 학습할 필요가 있다.



