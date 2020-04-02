# BEM

- 블록(Block), 요소(Element), 상태(Modifier)로 구분하여 클래스를 작성하며, 서로 다른 역할을 수행하도록 차별화합니다.

- Id는 사용하지 않고, class를 사용하여 작성을 합니다.

- 어떻게 보이는지가 아닌, 목적에 따라서 작명합니다.

- block__element--modifier-typea

## Block

### 설명

- 기능적으로 독립적이고 재사용이 가능한 Block 단위의 component를 의미합니다.

	- header block, footer block, nav block, main block 등 컨텐츠 영역을 block이라 할 수 있다.

	- 조금 더 구체적으로 menu block, form block, logo block도 가능하다.

- Block 은 Block을 감쌀 수 있습니다.

- block의 형태가 길어질 경우 (-)를 사용합니다.

	- header-top__

### 예시

- 예시: 한 단어 

```
<div class="header"></div>
<div class="footer"></div>
```

- 예시: 두 단어 

```
<div class="header-block"></div>
<div class="login-form"></div>
```


## Element

### 설명

- Element 요소는 Block 내부 구성을 표현하는 단위로, 독립적으로는 의미가 없으며 Block을 붙어서 사용하는 Component 입니다.

	- Element는 의존적인 형태로, 자신이 속한 Block내에서만 의미를 가집니다.

- Block 안에서 특정 기능을 수행하는 component로, **두 개의 언더스코어(_)**로 표기합니다.

### 예시

- 예시: 한 단어 

```
<div class="header">
	<div class="header__logo"></div>
	<a href="#none" class="header__link"></a>
	<div class="header__tab"></div>
</div>
```

- 예시: 두 단어 

```
<div class="search-block">
	<div class="search-block__content">
		<input class="search-block__input"></input>
		<button class="seach-block__button">Search</button>
	</div>
</div>
```

## Modifier

### 설명

- Block이나 Element의 상태를 나타낼 수 있는 속성으로, Block이나 Element의 상태, 외관을 표현합니다.

	- 특정 요소의 스타일을 수정해야할 필요가 있을 때 활용합니다.

- Block이나 Element 뒤에 **두 개의 하이픈(-)**을 추가하여 Modifier를 표시합니다.

- key-value 형태로도 표현할 수 있습니다.

	- search-form--theme-special

	- button--state-danger

### 예시

- 예시

```
<div class="gnb gnb--theme-header">
	<ul class="gnb__list">
		<li class="gnb__item">
			<button type="button" class="gnb__button'>
				Click
			</button>
		</li>
		<li class="gnb__item">
			<button type="button" class="gnb__button gnb__button--active'>
				Click
			</button>
		</li>
	</ul>
</div>
```

## 참고

- [BEM이란?_1](https://junwoo45.github.io/2019-08-29-BEM/)

- [BEM이란?_2](https://nykim.work/15)

- [BEM이란?_3](https://medium.com/@jinminkim_50502/css-bem-smacss-oocss-9e4d6beb0a38)