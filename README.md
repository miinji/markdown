# MARKDOWN
마크다운 연습하기

##1.마크다운 이란?
마크다운(markdown)은 일반 텍스트 문서의 양식을 편집하는 문법

###1.2 마크다운의 특징
1.특수 기호와 문자를 이용한 매우 간단한 구조의 문법을 사용하여
웹에서도 보다 빠르게 컨텐츠를 작성하고 직관적으로 인식 가능

2.마크다운을 통해서 설치방법, 소스코드 설명, 이슈 등을 간단하게 기록하고
가독성을 높일 수 있다는 장점이 부각되면서 점점 여러  곳으로 퍼짐

3.지원한 플랫폼이 다양하고 다양한 형태로 변환이 가능 하다는 장점이 있으나
표준이 없기 때문에 도구에 따라 변환방식이나 생성물이 다르다.

##2.마크다운 문법
###2.1 헤더(Header)

-># 개수로 조절가능

```
#This is H1()
##This is H2()
->H6까지 생성 가능
```

적용 예)
#This is H1() 
##This is H2()

##2.2 BlockQuote
->'<' 마크를 이용하여 문단을 엮어준다.

```buildoutcfg
> This is a first blockqute.
>	> This is a second blockqute.
>	>	> This is a third blockqute.
```

> This is a first blockqute.
>	> This is a second blockqute.
>	>	> This is a third blockqute.

##2.3 목록
-> 문서에 순서를 뒤죽박죽 작성하더라도 내림차순으로 정렬된다.
```buildoutcfg
1. 첫번째
3. 세번째
2. 두번째
```
1. 첫번째
3. 세번째
2. 두번째

###2.4 코드
->4개의 공백 또는 하나의 탭으로 들여쓰기를 만나면 변환되기 시작하여 들여쓰지 않은 행을 만날때까지 변환이 계속 됨

->한줄 띄어쓰지 않으면 인식이 제대로 안되는 문제가 발생함

->*코드가 아닌 글에서 줄 바꿈을 하기 위해서는 3칸 이상 띄어쓰기 해야 함
```buildoutcfg
This is a normal paragraph:

    This is a code block.
    
end code block.
```
적용 예시)

This is a normal paragraph:

    This is a code block.
    
end code block.

###2.4.1 코드 블럭
```buildoutcfg
 <pre><code>{code}</code></pre> 이용
```

```buildoutcfg
<pre>
<code>
public class BootSpringBootApplication {
  public static void main(String[] args) {
    System.out.println("Hello, Honeymon");
  }

}
</code>
</pre>
```

<pre>
<code>
public class BootSpringBootApplication {
  public static void main(String[] args) {
    System.out.println("Hello, Honeymon");
  }

}
</code>
</pre>

```
<pre><code></code></pre> 대신 ``` ``` 이용 가능
```

###2.5 수평선
```buildoutcfg
* * *

***

*****

- - -

---------------------------------------
```
->모두 아래와 같은 수평선을 만든다.

* * *

###2.6 링크

```buildoutcfg
*참조링크

[link keyword][id]

[id]: URL "Optional Title here"

// code
Link: [Google][googlelink]

[googlelink]: https://google.com "Go google"
```

[link keyword][id]

[id]: URL "Optional Title here"

// code
Link: [Google][googlelink]

[googlelink]: https://google.com "Go google"

```
*외부링크

사용문법: [Title](link)
적용예: [Google](https://google.com, "google link")
```

사용문법: [Title](link)

적용예: [Google](https://google.com, "google link")

```
일반적인 URL 혹은 이메일주소인 경우 적절한 형식으로 링크를 형성한다.

* 외부링크: <http://example.com/>
* 이메일링크: <address@example.com>
```

###2.8 이미지

```buildoutcfg
![Alt text](/path/to/img.jpg)
![Alt text](/path/to/img.jpg "Optional title")
```
![Haedal](https://avatars3.githubusercontent.com/u/47355438?s=280&v=4)
![Haedal](https://avatars3.githubusercontent.com/u/47355438?s=280&v=4 "Haedal")

*사이즈 조절
```buildoutcfg
<img src="/path/to/img.jpg" width="450px" height="300px" title="px(픽셀) 크기 설정" alt="RubberDuck"></img><br/>
<img src="/path/to/img.jpg" width="40%" height="30%" title="px(픽셀) 크기 설정" alt="RubberDuck"></img>
```




#git 사용법

git clone-git add-git commit-git push 순으로 진행

1. 저장소 받아오기
 
개인 github repository를 만든 뒤 clone or download 버튼을 클릭해서 URL 주소를 복사

```buildoutcfg
project terminal에

git clone <복사한 URL 주소>
```

2. 저장소에 변경된 파일을 추가

```buildoutcfg
git add .
```

3. 변경 내용 확정 

git commit -m "이번 확정본에 대한 설명" 

```buildoutcfg
git commit -m "edit README.md"
```
```
$ git commit -m  "edit README.md"
[master 8dc75e7] edit README.md
 1 file changed, 9 insertions(+)
```
-> 변경한 파일이 HEAD에는 반영이 되었으나 원격 저장소에는 아직 반영이 되지 않음

4.  변경 내용 push 하기

변경한 내용을 원격 서버롤 올리자

```buildoutcfg
git push origin master
```
* master는 branch의 한 종류


```
$ git push origin master
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 374 bytes | 74.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0)

```

