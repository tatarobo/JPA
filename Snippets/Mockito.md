# Mockito

* github : https://github.com/mockito/mockito
* document : https://javadoc.io/static/org.mockito/mockito-core/3.6.28/org/mockito/Mockito.html

### @RunWith(MockitoJUnitRunner.class)
- MockitoAnnotations.initMocks() 를 호출할 필요가 없다.

### Mockito.verfiy()
* 해당 메소드의 수행 여부를 확인한다.
* Mockito.when()으로 설정하지 않아도 된다.
* @Mock 으로 테스트하려는 클래스를 지정하면 문제없이 mock 클래스 인스턴스가 만들어지고, 메소드 호출시에도 문제없이 수행된다.
	* 예전 기억에는 @Mock처리를 해주어도, when()으로 설정하지 않은 메소드는 호출 시점에 해당 메소드에서 NullPointerException이 발생했던것 같다.
	* when() 처리를 안해주면 해당 메소드는 0 또는 null 값을 리턴한다.
	* @Mock처리된 메소드를 호출하는 로직에서 반환된 값을 사용하지 않는다면 문제가 없지만, 반환값을 사용하는 경우에는 경우에 따라 NullPointerException 이 발생하게 된다.
<!--stackedit_data:
eyJoaXN0b3J5IjpbMTc2NDYzNDU3MiwtMTg0NTkzODE1N119
-->