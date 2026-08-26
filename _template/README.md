# 새 플러그인 뼈대

이 폴더를 **복사해 이름을 바꾸면** 새 플러그인이 된다.

1. `_template` 폴더를 복사하고 이름을 바꾼다 (예: `team-hr`)
2. `.claude-plugin/plugin.json`의 `"여기에~"를 채운다 — `name`은 **폴더 이름과 같게** 한다
3. `skills/_skill-template`을 복사해 스킬 이름으로 바꾸고 `SKILL.md`를 채운다
4. 저장소 최상위 `.claude-plugin/marketplace.json`의 `plugins` 배열에 항목을 더한다

```json
    {
      "name": "team-hr",
      "source": "./team-hr",
      "description": "인사팀에서 반복되는 문서 업무 묶음"
    }
```

4번을 빠뜨리면 폴더는 저장소에 있어도 설치 목록에 뜨지 않는다.

`_`로 시작하는 이 폴더는 `marketplace.json`에 등록돼 있지 않다. 그래서 뼈대인 채로 남아 있어도 아무에게도 설치되지 않는다.
