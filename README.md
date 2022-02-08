# 텔레그램 개인 봇 만드는 법

1. 텔레그램 창에 "BotFather" 검색
<img width="593" alt="스크린샷 2022-02-06 오후 10 15 16" src="https://user-images.githubusercontent.com/80435502/152683041-11015126-a639-4d29-98c0-7dce348efdcb.png">
2. BotFather 대화창에 순서대로 입력
    -/start
    - /newbot
    - /{}_bot # 봇 이름 설정
    - /{}_bot # 봇 사용자 이름 설정
    - 토큰 발급
    <img width="567" alt="스크린샷 2022-02-06 오후 10 43 33" src="https://user-images.githubusercontent.com/80435502/152683806-94129e4e-b24e-4dd1-a2f2-79c893bf21e4.png">
    - 발급 받은 토큰으로 chat id 알아내기
        - 인터넷 검색 창에 아래와 같이 검색
            "https://api.telegram.org/bot{발급 받은 토큰}/getUpdates"
<img width="1167" alt="스크린샷 2022-02-06 오후 10 28 07" src="https://user-images.githubusercontent.com/80435502/152683255-e186b3cd-f53a-4aad-992b-7b44dbcf878d.png">

3. 라이브러리 설치

    pip3 install python-telegram-bot --upgrade

4. 코드 추가하기

    <code>
    import telegram

    chat_token = "발급 받은 API"

    bot = telegram.Bot(token = chat_token)

    chat_id = 1666417159

    start_text = '코드 시작'
    bot.sendMessage(chat_id=chat_id, text=start_text)

    (기존 코드)
    
    end_text = '코드 종료'
    bot.sendMessage(chat_id=chat_id, text=end_text)
    
    </code>
