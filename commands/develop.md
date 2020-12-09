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

### unsafe mode
봇을 보호하기 위해, 기본적으로 봇 토큰을 쉽게 접근할 수 없는 저장소로 이동한 뒤 코드를 실행합니다.
다만 이 동작이 코드 실행을 방해하거나, 최악의 경우 **for문 안에서 실행이 멈춰 봇 전체가 멈춰버리는 상황**이 생기기도 합니다.

이런 상황의 경우 토큰을 이동하지 않고 코드를 실행하는 `unsafe mode`를 사용해야 합니다.
명령어랑 코드 전에 `-u` 또는 `--unsafe` 옵션을 붙이면 unsafe mode로 작동합니다.

```
//eval -u <코드>
```

{% hint style="danger" %} 봇 토큰이 유출될 수 있으므로 코드를 실행하기 전에 **다시 한 번 확인하세요!** {% endhint %}

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

또한 `this`는 `EvalCommand#execute()` method를 가리킵니다.

## `//exec` 쉘 스크립트 실행

봇을 구동하는 시스템에서 쉘 명령어를 실행합니다.

{% hint style="danger" %} 이 명령어는 이 봇과 봇이 작동하고 있는 시스템에 **직접적인 영향을 줄 수 있습니다**. 명령어를 실행하기 전에 **입력한 내용을 한 번 더 확인하세요**. {% endhint %}

* 별칭: `execute`, `ㄷㅌㄷㅊ`, `ㄷㅌㄷ쳣ㄷ`
* **소유자만 사용 가능**

## `//load` 명령어 로드

명령어를 불러옵니다.

* 별칭: `ㅣㅐㅁㅇ`
* **소유자만 사용 가능**

```
//load <명령어 파일 경로>

# dev/eval.js
//load dev/eval
```

명령어 파일의 확장자(`.js`)는 입력하지 않습니다.

## `//maintenance` 점검 모드 설정

점검 모드 상태를 확인하거나 변경합니다.

* 별칭: `maintain`, `점검`, `ㅡ먀ㅜㅅ두뭋ㄷ`, `ㅡ먀ㅜㅅ먀ㅜ`, `wjarja`
* **소유자만 사용 가능**

```
# 점검 모드 상태 보기
//mainteanace

# 점검 모드 상태 변경
//maintenance <상태>
```

`상태`에는 다음 중 하나를 입력할 수 있습니다:

* 점검 모드를 설정할 경우: `start`, `on`, 또는 `시작`
* 점검 모드를 해제할 경우: `end`, `off`, 또는 `종료`

## `//notice` 공지 발송

봇 전체공지를 발송합니다.

* 별칭: `공지`, `ㅜㅐ샻ㄷ`, `rhdwl`
* **소유자만 사용 가능**

```
//notice <발송할 공지 내용>
```

{% hint style="info" %} 현재는 **공지 발송 기능**만 있으며, 추후에 공지 발송 상황 등을 확인하는 기능이 추가될 예정입니다. {% endhint %}


