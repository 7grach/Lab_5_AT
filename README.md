# Лабораторная работа №5

Четыре автотеста SauceDemo на Python, pytest и Playwright. Проверяются форма входа, успешная авторизация, добавление рюкзака в корзину и сообщение при неверном пароле.

## Запуск на macOS и Linux

```sh
python3.12 -m venv .venv
. .venv/bin/activate
python -m pip install -r requirements.txt
python -m playwright install chromium
python -m pytest -v
```

В Windows используйте `py -3.12 -m venv .venv` и интерпретатор `.venv\Scripts\python.exe` для остальных команд. Для запуска нужен доступ к SauceDemo. Параметры `--headed --slowmo 700` позволяют видеть работу тестов, а `--screenshot on` сохраняет снимки страниц в `test-results`.

## GitHub Actions

Workflow `.github/workflows/tests.yml` запускает тесты на Ubuntu и Python 3.12 при push, pull request и ручном запуске через вкладку Actions.
