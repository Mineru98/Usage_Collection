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

## 2.9 Chart(표)

표를 만들기 위해선 다음과 같은 형식을 유지한채 계속 이러서 해주면 된다.

표를 만들기 위한 가장 큰 핵심은 두번째 줄이다.

```
| 내 | 맘 | 대 | 로 |
|-|-|-|-|
| 모 | 양 | 도 |  |
| 내 | 맘 | 대 | 로 |
```

| 내 | 맘 | 대 | 로 |
|-|-|-|-|
| 모 | 양 | 도 |  |
| 내 | 맘 | 대 | 로 |

## 2.10 Special Characters(특수문자)
|문자|코드|
|-|-|
| |&Tab|
| |&NewLine|
|!|&excl|
|"|&quot|
|#|&num|
|$|&dollar|
|%|&percnt|
|&|&amp|
|'|&apos|
|(|&lpar|
|)|&rpar|
|*|&ast|
|+|&plus|
|,|&comma|
|.|&period|
|/|&sol|
|:|&colon|
|;|&semi|
|<|&lt|
|=|&equals|
|>|&gt|
|?|&quest|
|@|&commat|
|[|&lsqb|
|\|&bsol|
|]|&rsqb|
|^|&Hat|
|_|&lowbar|
|`|&grave|
|{|&lcub|
| |&verbar|
|}|&rcub|
||&NonBreakingSpace|
|¡|&iexcl|
|¢|&cent|
|£|&pound|
|¤|&curren|
|¥|&yen|
|¦|&brvbar|
|§|&sect|
|¨|&Dot|
|©|&copy|
|ª|&ordf|
|«|&laquo|
|¬|&not|
|­|&shy|
|®|&reg|
|¯|&macr|
|°|&deg|
|±|&plusmn|
|²|&sup2|
|³|&sup3|
|´|&acute|
|µ|&micro|
|¶|&para|
|·|&middot|
|¸|&cedil|
|¹|&sup1|
|º|&ordm|
|»|&raquo|
|¼|&frac14|
|½|&frac12|
|¾|&frac34|
|¿|&iquest|
|À|&Agrave|
|Á|&Aacute|
|Â|&Acirc|
|Ã|&Atilde|
|Ä|&Auml|
|Å|&Aring|
|Æ|&AElig|
|Ç|&Ccedil|
|È|&Egrave|
|É|&Eacute|
|Ê|&Ecirc|
|Ë|&Euml|
|Ì|&Igrave|
|Í|&Iacute|
|Î|&Icirc|
|Ï|&Iuml|
|Ð|&ETH|
|Ñ|&Ntilde|
|Ò|&Ograve|
|Ó|&Oacute|
|Ô|&Ocirc|
|Õ|&Otilde|
|Ö|&Ouml|
|×|&times|
|Ø|&Oslash|
|Ù|&Ugrave|
|Ú|&Uacute|
|Û|&Ucirc|
|Ü|&Uuml|
|Ý|&Yacute|
|Þ|&THORN|
|ß|&szlig|
|à|&agrave|
|á|&aacute|
|â|&acirc|
|ã|&atilde|
|ä|&auml|
|å|&aring|
|æ|&aelig|
|ç|&ccedil|
|è|&egrave|
|é|&eacute|
|ê|&ecirc|
|ë|&euml|
|ì|&igrave|
|í|&iacute|
|î|&icirc|
|ï|&iuml|
|ð|&eth|
|ñ|&ntilde|
|ò|&ograve|
|ó|&oacute|
|ô|&ocirc|
|õ|&otilde|
|ö|&ouml|
|÷|&divide|
|ø|&oslash|
|ù|&ugrave|
|ú|&uacute|
|û|&ucirc|
|ü|&uuml|
|ý|&yacute|
|þ|&thorn|
|ÿ|&yuml|
|Ā|&Amacr|
|ā|&amacr|
|Ă|&Abreve|
|ă|&abreve|
|Ą|&Aogon|
|ą|&aogon|
|Ć|&Cacute|
|ć|&cacute|
|Ĉ|&Ccirc|
|ĉ|&ccirc|
|Ċ|&Cdot|
|ċ|&cdot|
|Č|&Ccaron|
|č|&ccaron|
|Ď|&Dcaron|
|ď|&dcaron|
|Đ|&Dstrok|
|đ|&dstrok|
|Ē|&Emacr|
|ē|&emacr|
|Ė|&Edot|
|ė|&edot|
|Ę|&Eogon|
|ę|&eogon|
|Ě|&Ecaron|
|ě|&ecaron|
|Ĝ|&Gcirc|
|ĝ|&gcirc|
|Ğ|&Gbreve|
|ğ|&gbreve|
|Ġ|&Gdot|
|ġ|&gdot|
|Ģ|&Gcedil|
|Ĥ|&Hcirc|
|ĥ|&hcirc|
|Ħ|&Hstrok|
|ħ|&hstrok|
|Ĩ|&Itilde|
|ĩ|&itilde|
|Ī|&Imacr|
|ī|&imacr|
|Į|&Iogon|
|į|&iogon|
|İ|&Idot|
|ı|&imath|
|Ĳ|&IJlig|
|ĳ|&ijlig|
|Ĵ|&Jcirc|
|ĵ|&jcirc|
|Ķ|&Kcedil|
|ķ|&kcedil|
|ĸ|&kgreen|
|Ĺ|&Lacute|
|ĺ|&lacute|
|Ļ|&Lcedil|
|ļ|&lcedil|
|Ľ|&Lcaron|
|ľ|&lcaron|
|Ŀ|&Lmidot|
|ŀ|&lmidot|
|Ł|&Lstrok|
|ł|&lstrok|
|Ń|&Nacute|
|ń|&nacute|
|Ņ|&Ncedil|
|ņ|&ncedil|
|Ň|&Ncaron|
|ň|&ncaron|
|ŉ|&napos|
|Ŋ|&ENG|
|ŋ|&eng|
|Ō|&Omacr|
|ō|&omacr|
|Ő|&Odblac|
|ő|&odblac|
|Œ|&OElig|
|œ|&oelig|
|Ŕ|&Racute|
|ŕ|&racute|
|Ŗ|&Rcedil|
|ŗ|&rcedil|
|Ř|&Rcaron|
|ř|&rcaron|
|Ś|&Sacute|
|ś|&sacute|
|Ŝ|&Scirc|
|ŝ|&scirc|
|Ş|&Scedil|
|ş|&scedil|
|Š|&Scaron|
|š|&scaron|
|Ţ|&Tcedil|
|ţ|&tcedil|
|Ť|&Tcaron|
|ť|&tcaron|
|Ŧ|&Tstrok|
|ŧ|&tstrok|
|Ũ|&Utilde|
|ũ|&utilde|
|Ū|&Umacr|
|ū|&umacr|
|Ŭ|&Ubreve|
|ŭ|&ubreve|
|Ů|&Uring|
|ů|&uring|
|Ű|&Udblac|
|ű|&udblac|
|Ų|&Uogon|
|ų|&uogon|
|Ŵ|&Wcirc|
|ŵ|&wcirc|
|Ŷ|&Ycirc|
|ŷ|&ycirc|
|Ÿ|&Yuml|
|Ź|&Zacute|
|ź|&zacute|
|Ż|&Zdot|
|ż|&zdot|
|Ž|&Zcaron|
|ž|&zcaron|
|ƒ|&fnof|
|Ƶ|&imped|
|ǵ|&gacute|
|ȷ|&jmath|
|ˆ|&circ|
|ˇ|&caron|
|˘|&breve|
|˙|&dot|
|˚|&ring|
|˛|&ogon|
|˜|&tilde|
|˝|&dblac|
|,̑|&DownBreve|
|,̲|&UnderBar|
|Α|&Alpha|
|Β|&Beta|
|Γ|&Gamma|
|Δ|&Delta|
|Ε|&Epsilon|
|Ζ|&Zeta|
|Η|&Eta|
|Θ|&Theta|
|Ι|&Iota|
|Κ|&Kappa|
|Λ|&Lambda|
|Μ|&Mu|
|Ν|&Nu|
|Ξ|&Xi|
|Ο|&Omicron|
|Π|&Pi|
|Ρ|&Rho|
|Σ|&Sigma|
|Τ|&Tau|
|Υ|&Upsilon|
|Φ|&Phi|
|Χ|&Chi|
|Ψ|&Psi|
|Ω|&Omega|
|α|&alpha|
|β|&beta|
|γ|&gamma|
|δ|&delta|
|ε|&epsiv|
|ζ|&zeta|
|η|&eta|
|θ|&theta|
|ι|&iota|
|κ|&kappa|
|λ|&lambda|
|μ|&mu|
|ν|&nu|
|ξ|&xi|
|ο|&omicron|
|π|&pi|
|ρ|&rho|
|ς|&sigmav|
|σ|&sigma|
|τ|&tau|
|υ|&upsi|
|φ|&phi|
|χ|&chi|
|ψ|&psi|
|ω|&omega|
|ϑ|&thetav|
|ϒ|&Upsi|
|ϕ|&straightphi|
|ϖ|&piv|
|Ϝ|&Gammad|
|ϝ|&gammad|
|ϰ|&kappav|
|ϱ|&rhov|
|ϵ|&epsi|
|϶|&bepsi|
|Ё|&IOcy|
|Ђ|&DJcy|
|Ѓ|&GJcy|
|Є|&Jukcy|
|Ѕ|&DScy|
|І|&Iukcy|
|Ї|&YIcy|
|Ј|&Jsercy|
|Љ|&LJcy|
|Њ|&NJcy|
|Ћ|&TSHcy|
|Ќ|&KJcy|
|Ў|&Ubrcy|
|Џ|&DZcy|
|А|&Acy|
|Б|&Bcy|
|В|&Vcy|
|Г|&Gcy|
|Д|&Dcy|
|Е|&IEcy|
|Ж|&ZHcy|
|З|&Zcy|
|И|&Icy|
|Й|&Jcy|
|К|&Kcy|
|Л|&Lcy|
|М|&Mcy|
|Н|&Ncy|
|О|&Ocy|
|П|&Pcy|
|Р|&Rcy|
|С|&Scy|
|Т|&Tcy|
|У|&Ucy|
|Ф|&Fcy|
|Х|&KHcy|
|Ц|&TScy|
|Ч|&CHcy|
|Ш|&SHcy|
|Щ|&SHCHcy|
|Ъ|&HARDcy|
|Ы|&Ycy|
|Ь|&SOFTcy|
|Э|&Ecy|
|Ю|&YUcy|
|Я|&YAcy|
|а|&acy|
|б|&bcy|
|в|&vcy|
|г|&gcy|
|д|&dcy|
|е|&iecy|
|ж|&zhcy|
|з|&zcy|
|и|&icy|
|й|&jcy|
|к|&kcy|
|л|&lcy|
|м|&mcy|
|н|&ncy|
|о|&ocy|
|п|&pcy|
|р|&rcy|
|с|&scy|
|т|&tcy|
|у|&ucy|
|ф|&fcy|
|х|&khcy|
|ц|&tscy|
|ч|&chcy|
|ш|&shcy|
|щ|&shchcy|
|ъ|&hardcy|
|ы|&ycy|
|ь|&softcy|
|э|&ecy|
|ю|&yucy|
|я|&yacy|
|ё|&iocy|
|ђ|&djcy|
|ѓ|&gjcy|
|є|&jukcy|
|ѕ|&dscy|
|і|&iukcy|
|ї|&yicy|
|ј|&jsercy|
|љ|&ljcy|
|њ|&njcy|
|ћ|&tshcy|
|ќ|&kjcy|
|ў|&ubrcy|
|џ|&dzcy|
||&ensp|
||&emsp|
||&emsp13|
||&emsp14|
||&numsp|
||&puncsp|
||&thinsp|
||&hairsp|
|​|&ZeroWidthSpace|
|‌|&zwnj|
|‍|&zwj|
|‎|&lrm|
|‏|&rlm|
|‐|&hyphen|
|–|&ndash|
|—|&mdash|
|―|&horbar|
|‖|&Verbar|
|‘|&lsquo|
|’|&rsquo|
|‚|&lsquor|
|“|&ldquo|
|”|&rdquo|
|„|&ldquor|
|†|&dagger|
|‡|&Dagger|
|•|&bull|
|‥|&nldr|
|…|&hellip|
|‰|&permil|
|‱|&pertenk|
|′|&prime|
|″|&Prime|
|‴|&tprime|
|‵|&bprime|
|‹|&lsaquo|
|›|&rsaquo|
|‾|&oline|
|⁁|&caret|
|⁃|&hybull|
|⁄|&frasl|
|⁏|&bsemi|
|⁗|&qprime|
||&MediumSpace|
|⁠|&NoBreak|
|⁡|&ApplyFunction|
|⁢|&InvisibleTimes|
|⁣|&InvisibleComma|
|€|&euro|
|,⃛|&tdot|
|,⃜|&DotDot|
|ℂ|&Copf|
|℅|&incare|
|ℊ|&gscr|
|ℋ|&hamilt|
|ℌ|&Hfr|
|ℍ|&quaternions|
|ℎ|&planckh|
|ℏ|&planck|
|ℐ|&Iscr|
|ℑ|&image|
|ℒ|&Lscr|
|ℓ|&ell|
|ℕ|&Nopf|
|№|&numero|
|℗|&copysr|
|℘|&weierp|
|ℙ|&Popf|
|ℚ|&rationals|
|ℛ|&Rscr|
|ℜ|&real|
|ℝ|&reals|
|℞|&rx|
|™|&trade|
|ℤ|&integers|
|Ω|&ohm|
|℧|&mho|
|ℨ|&Zfr|
|℩|&iiota|
|Å|&angst|
|ℬ|&bernou|
|ℭ|&Cfr|
|ℯ|&escr|
|ℰ|&Escr|
|ℱ|&Fscr|
|ℳ|&phmmat|
|ℴ|&order|
|ℵ|&alefsym|
|ℶ|&beth|
|ℷ|&gimel|
|ℸ|&daleth|
|ⅅ|&CapitalDifferentialD|
|ⅆ|&DifferentialD|
|ⅇ|&ExponentialE|
|ⅈ|&ImaginaryI|
|⅓|&frac13|
|⅔|&frac23|
|⅕|&frac15|
|⅖|&frac25|
|⅗|&frac35|
|⅘|&frac45|
|⅙|&frac16|
|⅚|&frac56|
|⅛|&frac18|
|⅜|&frac38|
|⅝|&frac58|
|⅞|&frac78|
|←|&larr|
|↑|&uarr|
|→|&rarr|
|↓|&darr|
|↔|&harr|
|↕|&varr|
|↖|&nwarr|
|↗|&nearr|
|↘|&searr|
|↙|&swarr|
|↚|&nlarr|
|↛|&nrarr|
|↝|&rarrw|
|↞|&Larr|
|↟|&Uarr|
|↠|&Rarr|
|↡|&Darr|
|↢|&larrtl|
|↣|&rarrtl|
|↤|&LeftTeeArrow|
|↥|&UpTeeArrow|
|↦|&map|
|↧|&DownTeeArrow|
|↩|&larrhk|
|↪|&rarrhk|
|↫|&larrlp|
|↬|&rarrlp|
|↭|&harrw|
|↮|&nharr|
|↰|&lsh|
|↱|&rsh|
|↲|&ldsh|
|↳|&rdsh|
|↵|&crarr|
|↶|&cularr|
|↷|&curarr|
|↺|&olarr|
|↻|&orarr|
|↼|&lharu|
|↽|&lhard|
|↾|&uharr|
|↿|&uharl|
|⇀|&rharu|
|⇁|&rhard|
|⇂|&dharr|
|⇃|&dharl|
|⇄|&rlarr|
|⇅|&udarr|
|⇆|&lrarr|
|⇇|&llarr|
|⇈|&uuarr|
|⇉|&rrarr|
|⇊|&ddarr|
|⇋|&lrhar|
|⇌|&rlhar|
|⇍|&nlArr|
|⇎|&nhArr|
|⇏|&nrArr|
|⇐|&lArr|
|⇑|&uArr|
|⇒|&rArr|
|⇓|&dArr|
|⇔|&hArr|
|⇕|&vArr|
|⇖|&nwArr|
|⇗|&neArr|
|⇘|&seArr|
|⇙|&swArr|
|⇚|&lAarr|
|⇛|&rAarr|
|⇝|&zigrarr|
|⇤|&larrb|
|⇥|&rarrb|
|⇵|&duarr|
|⇽|&loarr|
|⇾|&roarr|
|⇿|&hoarr|
|∀|&forall|
|∁|&comp|
|∂|&part|
|∃|&exist|
|∄|&nexist|
|∅|&empty|
|∇|&nabla|
|∈|&isin|
|∉|&notin|
|∋|&niv|
|∌|&notni|
|∏|&prod|
|∐|&coprod|
|∑|&sum|
|−|&minus|
|∓|&mnplus|
|∔|&plusdo|
|∖|&setmn|
|∗|&lowast|
|∘|&compfn|
|√|&radic|
|∝|&prop|
|∞|&infin|
|∟|&angrt|
|∠|&ang|
|∡|&angmsd|
|∢|&angsph|
|∣|&mid|
|∤|&nmid|
|∥|&par|
|∦|&npar|
|∧|&and|
|∨|&or|
|∩|&cap|
|∪|&cup|
|∫|&int|
|∬|&Int|
|∭|&tint|
|∮|&conint|
|∯|&Conint|
|∰|&Cconint|
|∱|&cwint|
|∲|&cwconint|
|∳|&awconint|
|∴|&there4|
|∵|&becaus|
|∶|&ratio|
|∷|&Colon|
|∸|&minusd|
|∺|&mDDot|
|∻|&homtht|
|∼|&sim|
|∽|&bsim|
|∾|&ac|
|∿|&acd|
|≀|&wreath|
|≁|&nsim|
|≂|&esim|
|≃|&sime|
|≄|&nsime|
|≅|&cong|
|≆|&simne|
|≇|&ncong|
|≈|&asymp|
|≉|&nap|
|≊|&ape|
|≋|&apid|
|≌|&bcong|
|≍|&asympeq|
|≎|&bump|
|≏|&bumpe|
|≐|&esdot|
|≑|&eDot|
|≒|&efDot|
|≓|&erDot|
|≔|&colone|
|≕|&ecolon|
|≖|&ecir|
|≗|&cire|
|≙|&wedgeq|
|≚|&veeeq|
|≜|&trie|
|≟|&equest|
|≠|&ne|
|≡|&equiv|
|≢|&nequiv|
|≤|&le|
|≥|&ge|
|≦|&lE|
|≧|&gE|
|≨|&lnE|
|≩|&gnE|
|≪|&Lt|
|≫|&Gt|
|≬|&twixt|
|≭|&NotCupCap|
|≮|&nlt|
|≯|&ngt|
|≰|&nle|
|≱|&nge|
|≲|&lsim|
|≳|&gsim|
|≴|&nlsim|
|≵|&ngsim|
|≶|&lg|
|≷|&gl|
|≸|&ntlg|
|≹|&ntgl|
|≺|&pr|
|≻|&sc|
|≼|&prcue|
|≽|&sccue|
|≾|&prsim|
|≿|&scsim|
|⊀|&npr|
|⊁|&nsc|
|⊂|&sub|
|⊃|&sup|
|⊄|&nsub|
|⊅|&nsup|
|⊆|&sube|
|⊇|&supe|
|⊈|&nsube|
|⊉|&nsupe|
|⊊|&subne|
|⊋|&supne|
|⊍|&cupdot|
|⊎|&uplus|
|⊏|&sqsub|
|⊐|&sqsup|
|⊑|&sqsube|
|⊒|&sqsupe|
|⊓|&sqcap|
|⊔|&sqcup|
|⊕|&oplus|
|⊖|&ominus|
|⊗|&otimes|
|⊘|&osol|
|⊙|&odot|
|⊚|&ocir|
|⊛|&oast|
|⊝|&odash|
|⊞|&plusb|
|⊟|&minusb|
|⊠|&timesb|
|⊡|&sdotb|
|⊢|&vdash|
|⊣|&dashv|
|⊤|&top|
|⊥|&bottom|
|⊧|&models|
|⊨|&vDash|
|⊩|&Vdash|
|⊪|&Vvdash|
|⊫|&VDash|
|⊬|&nvdash|
|⊭|&nvDash|
|⊮|&nVdash|
|⊯|&nVDash|
|⊰|&prurel|
|⊲|&vltri|
|⊳|&vrtri|
|⊴|&ltrie|
|⊵|&rtrie|
|⊶|&origof|
|⊷|&imof|
|⊸|&mumap|
|⊹|&hercon|
|⊺|&intcal|
|⊻|&veebar|
|⊽|&barvee|
|⊾|&angrtvb|
|⊿|&lrtri|
|⋀|&xwedge|
|⋁|&xvee|
|⋂|&xcap|
|⋃|&xcup|
|⋄|&diam|
|⋅|&sdot|
|⋆|&sstarf|
|⋇|&divonx|
|⋈|&bowtie|
|⋉|&ltimes|
|⋊|&rtimes|
|⋋|&lthree|
|⋌|&rthree|
|⋍|&bsime|
|⋎|&cuvee|
|⋏|&cuwed|
|⋐|&Sub|
|⋑|&Sup|
|⋒|&Cap|
|⋓|&Cup|
|⋔|&fork|
|⋕|&epar|
|⋖|&ltdot|
|⋗|&gtdot|
|⋘|&Ll|
|⋙|&Gg|
|⋚|&leg|
|⋛|&gel|
|⋞|&cuepr|
|⋟|&cuesc|
|⋠|&nprcue|
|⋡|&nsccue|
|⋢|&nsqsube|
|⋣|&nsqsupe|
|⋦|&lnsim|
|⋧|&gnsim|
|⋨|&prnsim|
|⋩|&scnsim|
|⋪|&nltri|
|⋫|&nrtri|
|⋬|&nltrie|
|⋭|&nrtrie|
|⋮|&vellip|
|⋯|&ctdot|
|⋰|&utdot|
|⋱|&dtdot|
|⋲|&disin|
|⋳|&isinsv|
|⋴|&isins|
|⋵|&isindot|
|⋶|&notinvc|
|⋷|&notinvb|
|⋹|&isinE|
|⋺|&nisd|
|⋻|&xnis|
|⋼|&nis|
|⋽|&notnivc|
|⋾|&notnivb|
|⌅|&barwed|
|⌆|&Barwed|
|⌈|&lceil|
|⌉|&rceil|
|⌊|&lfloor|
|⌋|&rfloor|
|⌌|&drcrop|
|⌍|&dlcrop|
|⌎|&urcrop|
|⌏|&ulcrop|
|⌐|&bnot|
|⌒|&profline|
|⌓|&profsurf|
|⌕|&telrec|
|⌖|&target|
|⌜|&ulcorn|
|⌝|&urcorn|
|⌞|&dlcorn|
|⌟|&drcorn|
|⌢|&frown|
|⌣|&smile|
|⌭|&cylcty|
|⌮|&profalar|
|⌶|&topbot|
|⌽|&ovbar|
|⌿|&solbar|
|⍼|&angzarr|
|⎰|&lmoust|
|⎱|&rmoust|
|⎴|&tbrk|
|⎵|&bbrk|
|⎶|&bbrktbrk|
|⏜|&OverParenthesis|
|⏝|&UnderParenthesis|
|⏞|&OverBrace|
|⏟|&UnderBrace|
|⏢|&trpezium|
|⏧|&elinters|
|␣|&blank|
|Ⓢ|&oS|
|─|&boxh|
|│|&boxv|
|┌|&boxdr|
|┐|&boxdl|
|└|&boxur|
|┘|&boxul|
|├|&boxvr|
|┤|&boxvl|
|┬|&boxhd|
|┴|&boxhu|
|┼|&boxvh|
|═|&boxH|
|║|&boxV|
|╒|&boxdR|
|╓|&boxDr|
|╔|&boxDR|
|╕|&boxdL|
|╖|&boxDl|
|╗|&boxDL|
|╘|&boxuR|
|╙|&boxUr|
|╚|&boxUR|
|╛|&boxuL|
|╜|&boxUl|
|╝|&boxUL|
|╞|&boxvR|
|╟|&boxVr|
|╠|&boxVR|
|╡|&boxvL|
|╢|&boxVl|
|╣|&boxVL|
|╤|&boxHd|
|╥|&boxhD|
|╦|&boxHD|
|╧|&boxHu|
|╨|&boxhU|
|╩|&boxHU|
|╪|&boxvH|
|╫|&boxVh|
|╬|&boxVH|
|▀|&uhblk|
|▄|&lhblk|
|█|&block|
|░|&blk14|
|▒|&blk12|
|▓|&blk34|
|□|&squ|
|▪|&squf|
|▫|&EmptyVerySmallSquare|
|▭|&rect|
|▮|&marker|
|▱|&fltns|
|△|&xutri|
|▴|&utrif|
|▵|&utri|
|▸|&rtrif|
|▹|&rtri|
|▽|&xdtri|
|▾|&dtrif|
|▿|&dtri|
|◂|&ltrif|
|◃|&ltri|
|◊|&loz|
|○|&cir|
|◬|&tridot|
|◯|&xcirc|
|◸|&ultri|
|◹|&urtri|
|◺|&lltri|
|◻|&EmptySmallSquare|
|◼|&FilledSmallSquare|
|★|&starf|
|☆|&star|
|☎|&phone|
|♀|&female|
|♂|&male|
|♠|&spades|
|♣|&clubs|
|♥|&hearts|
|♦|&diams|
|♪|&sung|
|♭|&flat|
|♮|&natur|
|♯|&sharp|
|✓|&check|
|✗|&cross|
|✠|&malt|
|✶|&sext|
|❘|&VerticalSeparator|
|❲|&lbbrk|
|❳|&rbbrk|
|⟦|&lobrk|
|⟧|&robrk|
|⟨|&lang|
|⟩|&rang|
|⟪|&Lang|
|⟫|&Rang|
|⟬|&loang|
|⟭|&roang|
|⟵|&xlarr|
|⟶|&xrarr|
|⟷|&xharr|
|⟸|&xlArr|
|⟹|&xrArr|
|⟺|&xhArr|
|⟼|&xmap|
|⟿|&dzigrarr|
|⤂|&nvlArr|
|⤃|&nvrArr|
|⤄|&nvHarr|
|⤅|&Map|
|⤌|&lbarr|
|⤍|&rbarr|
|⤎|&lBarr|
|⤏|&rBarr|
|⤐|&RBarr|
|⤑|&DDotrahd|
|⤒|&UpArrowBar|
|⤓|&DownArrowBar|
|⤖|&Rarrtl|
|⤙|&latail|
|⤚|&ratail|
|⤛|&lAtail|
|⤜|&rAtail|
|⤝|&larrfs|
|⤞|&rarrfs|
|⤟|&larrbfs|
|⤠|&rarrbfs|
|⤣|&nwarhk|
|⤤|&nearhk|
|⤥|&searhk|
|⤦|&swarhk|
|⤧|&nwnear|
|⤨|&nesear|
|⤩|&seswar|
|⤪|&swnwar|
|⤳|&rarrc|
|⤵|&cudarrr|
|⤶|&ldca|
|⤷|&rdca|
|⤸|&cudarrl|
|⤹|&larrpl|
|⤼|&curarrm|
|⤽|&cularrp|
|⥅|&rarrpl|
|⥈|&harrcir|
|⥉|&Uarrocir|
|⥊|&lurdshar|
|⥋|&ldrushar|
|⥎|&LeftRightVector|
|⥏|&RightUpDownVector|
|⥐|&DownLeftRightVector|
|⥑|&LeftUpDownVector|
|⥒|&LeftVectorBar|
|⥓|&RightVectorBar|
|⥔|&RightUpVectorBar|
|⥕|&RightDownVectorBar|
|⥖|&DownLeftVectorBar|
|⥗|&DownRightVectorBar|
|⥘|&LeftUpVectorBar|
|⥙|&LeftDownVectorBar|
|⥚|&LeftTeeVector|
|⥛|&RightTeeVector|
|⥜|&RightUpTeeVector|
|⥝|&RightDownTeeVector|
|⥞|&DownLeftTeeVector|
|⥟|&DownRightTeeVector|
|⥠|&LeftUpTeeVector|
|⥡|&LeftDownTeeVector|
|⥢|&lHar|
|⥣|&uHar|
|⥤|&rHar|
|⥥|&dHar|
|⥦|&luruhar|
|⥧|&ldrdhar|
|⥨|&ruluhar|
|⥩|&rdldhar|
|⥪|&lharul|
|⥫|&llhard|
|⥬|&rharul|
|⥭|&lrhard|
|⥮|&udhar|
|⥯|&duhar|
|⥰|&RoundImplies|
|⥱|&erarr|
|⥲|&simrarr|
|⥳|&larrsim|
|⥴|&rarrsim|
|⥵|&rarrap|
|⥶|&ltlarr|
|⥸|&gtrarr|
|⥹|&subrarr|
|⥻|&suplarr|
|⥼|&lfisht|
|⥽|&rfisht|
|⥾|&ufisht|
|⥿|&dfisht|
|⦅|&lopar|
|⦆|&ropar|
|⦋|&lbrke|
|⦌|&rbrke|
|⦍|&lbrkslu|
|⦎|&rbrksld|
|⦏|&lbrksld|
|⦐|&rbrkslu|
|⦑|&langd|
|⦒|&rangd|
|⦓|&lparlt|
|⦔|&rpargt|
|⦕|&gtlPar|
|⦖|&ltrPar|
|⦚|&vzigzag|
|⦜|&vangrt|
|⦝|&angrtvbd|
|⦤|&ange|
|⦥|&range|
|⦦|&dwangle|
|⦧|&uwangle|
|⦨|&angmsdaa|
|⦩|&angmsdab|
|⦪|&angmsdac|
|⦫|&angmsdad|
|⦬|&angmsdae|
|⦭|&angmsdaf|
|⦮|&angmsdag|
|⦯|&angmsdah|
|⦰|&bemptyv|
|⦱|&demptyv|
|⦲|&cemptyv|
|⦳|&raemptyv|
|⦴|&laemptyv|
|⦵|&ohbar|
|⦶|&omid|
|⦷|&opar|
|⦹|&operp|
|⦻|&olcross|
|⦼|&odsold|
|⦾|&olcir|
|⦿|&ofcir|
|⧀|&olt|
|⧁|&ogt|
|⧂|&cirscir|
|⧃|&cirE|
|⧄|&solb|
|⧅|&bsolb|
|⧉|&boxbox|
|⧍|&trisb|
|⧎|&rtriltri|
|⧏|&LeftTriangleBar|
|⧐|&RightTriangleBar|
|⧚|&race|
|⧜|&iinfin|
|⧝|&infintie|
|⧞|&nvinfin|
|⧣|&eparsl|
|⧤|&smeparsl|
|⧥|&eqvparsl|
|⧫|&lozf|
|⧴|&RuleDelayed|
|⧶|&dsol|
|⨀|&xodot|
|⨁|&xoplus|
|⨂|&xotime|
|⨄|&xuplus|
|⨆|&xsqcup|
|⨌|&qint|
|⨍|&fpartint|
|⨐|&cirfnint|
|⨑|&awint|
|⨒|&rppolint|
|⨓|&scpolint|
|⨔|&npolint|
|⨕|&pointint|
|⨖|&quatint|
|⨗|&intlarhk|
|⨢|&pluscir|
|⨣|&plusacir|
|⨤|&simplus|
|⨥|&plusdu|
|⨦|&plussim|
|⨧|&plustwo|
|⨩|&mcomma|
|⨪|&minusdu|
|⨭|&loplus|
|⨮|&roplus|
|⨯|&Cross|
|⨰|&timesd|
|⨱|&timesbar|
|⨳|&smashp|
|⨴|&lotimes|
|⨵|&rotimes|
|⨶|&otimesas|
|⨷|&Otimes|
|⨸|&odiv|
|⨹|&triplus|
|⨺|&triminus|
|⨻|&tritime|
|⨼|&iprod|
|⨿|&amalg|
|⩀|&capdot|
|⩂|&ncup|
|⩃|&ncap|
|⩄|&capand|
|⩅|&cupor|
|⩆|&cupcap|
|⩇|&capcup|
|⩈|&cupbrcap|
|⩉|&capbrcup|
|⩊|&cupcup|
|⩋|&capcap|
|⩌|&ccups|
|⩍|&ccaps|
|⩐|&ccupssm|
|⩓|&And|
|⩔|&Or|
|⩕|&andand|
|⩖|&oror|
|⩗|&orslope|
|⩘|&andslope|
|⩚|&andv|
|⩛|&orv|
|⩜|&andd|
|⩝|&ord|
|⩟|&wedbar|
|⩦|&sdote|
|⩪|&simdot|
|⩭|&congdot|
|⩮|&easter|
|⩯|&apacir|
|⩰|&apE|
|⩱|&eplus|
|⩲|&pluse|
|⩳|&Esim|
|⩴|&Colone|
|⩵|&Equal|
|⩷|&eDDot|
|⩸|&equivDD|
|⩹|&ltcir|
|⩺|&gtcir|
|⩻|&ltquest|
|⩼|&gtquest|
|⩽|&les|
|⩾|&ges|
|⩿|&lesdot|
|⪀|&gesdot|
|⪁|&lesdoto|
|⪂|&gesdoto|
|⪃|&lesdotor|
|⪄|&gesdotol|
|⪅|&lap|
|⪆|&gap|
|⪇|&lne|
|⪈|&gne|
|⪉|&lnap|
|⪊|&gnap|
|⪋|&lEg|
|⪌|&gEl|
|⪍|&lsime|
|⪎|&gsime|
|⪏|&lsimg|
|⪐|&gsiml|
|⪑|&lgE|
|⪒|&glE|
|⪓|&lesges|
|⪔|&gesles|
|⪕|&els|
|⪖|&egs|
|⪗|&elsdot|
|⪘|&egsdot|
|⪙|&el|
|⪚|&eg|
|⪝|&siml|
|⪞|&simg|
|⪟|&simlE|
|⪠|&simgE|
|⪡|&LessLess|
|⪢|&GreaterGreater|
|⪤|&glj|
|⪥|&gla|
|⪦|&ltcc|
|⪧|&gtcc|
|⪨|&lescc|
|⪩|&gescc|
|⪪|&smt|
|⪫|&lat|
|⪬|&smte|
|⪭|&late|
|⪮|&bumpE|
|⪯|&pre|
|⪰|&sce|
|⪳|&prE|
|⪴|&scE|
|⪵|&prnE|
|⪶|&scnE|
|⪷|&prap|
|⪸|&scap|
|⪹|&prnap|
|⪺|&scnap|
|⪻|&Pr|
|⪼|&Sc|
|⪽|&subdot|
|⪾|&supdot|
|⪿|&subplus|
|⫀|&supplus|
|⫁|&submult|
|⫂|&supmult|
|⫃|&subedot|
|⫄|&supedot|
|⫅|&subE|
|⫆|&supE|
|⫇|&subsim|
|⫈|&supsim|
|⫋|&subnE|
|⫌|&supnE|
|⫏|&csub|
|⫐|&csup|
|⫑|&csube|
|⫒|&csupe|
|⫓|&subsup|
|⫔|&supsub|
|⫕|&subsub|
|⫖|&supsup|
|⫗|&suphsub|
|⫘|&supdsub|
|⫙|&forkv|
|⫚|&topfork|
|⫛|&mlcp|
|⫤|&Dashv|
|⫦|&Vdashl|
|⫧|&Barv|
|⫨|&vBar|
|⫩|&vBarv|
|⫫|&Vbar|
|⫬|&Not|
|⫭|&bNot|
|⫮|&rnmid|
|⫯|&cirmid|
|⫰|&midcir|
|⫱|&topcir|
|⫲|&nhpar|
|⫳|&parsim|
|⫽|&parsl|
|ﬀ|&fflig|
|ﬁ|&filig|
|ﬂ|&fllig|
|ﬃ|&ffilig|
|ﬄ|&ffllig|
|𝒜|&Ascr|
|𝒞|&Cscr|
|𝒟|&Dscr|
|𝒢|&Gscr|
|𝒥|&Jscr|
|𝒦|&Kscr|
|𝒩|&Nscr|
|𝒪|&Oscr|
|𝒫|&Pscr|
|𝒬|&Qscr|
|𝒮|&Sscr|
|𝒯|&Tscr|
|𝒰|&Uscr|
|𝒱|&Vscr|
|𝒲|&Wscr|
|𝒳|&Xscr|
|𝒴|&Yscr|
|𝒵|&Zscr|
|𝒶|&ascr|
|𝒷|&bscr|
|𝒸|&cscr|
|𝒹|&dscr|
|𝒻|&fscr|
|𝒽|&hscr|
|𝒾|&iscr|
|𝒿|&jscr|
|𝓀|&kscr|
|𝓁|&lscr|
|𝓂|&mscr|
|𝓃|&nscr|
|𝓅|&pscr|
|𝓆|&qscr|
|𝓇|&rscr|
|𝓈|&sscr|
|𝓉|&tscr|
|𝓊|&uscr|
|𝓋|&vscr|
|𝓌|&wscr|
|𝓍|&xscr|
|𝓎|&yscr|
|𝓏|&zscr|
|𝔄|&Afr|
|𝔅|&Bfr|
|𝔇|&Dfr|
|𝔈|&Efr|
|𝔉|&Ffr|
|𝔊|&Gfr|
|𝔍|&Jfr|
|𝔎|&Kfr|
|𝔏|&Lfr|
|𝔐|&Mfr|
|𝔑|&Nfr|
|𝔒|&Ofr|
|𝔓|&Pfr|
|𝔔|&Qfr|
|𝔖|&Sfr|
|𝔗|&Tfr|
|𝔘|&Ufr|
|𝔙|&Vfr|
|𝔚|&Wfr|
|𝔛|&Xfr|
|𝔜|&Yfr|
|𝔞|&afr|
|𝔟|&bfr|
|𝔠|&cfr|
|𝔡|&dfr|
|𝔢|&efr|
|𝔣|&ffr|
|𝔤|&gfr|
|𝔥|&hfr|
|𝔦|&ifr|
|𝔧|&jfr|
|𝔨|&kfr|
|𝔩|&lfr|
|𝔪|&mfr|
|𝔫|&nfr|
|𝔬|&ofr|
|𝔭|&pfr|
|𝔮|&qfr|
|𝔯|&rfr|
|𝔰|&sfr|
|𝔱|&tfr|
|𝔲|&ufr|
|𝔳|&vfr|
|𝔴|&wfr|
|𝔵|&xfr|
|𝔶|&yfr|
|𝔷|&zfr|
|𝔸|&Aopf|
|𝔹|&Bopf|
|𝔻|&Dopf|
|𝔼|&Eopf|
|𝔽|&Fopf|
|𝔾|&Gopf|
|𝕀|&Iopf|
|𝕁|&Jopf|
|𝕂|&Kopf|
|𝕃|&Lopf|
|𝕄|&Mopf|
|𝕆|&Oopf|
|𝕊|&Sopf|
|𝕋|&Topf|
|𝕌|&Uopf|
|𝕍|&Vopf|
|𝕎|&Wopf|
|𝕏|&Xopf|
|𝕐|&Yopf|
|𝕒|&aopf|
|𝕓|&bopf|
|𝕔|&copf|
|𝕕|&dopf|
|𝕖|&eopf|
|𝕗|&fopf|
|𝕘|&gopf|
|𝕙|&hopf|
|𝕚|&iopf|
|𝕛|&jopf|
|𝕜|&kopf|
|𝕝|&lopf|
|𝕞|&mopf|
|𝕟|&nopf|
|𝕠|&oopf|
|𝕡|&popf|
|𝕢|&qopf|
|𝕣|&ropf|
|𝕤|&sopf|
|𝕥|&topf|
|𝕦|&uopf|
|𝕧|&vopf|
|𝕨|&wopf|
|𝕩|&xopf|
|𝕪|&yopf|
|𝕫|&zopf|

# 3. Markdown Extenstion(확장)

## 3.1 [Badge Icon](https://shields.io/)
## 3.1.1 Usage
LABEL, MESSAGE, COLOR에 적절한 파라미터를 입력해주면 뱃지를 만들 수 있다.

```
https://img.shields.io/badge/<LABEL>-<MESSAGE>-<COLOR>
```

예를 들면
```
https://img.shields.io/badge/github-GIVEME--STAR-yello
```

![](https://img.shields.io/badge/github-star-yellow)

###### LABEL, MESSAGE에서 밑줄, 대시, 공백을 쓰고 싶으면 이렇게 __, --, _ 를 쓰면 된다.

## 3.1.2 Style

```
https://img.shields.io/badge/style-plastic-red?style=plastic
https://img.shields.io/badge/style-flat-red?style=flat
https://img.shields.io/badge/style-square-red?style=flat-square
https://img.shields.io/badge/style-forthebage-red?style=for-the-badge
https://img.shields.io/badge/style-social-red?style=social
```

![](https://img.shields.io/badge/style-plastic-yellow?style=plastic)
![](https://img.shields.io/badge/style-flat-yellow?style=flat)
![](https://img.shields.io/badge/style-square-yellow?style=flat-square)
![](https://img.shields.io/badge/style-forthebage-yellow?style=for-the-badge)
![](https://img.shields.io/badge/style-social-yellow?style=social)

## 3.1.3 Logo

```
https://img.shields.io/badge/logo-test-blue?logo=facebook
https://img.shields.io/badge/logo-test-blue?logo=facebook&logoColor=white
https://img.shields.io/badge/logo-test-blue?logo=facebook&logoColor=white&logoWidth=40
```

![](https://img.shields.io/badge/logo-test-blue?logo=facebook)
![](https://img.shields.io/badge/logo-test-blue?logo=facebook&logoColor=white)
![](https://img.shields.io/badge/logo-test-blue?logo=facebook&logoColor=white&logoWidth=40)

Logo의 경우엔  [**이곳**](https://simpleicons.org/ "https://simpleicons.org/")에서의 Logo 종류를 전부 사용 가능하다고 한다.

그럼 내가 사랑하는 Airbnb도 해볼까?

![](https://img.shields.io/badge/logo-Airbnb-pink?logo=airbnb&logoColor=white)

하지만 일반적으로 자기가 사용한 Langague Icon를 사용하니.

![](https://img.shields.io/badge/logo-Node.js-green?logo=Node.js&logoColor=white)

## 3.1.4 Your GitHub Repository Stack

사용법은 다음과 같다.

```
https://img.shields.io/github/languages/count/{GithubName}/{ProjectName}
```

```
GitHub 사용 언어 수
https://img.shields.io/github/languages/count/Mineru98/AutoBench
GitHub 최다빈도 언어
https://img.shields.io/github/languages/top/Mineru98/AutoBench
GitHub 코드 용량
https://img.shields.io/github/languages/Mineru98/AutoBench
GitHub 용량
https://img.shields.io/github/repo-size/Mineru98/AutoBench
GitHub 오픈 이슈 개수
https://img.shields.io/github/issues/Mineru98/AutoBench
GitHub 닫힌 이슈 개수
https://img.shields.io/github/issues-closed/Mineru98/AutoBench
GitHub 주간 커밋 수
https://img.shields.io/github/commit-activity/w/Mineru98/AutoBench
GitHub 라스트 커밋 날짜
https://img.shields.io/github/last-commit/Mineru98/AutoBench
```

![](https://img.shields.io/github/languages/count/Mineru98/AutoBench)
![](https://img.shields.io/github/languages/top/Mineru98/AutoBench)
![](https://img.shields.io/github/languages/code-size/Mineru98/AutoBench)
![](https://img.shields.io/github/repo-size/Mineru98/AutoBench)
![](https://img.shields.io/github/issues/Mineru98/AutoBench)
![](https://img.shields.io/github/issues-closed/Mineru98/AutoBench)
![](https://img.shields.io/github/commit-activity/w/Mineru98/AutoBench)
![](https://img.shields.io/github/last-commit/Mineru98/AutoBench)

## 3.2. Commit & Description & Profile & ReadME.md (Emoji with GitHub)

Github에서 커밋을 할 때 다음과 같이 써주면
```
git commit -m ":seedling: Write about setting github markdown icon"
```

이런식으로 commit list에 결과가 나온다.

> :seedling: __Write about setting github markdown icon__

>__mineru98__ committied a minute ago :heavy_check_mark:

Description, ReadME, Profile 모두 마찬가지로 작동한다.

#### People

| :bowtie: `:bowtie:` | :smile: `:smile:` | :laughing: `:laughing:` |
|---|---|---|
| :blush: `:blush:` | :smiley: `:smiley:` | :relaxed: `:relaxed:` |
| :smirk: `:smirk:` | :heart_eyes: `:heart_eyes:` | :kissing_heart: `:kissing_heart:` |
| :kissing_closed_eyes: `:kissing_closed_eyes:` | :flushed: `:flushed:` | :relieved: `:relieved:` |
| :satisfied: `:satisfied:` | :grin: `:grin:` | :wink: `:wink:` |
| :stuck_out_tongue_winking_eye: `:stuck_out_tongue_winking_eye:` | :stuck_out_tongue_closed_eyes: `:stuck_out_tongue_closed_eyes:` | :grinning: `:grinning:` |
| :kissing: `:kissing:` | :kissing_smiling_eyes: `:kissing_smiling_eyes:` | :stuck_out_tongue: `:stuck_out_tongue:` |
| :sleeping: `:sleeping:` | :worried: `:worried:` | :frowning: `:frowning:` |
| :anguished: `:anguished:` | :open_mouth: `:open_mouth:` | :grimacing: `:grimacing:` |
| :confused: `:confused:` | :hushed: `:hushed:` | :expressionless: `:expressionless:` |
| :unamused: `:unamused:` | :sweat_smile: `:sweat_smile:` | :sweat: `:sweat:` |
| :disappointed_relieved: `:disappointed_relieved:` | :weary: `:weary:` | :pensive: `:pensive:` |
| :disappointed: `:disappointed:` | :confounded: `:confounded:` | :fearful: `:fearful:` |
| :cold_sweat: `:cold_sweat:` | :persevere: `:persevere:` | :cry: `:cry:` |
| :sob: `:sob:` | :joy: `:joy:` | :astonished: `:astonished:` |
| :scream: `:scream:` | :neckbeard: `:neckbeard:` | :tired_face: `:tired_face:` |
| :angry: `:angry:` | :rage: `:rage:` | :triumph: `:triumph:` |
| :sleepy: `:sleepy:` | :yum: `:yum:` | :mask: `:mask:` |
| :sunglasses: `:sunglasses:` | :dizzy_face: `:dizzy_face:` | :imp: `:imp:` |
| :smiling_imp: `:smiling_imp:` | :neutral_face: `:neutral_face:` | :no_mouth: `:no_mouth:` |
| :innocent: `:innocent:` | :alien: `:alien:` | :yellow_heart: `:yellow_heart:` |
| :blue_heart: `:blue_heart:` | :purple_heart: `:purple_heart:` | :heart: `:heart:` |
| :green_heart: `:green_heart:` | :broken_heart: `:broken_heart:` | :heartbeat: `:heartbeat:` |
| :heartpulse: `:heartpulse:` | :two_hearts: `:two_hearts:` | :revolving_hearts: `:revolving_hearts:` |
| :cupid: `:cupid:` | :sparkling_heart: `:sparkling_heart:` | :sparkles: `:sparkles:` |
| :star: `:star:` | :star2: `:star2:` | :dizzy: `:dizzy:` |
| :boom: `:boom:` | :collision: `:collision:` | :anger: `:anger:` |
| :exclamation: `:exclamation:` | :question: `:question:` | :grey_exclamation: `:grey_exclamation:` |
| :grey_question: `:grey_question:` | :zzz: `:zzz:` | :dash: `:dash:` |
| :sweat_drops: `:sweat_drops:` | :notes: `:notes:` | :musical_note: `:musical_note:` |
| :fire: `:fire:` | :hankey: `:hankey:` | :poop: `:poop:` |
| :shit: `:shit:` | :+1: `:+1:` | :thumbsup: `:thumbsup:` |
| :-1: `:-1:` | :thumbsdown: `:thumbsdown:` | :ok_hand: `:ok_hand:` |
| :punch: `:punch:` | :facepunch: `:facepunch:` | :fist: `:fist:` |
| :v: `:v:` | :wave: `:wave:` | :hand: `:hand:` |
| :raised_hand: `:raised_hand:` | :open_hands: `:open_hands:` | :point_up: `:point_up:` |
| :point_down: `:point_down:` | :point_left: `:point_left:` | :point_right: `:point_right:` |
| :raised_hands: `:raised_hands:` | :pray: `:pray:` | :point_up_2: `:point_up_2:` |
| :clap: `:clap:` | :muscle: `:muscle:` | :metal: `:metal:` |
| :fu: `:fu:` | :walking: `:walking:` | :runner: `:runner:` |
| :running: `:running:` | :couple: `:couple:` | :family: `:family:` |
| :two_men_holding_hands: `:two_men_holding_hands:` | :two_women_holding_hands: `:two_women_holding_hands:` | :dancer: `:dancer:` |
| :dancers: `:dancers:` | :ok_woman: `:ok_woman:` | :no_good: `:no_good:` |
| :information_desk_person: `:information_desk_person:` | :raising_hand: `:raising_hand:` | :bride_with_veil: `:bride_with_veil:` |
| :person_with_pouting_face: `:person_with_pouting_face:` | :person_frowning: `:person_frowning:` | :bow: `:bow:` |
| :couplekiss: `:couplekiss:` | :couple_with_heart: `:couple_with_heart:` | :massage: `:massage:` |
| :haircut: `:haircut:` | :nail_care: `:nail_care:` | :boy: `:boy:` |
| :girl: `:girl:` | :woman: `:woman:` | :man: `:man:` |
| :baby: `:baby:` | :older_woman: `:older_woman:` | :older_man: `:older_man:` |
| :person_with_blond_hair: `:person_with_blond_hair:` | :man_with_gua_pi_mao: `:man_with_gua_pi_mao:` | :man_with_turban: `:man_with_turban:` |
| :construction_worker: `:construction_worker:` | :cop: `:cop:` | :angel: `:angel:` |
| :princess: `:princess:` | :smiley_cat: `:smiley_cat:` | :smile_cat: `:smile_cat:` |
| :heart_eyes_cat: `:heart_eyes_cat:` | :kissing_cat: `:kissing_cat:` | :smirk_cat: `:smirk_cat:` |
| :scream_cat: `:scream_cat:` | :crying_cat_face: `:crying_cat_face:` | :joy_cat: `:joy_cat:` |
| :pouting_cat: `:pouting_cat:` | :japanese_ogre: `:japanese_ogre:` | :japanese_goblin: `:japanese_goblin:` |
| :see_no_evil: `:see_no_evil:` | :hear_no_evil: `:hear_no_evil:` | :speak_no_evil: `:speak_no_evil:` |
| :guardsman: `:guardsman:` | :skull: `:skull:` | :feet: `:feet:` |
| :lips: `:lips:` | :kiss: `:kiss:` | :droplet: `:droplet:` |
| :ear: `:ear:` | :eyes: `:eyes:` | :nose: `:nose:` |
| :tongue: `:tongue:` | :love_letter: `:love_letter:` | :bust_in_silhouette: `:bust_in_silhouette:` |
| :busts_in_silhouette: `:busts_in_silhouette:` | :speech_balloon: `:speech_balloon:` | :thought_balloon: `:thought_balloon:` |
| :feelsgood: `:feelsgood:` | :finnadie: `:finnadie:` | :goberserk: `:goberserk:` |
| :godmode: `:godmode:` | :hurtrealbad: `:hurtrealbad:` | :rage1: `:rage1:` |
| :rage2: `:rage2:` | :rage3: `:rage3:` | :rage4: `:rage4:` |
| :suspect: `:suspect:` | :trollface: `:trollface:` | 

#### Nature

| :sunny: `:sunny:` | :umbrella: `:umbrella:` | :cloud: `:cloud:` |
|---|---|---|
| :snowflake: `:snowflake:` | :snowman: `:snowman:` | :zap: `:zap:` |
| :cyclone: `:cyclone:` | :foggy: `:foggy:` | :ocean: `:ocean:` |
| :cat: `:cat:` | :dog: `:dog:` | :mouse: `:mouse:` |
| :hamster: `:hamster:` | :rabbit: `:rabbit:` | :wolf: `:wolf:` |
| :frog: `:frog:` | :tiger: `:tiger:` | :koala: `:koala:` |
| :bear: `:bear:` | :pig: `:pig:` | :pig_nose: `:pig_nose:` |
| :cow: `:cow:` | :boar: `:boar:` | :monkey_face: `:monkey_face:` |
| :monkey: `:monkey:` | :horse: `:horse:` | :racehorse: `:racehorse:` |
| :camel: `:camel:` | :sheep: `:sheep:` | :elephant: `:elephant:` |
| :panda_face: `:panda_face:` | :snake: `:snake:` | :bird: `:bird:` |
| :baby_chick: `:baby_chick:` | :hatched_chick: `:hatched_chick:` | :hatching_chick: `:hatching_chick:` |
| :chicken: `:chicken:` | :penguin: `:penguin:` | :turtle: `:turtle:` |
| :bug: `:bug:` | :honeybee: `:honeybee:` | :ant: `:ant:` |
| :beetle: `:beetle:` | :snail: `:snail:` | :octopus: `:octopus:` |
| :tropical_fish: `:tropical_fish:` | :fish: `:fish:` | :whale: `:whale:` |
| :whale2: `:whale2:` | :dolphin: `:dolphin:` | :cow2: `:cow2:` |
| :ram: `:ram:` | :rat: `:rat:` | :water_buffalo: `:water_buffalo:` |
| :tiger2: `:tiger2:` | :rabbit2: `:rabbit2:` | :dragon: `:dragon:` |
| :goat: `:goat:` | :rooster: `:rooster:` | :dog2: `:dog2:` |
| :pig2: `:pig2:` | :mouse2: `:mouse2:` | :ox: `:ox:` |
| :dragon_face: `:dragon_face:` | :blowfish: `:blowfish:` | :crocodile: `:crocodile:` |
| :dromedary_camel: `:dromedary_camel:` | :leopard: `:leopard:` | :cat2: `:cat2:` |
| :poodle: `:poodle:` | :paw_prints: `:paw_prints:` | :bouquet: `:bouquet:` |
| :cherry_blossom: `:cherry_blossom:` | :tulip: `:tulip:` | :four_leaf_clover: `:four_leaf_clover:` |
| :rose: `:rose:` | :sunflower: `:sunflower:` | :hibiscus: `:hibiscus:` |
| :maple_leaf: `:maple_leaf:` | :leaves: `:leaves:` | :fallen_leaf: `:fallen_leaf:` |
| :herb: `:herb:` | :mushroom: `:mushroom:` | :cactus: `:cactus:` |
| :palm_tree: `:palm_tree:` | :evergreen_tree: `:evergreen_tree:` | :deciduous_tree: `:deciduous_tree:` |
| :chestnut: `:chestnut:` | :seedling: `:seedling:` | :blossom: `:blossom:` |
| :ear_of_rice: `:ear_of_rice:` | :shell: `:shell:` | :globe_with_meridians: `:globe_with_meridians:` |
| :sun_with_face: `:sun_with_face:` | :full_moon_with_face: `:full_moon_with_face:` | :new_moon_with_face: `:new_moon_with_face:` |
| :new_moon: `:new_moon:` | :waxing_crescent_moon: `:waxing_crescent_moon:` | :first_quarter_moon: `:first_quarter_moon:` |
| :waxing_gibbous_moon: `:waxing_gibbous_moon:` | :full_moon: `:full_moon:` | :waning_gibbous_moon: `:waning_gibbous_moon:` |
| :last_quarter_moon: `:last_quarter_moon:` | :waning_crescent_moon: `:waning_crescent_moon:` | :last_quarter_moon_with_face: `:last_quarter_moon_with_face:` |
| :first_quarter_moon_with_face: `:first_quarter_moon_with_face:` | :moon: `:moon:` | :earth_africa: `:earth_africa:` |
| :earth_americas: `:earth_americas:` | :earth_asia: `:earth_asia:` | :volcano: `:volcano:` |
| :milky_way: `:milky_way:` | :partly_sunny: `:partly_sunny:` | :octocat: `:octocat:` |
| :squirrel: `:squirrel:` |

#### Objects

| :bamboo: `:bamboo:` | :gift_heart: `:gift_heart:` | :dolls: `:dolls:` |
|---|---|---|
| :school_satchel: `:school_satchel:` | :mortar_board: `:mortar_board:` | :flags: `:flags:` |
| :fireworks: `:fireworks:` | :sparkler: `:sparkler:` | :wind_chime: `:wind_chime:` |
| :rice_scene: `:rice_scene:` | :jack_o_lantern: `:jack_o_lantern:` | :ghost: `:ghost:` |
| :santa: `:santa:` | :christmas_tree: `:christmas_tree:` | :gift: `:gift:` |
| :bell: `:bell:` | :no_bell: `:no_bell:` | :tanabata_tree: `:tanabata_tree:` |
| :tada: `:tada:` | :confetti_ball: `:confetti_ball:` | :balloon: `:balloon:` |
| :crystal_ball: `:crystal_ball:` | :cd: `:cd:` | :dvd: `:dvd:` |
| :floppy_disk: `:floppy_disk:` | :camera: `:camera:` | :video_camera: `:video_camera:` |
| :movie_camera: `:movie_camera:` | :computer: `:computer:` | :tv: `:tv:` |
| :iphone: `:iphone:` | :phone: `:phone:` | :telephone: `:telephone:` |
| :telephone_receiver: `:telephone_receiver:` | :pager: `:pager:` | :fax: `:fax:` |
| :minidisc: `:minidisc:` | :vhs: `:vhs:` | :sound: `:sound:` |
| :speaker: `:speaker:` | :mute: `:mute:` | :loudspeaker: `:loudspeaker:` |
| :mega: `:mega:` | :hourglass: `:hourglass:` | :hourglass_flowing_sand: `:hourglass_flowing_sand:` |
| :alarm_clock: `:alarm_clock:` | :watch: `:watch:` | :radio: `:radio:` |
| :satellite: `:satellite:` | :loop: `:loop:` | :mag: `:mag:` |
| :mag_right: `:mag_right:` | :unlock: `:unlock:` | :lock: `:lock:` |
| :lock_with_ink_pen: `:lock_with_ink_pen:` | :closed_lock_with_key: `:closed_lock_with_key:` | :key: `:key:` |
| :bulb: `:bulb:` | :flashlight: `:flashlight:` | :high_brightness: `:high_brightness:` |
| :low_brightness: `:low_brightness:` | :electric_plug: `:electric_plug:` | :battery: `:battery:` |
| :calling: `:calling:` | :email: `:email:` | :mailbox: `:mailbox:` |
| :postbox: `:postbox:` | :bath: `:bath:` | :bathtub: `:bathtub:` |
| :shower: `:shower:` | :toilet: `:toilet:` | :wrench: `:wrench:` |
| :nut_and_bolt: `:nut_and_bolt:` | :hammer: `:hammer:` | :seat: `:seat:` |
| :moneybag: `:moneybag:` | :yen: `:yen:` | :dollar: `:dollar:` |
| :pound: `:pound:` | :euro: `:euro:` | :credit_card: `:credit_card:` |
| :money_with_wings: `:money_with_wings:` | :e-mail: `:e-mail:` | :inbox_tray: `:inbox_tray:` |
| :outbox_tray: `:outbox_tray:` | :envelope: `:envelope:` | :incoming_envelope: `:incoming_envelope:` |
| :postal_horn: `:postal_horn:` | :mailbox_closed: `:mailbox_closed:` | :mailbox_with_mail: `:mailbox_with_mail:` |
| :mailbox_with_no_mail: `:mailbox_with_no_mail:` | :door: `:door:` | :smoking: `:smoking:` |
| :bomb: `:bomb:` | :gun: `:gun:` | :hocho: `:hocho:` |
| :pill: `:pill:` | :syringe: `:syringe:` | :page_facing_up: `:page_facing_up:` |
| :page_with_curl: `:page_with_curl:` | :bookmark_tabs: `:bookmark_tabs:` | :bar_chart: `:bar_chart:` |
| :chart_with_upwards_trend: `:chart_with_upwards_trend:` | :chart_with_downwards_trend: `:chart_with_downwards_trend:` | :scroll: `:scroll:` |
| :clipboard: `:clipboard:` | :calendar: `:calendar:` | :date: `:date:` |
| :card_index: `:card_index:` | :file_folder: `:file_folder:` | :open_file_folder: `:open_file_folder:` |
| :scissors: `:scissors:` | :pushpin: `:pushpin:` | :paperclip: `:paperclip:` |
| :black_nib: `:black_nib:` | :pencil2: `:pencil2:` | :straight_ruler: `:straight_ruler:` |
| :triangular_ruler: `:triangular_ruler:` | :closed_book: `:closed_book:` | :green_book: `:green_book:` |
| :blue_book: `:blue_book:` | :orange_book: `:orange_book:` | :notebook: `:notebook:` |
| :notebook_with_decorative_cover: `:notebook_with_decorative_cover:` | :ledger: `:ledger:` | :books: `:books:` |
| :bookmark: `:bookmark:` | :name_badge: `:name_badge:` | :microscope: `:microscope:` |
| :telescope: `:telescope:` | :newspaper: `:newspaper:` | :football: `:football:` |
| :basketball: `:basketball:` | :soccer: `:soccer:` | :baseball: `:baseball:` |
| :tennis: `:tennis:` | :8ball: `:8ball:` | :rugby_football: `:rugby_football:` |
| :bowling: `:bowling:` | :golf: `:golf:` | :mountain_bicyclist: `:mountain_bicyclist:` |
| :bicyclist: `:bicyclist:` | :horse_racing: `:horse_racing:` | :snowboarder: `:snowboarder:` |
| :swimmer: `:swimmer:` | :surfer: `:surfer:` | :ski: `:ski:` |
| :spades: `:spades:` | :hearts: `:hearts:` | :clubs: `:clubs:` |
| :diamonds: `:diamonds:` | :gem: `:gem:` | :ring: `:ring:` |
| :trophy: `:trophy:` | :musical_score: `:musical_score:` | :musical_keyboard: `:musical_keyboard:` |
| :violin: `:violin:` | :space_invader: `:space_invader:` | :video_game: `:video_game:` |
| :black_joker: `:black_joker:` | :flower_playing_cards: `:flower_playing_cards:` | :game_die: `:game_die:` |
| :dart: `:dart:` | :mahjong: `:mahjong:` | :clapper: `:clapper:` |
| :memo: `:memo:` | :pencil: `:pencil:` | :book: `:book:` |
| :art: `:art:` | :microphone: `:microphone:` | :headphones: `:headphones:` |
| :trumpet: `:trumpet:` | :saxophone: `:saxophone:` | :guitar: `:guitar:` |
| :shoe: `:shoe:` | :sandal: `:sandal:` | :high_heel: `:high_heel:` |
| :lipstick: `:lipstick:` | :boot: `:boot:` | :shirt: `:shirt:` |
| :tshirt: `:tshirt:` | :necktie: `:necktie:` | :womans_clothes: `:womans_clothes:` |
| :dress: `:dress:` | :running_shirt_with_sash: `:running_shirt_with_sash:` | :jeans: `:jeans:` |
| :kimono: `:kimono:` | :bikini: `:bikini:` | :ribbon: `:ribbon:` |
| :tophat: `:tophat:` | :crown: `:crown:` | :womans_hat: `:womans_hat:` |
| :mans_shoe: `:mans_shoe:` | :closed_umbrella: `:closed_umbrella:` | :briefcase: `:briefcase:` |
| :handbag: `:handbag:` | :pouch: `:pouch:` | :purse: `:purse:` |
| :eyeglasses: `:eyeglasses:` | :fishing_pole_and_fish: `:fishing_pole_and_fish:` | :coffee: `:coffee:` |
| :tea: `:tea:` | :sake: `:sake:` | :baby_bottle: `:baby_bottle:` |
| :beer: `:beer:` | :beers: `:beers:` | :cocktail: `:cocktail:` |
| :tropical_drink: `:tropical_drink:` | :wine_glass: `:wine_glass:` | :fork_and_knife: `:fork_and_knife:` |
| :pizza: `:pizza:` | :hamburger: `:hamburger:` | :fries: `:fries:` |
| :poultry_leg: `:poultry_leg:` | :meat_on_bone: `:meat_on_bone:` | :spaghetti: `:spaghetti:` |
| :curry: `:curry:` | :fried_shrimp: `:fried_shrimp:` | :bento: `:bento:` |
| :sushi: `:sushi:` | :fish_cake: `:fish_cake:` | :rice_ball: `:rice_ball:` |
| :rice_cracker: `:rice_cracker:` | :rice: `:rice:` | :ramen: `:ramen:` |
| :stew: `:stew:` | :oden: `:oden:` | :dango: `:dango:` |
| :egg: `:egg:` | :bread: `:bread:` | :doughnut: `:doughnut:` |
| :custard: `:custard:` | :icecream: `:icecream:` | :ice_cream: `:ice_cream:` |
| :shaved_ice: `:shaved_ice:` | :birthday: `:birthday:` | :cake: `:cake:` |
| :cookie: `:cookie:` | :chocolate_bar: `:chocolate_bar:` | :candy: `:candy:` |
| :lollipop: `:lollipop:` | :honey_pot: `:honey_pot:` | :apple: `:apple:` |
| :green_apple: `:green_apple:` | :tangerine: `:tangerine:` | :lemon: `:lemon:` |
| :cherries: `:cherries:` | :grapes: `:grapes:` | :watermelon: `:watermelon:` |
| :strawberry: `:strawberry:` | :peach: `:peach:` | :melon: `:melon:` |
| :banana: `:banana:` | :pear: `:pear:` | :pineapple: `:pineapple:` |
| :sweet_potato: `:sweet_potato:` | :eggplant: `:eggplant:` | :tomato: `:tomato:` |
| :corn: `:corn:` |

#### Places

| :house: `:house:` | :house_with_garden: `:house_with_garden:` | :school: `:school:` |
|---|---|---|
| :office: `:office:` | :post_office: `:post_office:` | :hospital: `:hospital:` |
| :bank: `:bank:` | :convenience_store: `:convenience_store:` | :love_hotel: `:love_hotel:` |
| :hotel: `:hotel:` | :wedding: `:wedding:` | :church: `:church:` |
| :department_store: `:department_store:` | :european_post_office: `:european_post_office:` | :city_sunrise: `:city_sunrise:` |
| :city_sunset: `:city_sunset:` | :japanese_castle: `:japanese_castle:` | :european_castle: `:european_castle:` |
| :tent: `:tent:` | :factory: `:factory:` | :tokyo_tower: `:tokyo_tower:` |
| :japan: `:japan:` | :mount_fuji: `:mount_fuji:` | :sunrise_over_mountains: `:sunrise_over_mountains:` |
| :sunrise: `:sunrise:` | :stars: `:stars:` | :statue_of_liberty: `:statue_of_liberty:` |
| :bridge_at_night: `:bridge_at_night:` | :carousel_horse: `:carousel_horse:` | :rainbow: `:rainbow:` |
| :ferris_wheel: `:ferris_wheel:` | :fountain: `:fountain:` | :roller_coaster: `:roller_coaster:` |
| :ship: `:ship:` | :speedboat: `:speedboat:` | :boat: `:boat:` |
| :sailboat: `:sailboat:` | :rowboat: `:rowboat:` | :anchor: `:anchor:` |
| :rocket: `:rocket:` | :airplane: `:airplane:` | :helicopter: `:helicopter:` |
| :steam_locomotive: `:steam_locomotive:` | :tram: `:tram:` | :mountain_railway: `:mountain_railway:` |
| :bike: `:bike:` | :aerial_tramway: `:aerial_tramway:` | :suspension_railway: `:suspension_railway:` |
| :mountain_cableway: `:mountain_cableway:` | :tractor: `:tractor:` | :blue_car: `:blue_car:` |
| :oncoming_automobile: `:oncoming_automobile:` | :car: `:car:` | :red_car: `:red_car:` |
| :taxi: `:taxi:` | :oncoming_taxi: `:oncoming_taxi:` | :articulated_lorry: `:articulated_lorry:` |
| :bus: `:bus:` | :oncoming_bus: `:oncoming_bus:` | :rotating_light: `:rotating_light:` |
| :police_car: `:police_car:` | :oncoming_police_car: `:oncoming_police_car:` | :fire_engine: `:fire_engine:` |
| :ambulance: `:ambulance:` | :minibus: `:minibus:` | :truck: `:truck:` |
| :train: `:train:` | :station: `:station:` | :train2: `:train2:` |
| :bullettrain_front: `:bullettrain_front:` | :bullettrain_side: `:bullettrain_side:` | :light_rail: `:light_rail:` |
| :monorail: `:monorail:` | :railway_car: `:railway_car:` | :trolleybus: `:trolleybus:` |
| :ticket: `:ticket:` | :fuelpump: `:fuelpump:` | :vertical_traffic_light: `:vertical_traffic_light:` |
| :traffic_light: `:traffic_light:` | :warning: `:warning:` | :construction: `:construction:` |
| :beginner: `:beginner:` | :atm: `:atm:` | :slot_machine: `:slot_machine:` |
| :busstop: `:busstop:` | :barber: `:barber:` | :hotsprings: `:hotsprings:` |
| :checkered_flag: `:checkered_flag:` | :crossed_flags: `:crossed_flags:` | :izakaya_lantern: `:izakaya_lantern:` |
| :moyai: `:moyai:` | :circus_tent: `:circus_tent:` | :performing_arts: `:performing_arts:` |
| :round_pushpin: `:round_pushpin:` | :triangular_flag_on_post: `:triangular_flag_on_post:` | :jp: `:jp:` |
| :kr: `:kr:` | :cn: `:cn:` | :us: `:us:` |
| :fr: `:fr:` | :es: `:es:` | :it: `:it:` |
| :ru: `:ru:` | :gb: `:gb:` | :uk: `:uk:` |
| :de: `:de:` |

#### Symbols

| :one: `:one:` | :two: `:two:` | :three: `:three:` |
|---|---|---|
| :four: `:four:` | :five: `:five:` | :six: `:six:` |
| :seven: `:seven:` | :eight: `:eight:` | :nine: `:nine:` |
| :keycap_ten: `:keycap_ten:` | :1234: `:1234:` | :zero: `:zero:` |
| :hash: `:hash:` | :symbols: `:symbols:` | :arrow_backward: `:arrow_backward:` |
| :arrow_down: `:arrow_down:` | :arrow_forward: `:arrow_forward:` | :arrow_left: `:arrow_left:` |
| :capital_abcd: `:capital_abcd:` | :abcd: `:abcd:` | :abc: `:abc:` |
| :arrow_lower_left: `:arrow_lower_left:` | :arrow_lower_right: `:arrow_lower_right:` | :arrow_right: `:arrow_right:` |
| :arrow_up: `:arrow_up:` | :arrow_upper_left: `:arrow_upper_left:` | :arrow_upper_right: `:arrow_upper_right:` |
| :arrow_double_down: `:arrow_double_down:` | :arrow_double_up: `:arrow_double_up:` | :arrow_down_small: `:arrow_down_small:` |
| :arrow_heading_down: `:arrow_heading_down:` | :arrow_heading_up: `:arrow_heading_up:` | :leftwards_arrow_with_hook: `:leftwards_arrow_with_hook:` |
| :arrow_right_hook: `:arrow_right_hook:` | :left_right_arrow: `:left_right_arrow:` | :arrow_up_down: `:arrow_up_down:` |
| :arrow_up_small: `:arrow_up_small:` | :arrows_clockwise: `:arrows_clockwise:` | :arrows_counterclockwise: `:arrows_counterclockwise:` |
| :rewind: `:rewind:` | :fast_forward: `:fast_forward:` | :information_source: `:information_source:` |
| :ok: `:ok:` | :twisted_rightwards_arrows: `:twisted_rightwards_arrows:` | :repeat: `:repeat:` |
| :repeat_one: `:repeat_one:` | :new: `:new:` | :top: `:top:` |
| :up: `:up:` | :cool: `:cool:` | :free: `:free:` |
| :ng: `:ng:` | :cinema: `:cinema:` | :koko: `:koko:` |
| :signal_strength: `:signal_strength:` | :u5272: `:u5272:` | :u5408: `:u5408:` |
| :u55b6: `:u55b6:` | :u6307: `:u6307:` | :u6708: `:u6708:` |
| :u6709: `:u6709:` | :u6e80: `:u6e80:` | :u7121: `:u7121:` |
| :u7533: `:u7533:` | :u7a7a: `:u7a7a:` | :u7981: `:u7981:` |
| :sa: `:sa:` | :restroom: `:restroom:` | :mens: `:mens:` |
| :womens: `:womens:` | :baby_symbol: `:baby_symbol:` | :no_smoking: `:no_smoking:` |
| :parking: `:parking:` | :wheelchair: `:wheelchair:` | :metro: `:metro:` |
| :baggage_claim: `:baggage_claim:` | :accept: `:accept:` | :wc: `:wc:` |
| :potable_water: `:potable_water:` | :put_litter_in_its_place: `:put_litter_in_its_place:` | :secret: `:secret:` |
| :congratulations: `:congratulations:` | :m: `:m:` | :passport_control: `:passport_control:` |
| :left_luggage: `:left_luggage:` | :customs: `:customs:` | :ideograph_advantage: `:ideograph_advantage:` |
| :cl: `:cl:` | :sos: `:sos:` | :id: `:id:` |
| :no_entry_sign: `:no_entry_sign:` | :underage: `:underage:` | :no_mobile_phones: `:no_mobile_phones:` |
| :do_not_litter: `:do_not_litter:` | :non-potable_water: `:non-potable_water:` | :no_bicycles: `:no_bicycles:` |
| :no_pedestrians: `:no_pedestrians:` | :children_crossing: `:children_crossing:` | :no_entry: `:no_entry:` |
| :eight_spoked_asterisk: `:eight_spoked_asterisk:` | :eight_pointed_black_star: `:eight_pointed_black_star:` | :heart_decoration: `:heart_decoration:` |
| :vs: `:vs:` | :vibration_mode: `:vibration_mode:` | :mobile_phone_off: `:mobile_phone_off:` |
| :chart: `:chart:` | :currency_exchange: `:currency_exchange:` | :aries: `:aries:` |
| :taurus: `:taurus:` | :gemini: `:gemini:` | :cancer: `:cancer:` |
| :leo: `:leo:` | :virgo: `:virgo:` | :libra: `:libra:` |
| :scorpius: `:scorpius:` | :sagittarius: `:sagittarius:` | :capricorn: `:capricorn:` |
| :aquarius: `:aquarius:` | :pisces: `:pisces:` | :ophiuchus: `:ophiuchus:` |
| :six_pointed_star: `:six_pointed_star:` | :negative_squared_cross_mark: `:negative_squared_cross_mark:` | :a: `:a:` |
| :b: `:b:` | :ab: `:ab:` | :o2: `:o2:` |
| :diamond_shape_with_a_dot_inside: `:diamond_shape_with_a_dot_inside:` | :recycle: `:recycle:` | :end: `:end:` |
| :on: `:on:` | :soon: `:soon:` | :clock1: `:clock1:` |
| :clock130: `:clock130:` | :clock10: `:clock10:` | :clock1030: `:clock1030:` |
| :clock11: `:clock11:` | :clock1130: `:clock1130:` | :clock12: `:clock12:` |
| :clock1230: `:clock1230:` | :clock2: `:clock2:` | :clock230: `:clock230:` |
| :clock3: `:clock3:` | :clock330: `:clock330:` | :clock4: `:clock4:` |
| :clock430: `:clock430:` | :clock5: `:clock5:` | :clock530: `:clock530:` |
| :clock6: `:clock6:` | :clock630: `:clock630:` | :clock7: `:clock7:` |
| :clock730: `:clock730:` | :clock8: `:clock8:` | :clock830: `:clock830:` |
| :clock9: `:clock9:` | :clock930: `:clock930:` | :heavy_dollar_sign: `:heavy_dollar_sign:` |
| :copyright: `:copyright:` | :registered: `:registered:` | :tm: `:tm:` |
| :x: `:x:` | :heavy_exclamation_mark: `:heavy_exclamation_mark:` | :bangbang: `:bangbang:` |
| :interrobang: `:interrobang:` | :o: `:o:` | :heavy_multiplication_x: `:heavy_multiplication_x:` |
| :heavy_plus_sign: `:heavy_plus_sign:` | :heavy_minus_sign: `:heavy_minus_sign:` | :heavy_division_sign: `:heavy_division_sign:` |
| :white_flower: `:white_flower:` | :100: `:100:` | :heavy_check_mark: `:heavy_check_mark:` |
| :ballot_box_with_check: `:ballot_box_with_check:` | :radio_button: `:radio_button:` | :link: `:link:` |
| :curly_loop: `:curly_loop:` | :wavy_dash: `:wavy_dash:` | :part_alternation_mark: `:part_alternation_mark:` |
| :trident: `:trident:` | :black_square: `:black_square:` | :white_square: `:white_square:` |
| :white_check_mark: `:white_check_mark:` | :black_square_button: `:black_square_button:` | :white_square_button: `:white_square_button:` |
| :black_circle: `:black_circle:` | :white_circle: `:white_circle:` | :red_circle: `:red_circle:` |
| :large_blue_circle: `:large_blue_circle:` | :large_blue_diamond: `:large_blue_diamond:` | :large_orange_diamond: `:large_orange_diamond:` |
| :small_blue_diamond: `:small_blue_diamond:` | :small_orange_diamond: `:small_orange_diamond:` | :small_red_triangle: `:small_red_triangle:` |
| :small_red_triangle_down: `:small_red_triangle_down:` | :shipit: `:shipit:` |


## ● 출처
* [John gruber 마크다운 번역본](http://nolboo.github.io/blog/2013/09/07/john-gruber-markdown/)
* [깃허브 취향의 마크다운 번역](http://nolboo.github.io/blog/2014/03/25/github-flavored-markdown/)
* [허니몬의 마크다운 작성법](http://www.slideshare.net/ihoneymon/ss-40575068)
* [Github Emoji 소스](https://gist.github.com/rxaviers/7360908)