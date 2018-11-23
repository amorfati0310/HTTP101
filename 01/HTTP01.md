### CORS

Same Origin Policy로 인하여 다른 domain자원 요청이 block되는 이슈를

No 'Access-Control-Allow-Origin'

Cross origin http요청을 제한합니다. 이러한 문제를 해결하기 위해서 Cross Origin Resource Sharing

Cors 메커니즘을 권하고 있다.

API 컨테이너 내에서 CORS를 사용합니다

Same Origin Poilcy -> 다른 Domain 요청을 할 수 있게 해주는 방식

1. CORS ->
2. JSONP Front단에서 해줄 수 있음 Script내에서 ..? 뭐였더라

네트워크 탭

서버 요청-> 응답

HTTP 메시지는 시작줄, 헤더, 본문으로 구성됩니다.

- 요청

GET/url/ 버전

헤더

User-agent

Upgrade-insecure-requests

body

- 응답

HTTPversion status code message

Connection

Content-Encoding

Content-Length

Content-Type

HTTP 메서드

- Get 가져오기
- Post 게시
- Put 집어넣다
- Patch 고치다
- Delete 지우다

- Option
- Head
- Connect
- Trace

Reference

- zerocho

- 웹지탱기술

- mdn

* Get QueryString Parameter

HTTP 헤더

공통 헤더

Data

Connection

CacheControl

ConentLength

ContentType

ContentEncoding Gzip

Req Header

Host - Domain Name

User-Agent 어떤 클라이언트를 이용해 요청했는지

Accept MIME 파일 형식

Authorization

Origin

Referer

Res Header

Acess-Control-Allow-Origin /

백엔드 주소와 프론트 주소가 같지 않으면 Cors Error

서버 응답 메시지에 헤더에 프론트 주소를 적어줘야 에러가 나지 않음

Allow 허용지정하는 헤더

Allow:Get Get요청만 받겠다

Content-Disposition 응답 본문을 브라우저가 어떻게 표시해야 할지 알려주는 헤더

ex) 다운로드 -> attachment

inline

Location

300번대나 201응답일 때 어느 페이지로 이동해야 할지 알려주는 헤더

Content-Secure-Policy

Content-Secure-Policy-src: 'self' 자신의 domain만 가져올 수 있습니다.

https로 지정

or none 가져올 수 없습니다.

질문

- HTTP가 뭔가여?
- HTTP 특징이 뭔가여?
- 캐싱

LocalStorage - 쿠기 - 세션 - IndexedDB

웹 자원을 효율적으로 쓰기 위해서 캐싱 !

저장해뒀다가 쓰는 것

크롬 Application Tab에서 자세한 정보를 확인 할 수 있다.

- Local Storage
- Session Storage
- IndexedDB
- Web SQL
- Cookies

보통 Cache Get요청을 통해서 캐시함

Cache-Control: no-cache 물어보기

Cache-Control: must-revalidate 만료된 캐시 받기

Cache-Control: public, max-age=3600 시간 유효기간

Cache-Control: public, private

Public 공유캐시에 저장 가능 Private 특정 사용자 환경에서만 저장

이런 옵션들은 혼합해서 써도 됨

Age: -> 초단위로 얼마나 지났는지 캐시 응답 헤더에 나타남

Expires로 만료기한을 줄 수 있다. Max-age가 있다면 무시됨

ETag git같이 컨텐츠가 바뀌었는지 검사할 수 있는 Tag

If-None-Match Etag가 다를 경우에만 서버에서 내려주고

캐시를 사용해라

쿠기

CDN같은 공유 캐시?

더 알아봐야 하는 용어 들

- CDN
- CORS 해결하는 방법 직접 해보기
  - JSONP
  - Header설정
- LocalStorage - 쿠기 - 세션 - IndexedDB 설명
- JWT 토큰?
