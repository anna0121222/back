# 리바운드 REBOUND

## 마음의 안정감을 찾기 위한 플랫폼
<br>

## 🔍 기획 의도
<img alt="기획의도" src="https://github.com/user-attachments/assets/65730cd7-20b2-4b25-b3be-79be8bda5f80" />

<br>
통계적으로 볼 때, 한국 사회는 <strong>도전과 실패에 대해 비교적 관대한 편이 아니다. </strong>실패를 공개적으로 이야기하는 것이 중요하다고들 하지만, 정작 <strong>그런 경험을 솔직하고 구체적으로 나눌 수 있는 창구는 거의 없는 상황이다.</strong>
누구나 크고 작은 실패를 겪지만, 그 이유와 상황이 제각각이라 <strong>극복 방법을 찾기 어렵고,</strong> 그로 심해  <strong>심리적 고통이나 마음의 병</strong>으로 이어지는 경우도 적지 않다. <br> 
그래서 일상 속 다양한 실패 경험을 공유하고, <strong>서로의 극복 과정과 회복의 이야기를 나눌 수 있는 공간</strong>이 필요하다고 느꼈다. 이러한 문제의식에서 출발해, '실패를 함께 이야기하고 극복하는 플랫폼'을 기획하게 되었다. 
<br><br>

## ⚡ 기대 효과
<img alt="기대효과" src="https://github.com/user-attachments/assets/b86e2ca6-b524-41eb-bcc1-5a4d3ad3d0f2" />

<br>
<strong>마음의 휴식처 마련</strong>
<br>: 실패를 숨기거나 부끄러워하지 않아도 되는 공간을 제공함으로써, 개인이 마음의 짐을 덜고 스스로를 돌아볼 수 있는 심리적 안식처를 마련. 사용자는 자신의 경험을 솔직히 털어놓으며 감정을 정리하고, 타인의 공감 속에서 위로를 받을 수 있음

<strong>위안을 주고받는 선순환 </strong>
<br>: 한 사람의 극복 사례가 또 다른 사람에게 공감과 위로, 용기가 되어 돌아가는 선순환 구조 및 자연스러운 지지와 응원의 문화 형성.

<strong>실패를 부정적으로만 여기는 사회 분위기 타파</strong>
<br>: 사람들이 나누는 다양한 실패와 극복의 사례를 통해, 실패를 성장의 일부로 바라보는 시각과 도전을 두려워하지 않는 건강한 사회 분위기 형성을 도움.
<br><br>



## 🛠️ 기술 스택 (Tech Stack)

| 구분 | 사용 기술 |
|------|------------|
| **HTML Engine** | Thymeleaf |
| **Frontend** | HTML, JavaScript, CSS |
| **Backend** | Spring Boot, Java |
| **Database** | PostgreSQL, Redis |
| **Infra** | AWS EC2, AWS IAM, AWS S3 |
| **Development Tools** | VS Code, IntelliJ IDEA |
| **API & Library** | Kakao Login, Kakao Map, Kakao 주소 API, SMTP Gmail API, REST API, Lombok, MyBatis, OAuth 2.0, Google Login, Boot Pay, Naver Login, JWT, Spring Security, CoolSMS, Swagger UI |
| **Collaboration & Version Control** | Git, GitHub, Slack, Postman, Sourcetree |
| **Testing** | JUnit5 |

<br><br>

## 🧱 ERD
<img alt="rebound_ERD" src="https://github.com/user-attachments/assets/4e0754a7-2702-4b25-9595-67663645c20d" />
<br><br>


## 👨‍💻 담당 업무
### 🗂️ 프론트엔드
<img alt="rebound_front" src="https://github.com/user-attachments/assets/e353aa72-38cf-4342-a9c1-82fda290dc9b" />
<br>

▶ 커뮤니티
- 경험담 작성
- 실패 경험담 목록(작성자)
- 실패 경험담 목록(타인)
- 실패 경험담 상세

▶ 오늘의 좋은 말
- 작성
- 목록

<br>

### 🗂️ 백엔드
<img alt="rebound_back" src="https://github.com/user-attachments/assets/1da85391-a3a2-48db-bc82-bc63facfc941" />
<br>

▶ 결제
- 구독 결제
<br>

▶ 메인 페이지
- 메인 페이지 구성: 게시글 및 공지사항 등 최신순으로 정해진 개수만큼 보이게 설정
- header: 로그인 한 계정의 댓글 알림 서비스
- footer: 연결되는 페이지 경로 작성
<br><br>


## 문제 해결

### 📌구독 결제 후에도 일반 회원
<ul>
<li><strong> 🌩문제 상황 </strong>
<br>: 결제 후, 결제한 회원의 계정 정보를 '일반 회원'에서 '구독 회원'으로 변경하고자 했으나 여전히 일반회원이었다.
</li><br>

<li><strong> 🚨문제 원인 </strong>
<br>: 쿼리문을 작성할 때 결제 정보만 저장되게 하고 회원 정보는 수정하지 않았다.
</li><br>

<li><strong>🚀해결 방법 </strong>
<br>: 회원 정보를 수정하는 쿼리문을 추가로 작성하고 ServiceImpl.java에서 한 메소드 안에서 두 개가 모두 작동되도록 했다.
</li><br><br>
</ul>

### 📌댓글이 달렸지만 불러와지지 않는 알림 
<ul>
<li><strong>🌩문제 상황 </strong>
<br>: 자신이 작성한 게시글에 새로운 댓글이 달렸으나 알림창을 확인해도 새 알림이 뜨지 않았다. 
</li><br>

<li><strong>🚨문제 원인 </strong>
<br>: 대부분의 페이지에서 알림을 확인할 수 있어야 하는데, 한곳에서만 확인할 수 있도록 작성되어 있었다. <br>
</li><br>

<li><strong>🚀해결 방법 </strong>
<br>: 알림을 확인할 수 있어야 하는 페이지의 경로들을 WebMvcConfig.java에 작성하여 문제를 해결했다.
</li>
</ul>
<br><br>


## 느낀점

#### 🌟 끝나지 않는 기획
프로젝트 초반에는 기획이 일정 단계에서 마무리될 줄 알았지만, 진행 내내 계속 수정과 변경이 반복되었다. 새로운 페이지가 추가되거나, 예상치 못했던 기능이 필요하다는 사실을 뒤늦게 발견하기도 했고, 그로 인해 기존 페이지가 사라지거나 구조가 바뀌는 혼란도 있었다.<br>
기획이 끝나지 않은 채로 개발이 진행되다 보니, 중간중간 회의를 통해 문제를 조율하고 수정하는 과정을 여러 번 거쳤다. 그 과정에서 <strong>기획이 단순히 시작 단계에서 끝나는 일이 아니라, 프로젝트 전반에 걸쳐 영향을 미치는 핵심 단계</strong>라는 점을 깨달았다.<br>
이번 경험을 통해, <strong>기획이 탄탄해야 이후의 개발이 막히지 않고 원활하게 진행될 수 있다는 것을 배웠다.</strong> 다음에는 초반 기획 단계에서 더 많은 시간을 들여 구조를 명확히 하고, 이번에 느꼈던 아쉬움을 보완하여 더 완성도 높은 기획과 개발을 이뤄내고 싶다.

#### 🌟 스스로의 부족함을 깨달은 경험
이번 프로젝트를 통해 내 이해도와 실력의 한계를 뚜렷하게 느꼈다. 분명 이해했다고 생각했던 개념들도 막상 코드를 작성하려니 헷갈리거나 제대로 구현하지 못하는 부분이 많았다. 단순히 '아는 것'이 아니라, <strong>스스로 설명하고 적용할 수 있을 만큼 확실히 이해하는 것의 중요성을 실감했다.</strong><br>
부족한 상태로 프로젝트에 참여하다 보니 아쉬움이 컸지만, 그만큼 포기하지 않고 끝까지 해냈다는 점에서 의미가 있었다. 이번 경험을 발판 삼아 다음에는 같은 실수를 반복하지 않도록 더 단단히 준비해야겠다고 다짐했다.

#### 🌟 다음 프로젝트를 향한 다짐
이번 경험을 통해 스스로의 부족한 부분을 인식하고 채워나가는 공부의 중요성을 다시금 깨달았다. 아쉬운 점이 많았던 만큼, 다음에는 그런 후회가 남지 않도록 준비하고 싶다.<br>
이를 위해 지금까지 배운 내용을 복습하고 체계적으로 점검하며, <strong>이론뿐 아니라 실전에서도 적용할 수 있는 역량을 키워나가야겠다.</strong> 다음 프로젝트에서는 온전한 1인분을 해내는 개발자로서 팀에 보탬이 되고 싶다고 생각했다.
