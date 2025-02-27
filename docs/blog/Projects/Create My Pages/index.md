---
language: kr
---

# 내 웹페이지 만들기

## Introduction

인터넷을 돌아다니다 보면 여러 블로그들을 만나볼 수 있다.  
최근에는 Github Pages로 블로그를 만들어서 쓰는 사람들을 종종 볼수 있다.  

나도 시도해보려고 했으나 사용법이 어려워 쉽지는 않았다. 
여러번의 시도 끝에 디자인이 마음에 들고 사용하기도 (비교적) 쉬운 템플릿을 찾았다.  

그 결과로 나온 것이 바로 이 웹페이지이다.  
이후 까먹을 것을 대비하면서, 혹시나 다른 사람들이 참고할 수 있도록, 어떻게 만들었는지 간단히 정리해놓고자 한다.

## MkDocs 와 Material
MkDocs 는 파이썬 패키지인데, 마크다운으로 작성된 파일을 쉽게 웹 페이지로 만들어주는 도구이다.

여기서 사용할 수 있는 테마는 여럿 있지만, 그 중 Material 이라는 테마가 세련되고 쓰기 좋은 것 같다.

> 관련 링크  
> [Documentaion](https://squidfunk.github.io/mkdocs-material/)  
> [Github](https://github.com/squidfunk/mkdocs-material)  
> [Guide YouTube Video](https://www.youtube.com/watch?v=xlABhbnNrfI)  

## Install and Initialize
일단 Python 3.12 가 설치되어 있어야 한다.  
그다음 pip 를 통해 mkdocs-material 을 설치한다.

파이썬 가상환경을 사용하는 것이 좋다.

```title="terminal"
# (선택) 파이썬 가상환경을 사용하는 경우
python -m venv .venv
.venv\Scripts\activate

# 설치
pip install mkdocs-material

# 현재 폴더에서 mkdocs 초기화
mkdocs new .
```

로컬에서 서버를 시작하려면,
```title="terminal"
mkdocs serve
```
이후 터미널에 뜨는 http://127.0.0.1:8000 으로 들어가면 로컬에서 페이지가 보인다.

## Configuration
처음 시작하는 경우, [Guide YouTube Video](https://www.youtube.com/watch?v=xlABhbnNrfI) 를 보면 도움이 된다.

mkdocs.yml 을 수정하여 기본 설정을 적용한다.

아래는 본인이 사용한 설정의 예시

```yaml title="mkdocs.yml"
site_name: {Page Title}
site_url: https://{user name}.github.io

theme:
  name: material
  custom_dir: overrides

  font:
    text: Nanum Gothic
    code: Consolas

  logo: assets/logo-512x512.png
  favicon: assets/favicon.ico

  features:
    - navigation.instant    # 페이지를 완전히 다시 로딩하지 않고 바뀌는 부분만 로딩딩
    - navigation.tabs       # 최상위 섹션이 헤더 아래의 메뉴 레이어로 렌더링됨
    - navigation.sections   # 최상위 섹션이 사이드바에서 그룹으로 렌더링됨;
                            # 참고: tab & sections 는 함께 활성화될 수 있음
    # - navigation.expand     # 사이드바는 기본적으로 모든 하위 섹션을 확장
    # - navigation.path       # 제목 위에 브레드크럼 탐색이 렌더링됨 > 스폰서만 가능함
    - navigation.indexes    # 섹션 인덱스 페이지가 활성화되어 문서를 섹션에 직접 첨부 가능. 개요 페이지를 제공하는 목적
    - toc.follow            # 사이드바가 자동으로 스크롤되어 항상 표시됨
    - navigation.top        # 맨 위로 돌아가기 버튼 활성화화

  palette:
    # Palette toggle for light mode
    - media: "(prefers-color-scheme: light)"
      scheme: default
      primary: blue
      accent: deep orange
      toggle:
        icon: material/brightness-7
        name: Switch to Dark mode

    # Palette toggle for dark mode
    - media: "(prefers-color-scheme: dark)"
      scheme: slate
      primary: deep orange
      accent: blue
      toggle:
        icon: material/brightness-4
        name: Switch to Light mode

markdown_extensions: 
  - attr_list
  - pymdownx.highlight:
      anchor_linenums: true
      line_spans: __span
      pygments_lang_class: true
  - pymdownx.inlinehilite
  - pymdownx.snippets
  - pymdownx.superfences:
      custom_fences:
        - name: mermaid
          class: mermaid
  - pymdownx.tabbed:
      alternate_style: true
  - admonition
  - pymdownx.details

plugins:
  - meta

copyright: Copyright &copy; 2025 {name}. All rights reserved.

```

> 참고: favicon 의 경우 본인은 [favicon.io](https://favicon.io/) 에서 생성했다.  
> favicon 이나 logo 같은 이미지는 /docs/assets/ 디렉토리 안에 들어간다.

## Generate Pages
페이지를 생성하는 것은 쉽다.
/docs/ 디렉토리 안에 파일을 생성하면 된다.  
docs 바로 안에 있는 index.md 가 루트 경로의 페이지가 된다.

안에 폴더를 만들고 그 안에 .md 페이지를 두면 하위 섹션 분류 하에서 페이지가 생성된다.  
페이지들은 같은 폴더 안에서 이름 순으로 나열된다.  
별도의 정렬 순서를 만들고 싶으면 파일이름 앞에 숫자를 붙여주면 된다.
파일 앞 숫자는 페이지 상에서 빠진채로 렌더링된다.
폴더의 숫자는 그대로 표시된다.