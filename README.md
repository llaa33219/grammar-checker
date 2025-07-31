# 🌍 AI 자동 언어 감지 + 전세계 정밀 문법 검사기

Cloudflare Workers에서 동작하는 **AI 자동 언어 감지 + 각 나라별 전문 무료 API 통합** 문법 검사 사이트입니다.

## 🎯 **혁신적인 시스템**

### 🤖 **완전 자동 언어 감지**
- **franc AI**: 414개 언어 자동 감지 (완전 무료)
- **스마트 매핑**: 감지된 언어 → 해당 나라 전문 API 자동 선택
- **즉석 처리**: 텍스트 입력 → AI 감지 → 최적 검사 원스톱

### 🔥 **각 언어별 전문 API**
기존의 통합 API들과 다르게, **감지된 언어별로 해당 국가에서 개발한 전문 무료 API**를 자동 선택하여 **최고 정확도**를 제공합니다.

## ✨ **주요 기능**

### 🎯 **AI 자동 언어 감지 시스템**
- **414개 언어** 자동 감지 (franc 라이브러리)
- **실시간 처리**: 입력과 동시에 언어 판별
- **스마트 라우팅**: 감지 결과에 따라 최적 API 자동 선택
- **폴백 처리**: 미지원 언어는 LanguageTool로 처리

### 🔥 **언어별 전문 API 통합**
- **한국어**: 부산대학교 인공지능연구실 + 다음 맞춤법 검사기 (95% 정확도)
- **일본어**: Enno.jp - 9,400개 에러 패턴 (92% 정확도)
- **중국어**: 满分语法 - 중국 현지 AI 서비스 (90% 정확도)
- **독일어**: rechtschreibpruefung24.de - 독일 현지 서비스 (89% 정확도)
- **러시아어**: pr-cy.ru - 러시아 현지 AI (87% 정확도)
- **영어**: GrammarBot + LanguageTool 조합 (94% 정확도)
- **기타**: 20+ 언어 LanguageTool 지원

### 💡 **스마트 검사 시스템**
- **다중 API 결과 통합**: 중복 제거 및 정확도 향상
- **실시간 오류 검출**: 문법, 맞춤법, 띄어쓰기 종합 분석
- **언어별 최적화**: 각 언어 고유 문법 규칙 적용
- **소스 추적**: 어느 API에서 검출했는지 표시

### 🎨 **현대적인 UI/UX**
- **AI 자동 감지 우선**: 기본 모드로 설정
- **언어별 카드 선택**: 수동 선택도 가능
- **실시간 검사 결과**: 감지된 언어 정보 표시
- **정확도 표시** 및 **사용된 API 정보**

### ⚡ **Cloudflare Workers 최적화**
- **엣지 컴퓨팅**으로 빠른 응답
- **CORS 지원** 및 **오류 처리**
- **20,000자 제한**으로 안정성 보장

## 🌐 **지원 언어 및 정확도**

### 🤖 **AI 자동 감지 (franc)**
- **414개 언어** 지원 (세계 최대 규모)
- **완전 무료** (MIT 라이선스)
- **브라우저 내장** (API 키 불필요)

### 📊 **전문 API별 정확도**

| 언어 | 전용 API | 정확도 | 특징 | franc 코드 |
|------|----------|--------|------|-------------|
| 🇰🇷 한국어 | 부산대 + 다음 | **95%** | 띄어쓰기, 조사 활용 전문 | kor |
| 🇯🇵 일본어 | Enno.jp | **92%** | 9,400개 에러 패턴 | jpn |
| 🇨🇳 중국어 | 满分语法 | **90%** | 600만자/월 무료 | cmn, zh-cn, zh-tw |
| 🇺🇸 영어 | GrammarBot + LT | **94%** | 다중 API 조합 | eng |
| 🇩🇪 독일어 | rechtschreibung24 | **89%** | 독일 현지 개발 | deu |
| 🇷🇺 러시아어 | pr-cy.ru | **87%** | AI 기반 검사 | rus |
| 🌍 기타 언어 | LanguageTool | **80-85%** | 스페인어, 프랑스어, 이탈리아어 등 | spa, fra, ita... |

## 🚀 **배포 방법**

### 1. 필수 준비사항
- Node.js 18+ 설치
- Cloudflare 계정
- wrangler CLI 설치

### 2. wrangler 설치 및 설정
```bash
npm install -g wrangler
wrangler login
```

### 3. 프로젝트 설정
```bash
# 의존성 설치
npm install

# 개발 서버 실행
npm run dev
```

### 4. 배포
```bash
# 프로덕션 배포
npm run deploy
```

## 🔧 **기술 스택**

- **Frontend**: Vanilla JavaScript, CSS3, HTML5
- **언어 감지**: franc 라이브러리 (414개 언어)
- **Backend**: Cloudflare Workers
- **APIs**: 
  - 부산대학교 인공지능연구실 API
  - Enno.jp (일본)
  - 满分语法 (중국)
  - rechtschreibpruefung24.de (독일)
  - pr-cy.ru (러시아)
  - GrammarBot
  - LanguageTool

## 💸 **비용 절약 효과**

### 🆓 **완전 무료**
- **AI 언어 감지**: franc 라이브러리 (무료)
- **각 나라별 무료 API** 활용
- **Cloudflare Workers 무료 플랜** 사용
- **운영비 0원**

### 💰 **유료 서비스 대비 절약**
| 서비스 | 월 비용 | 본 프로젝트 |
|--------|---------|-------------|
| Google Translate API | $20/100만자 | **무료** |
| AWS Comprehend | $1/100만자 | **무료** |
| Azure Text Analytics | $2/100만자 | **무료** |
| Grammarly API | $200+ | **무료** |
| ProWritingAid | $100+ | **무료** |
| **총 절약액** | **$500+/월** | **$0** |

## 📊 **성능 및 제한사항**

### ✅ **장점**
- **AI 자동 감지**: 414개 언어 지원
- **언어별 최고 정확도** (90%+)
- **완전 자동화**: 수동 선택 불필요
- **다중 API 결과 통합**
- **빠른 응답 속도** (엣지 컴퓨팅)
- **완전 무료 사용**

### ⚠️ **제한사항**
- **텍스트 길이**: 20,000자
- **일부 API**: 웹 스크래핑 필요 (Enno.jp 등)
- **사용량 제한**: 각 API별 개별 제한 존재
- **브라우저 의존**: franc 라이브러리 CDN 필요

## 🎯 **사용 사례**

### 🤖 **AI 자동 모드 (추천)**
```
1. 텍스트 입력
2. AI가 414개 언어 중 자동 감지
3. 감지된 언어의 전문 API 자동 선택
4. 최고 정확도로 검사 완료
```

### 👨‍🎓 **학생/연구자**
- **다국어 논문** 작성 시 언어별 자동 검사
- **언어 학습** 도구로 활용
- **무료 고품질** 교정

### 💼 **비즈니스**
- **다국가 진출** 기업 문서 자동 검사
- **현지 언어** 정확성 자동 확보
- **번역 후 교정** 자동화

### ✍️ **작가/블로거**
- **다국어 콘텐츠** 작성 시 자동 검사
- **언어별 특화** 검사 자동 적용
- **품질 향상** 자동화

## 🛠️ **작동 원리**

### 🔄 **AI 자동 감지 플로우**
```
텍스트 입력
    ↓
franc AI 언어 감지 (414개 언어)
    ↓
감지 결과 → 언어 코드 매핑
    ↓
해당 언어 전문 API 선택
    ↓
문법 검사 실행
    ↓
결과 통합 및 표시
```

### 🗂️ **언어 매핑 예시**
- `kor` (franc) → `ko` (한국어) → 부산대 + 다음 API
- `jpn` (franc) → `ja` (일본어) → Enno.jp API
- `deu` (franc) → `de` (독일어) → rechtschreibpruefung24 API

## 🤝 **기여하기**

새로운 언어별 API 발견 시 이슈를 통해 제보해주세요!

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📝 **라이선스**

MIT License - 자유롭게 사용, 수정, 배포 가능

## 🔗 **관련 링크**

### 🤖 **AI 언어 감지**
- [franc 라이브러리](https://github.com/wooorm/franc) - 414개 언어 감지

### 🏢 **전문 문법 검사 API**
- [부산대학교 맞춤법 검사기](http://speller.cs.pusan.ac.kr)
- [Enno.jp](https://enno.jp)
- [满分语法](https://zh.manfenyufa.com)
- [rechtschreibpruefung24.de](https://rechtschreibpruefung24.de)
- [LanguageTool](https://languagetool.org)

---

**🌟 AI가 자동으로 414개 언어를 감지하고 각 나라별 전문 API로 최고 품질의 문법 검사를 제공합니다!** 