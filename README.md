# League of legend Winner team predict to Using Riot API

> 2019.07.02-2019.11.12 데이터 분석 개인 프로젝트

A project to collect league-of-legend game records to analyze the factors that affect victory and to predict winning rates based on real-time score fluctuations.

리그 오브 레전드 경기 기록을 수집하고, 가공하여 승률에 영향을 주는 요인 분석과 실시간 스코어 변동에 따른 승률 예측 프로젝트

![image](https://i.imgur.com/8YdHEAB.jpg)

## 프로젝트 동기

많은 사람이 리그 오브 레전드, 롤을 즐기고 나 또한 이 게임을 매우 좋아하고 즐겨한다. 어릴때부터 친구들과 랭크 경쟁을 하면서 롤을 잘하고 싶었다.

나는 롤을 시즌4, 2014년부터 해온 흔히 말하는 골수 유저인데 티어대가 실버, 골드(상위 30%-40%)에 머물며 매 시즌마다 크게 향상이 없었다. 친구들은 내가  피지컬(반응속도, 순간 판단력 등)은 좋은데 게임을 볼 줄 모른다고 하였다. 오브젝트, KDA, 등등 게임 내의 지표를 보면서 전체적인 게임을 봐야 승률이 오   르는데 라인전에 바쁜 내가 언제 그걸 보고 분석하는가. 많은 플레이를 하면 되겠지만 게임만 하고 지낼 순 없었다. 하지만 또 티어는 높이고 싶었다.

가장 유명한 롤 전적 사이트인 OP.GG는 RIOT(롤 개발사)에서 제공하는 API를 이용해 유저의 전적과 게임의 기록을 표시해준다. 하지만 그뿐, 그에 대한 피드백  은 또 유저 자신이 보고 알아야한다.

그래서 나는 게임 실력도 올리고 개발, 데이터 분석 공부도 할 겸, 파이썬을 이용해 천상계(게임의 최고위 티어인 챌린저, 그랜드마스터, 마스터)의 전적을 수집하고, 머신러닝과 다양한 기법으로 데이터 분석을 진행해 천상계의 게임은 어떻게 진행되는지, 승률에 미치는 중요한 지표와 해당 지표에 따른 승률을 예측해보고, 내 전적을 피드백해 나의 롤 실력을 향상시킬 것이다.

## 프로젝트 구성

### 1. DATA ETL(Extract, Transform, Load) 2019.07.02 - 2019.08.23

RIOT에서 제공하는 API를 이용해 데이터를 수집하고 가공하고, 파일화하여 저장한다.

### 2. Match Data EDA(Exploratory Data Analysis) 2019.08.23 - 2019.09.01

모은 데이터를 분석에 용이하도록 전처리하고, 승패에 영향이 가는 변수를 분석한다.

### 3. Winner / Loser predict Model Build 2019.09.01 - 2019.09.10

승패 예측을 진행할 모델을 구축하고 튜닝을 통해 예측의 정확도를 올려 신뢰성 있는 모델을 만든다.

### 4.Project Result 2019.09.12 - 2019.11.12( 랭크 게임 종료시까지 )

모델의 feature_importance 를 확인과, 해당 지표가 실제로 승률에 영향을 미치는가 확인.
이후 이 지표를 중심으로 게임을 한다.

## ALL DATA SET LINK

모든 데이터 셋은 Kaggle 에 공개하였음.

<https://www.kaggle.com/shinbg/lol-classic-rank-game-datakrtop-3-tier>

코드 복제와 데이터 셋 사용은 자유이며 다른 사람도 유용한 인사이트를 도출해 실버 골드를 탈출하길 바람.
