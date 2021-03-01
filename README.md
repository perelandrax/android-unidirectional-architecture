# 안드로이드 단방향 아키텍쳐

안드로이드 단방향 아키텍쳐에 대한 고찰 (정리되지 않은 아이디어들)

---

## 키워드

- Flow
- ViewModel
- Databinding (+LiveData)
- Testable
- Abstraction
- Coroutines
- Kotlin

## 추상화

- 앱의 가장 중요한 본질을 찾는다.
- 어떻게 하면 사용자 원하는 정보를 보여줄 수 있는가?
- 사용자가 앱에 액션을 입력하면 서비스와 관련된 정보를 화면에 표시한다.
- 기본적인 추상화 클래스를 도출한다. View, Model
- 만들어진 추상화 클래스의 행위를 도출한다.
- View
  - 사용자의 입력을 전달받는 역할
  - 정보를 화면에 표시하는 역할
- Model
  - 서비스 정보를 저장하고 있는 역할
  - 정보를 화면에 전달하는 역할

## 아이디어

- Backend 아키텍쳐 참고
  - Controller (MVC 컨트롤러에서 사용. 모바일에서는 View 역할)
  - Service (비지니스 로직에서 사용. 모바일에서는 ViewModel, Presenter 역할)
  - Repository (데이터 접근 계층에서 사용. 모바일에서는 네트워크, 디비, 메모리를 추상화 한 역할)
