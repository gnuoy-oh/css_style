# CSS방법론

## 설명

- 프로젝트의 규모가 커지면 CSS의 복잡도는 증가하면서, 다수의 개발자 분들과 작업을 하게될 시, CSS 코드를 일관성 있는 규칙을 가지고 작업할 필요가 있습니다.

### 구체적인 목적

- 코드의 재사용성을 높이는 것

	- 공통 ui를 module화 하는 것

- 혼자가 아닌, 모두가 이해하기 쉬운 코드를 만드는 것

	- class 이름으로도 어디에 사용되는지 예측이 쉽도록 하는 것

## 대표적인 CSS 방법론 

### BEM

- Block Element Modifier

- 블록 Block, 요소 Element, 상태 Modifier로 구분하여 class를 작성하며, 엄격한 네이밍 규칙을 따릅니다.

### SMACSS (스맥스)

- Scalable Modular Architecture CSS

- CSS의 확장형 모듈식 구조로, 각 유형에 맞는 선택자(selector)와 네이밍 작성법(naming convention), 코딩 기법을 제시합니다.
	
	- 기본(Base)

	- 레이아웃(Layout)

	- 모듈(Module)

	- 상태(State)

	- 테마(Theme)

### OOCSS

- Object oriented CSS

- 중복을 최소화하고, Capsule화를 원칙으로 하는 방법론으로 중복을 최소화하는 기법을 제시합니다.

## 참고한 블로그

- [CSS 방법론_1](https://bonedev.tistory.com/162)

- [CSS 방법론_2](https://medium.com/@jinminkim_50502/css-bem-smacss-oocss-9e4d6beb0a38)

- [CSS 방법론_3](https://webmaster.wspaper.org/archives/devsharing/smacss-%EC%9C%A0%EC%97%B0%ED%95%98%EA%B3%A0-%EB%AA%A8%EB%93%88%ED%99%94%EB%90%9C-css-%EB%B0%A9%EB%B2%95%EB%A1%A0-%ED%95%99%EC%8A%B5-1-%EC%8A%A4%ED%83%80%EC%9D%BC%EC%9D%98)

- [CSS 방법론_4](https://frontdev.tistory.com/entry/CSS-%EB%B0%A9%EB%B2%95%EB%A1%A0Methodologies)