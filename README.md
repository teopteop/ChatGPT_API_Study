summeruze_app<br/>
//구문 요약 프로그램<br/>
<br/>
generate_ads_app<br/>
//광고문구 생성 프로그램<br/>
<br/>
telegrambot_app<br/>
//텔레그렘 챗봇 프로그램<br/>
/ask 질문내용 으로 챗지피티에게 응답요청 받은 내용을 답변해줌<br/>
//별도의 api키 입력 필요<br/>
<br/>
kakaochatbot_app<br/>
//카카오톡 챗봇 프로그램<br/>
/ask 질문내용 으로 챗지피티에게 응답요청 받은 내용을 답변해줌<br/>
//별도의 api키 입력 필요<br/>
***
DALL.E3<br/>
openai.com/dall-e-3<br/>
자연어 처리와 컴퓨터 비전의 최신 기술을 활용해서 생성하고자 하는 이미지의 입력을<br/>
고품질의 이미지로 생성해주는 api<br/>
<br/>
랭체인(LangChain) 프레임워크<br/>
AI 모델을 쉽게 연결하고 활용할 수 있도록 도와주는 도구로써<br/>
챗봇을 만들 때 여러 모델과 데이터의 연계를 통해 효율적인 대화를 가능하게 해주는 프레임워크<br/>
<br/>
Max Token 이상의 긴글을 챗지피티로 요약하는 방법?<br/>
글을 쪼개서 이용한다<br/>
글을 일정한 수로 분할한 후 각각을 따로 요약을 요청한다<br/>
추후에 모든 요약본을 취합해서 최종 요약본을 요청한다.<br/>
렝체인의 모듈화를 사용해서 짧게 이용할 수 있다.<br/>
<br/>
텍스트 임베딩<br/>
문서, 문장, 단어 등의 텍스트를 인공지능 모델이 처리할때는<br/>
실수가 나열된 값인 벡터로 변환해서 입력을 사용하며<br/>
텍스트를 벡터화하는 과정을 임베딩이라고 부른다.<br/>
<br/>
gTTS 구글 번역의 음성재생 기능을 활용한 TTS서비스<br/>
별도의 API 키 없이도 패키지 설치시 무료로 사용가능<br/>
<br/>
STT  Speech TO Text 음성을 분석해서 텍스트를 생성<br/>
Whisper OpenAI의 STT<br/>
<br/>
FFmpeg<br/>
오픈소스 멀티미디어 프레임워크로, 비디오, 오디오, 그리고 기타 멀티미디어 파일 및 스트림을 <br/>
레코드, 변환 및 스트리밍하는 데 사용 음성 파일 input을 ffmpeg를 통해 받음<br/>
<br/>
audiorecorder<br/>
사용자의 마이크로 오디오 인풋을 쉽게 받을 수 있도록 해주는 스트림릿 오픈소스<br/>
***  
HTTP 통신 개념을 파이썬 환경에서 실습하기<br/>
<br/>
HTTP Request 서버 요청<br/>
URL 과 요청 메서드를 통해 특정 리소스를 요청하는 서버로 보내는 메세지<br/>
header와 본문이 포함되며<br/>
header에는 요청중인 리소스의 url 과 get, post 두 가지의 요청 메서드가 포함<br/>
본문에는 양식 데이터 또는 JSON payload와 같은 추가 데이터가 포함<br/>
<br/>
클라이언트 >>> HTTP Request 서버 요청   >>> 서버<br/>
클라이언트 <<< HTTP Response 서버 응답 <<< 서버<br/>
<br/>
HTTP Response 서버 응답<br/>
요청에 대한 응답으로 서버에서 클라이언트로 보내는 메세지<br/>
header와 본문이 포함되며<br/>
header에는 사용중인 http버전과 상태 코드 정보 및 쿠키, 캐싱정보 등의 다양한 정보가 포함<br/>
본문에는 HTML, CSS, JavaScript, 이미지 또는 JSON  데이터 등의 실제 콘텐츠가 포함<br/>
<br/>
파이썬 환경에서 HTTP 통신을 하려면<br/>
urllib3라는 패키지를 사용<br/>
<br/>
텔레그렘 챗봇<br/>
텔레그렘 실행후 BotFather와 대화 시작<br/>
/newbot으로 새 챗봇을 생성<br/>
토큰을 발급받고 따로 저장해둔다<br/>
<br/>
텔레그렘 API의 URL 양식<br/>
https://api.telegram.org/bot<token>/METHOD_NAME<br/>
token에 발급받은 토큰을 입력 후 요청할 메소드 네임을 입력하면된다.<br/>
<br/>
FastAPI 와 ngrok를 사용<br/>
로컬서버 생성해서 텔레그렘과 연동<br/>
FastAPI를 사용해서 로컬 서버 생성<br/>
ngrok를 통해 외부에서 로컬로 접속하기 위한 주소 발급<br/>
해당 주소를 Telegram API의 웹훅과 연결<br/>
<br/>
ngrok설치 및 토큰 입력후<br/>
터미널 창에 ngrok http 8000 명령어 입력 > 8000번 포트로 외부서버에서 접속 가능한 서버 주소 생성<br/>
url을 통해 Webhook을 설정<br/>
<br/>
아마존 웹 서비스(AWS)를 활용하여 텔레그렘 챗봇 만들기<br/>
aws에서 람다 함수 생성<br/>
키 유출을 막기위해 환경변수를 사용해서 api키와 텔레그램 토큰을 입력<br/>
람다함수에 코드를 작성<br/>
aws내부에서 직접 패키지를 설치할 수 없기에  패키지를 업로드<br/>
API 게이트웨이 생성
url을 통해 Webhook을 설정<br/>
모니터링에서 로그를 통해 사용기록 확인가능<br/>
***
카카오톡 챗봇<br/>
카카오톡 채널 및 챗봇을 생성<br/>
텔레그램 챗봇과 같은 방식으로 로컬서버 생성 및 외부 접속 주소 생성<br/>
카카오톡 챗봇 관리자 센터에서 카카오톡 서버와 로컬 서버 연결하기<br/>
스킬목록에 ngrok를 통해 생성된 url 입력<br/>
배포진행<br/>
