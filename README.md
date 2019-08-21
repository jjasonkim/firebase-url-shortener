# Serverless url shortener with Google Firebase

slack-hubot 과 함께 사용하도록 만들어졌습니다. 어뷰징을 막기위해 hubot API token 이 요청 헤더에 있을 때만 동작 하도록 설계되었습니다. → [sunjae.kim/slack-hubot](http://sunjae.kim/slack-hubot)

단순 URL 저장을 위해 [Firebase 실시간 데이터베이스](https://firebase.google.com/docs/database/?hl=ko) 를 사용했습니다.

![화면캡처](https://user-images.githubusercontent.com/40228715/63393446-1a2c6900-c3f6-11e9-8da3-f3a2eddf8cbc.png)

→ [sunjae.kim/github](http://sunjae.kim/github)

---

## Getting Started

### Install

1. Install node modules
    ```bash
    $ cd functions && npm install
    ```

2. Set environment variables
    ```python
    # functions/.env
    FIREBASE_DATABASE_URL=""
    HUBOT_SLACK_TOKEN=""
    ```

3. Set firebase service_account file at `functions/service_account.json`
    
    - Firebase Console  →  Settings  →  Service accounts  →  Generate new private key

### Start

1. Compiles and hot-reloads for development
    ```bash
    $ firebase serve --only functions
    # or
    $ cd functions && npm run serve
    ```

2. Deploy
    ```bash
    $ firebase deploy --only functions
    # or
    $ cd functions && npm run deploy
    ```