# 설치

이 페이지는 FlashBot을 가동하기 위한 환경을 설정하는 방법에 대해 안내합니다.

1. [GitHub](https://github.com/flashbot-discord/flashbot)에서 최신 버전의 소스코드를 `clone`합니다.

   ```bash
   git clone https://github.com/flashbot-discord/flashbot.git
   ```

2. 의존성 패키지들을 설치합니다.

   ```bash
   # yarn 사용 (권장)
   yarn

   # npm 사용
   npm i
   ```

3. `config.example.json`을 `config.json`으로 복사합니다.
4. `config.json`을 수정합니다. 설정 파일에 대한 설명은 [여기](https://github.com/flashbot-discord/docs/tree/7de5c29a3bb7ed60704defdad6d5ad67f6b860c7/selfhosting/config.md)에서 볼 수 있습니다.

