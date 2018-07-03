---
layout: post
title: pgAdmin 을 웹버전으로 사용해 보자
---

pgAdmin 은 PostgresDB 를 GUI 환경으로 접근할 수 있는 가장 강력한 툴이다.
그러나, (다른 OS 에서는 사용해 보지 않았지만) 최소한 macOS 에서 pgAdmin4 는 종종 암을 유발하는 경우가 있다.
먹통이 되는 현상이랄까... 

만약 단지 여기까지 읽었을 뿐임에도 당신이 필자의 말에 공감한다면, 망설이지 말고 Python Wheel 버전으로 갈아타기 바란다.
사실 pgAdmin 내부는 원래부터 웹을 근간하고 하고 있으며, 각 OS 별 응용프로그램으로 레핑되어 배고되고 있을 뿐인 것으로 알고 있다. (electron 을 떠올리면 됨)

따라서 Python Wheel 버전은 웹버전이라기 보다는 퓨어한 버전의 pgAdmin4 라 할 수 있다.

설치는 뭐 별거 없다.

우선, https://www.pgadmin.org/download/pgadmin-4-python-wheel/ 에서 최신버전 다운로드.
(Home 디렉토리에 저장했다고 가정하겠다.)
``` sh
$ pip install ~/pgadmin4-(버전)-py2.py3-none-any.whl
```

설치가 끝나면 실행해 준다.

``` sh
$ python /usr/local/lib/python(system Python 버전)/site-packages/pgadmin4/pgAdmin4.py

Starting pgAdmin 4. Please navigate to http://127.0.0.1:5050 in your browser.
```
(아마 처음 실행시에는 로그인을 위한 이메일주소, 패스워드를 등록하게 될 것이다.)

로컬 웹서버로 pgAdmin4 가 런칭 되었으면, 안내대로 `http://127.0.0.1:5050` 에 접속해 준다.



**완전히 똑같지만, 훨씬 안정적으로 동작하는 순수 pgAdmin4 와의 조우...!**


<ins class="adsbygoogle" style="display:block; text-align:center;" 
    data-ad-layout="in-article" data-ad-format="fluid" data-ad-client="ca-pub-6472474470403321" data-ad-slot="4953204744"></ins>
