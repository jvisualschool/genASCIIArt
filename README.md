# genASCIIArt 🎨

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![HTML5](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/HTML)
[![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?logo=javascript&logoColor=black)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
[![TailwindCSS](https://img.shields.io/badge/Tailwind_CSS-38B2AC?logo=tailwind-css&logoColor=white)](https://tailwindcss.com/)

> 🌟 이미지를 멋진 아스키 아트로 변환하는 웹 애플리케이션

### 📸 스크린샷

<table>
  <tr>
    <td align="center">
      <img src="screenshot/screen1.png" width="400" alt="라이트 모드 스크린샷">
      <br><b>라이트 모드</b>
    </td>
    <td align="center">
      <img src="screenshot/screen2.png" width="400" alt="다크 모드 스크린샷">
      <br><b>다크 모드 & 파티 효과</b>
    </td>
  </tr>
</table>

## ✨ 주요 기능

### 🖼️ 이미지 변환
- **드래그 & 드롭** 인터페이스로 쉬운 파일 업로드
- **다양한 이미지 포맷** 지원 (JPG, PNG, GIF, WebP)
- **실시간 변환** 및 미리보기

### 🎛️ 커스터마이징 옵션
- **출력 크기 조정**: 20-200 문자 폭
- **다양한 문자 세트**:
  - 표준 ( .:-=+*#%@)
  - 상세 ( .`^":;Il!i><~+_-?...)
  - 블록 ( ░▒▓█)
  - 숫자 ( 123456789)
  - 커스텀 (사용자 정의)
- **색상 반전** 모드

### 🎭 8가지 애니메이션 효과
1. **위→아래 순차**: 클래식한 타이핑 효과
2. **좌→우 순차**: 좌에서 우로 한 열씩
3. **위아래→중앙**: 양쪽에서 중앙으로 만남
4. **좌우→중앙**: 좌우에서 중앙으로 만남
5. **바깥→안쪽 나선**: 달팽이 모양으로 안쪽으로
6. **안쪽→바깥 나선**: 중앙에서 바깥쪽으로
7. **랜덤**: 무작위 순서로 나타남
8. **파티 🎉**: 컬러풀한 반짝반짝 효과

### 🎨 UI/UX 특징
- **다크/라이트 모드** 토글
- **반응형 디자인** (모바일 친화적)
- **따뜻한 오렌지 톤** 라이트 모드
- **부드러운 전환** 애니메이션

### 💾 결과 활용
- **클립보드 복사** 원클릭
- **텍스트 파일 다운로드** (.txt)
- **SNS 공유** 준비된 텍스트 아트

## 🚀 사용법

### 1. 이미지 업로드
- 드래그 앤 드롭으로 이미지 끌어다 놓기
- 또는 클릭해서 파일 선택

### 2. 설정 조정
- 출력 너비 슬라이더로 크기 조정
- 원하는 문자 세트 선택
- 필요시 색상 반전 옵션 활성화

### 3. 변환 및 감상
- 'ASCII 아트 생성' 버튼 클릭
- 애니메이션 스타일 선택
- '재생' 버튼으로 멋진 효과 감상

### 4. 결과 활용
- '복사' 버튼으로 클립보드에 복사
- '다운로드' 버튼으로 텍스트 파일 저장

## 🛠️ 기술 스택

- **HTML5** - 구조 및 마크업
- **CSS3** - 스타일링 및 애니메이션
- **Vanilla JavaScript** - 핵심 로직
- **Tailwind CSS** - 유틸리티 기반 스타일링
- **Font Awesome** - 아이콘
- **Canvas API** - 이미지 처리
- **FileReader API** - 파일 읽기
- **Clipboard API** - 복사 기능

## 📁 프로젝트 구조

```
genASCIIArt/
├── index.html          # 메인 애플리케이션 파일 (모든 코드 포함)
├── README.md           # 프로젝트 설명서
└── screenshot/         # 스크린샷 모음
    ├── screen1.png     # 라이트 모드 스크린샷
    └── screen2.png     # 다크 모드 & 파티 효과 스크린샷
```

## 🎯 알고리즘 원리

### 밝기 계산
```javascript
brightness = (R * 0.299 + G * 0.587 + B * 0.114) / 255
```

### 문자 매핑
```javascript
charIndex = Math.floor(brightness * (charSet.length - 1))
asciiChar = charSet[charIndex]
```

### 컬러 그룹핑 (파티 모드)
- 인접한 비공백 문자들을 연결된 컴포넌트로 그룹화
- 각 그룹별로 고유한 색상 할당
- 시간에 따른 동적 색상 변경

## 🌐 배포

### 온라인 버전
**DEMO**: [https://ai.jvisualschool.com/genASCIIArt/](https://ai.jvisualschool.com/genASCIIArt/)

### 로컬 실행
1. 파일 다운로드
2. `index.html`을 웹 브라우저에서 열기
3. 별도의 서버 설정 불필요

## 🔒 보안

- ✅ **XSS 방지**: 사용자 입력 검증 및 안전한 DOM 조작
- ✅ **클라이언트 사이드**: 서버로 데이터 전송 없음
- ✅ **파일 타입 검증**: 이미지 파일만 허용
- ✅ **로컬 처리**: 모든 변환이 브라우저에서 수행

## 🎨 사용 예시

### 텍스트 아트 활용
- **GitHub README** 파일 장식
- **소셜 미디어** 게시물
- **터미널** 시작 화면
- **코드 주석** 아트
- **이메일 시그니처**

## 🤝 기여하기

1. 프로젝트 Fork
2. 새 브랜치 생성 (`git checkout -b feature/amazing-feature`)
3. 변경사항 커밋 (`git commit -m 'Add some amazing feature'`)
4. 브랜치에 Push (`git push origin feature/amazing-feature`)
5. Pull Request 생성



## 📄 라이선스

이 프로젝트는 MIT 라이선스 하에 배포됩니다. 자세한 내용은 [LICENSE](LICENSE) 파일을 참조하세요.

## 👨‍💻 개발자

**정진호** - 작가, 디자이너, 일러스트레이터, 취미개발자, 교수

> 💡 **개발자 노트**: 이 프로젝트는 단순한 이미지 처리를 넘어서, 디지털과 아날로그의 경계를 탐험하는 창조적 도구입니다. 교육자이자 아티스트로서, 기술과 예술의 융합을 통해 새로운 표현의 가능성을 열어갑니다.

---

⭐ **이 프로젝트가 마음에 드셨다면 Star를 눌러주세요!**

📧 **문의사항이나 제안사항이 있으시면 언제든 연락해주세요.**

🎉 **Happy ASCII Art Making!**
