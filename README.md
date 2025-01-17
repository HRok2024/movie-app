# 영화 검색 및 선호작 관리 웹 애플리케이션

이 프로젝트는 영화 검색과 선호작을 관리하는 웹 애플리케이션입니다. 사용자는 영화 제목을 검색하고, 선호하는 영화를 추가하거나 삭제할 수 있습니다. 이 웹 애플리케이션은 **OMDb API**를 사용하여 영화 정보를 가져옵니다. `Vite`로 생성된 리액트 웹앱이며, **Netlify**에 배포되었습니다.

## 🚀 기능

- **영화 검색**: 사용자가 입력한 영화 제목으로 OMDb API를 통해 영화를 검색합니다.
- **선호작 등록/삭제**: 사용자가 마음에 드는 영화를 선호작 목록에 추가하고, 목록에서 제거할 수 있습니다.
- **로컬 스토리지**: 사용자가 추가한 선호작은 로컬 스토리지에 저장되어 페이지 새로고침 후에도 유지됩니다.
- **반응형 디자인**: 모바일 및 데스크탑 화면에서 모두 원활하게 작동합니다.

## 🌐 배포

이 프로젝트는 **Netlify**에 배포되었습니다. 아래 링크에서 사이트를 확인할 수 있습니다.

- [movie-app 링크](https://sparkling-malasada-c8ff3d.netlify.app/)

## 🧑‍💻 기술 스택

- **React**: 사용자 인터페이스 구성
- **Vite**: 빠른 빌드 도구
- **OMDb API**: 영화 데이터를 제공
- **Bootstrap**: 스타일링
- **React-Indiana-Drag-Scroll**: 수평 스크롤 기능 구현

## 🎥 주요 컴포넌트

- **App.jsx**: 영화 검색 및 선호작 관리의 전체적인 로직을 담당합니다. OMDb API로 영화 데이터를 가져오고, 선호작 목록을 로컬 스토리지에 저장합니다.
- **MovieList.jsx**: 영화 목록을 출력하며, 각 영화에 선호작 추가/삭제 기능을 제공합니다.
- **MovieListHeading.jsx**: 영화 목록의 제목을 출력합니다.
- **SearchBox.jsx**: 사용자가 영화 제목을 검색할 수 있는 입력 필드를 제공합니다.

## ⚠️ 빌드 오류 및 해결 방법

### Mixed Content 문제 해결

Mixed Content는 HTTPS 사이트에서 HTTP 사이트를 요청할 때 발생하는 보안 문제입니다.
이 문제를 해결하기 위해, **index.html** 파일에 `Content-Security-Policy` 메타 태그를 추가했습니다.

#### 해결 방법

1. **index.html** 파일에 `Content-Security-Policy` 메타 태그를 추가, HTTP 요청을 자동으로 HTTPS로 업그레이드하도록 설정했습니다.

<meta
  http-equiv="Content-Security-Policy"
  content="upgrade-insecure-requests"
/>
