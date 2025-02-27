# Leo's Pages generated by Material for MkDocs

## Abount Material for MkDocs
[Documentaion](https://squidfunk.github.io/mkdocs-material/)  
[Guide YouTube Video](https://www.youtube.com/watch?v=xlABhbnNrfI)  


## Getting Start
### PIP install
- create venv
  ```
  python -m venv .venv
  .venv\Scripts\activate
  ```

- install mkdocs-material
  ```
  pip install mkdocs-material

  # 선택사항
  pip install "mkdocs-material[imaging]"
  ```
### Working mkdocs
- Init mkdocs
  ```
  mkdocs new .
  ```

- Edit mkdocs.yml
  ```
  site_name: Leo's Pages
  site_url: https://jeongleo.github.io
  theme:
    name: material
  ```

- Serve mkdocs
  ```
  mkdocs serve
  ```

- 각각의 설정파일로 빌드 or 실행
```
mkdocs build -f mkdocs.en.yml
mkdocs build -f mkdocs.ko.yml
mkdocs build -f mkdocs.blog.yml

mkdocs serve -f mkdocs.en.yml
mkdocs serve -f mkdocs.ko.yml
mkdocs serve -f mkdocs.blog.yml

```

- github pages deply
```
mkdocs gh-deploy --force
```

## 참고; 다국어 지원
[MkDocs i18n plugin](https://ultrabug.github.io/mkdocs-static-i18n/)
