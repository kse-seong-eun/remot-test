# API 활용 과제
# 📌 할 일 관리(Todo)

작업물 배포 링크 : '[오늘의 할 일](https://todolistkse.netlify.app)'

![image](https://github.com/kse-seong-eun/-Git-practice/assets/66905959/39ef2d6f-d1fe-458e-a431-ea1d24086b83)
![image](https://github.com/kse-seong-eun/-Git-practice/assets/66905959/d516ce9b-2f89-41e9-becb-6eb6bedcf789)
![image](https://github.com/kse-seong-eun/-Git-practice/assets/66905959/05d7a855-72d0-4c09-be3d-709aa53689f4)

## 스택
- <img src="https://img.shields.io/badge/Sass-CC6699?style=flat&logo=sass&logoColor=white">
- <img src="https://img.shields.io/badge/React-61DAFB?style=flat&logo=React&logoColor=white"/>
- <img src="https://img.shields.io/badge/vite-646CFF?style=flat&logo=vite&logoColor=white"/>
- <img src="https://img.shields.io/badge/eslint-4B32C3?style=flat&logo=eslint&logoColor=white"/>
- <img src="https://img.shields.io/badge/prettier-F7B93E?style=flat&logo=prettier&logoColor=white"/>

### 오류 수정 중
- [x] 새로고침 시 todolist의 텍스트 사라짐
- [ ] 완료한 list 비활성화 안됨
- [ ] list 내용 수정 기능 추가 필요

### ❗ 기능 구현
- [x] 할 일 목록(List)이 출력. 
- [x] 할 일 항목(Item)을 새롭게 추가. 
- [x] 할 일 항목을 삭제. 

### ❔ 기능 추가 예정
- [ ] 할 일 항목의 순서를 바꿀 수 있도록 만들어보세요. (추천 라이브러리 - [SortableJS](http://sortablejs.github.io/Sortable/))
- [ ] 할 일을 완료하지 않은 항목과 완료한 항목을 분류해서 출력해보세요.
- [ ] 할 일을 완료한 항목을 한 번에 삭제할 수 있도록 만들어보세요.
- [ ] 할 일 항목의 최신 수정일을 표시해보세요.
- [ ] 할 일 목록이 출력되기 전에 로딩 애니메이션이 보이도록 만들어보세요.
- [ ] 기타 동작이 완료되기 전에 로딩 애니메이션이 보이도록 만들어보세요.
- [ ] 차별화가 가능하도록 프로젝트를 최대한 예쁘게 만들어보세요.
- [ ] 할 일과 관련된 기타 기능도 고려해보세요.

----
# 🎬 영화 검색
작업물 배포 링크 :'[완성 사이트](https://omdbapikse.netlify.app)'



<영화 검색 메인 페이지>
![image](https://github.com/kse-seong-eun/-Git-practice/assets/66905959/5e52ca63-86a0-4b4e-9e51-555d553c30f4)

<영화 검색 결과>
![image](https://github.com/kse-seong-eun/-Git-practice/assets/66905959/16804a90-6040-4721-8722-1ef035004112)

<영화 상세 페이지>
![image](https://github.com/kse-seong-eun/-Git-practice/assets/66905959/f3923ff6-222e-4e3d-92c7-279e007a9ddf)

![M2 영화검색 APImobile (1)](https://github.com/kse-seong-eun/-Git-practice/assets/66905959/3d5c1b16-7a75-44d1-8887-bb9792c13e7a)

<페이지 구성>
![M2 영화검색 APImobile (2)](https://github.com/kse-seong-eun/-Git-practice/assets/66905959/28f7d069-09e1-4f0b-a999-4a29a6a4a15a)


## 스택
- 언어 : JS
- 번들러 : Webpack
- 스타일 : Scss
- 배포 : 넷리파이

## 구조

- 진입점 : main.js

```
  ______________   _________     _________    __________________________
  | index.html |--| main.js |---|  App.js |--| TheNav.js, TheFooter.js |
  ¯¯¯¯¯¯¯¯¯¯¯¯¯¯   ¯¯¯¯¯¯¯¯¯  |  ¯¯¯¯¯¯¯¯¯    ¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯
                              | ___________    __________   __________________________________________________________
                              ㄴ| index.js |---| Home.js |--| TheHeader.js, Search.js, MovieList.js, MovieListMore.js |
                                ¯¯¯¯¯¯¯¯¯¯¯ |  ¯¯¯¯¯¯¯¯¯¯   ¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯
                                            |  __________
                                            |-| About.js |
                                            |  ¯¯¯¯¯¯¯¯¯¯
                                            | ___________
                                            ㄴ| Movie.js |
                                              ¯¯¯¯¯¯¯¯¯¯¯
```

## 문제사항

- add.hide // remove.hide 적용이 안됌. (영화 검색 로딩 애니메이션 & 검색 더보기 버튼)
- 영화 검색 시 포스터, 제목, 출시년도 중 년도 데이터 못읽음 ->undefined
- 영화를 검색하고 'view more'버튼으로 다음 페이지를 불러는것 까지는 작동. 이후에 같은 영화목록이 무한대로 불러와짐

### ❗ 기능구현

- [x] 영화 제목으로 검색이 가능!
- [x] 검색된 결과의 영화 목록이 출력!
- [x] 단일 영화의 상세정보(제목, 개봉연도, 평점, 장르, 감독, 배우, 줄거리, 포스터 등)조회!
- [x] 한 번의 검색으로 영화 목록이 20개 이상 검색.
- [x] 영화 목록을 검색하는 동안 로딩 애니메이션이 보이도록.
- [x] 무한 스크롤 기능을 추가.
- [x]  영화 상세정보가 출력되기 전에 로딩 애니메이션이.
- [x] 영화 상세정보 포스터를 고해상도로 출력(실시간 이미지 리사이징)

### ❔ 추가 기능 예정
- [ ] 영화 개봉연도로 검색할 수 있도록.
- [ ] 영화 포스터가 없을 경우 대체 이미지를 출력하도록.
- [△] 차별화가 가능하도록 프로젝트를 최대한 예쁘게.
- [ ] 영화와 관련된 기타 기능도 고려.

