# spring-boot-study


## 22/01/03
 - @SpringBootApplication은 해당 패키지에 사용된 어노테이션(컴포넌트)을 스캔하여 한데 모아준다. 
 그러므로 반드시 트리구조를 맞추어 사용해야한다.

 - pom.xml dependency에 spring-boot-starter-web 라이브러리를 업데이트 시켜야 내장 톰캣(was) 작동
 
 - pom.xml parent에 spring-boot-starter-parent 라이브러리를 선언하면 부모객체가 되어 오버라이딩된다.
 다만 자체제작된 설정이 있다면 그것을 parent에 설정 또는 dependencyManagement를 사용하면 되지만 오버라이딩이 안되며
 스프링부트를 사용하는 큰 장점이 없어지기에 parent 권장

 - properties 태그에 있는 spring 버전 변경 등의 설정은 위의 방법대로 오버라이딩하면 된다.

 - @ComponentScan은 컴포넌트(@Configuration @Repository @Service @Controller @RestController)로 등록된 객체들을 Bean으로 등록하라는 명령