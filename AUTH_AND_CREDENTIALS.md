# ServiceTitan Connector — Auth & Credentials Standard

**Compliance:** AUTH_AND_CREDENTIALS_STANDARD.md (B1–B10)

## Схема аутентификации
- **Метод:** OAuth 2.0 Client Credentials + App Key (ST-App-Key header)
- **Хранение:** Секреты сохраняются изолированно в хранилище секретов платформы Imperal.
- **Валидация:** При сохранении ключа выполняется тестовый запрос `GET /jpm/v2/job-types`.
- **Отключение:** Удаление локальных ключей без воздействия на аккаунт вендора.
