# Makefile-Test-Action
간단하게 루트 하위계층의 모든 Makefile의 성공 여부를 테스트할 수 있는 공개 Action 입니다.

# 사용법
```yml
name: Your Workflow
on: push
jobs:
  calculate:
    runs-on: ubuntu-latest
    steps:
      - id: Make Test
        uses: fing9/42cursus-makefile-test@v1
        with:
          dir: . # 하위 계층의 모든 Makefile에 대해서 Make를 실행할 루트 계층, 따로 지정하지 않을 시 .(루트 디렉토리)로 지정됨
```
