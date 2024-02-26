# Makefile-Test-Action
간단하게 루트 하위계층의 모든 Makefile의 성공 여부를 테스트할 수 있는 공개 Action 입니다.

# 사용법
```yml
name: Your Workflow
on: push
jobs:
  test-makefiles:
    runs-on: ubuntu-latest
    steps:
      - name: Make Test
        uses: fing9/42Cursus-Makefile-Test@v3.0.2
        with:
          dir: . # 하위 계층의 모든 Makefile에 대해서 Make를 실행할 루트 계층, 따로 지정하지 않을 시 .(루트 디렉토리)로 지정됨
```


# 예시
```yml
name: 42Cursus CPP Makefile Test

on:
  push:
    branches: [ "master" ]
  pull_request:
    branches: [ "master" ]

jobs:
  test-makefiles:
    runs-on: ubuntu-latest
    steps:
      - name: Checkout repository
        uses: actions/checkout@v3
      - name: 42Cursus C/CPP Makefile Testing
        uses: fing9/42Cursus-Makefile-Test@v3.0.2
```
