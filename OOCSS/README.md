# OOCSS

- Object Oriented CSS 의 약자입니다.

- 중복을 최소화 하고 module화를 원칙으로 하는 스타일 방법입니다.

- 어떻게 보이는지가 아닌, 목적에 따라서 작명합니다.

## 디테일

- 구조(sturcture)와 외양(skin)을 분리합니다.

	- 반복적인 시간적 기능(배경, 테두리, 사이즈 등)을 별도의 skin으로 정의하여 다양한 객체에 사용하여, 중복 코드를 방지하면서 스타일을 표현합니다.

	- 예시

	```
	// structure
	.button{
		...
	}
	.box{
		...
	}

	// style
	.skin{
		background: #ccc;
		box-shadow: 2px 2px 11px 11px rgba(0,0,0,0.2);
	}
	```

- 컨테이너와 컨텐츠을 분리합니다.

	- 스타일을 정의할 때 위치에 의존적으로 스타일을 지정하지 않고, 사물의 모양은 어디에 위치하던지 동일하게 보이도록 합니다. 

	- 예시

	```
	// bad
	h2{
		bakcground: red
	}
	.content h2 {
		background: black;
	}

	//nice
	h2{
		background: red;
	}
	h2.title{
		background: black
	}
	```

### 예시

- 컨텐츠과 컨테이너 분리 예시

```
// html
<div class="header_inside common_conatiner"></div>
<div class="main common_conatiner"></div>
<div class="footer_inside common_conatiner"></div>

// css
.common_conatiner{
	position: relative;
	padding-left: 20px;
	padding-right: 20px;
	margin: 0 auto;
	width: 980px;
	overflow: hidden;
}

.header_inside{
	padding-top: 20px;
	padding-bottom: 20px;
	height: 260px;
}

.main{
	...
}

.footer_inside{
	...
}
```

- 오버라이딩 CSS 줄이기 예시

```
// html
<button type="button" class="btn_common btn_twitter">Twitter</button>
<button type="button" class="btn_common btn_instagram">Instagram</button>

// css
.btn_common{
	border:3px solid #000;
  padding:10px 20px;
  color:#fff;
  border-radius:10px;
}

.btn_twitter{
	backgrond-color: red;
}

.btn_instagram{
	background-color: blue;
}
```


## 참고

- [OOCSS란?_1](https://wit.nts-corp.com/2015/04/16/3538)

- [OOCSS란?_2](https://medium.com/witinweb/css-%EB%B0%A9%EB%B2%95%EB%A1%A0-2-oocss-object-oriented-css-4064e1119354)

- [OOCSS란?_3](https://medium.com/@jinminkim_50502/css-bem-smacss-oocss-9e4d6beb0a38)