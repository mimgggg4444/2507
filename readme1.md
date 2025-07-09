* **.NET 데스크톱 개발 워크로드:** Visual Studio에서 Windows용 데스크톱 애플리케이션(.NET Framework 또는 .NET Core) 개발에 필요한 도구와 라이브러리를 포함하는 설치 옵션입니다.
* **NuGet `System.Data.SQLite`:** SQLite 데이터베이스 접근을 위한 ADO.NET 호환 라이브러리를 손쉽게 추가·관리할 수 있게 해 주는 NuGet 패키지입니다.
* **Windows Form:** .NET 기반으로 데스크톱 GUI(그래픽 사용자 인터페이스)를 빠르게 설계하고 구현할 수 있는 프레임워크입니다.
* **ADO.NET CRUD:** ADO.NET을 이용해 데이터베이스에 대해 생성(Create), 조회(Read), 수정(Update), 삭제(Delete) 작업을 수행하는 기본 데이터 액세스 패턴입니다.
* **DeviceNet:** CAN 버스를 기반으로 CIP(Common Industrial Protocol)를 이용해 산업용 장비와 센서 간 데이터를 교환하는 필드버스 프로토콜입니다.
* **CAN:** 차량 및 산업용 네트워크에서 다수의 노드가 안정적으로 통신할 수 있도록 설계된 직렬 통신 버스 표준입니다.
* **CIP 프로토콜:** DeviceNet·EtherNet/IP 등 산업용 네트워크에서 애플리케이션 계층의 메시지 구조와 메소드 호출 방식을 정의하는 통신 규격입니다.
* **EtherCAT:** 이더넷을 기반으로 한 고속·실시간 산업용 이더넷 프로토콜로, 마스터가 슬레이브 장치의 메모리에 직접 접근하여 매우 낮은 지연 시간을 구현합니다.
* **Ethernet 기반 마스터/슬레이브 구조:** 마스터 장치가 네트워크를 통해 슬레이브 장치 제어 및 데이터 수집을 중앙집중식으로 수행하는 통신 구조입니다.
* **PDO (Process Data Object):** EtherCAT 등에서 실시간 제어 데이터를 주고받을 때 사용하는 고정 길이의 데이터 오브젝트로, 주기적 전송에 최적화되어 있습니다.
* **HMS Anybus:** CAN·DeviceNet·EtherCAT 등 다양한 산업용 네트워크 프로토콜을 PC나 PLC에 간편하게 연결하도록 해 주는 시뮬레이터 및 어댑터 제품군입니다.
* **DeviceNet/CAN 시뮬레이터:** 실제 하드웨어 없이 PC 상에서 CAN 또는 DeviceNet 통신을 가상으로 테스트·디버깅할 수 있게 해 주는 소프트웨어 도구입니다.
* **TwinCAT EtherCAT 시뮬레이션:** Beckhoff의 TwinCAT 소프트웨어에서 제공하는 가상 EtherCAT 네트워크 환경으로, 실제 장비 없이도 마스터/슬레이브 통신을 실습할 수 있는 기능입니다.


1. **프로그램 구조**

   * C# 애플리케이션은 `namespace` → `class` → `Main()` 메서드 순으로 구성되고, `using` 지시문으로 외부 네임스페이스를 참조합니다.

2. **데이터 타입**

   * 값형(`int`, `double`, `bool`, `struct` 등)과 참조형(`string`, `class`, `interface` 등)으로 나뉘며, 스택/힙 메모리 관리가 달라집니다.

3. **변수 및 상수**

   * `var`로 타입을 추론하거나 명시적 타입 선언이 가능하며, `const`와 `readonly`로 불변 값을 만듭니다.

4. **연산자**

   * 산술(+, –, \*, /, %), 비교(==, !=, <, >), 논리(&&, ||, !), 할당(=, += 등), 기타(null 병합 `??`, 조건부 `?:`) 연산자를 지원합니다.

5. **제어문**

   * `if`/`else`, `switch`(패턴 매칭 지원), `for`/`while`/`do-while`, `foreach`로 흐름 제어합니다.

6. **메서드**

   * `static` vs 인스턴스 메서드, 기본값 매개변수, `ref`/`out` 키워드, 가변 인자(`params`) 등을 사용할 수 있습니다.

7. **클래스와 객체지향**

   * 캡슐화(`public`/`private` 등), 상속(`: BaseClass`), 다형성(`virtual`/`override`), 추상 클래스(`abstract`), 인터페이스(`interface`)를 통해 설계합니다.

8. **프로퍼티 & 인덱서**

   * `get`/`set` 접근자, 자동 구현 프로퍼티(`{ get; set; }`), 읽기 전용/쓰기 전용 프로퍼티 설정이 가능합니다. 인덱서로 배열처럼 접근 가능.

9. **예외 처리**

   * `try`/`catch`/`finally`, 커스텀 예외 클래스(`: Exception`), `throw`로 예외 발생 및 재던지기.

10. **컬렉션**

    * 배열(`T[]`), `List<T>`, `Dictionary<TKey, TValue>`, `Queue<T>`, `Stack<T>` 등 제네릭 컬렉션과 비제네릭 `ArrayList` 등이 있습니다.

11. **제네릭**

    * 타입 안전성을 높이고 박싱/언박싱을 줄이기 위해 `List<T>`, `Dictionary<K,V>`, `Func<T>`, `Action<T>` 같은 제네릭을 사용합니다.

12. **델리게이트 & 이벤트**

    * 메서드 참조를 저장하는 델리게이트(`delegate`), 이를 활용한 이벤트 패턴(`event`)으로 느슨한 결합 구조 구현.

13. **LINQ**

    * 컬렉션에 SQL 같은 쿼리를 적용하는 `Enumerable`/`Queryable` 확장 메서드(`Where`, `Select`, `OrderBy` 등)를 사용해 간결한 데이터 처리.

14. **비동기 프로그래밍**

    * `async`/`await` 키워드로 비동기 메서드를 정의하고, `Task`/`Task<T>`로 백그라운드 작업을 처리합니다.

15. **네임스페이스 & 어셈블리**

    * 코드를 논리적으로 그룹화하는 `namespace`와, 컴파일된 출력물인 `.dll`/`.exe` 형태의 어셈블리를 관리합니다.

16. **메모리 관리 & GC**

    * .NET 런타임의 가비지 컬렉터가 더 이상 참조되지 않는 객체를 자동 회수하며, `IDisposable` 인터페이스와 `using` 블록으로 자원 해제를 명시적으로 처리합니다.

17. **속성(Attribute)**

    * `[`AttributeName`]` 형태로 메타데이터를 클래스·메서드 등에 부여해 리플렉션이나 프레임워크 기능과 연동합니다.
