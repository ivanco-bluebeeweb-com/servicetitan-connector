# ServiceTitan Connector — Connector Discovery

**Category:** C47. Construction & Field Service Management  
**Vendor:** ServiceTitan  
**Official Website:** https://www.servicetitan.com

## 1. Официальный API
- **Базовый URL API:** `https://api.servicetitan.io`
- **Поддерживаемая модель авторизации:** OAuth 2.0 Client Credentials + App Key (ST-App-Key header)

## 2. Архитектура сущностей
- Ключевые ресурсы платформы ServiceTitan:
  - наряд-заказы (/jpm/v2/jobs)
  - вызовы/назначения (/dispatch/v2/appointments)
  - клиенты (/crm/v2/customers)
  - счета (/accounting/v2/invoices)

## 3. Требования к отказоустойчивости и безопасности
- Соблюдение вендорных лимитов запросов (Rate Limiting) с экспоненциальной задержкой.
- Строгая валидация Pydantic-схем на входе и выходе каждого запроса.
- Тестовая точка проверки подключения: `GET /jpm/v2/job-types`.
