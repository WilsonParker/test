### 작업 내역

https://www.myluck.kr/

등록
https://www.myluck.kr/admin/theme/dosa/new_dosa_register.php

상세
https://www.myluck.kr/admin/theme/dosa/new_dosa_detail.php

수정
https://www.myluck.kr/admin/theme/dosa/new_dosa_modify.php

크롤링 데이터 등록
https://www.myluck.kr/admin/theme/dosa/crawling_register.php

Admin
--

### theme/dosa

- new_dosa_register.php
- new_dosa_detail.php
- new_dosa_modify.php

### admin/server

- new_dosa_register_server.php
- new_dosa_modify_server.php
- crawling_information_register.php

API
--

### callmix

- Callmix.php\
  (callmix api 연동 관련 파일)

> 가상 번호 할당

```injectablephp
include_once("/home/mydestiny/html/private/private_resource.php");
require('CallMix.php');

$service = new CallMix($connect); /* DB 연결 정보, private_resource.php 를 include 하면 사용 가능 합니다 */
$vn /* 가상 번호 */ = $service->mappingNumber($rn /* 실제 번호*/);
```

> 가상 번호 할당 취소

```injectablephp
include_once("/home/mydestiny/html/private/private_resource.php");
require('CallMix.php');

$service = new CallMix($connect); /* DB 연결 정보, private_resource.php 를 include 하면 사용 가능 합니다 */
$result /* 할당 취소 여부 bool */ = $service->releaseNumber($vn /* 가상 번호 */);
```

- response.php\
  (api 결과 출력 관련 파일)

- mapping.php\
  (가상 번호 할당 api)

- release.php\
  (가상 번호 할당 취소 api)

File
--
> 소개 이미지 1,2 는 mobile/dosa_profile_images 에 저장

Database
--

### callmix 추가

> callmix 가상 번호 할당 내역 정보 수집

### dosa_information 수정

> 소개 이미지 introduce_image_1, introduce_image_2\
> 소개 글 introduce_text_1, introduce_text_2, introduce_text_3\
> 영업 시간 working_time, 홈페이지 주소 homepage_url, 영상 주소 media_url

### test_crawling_information 추가
### test_crawling_review 추가
