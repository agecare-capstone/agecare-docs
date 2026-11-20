# Integración continua — AgeCare

El repositorio de la app ([CapstoneAgecare](https://github.com/agecare-capstone/CapstoneAgecare)) tiene dos flujos de GitHub Actions.

## 1. AgeCare CI/CD Pipeline (`.github/workflows/ci_cd_pipeline.yml`)

Se ejecuta en cada **pull request** y en cada **push** a `main`, `master` y `dev`.

| Job | Qué hace | Cuándo |
|---|---|---|
| Lint, Static Analysis & Unit Tests | `flutter pub get`, `flutter analyze --fatal-infos` (cero advertencias, DAC05-199) y `flutter test` | Siempre, también en cada pull request |
| Build Android APK | Compila el APK de release y lo publica como artefacto | Solo en push a las ramas principales |
| Build iOS | `flutter build ios --release --no-codesign` | Solo en push a las ramas principales |

Un pull request no se integra si el análisis estático o las pruebas fallan. Esto es parte de la Definition of Done.

## 2. Web (Vercel) (`.github/workflows/web-vercel.yml`)

En cada push a `main` compila la versión web y la publica en Vercel (**agecare-tan.vercel.app**). Así la versión navegable siempre corresponde al último código integrado y se puede mostrar en cada Sprint Review.

## Flujo de trabajo

1. Cada historia de Jira se trabaja en una rama con su clave (por ejemplo, `DAC05-18-flujo-critico-caidas`).
2. Se abre un pull request y otro integrante lo revisa (subtarea "PR: Peer review y merge a main" en Jira).
3. GitHub Actions ejecuta el análisis estático y las pruebas.
4. Con la aprobación y el pipeline en verde, se integra a `main` y se despliega la web.

El detalle de cada pull request está en `pull-requests.xlsx`.
