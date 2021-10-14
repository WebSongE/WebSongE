# 웹 프로그래밍(풀스택)
> 수강 중
* 부스트코스 수강 이외에 추가로 do it! 클론 코딩 트위터 도서를 실습하고있습니다.<br>
*<a href="https://github.com/KimDahui42/nwitter">해당 repository로 이동</a>*
## 2021.09
<details>
<summary> DB 연결 웹 앱(2.2~2.12)</summary>
<div markdown="1">
	<ul>
		<li> [09.12.21] ~2.7 수강</li>
	</ul>
</div>
</details>
<details>
<summary> DB 연결 웹 앱(2.7~2.12)</summary>
<div markdown="1">
	<ul>
		<li>과제 B 시작 -> 자바스크립트 학습으로 변경했습니다(문법이 부족한 것 같아요) </li>
	</ul>
</div>
</details>
* ~do it! 클론코딩 완료~

## 2021.10
### 실행을 하지만 오류가 나면서 실행이 안 되는 경우

* 이클립스의 버그로, 수정되기 전의 데이터와 수정된 데이터가 섞여서 실행되기 때문입니다.

	* 이 경우 웹 어플리케이션을 깔끔히 초기화하고 실행하는 것이 좋을 수 있습니다.

	1. 기존 tomcat을 종료합니다.
	2. 혹시 바뀌지 않았다면 프로젝트를 선택하고, 우측버튼을 눌러서 Maven 메뉴 아래의 update project를 선택한 후 확인하세요.
	3. Servers view에서 기존 Tomcat Runtime을 삭제
	4. Project 메뉴의 Clean선택
	5. 프로젝트 익스플로러에서 Servers 삭제
	6. Run on Server로 실행(서버 포트 추가-8005)
### JDBCExam1 실행 오류
* mysql 버젼이 달라서 발생
	* mysql 8.0.26 dependency 코드
	```xml
	<dependency>
    	<groupId>mysql</groupId>
    	<artifactId>mysql-connector-java</artifactId>
    	<version>8.0.26</version>
	</dependency>
	```
	* RoleDao.java
	```java
	private static String dburl="jdbc:mysql://localhost:3306/connectdb?serverTimezone=Asia/Seoul&useSSL=false";
	Class.forName("com.mysql.cj.jdbc.Driver");
	
	```
### webAPI 실습 500 - java.lang.NoClassDefFoundError: com/fasterxml/jackson/databind/ObjectMapper
`.classpath` 파일 수정
````
<classpathentry kind="con" path="org.eclipse.m2e.MAVEN2_CLASSPATH_CONTAINER">
	<attributes>
		<attribute name="maven.pomderived" value="true"/>
		<attribute name="org.eclipse.jst.component.dependency" value="/WEB-INF/lib"/>
	</attributes>
</classpathentry>

```