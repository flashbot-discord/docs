---
description: 개발용 명령어들
---

# 개발용

{% hint style="warning" %} **이 명령어는 대부분 봇 소유자로 등록된 사람만 사용할 수 있습니다.** {% endhint %}

## `//args-info` 명령어 인수 테스트

봇에서 감지하는 명령어 인수를 알려줍니다.

* 별칭: `argsinfo`, `ㅁㄱㅎㄴ-ㅑㅜ래`, `ㅁㄱㅎ냐ㅜ래`

```text
//args-info <인수...>
```

## ~~`//blacklist` 블랙리스트~~

{% hint style="danger" %} 이 명령어는 아직 완성되지 않았고 작동하지 않습니다! {% endhint %}

이 봇의 블랙리스트(봇을 이용할 수 없는 사람)를 관리합니다.

## `//error` 오류 강제로 발생

오류를 강제로 발생시켜 오류 처리 과정을 테스트합니다.

* 별칭: `에러`, `ㄷㄱ객`, `dpfj`
* **소유자만 사용 가능**

## `//eval` 코드 실행

Javascript 코드를 실행합니다.

{% hint style="danger" %} 이 명령어는 이 봇과 봇이 작동하고 있는 시스템에 **직접적인 영향을 줄 수 있습니다**. 명령어를 실행하기 전에 **입력한 내용을 한 번 더 확인하세요**. {% endhint %}

* 별칭: `evaluate`, `ㄷㅍ미`, `ㄷㅍ미ㅕㅁㅅㄷ`
* **소유자만 사용 가능**

### 사전정의된 값
명령어 사용의 편의를 위해 다음 값들이 사전에 정의되어 있습니다:
```js
// msg = Message 객체

const client = msg.client
const guild = msg.guild
const channel = msg.channel
const author = msg.author
const member = msg.member
const Discord = require('discord.js')
const childProcess = require('child_process')
const fs = require('fs')
const os = require('os')
const jsondb = msg.client.db.obj // json 사용 시 데이터 위치
const knex = msg.client.db.knex // knex 관련 db 사용 시
```
