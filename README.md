# Смены Аллы

Компактное PWA-приложение для iPhone. Читает смены из Google Calendar с разрешением только на чтение.

## Публикация GitHub Pages
Откройте Settings → Pages → Build and deployment → Deploy from a branch → main → /(root) → Save.

Адрес после публикации: https://rostislav-swimmer.github.io/alla-shifts/

## Google Calendar OAuth
1. Откройте Google Cloud Console, создайте проект и включите Google Calendar API.
2. Настройте Google Auth Platform / OAuth consent screen. Если статус Testing, добавьте свой Gmail как test user.
3. Создайте OAuth Client ID типа Web application.
4. В Authorized JavaScript origins добавьте **https://rostislav-swimmer.github.io** (без пути).
5. Откройте опубликованное приложение → ⚙️ → введите Client ID → Сохранить → Подключить Google.
6. Разрешите чтение Google Calendar. Выберите нужный календарь и настройте фильтр «Алла».

Не добавляйте в публичный репозиторий токены, Client Secret или события личного календаря. Client ID сам по себе не секрет. OAuth access token хранится только в памяти вкладки, повторная авторизация может потребоваться после закрытия приложения. Обновление каждые пять минут работает, пока приложение открыто.

Приложение ещё не проверено на физическом iPhone. Сначала настройте GitHub Pages и OAuth, затем протестируйте чтение календаря.
