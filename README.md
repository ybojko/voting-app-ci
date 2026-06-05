# voting-app-ci

Централізовані reusable GitHub Actions pipelines для всіх сервісів voting app.

## Пайплайни

| Workflow | Опис |
|----------|------|
| `build.yml` | Збірка multi-arch образу + пуш в registry |
| `deploy.yml` | Оновлення image.tag у GitOps-репо |

## Використання

Сервісні репо викликають через:
```yaml
uses: ybojko/voting-app-ci/.github/workflows/build.yml@main
```

## Переваги

- Одне місце правди для CI
- Зміна в CI підхоплюється всіма сервісами
- Нуль копіпасти між репо
