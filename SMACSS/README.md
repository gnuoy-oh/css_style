# SMACSS

- 스맥스는 다섯가지 스타일로 분류하고, 각 유형에 맞는 선택자(selector)와 작명법(naming convention), 코딩기법을 제시합니다.

	- 기초(Base)

	- 레이아웃(Layout)

	- 모듈(Module)

	- 상태(Status)

	- 테마(Theme)

- CSS를 module화하고 확장 가능하게 만들기 위한 목적이고, 프레임워크 보다는 스타일 가이드에 초점을 맞추고 있습니다.

- Class명을 통한 예측, 재사용성, 보다 쉬운 유지보수, 확장 가능성의 목적을 하고 있습니다.

## Base

### 설명

- 각 브라우저의 스타일을 초기화 시키는 목적으로 사용합니다. (스타일 초기화)

	- reset, common, default, variables, mixin 

- !important를 사용하지 않습니다.

### 예시

- PC reset 

```
	
	/* reset */
	body,div,dl,dt,dd,ul,ol,li,h1,h2,h3,h4,h5,h6,pre,code,form,fieldset,legend,textarea,p,blockquote,th,td,input,select,button{margin:0;padding:0}
	fieldset,img{border:0 none}
	dl,ul,ol,menu,li{list-style:none}
	blockquote, q{quotes: none}
	blockquote:before, blockquote:after,q:before, q:after{content:'';content:none}
	input,select,textarea,button{vertical-align:middle}
	input::-ms-clear{display:none}
	button{border:0 none;background-color:transparent;cursor:pointer}
	body{background:#fff}
	body,th,td,input,select,textarea,button{font-size:12px;line-height:1.5;font-family:'돋움',dotum,sans-serif;color:#333} /* color값은 디자인가이드에 맞게사용 */
	a{color:#333;text-decoration:none}
	a:active, a:hover{text-decoration:underline}
	a:active{background-color:transparent}
	address,caption,cite,code,dfn,em,var{font-style:normal;font-weight:normal}
```

## Layout

### 설명

- 큰 하나의 Block을 구성하는 레이아웃, 상위 선택자에 위치해서 페이지를 구획하는 스타일로써 사용합니다. 

- 레이아웃과 관련된 스타일을 정의할 때 사용합니다.

	- 주요 component: header, footer, content, aside 등

	- 하위 component: 주요 component 내에 있는 component를 의미합니다.

		- nav, gnb, item list, form 등

- 	선택자 사용

	- 주요 component: id, class로 지정합니다.

	- 하위 component: class에 prefix fh **l-**, **layout-** 을 명시적으로 사용합니다.

### 예시

- 주요 component layout

```
#header { width: 400px; }
#aside { width: 30px; }
```

- 하위 component layout

```
.l-fixed #content {
  width: 600px;
  margin-right: 10px;
}
.l-fixed #aside {
  width: 200px
}
```

## Module

### 설명

- 페이지에서 module화가 가능한, 재사용이 가능한 스타일로써 사용합니다.

	- button, widget, banner, logo 등

- 레이아웃 구성요소 안에 존재하지만, 다른 모듈에도 존재할 수 있습니다.

	- 즉, 독립적으로 존재하도록 설계합니다.

- 재사용을 위해 class으로 선택자를 지정합니다. (id 사용하지 않음)

	- 모듈의 상태 변화는 하위 클래스로 스타일링을 합니다.

### 예시

- box module

```
// html
<div class="box">
  <span class="box-name"> ... </span>
  <span class="box-items"> ... </span>
</div>

// css 
.box { ... }
.box-name { ... }
.box-items { ... }

// css 2
.pod {
    width: 100%;
}
.pod input[type=text] {
    width: 50%;
}
.pod-constrained input[type=text] {
    width: 100%;
}
.pod-callout {
    width: 200px;
}
.pod-callout input[type=text] {
    width: 180px;
}
```

## State

### 설명

- 여기부터~~~~~

### 예시

- 여기부터~~~~~

## 참고

- [BEM이란?_1](https://junwoo45.github.io/2019-08-29-BEM/)

- [BEM이란?_2](https://nykim.work/15)

- [BEM이란?_3](https://medium.com/@jinminkim_50502/css-bem-smacss-oocss-9e4d6beb0a38)