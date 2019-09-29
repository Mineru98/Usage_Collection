How can I write markdown?
======================

# 1. About Markdown
## 1.1. What is MD(MarkDown)?
[**Markdown**](http://whatismarkdown.com/)은 텍스트 기반의 마크업언어로 2004년에 [존그루버](https://en.wikipedia.org/wiki/John_Gruber)에 의해 고안이되었다. 쉽게 쓰고 읽을 수 있으며 HTML로 변환이 가능하다. 특수기호와 문자를 사용한 매우 간단한 구조의 문법을 사용하여 웹에서도 보다 빠르게 컨텐츠를 작성하고 보다 직관적으로 인식할 수 있다.

마크다운이 최근 각광받기 시작한 이유는 [GitHub](https://github.com) 덕분이다. GitHub의 저장소인 Repository에 관한 정보에 대한 설명을 README.md로 하기 떄문에 이는 GitHub를 사용하는 사람이라면 가장 먼저 접하게 되는 마크다운 문서였다. 마크다운을 통해서 어떠한 소스에 대한 다른 소스의 설치방법, 소스코드 설명, 이슈 등을 간단하게 기록하고 가독성을 높일 수 있다는 강점이 부각되면서 점점 여러 곳으로 퍼져가게 된다.

## 1.2. Pros and Cons of Markdown(마크다운의 장단점)
### 1.2.1. pros(장점)
 - Simple(간결하다)
 - 별도의 도구없이 작성가능하다.
 - 다양한 형태로 변환이 가능하다.
 - Text로 저장되기 때문에 용량이 적어 보관이 용이하다.
 - TextFile이기 때문에 Version Control System을 이용하여 변경이력을 관리할 수 있다.
 - 지원하는 프로그램과 플랫폼이 다양하다(호환성이 좋다).
### 1.2.2. Cons(단점)
 - 표준이 없다.
 - 표준이 없기 때문에 도구에 따라서 변환방식이나 결과물이 다르다.(단점인가?)
 - 모든 HTML 마크업을 대신하지 못한다.

****
# 2. Markdown Syntax(문법)
## 2.1. Headers
* 큰제목: 문서 제목
    ```
    This is an H1 (꼭 여러개가 아니어도 됌. '=' 두개부터 적용됨.)
    =============
    ```
    This is an H1
  	=============

* 작은제목: 문서 부제목
    ```
    This is an H2 (마찬가지로 '-' 두개부터 적용 됨.)
    -------------
    ```
    This is an H2
    -------------

* 글머리: 1~6까지만 지원
```
# This is a H1
## This is a H2
### This is a H3
#### This is a H4
##### This is a H5
###### This is a H6
```
# '='랑 동일한 크기
## '-'랑 동일한 크기
### 점점
#### 작아지는
##### 기분이지만
###### 여긴 색깔이 약간 옅어진다.
####### 7개 부터는 적용 안됨.

## 2.2. BlockQuote
누군가의 말을 인용했다고 할 때 사용하는 인용구는 ```>``` <= 요녀석을 이용한다.

```
> 이렇게 blockqute를 사용하면 돼요.
```

> 이렇게 blockqute를 사용하면 돼요.

```
> 이렇게 한문장이 아니라

> 여러 문장을 할 때는

> 이런식으로
```

> 이렇게 한문장이 아니라

> 여러 문장을 할 때는

> 이런식으로

```
> 실수로 문장을 안띄우면
> 이런 일이 발생합니다.
```

> 실수로 문장을 안띄우면
> 이런 일이 발생합니다.

인용구 안에서는 다른 마크다운 요소를 포함할 수 있다.
> ### Title
> * Subtitle
>	```
>	code
>	```

## 2.3. List(목록)
### ● 순서있는 목록(번호)
순서있는 목록은 숫자와 점을 사용한다.
```
1. 하나
2. 둘
3. 삼
4. 넷
5. 오
```
1. 하나
2. 둘
3. 삼
4. 넷
5. 오

**어떤 번호를 입력해도 순서는 내림차순으로 정의된다.**
```
9. 여섯
8. 칠
7. 팔
6. 아홉
```
9. 여섯
8. 칠
7. 팔
6. 아홉

### ● 순서없는 목록(글머리 기호)
```
* 빨강
  * 녹색
    * 파랑

+ 빨강
  + 녹색
    + 파랑

- 빨강
  - 녹색
    - 파랑
```
* 빨강
  * 녹색
    * 파랑

+ 빨강
  + 녹색
    + 파랑

- 빨강
  - 녹색
    - 파랑

혼합해서 사용하는 것도 가능함(님 꼴리는대로)
```
* 1단계
 - 2단계
  + 3단계
   * 4단계
    - 5단계
     + 6단계
      * 다단계
```

* 1단계
 - 2단계
   + 3단계
	  * 4단계
		 - 5단계
		  + 6단계
			 * 다단계

## 2.4. Code```<pre><code></code></pre>```
일반적으로 사용하는 방법은 다음과 같다.

```
키보드에서 Tab 위에 있거나 ! 왼족에 있는 키를 Shift를 누르지않고
그냥 누르면 '`' 요녀석이 있는데 이녀석을 한번만 쓰거나
행열을 바꾸지 않고 이어서 쓰지 않고 세번을 연타하면 이렇게 적용된다.
```

`
한번만 쓰면 이렇게 된다.
`

```세번을 다 눌러도 행열을 바꾸지 않으면 이렇게 됨.```

또 다른 방법은 4개의 공백 또는 하나의 탭으로 들여쓰기를 만나면 변환되기 시작하여 들여쓰지 않은 행을 만날때까지 변환이 계속된다.

    이렇게 띄어쓰기를 4번 하거나
.
	
	이렇게 Tab을 하거나
    Tab과 띄어쓰기 네번을 결합해도 된다.

> 한줄 띄어쓰면 인식이 제대로 안되는 문제가 발생하곤 함.



## 2.5. Horizon(수평선)```<hr/>```
아래 줄은 모두 글간의 **구분**을 해주는 수평선을 만들어 준다. (조건: 세개 이상씩 입력해줘야 한다.)
```
* * *

***

*****

- - -

---------------------------------------
```

* * *

***

*****

- - -

---------------------------------------


## 2.6. Link(링크)
* 참조링크

```
[link keyword][id]
[id]: URL "Optional Title here"

Link: [Naver][naverlink "description"]
[naverlink]: https://www.naver.com "Go Naver"
```

Link: [Naver][naverlink]
[naverlink]: https://www.naver.com "Go Naver"

* inLine Link
```
syntax: [Title](link, "description")
```
Link: [Naver](https://www.naver.com, "naver link")

* Auto Connection
```
<http://example.com/>
<address@example.com>
```

<http://example.com/>

<address@example.com>

## 2.7. Decoration(강조)
```
*문자 기울기(별표)*

_문자 기울기(언더라인)_

**볼드체(별표)**

__볼드체(언더라인)__

~~취소선~~
```
*문자 기울기(별표)*

_문자 기울기(언더라인)_

**볼드체(별표)**

__볼드체(언더라인)__

~~취소선~~

## 2.8. Image(이미지)
```
![Alt text](/path/to/img.jpg)
![Alt text](/path/to/img.jpg "Description")
```
![GithubIcon](https://github.githubassets.com/images/modules/logos_page/Octocat.png)
![GithubIcon](https://github.githubassets.com/images/modules/logos_page/Octocat.png "Github Icon")

사이즈 조절 기능 따위는 없다.

****

## ● 출처
* [John gruber 마크다운 번역본](http://nolboo.github.io/blog/2013/09/07/john-gruber-markdown/)
* [깃허브 취향의 마크다운 번역](http://nolboo.github.io/blog/2014/03/25/github-flavored-markdown/)
* [허니몬의 마크다운 작성법](http://www.slideshare.net/ihoneymon/ss-40575068)