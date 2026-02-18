[🇰🇷 한국어(Korean)](README.md) | [🇯🇵 日本語(Japanese)](README_ja.md)
# 🚀 ContentsPick

> ユーザーの好みに合ったコンテンツを推薦するウェブサイトです。

<br>

## 📖 目次

1. [プロジェクト紹介](#-プロジェクト紹介)
2. [主な機能](#-주요-기능)
3. [プレビュー](#%EF%B8%8F-미리보기)
4. [使用技術](#%EF%B8%8F-사용-기술)
5. [インストール及び実行方法](#%EF%B8%8F-설치-및-실행-방법)
6. [チームメンバー紹介](#%E2%80%8D%E2%80%8D%E2%80%8D-팀원-소개)
   
<br>

## 📌 プロジェクト紹介

Contents Pickは、多様なOTTサービスに分散しているコンテンツ情報を一箇所で確認し、ユーザーの選択をサポートするために制作された情報要約および推薦ウェブサービスです。

現代人が抱える「選択の疲労感」を軽減するために企画され、TMDB APIを通じて信頼性の高い基本情報を提供し、PythonクローリングによってIMDbの詳細レビューデータを収集・提供します。

データ収集(Python)から保存(MySQL)、APIサーバー(Spring Boot)、クライアントアプリ(Flutter)へと繋がる全体的なデータパイプラインを構築し、実際のサービス運用が可能なレベルの統合体験を目標に開発されました。

<br>

## ✨ 주요 기능

- **인기 컨텐츠 큐레이션:** TMDB API를 활용하여 '오늘의 트렌드', 'OTT별 순위' 등 사용자가 흥미를 가질만한 인기 영화 목록을 시각적으로 제공합니다. 
- **리뷰 데이터 데이터베이스 구축:** Python 스크립트를 활용하여 IMDb의 상세 리뷰 데이터를 수집 및 가공하고, 이를 DB에 적재하여 앱에서 볼 수 있도록 구현했습니다.
- **스마트 검색 및 필터링:** 제목의 일부만 입력해도 검색이 가능하며, 장르/최신순/별점순 등 다양한 기준으로 컨텐츠를 분류하여 탐색할 수 있습니다.
- **개인화 서비스 (My Page):** '관심 목록(찜하기)'과 '시청 기록' 기능을 통해 나만의 컨텐츠 리스트를 관리하고, 작성한 리뷰를 수정하거나 삭제할 수 있습니다.
- **사용자 인증 시스템:** 이메일 인증을 통한 회원가입, 비밀번호 암호화 저장(SHA-256), 로그인 세션 관리 등을 구현했습니다.

<br>

## 🖼️ 미리보기
![그림2](https://github.com/user-attachments/assets/b099d213-da07-44a0-9c0c-826613671154)


<br>

## 🛠️ 사용 기술

- **Backend:** `Java`, `Spring Boot`, `Spring Data JPA`
- **Frontend:** `Flutter`
- **Database:** `MySQL`
- **Data Collection:** `Python`
- **APIs:** `TMDB API`
<br>

## ⚙️ 설치 및 실행 방법

```bash
이 프로젝트는 Python(데이터 수집), MySQL(DB), Spring Boot(서버), Flutter(앱)로 구성되어 있습니다.
정상적인 구동을 위해 반드시 아래 순서(DB -> 크롤링 -> 서버 -> 앱)를 지켜주세요.

# 1. 저장소 클론
git clone https://github.com/Yun-Gi/ContentsPick-Movie-Recommendation.git

# 2. 데이터베이스 설정 (MySQL)
MySQL을 실행하고 'content_pick' 스키마를 생성합니다.
backend/src/resources/application.properties 파일에서 DB 접속 정보를 본인 환경에 맞게 수정합니다.

# 3. 데이터 수집
crawling폴더로 이동하여 의존성을 설치하고 크롤러를 실행해 DB에 초기 데이터를 적재합니다.
pip install -r requirements.txt
python crawler.py

# 4. 백엔드 서버 실행 (Spring Boot)
backend폴더를 IDE로 열고 Application.java 파일을 찾아 실행(Run)합니다.
서버가 8080 포트에서 정상적으로 실행되는지 확인합니다.

# 5. 애플리케이션 실행 (Flutter)
frontend폴더로 이동하여 패키지를 설치하고 앱을 실행합니다.

```

<br>

## 👨‍👩‍👧‍👦 팀원 소개

| 이름 | 역할 |  
| 이윤기 | DB 설계 및 API 개발 |  
| 오찬빈 | IMDb 리뷰 데이터 수집 및 TMDB 메타데이터 수집, 수집 데이터 전처리 및 정제 과정 담당 |  
| 김윤정 | UI/UX 디자인 및 개발, 백엔드 API 연동 |  
| 박성원 | 서비스 기획 및 아이디어 구체화, 프로젝트 일정 관리 및 문서화 |  
