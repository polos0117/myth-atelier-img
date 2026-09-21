# myth-atelier-img

`myth-atelier` 의 그림 저장소다. 코드는 [myth-atelier](https://github.com/polos0117/myth-atelier) 에 있다.
그림을 코드와 같이 두면 `.git` 이 수백 MB 가 되므로 처음부터 나눈다. Pages 를 켜 두어야
`https://polos0117.github.io/myth-atelier-img/img/…` 로 읽힌다.

## 자리

```
img/<카드>_<화풍>_f.webp           액션 한 장. 1024×1536 (2:3)
img/<카드>_<화풍>_f_awaken.webp    각성 (선택). 같은 구도에서 무기가 빛난다
img/<카드>_<화풍>_f_casualN.webp   일상컷 (선택)
img/thumb/<같은 이름>              목록용. 워크플로가 만든다
```

파일 이름이 곧 등록 정보다. 카드 이름은 코드 저장소 `data/card.json` 의 `name` 그대로.
폼도 시트도 없다 — 캐릭터당 그림 한 장이 규격이다.

## 올린 뒤에 할 일

없다. `썸네일` 워크플로가 `img/*.webp` 푸시를 보고 `img/thumb/` 를 만들어 되커밋하고,
이 저장소의 Actions 비밀 `CODE_REPO_TOKEN` 이 있으면 코드 저장소의 `그림 등록` 을 깨운다.
토큰 만드는 법은 pkm-atelier-img README 와 같다: Fine-grained token, 저장소 `myth-atelier`
하나, Contents Read and write, 이 저장소 Secrets 에 `CODE_REPO_TOKEN`.
