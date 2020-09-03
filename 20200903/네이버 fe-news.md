ref : https://github.com/naver/fe-news

네이버 FE 엔지니어들이 엄선한 양질의 FE 및 주요한 기술 소식들을 큐레이션해 공유하는 것을 목표로

JavaScript 번들러로 본 조선시대 붕당의 이해

아래의 JS 객체 리터럴과 JSON.parse()를 통한 문자열 파싱 방식들 중, 어떤 것이 성능적으로 더 빠를까?

const data = { foo: 42, bar: 1337 };
const data = JSON.parse('{"foo":42,"bar":1337}');
JSON.parse()는 파싱, 컴파일 그리고 실행 모든 단계에 있어, 대다수의 JS 엔진에서 객체 리터럴 대비 약 1.7배 이상 더 빠르게 처리된다.

JSON의 빠른 파싱을 위해 SIMD(Single Instruction Multiple Data)를 사용해 GB 단위의 데이터를 초당 처리할 수 있는 simdjson 프로젝트도 흥미로워 보이며, 다양한 바인딩(Node.js 바인딩은 simdjson_nodejs)과 포트들이 제공된다.

암호화폐 호가 JSON 데이터를 simdjson보다 더 빠르게 파싱하는 C++ 코드를 작성한 경험을 다룬 "세계에서 제일 빠른 JSON 파서 만들기" 글도 재밌게 읽어볼 수 있다.


또한 javascript에서 문자열 출력 문제에 관하여
https://dmitripavlutin.com/what-is-string-in-javascript/
