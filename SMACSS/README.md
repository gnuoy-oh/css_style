# SMACSS

- 블록(Block), 요소(Element), 상태(Modifier)로 구분하여 클래스를 작성하며, 서로 다른 역할을 수행하도록 차별화합니다.

- Id는 사용하지 않고, class를 사용하여 작성을 합니다.

- 어떻게 보이는지가 아닌, 목적에 따라서 작명합니다.

- block__element--modifier-typea

## Block

![img_block](image/img_block.png)

### 설명

- 기능적으로 독립적이고 재사용이 가능한 Block 단위의 component를 의미합니다.

	- header block, footer block, nav block, main block 등 컨텐츠 영역을 block이라 할 수 있습니다.

	- 조금 더 구체적으로 menu block, form block, logo block도 가능합니다.

- Block 은 Block을 감쌀 수 있습니다.

- block의 형태가 길어질 경우 (-)를 사용합니다.

	- header-top__element--modifier

### 예시

- 한 단어 

```
<div class="header"></div>
<div class="footer"></div>
```

- 두 단어 

```
<div class="header-block"></div>
<div class="login-form"></div>
```



## 참고

- [BEM이란?_1](https://junwoo45.github.io/2019-08-29-BEM/)

- [BEM이란?_2](https://nykim.work/15)

- [BEM이란?_3](https://medium.com/@jinminkim_50502/css-bem-smacss-oocss-9e4d6beb0a38)