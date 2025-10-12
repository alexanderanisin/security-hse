## US-001 - Регистрация пользователя

- **Роль-Цель-Ценность:** Как гость, я хочу зарегистрировать учётную запись, чтобы получить доступ к функционалу приложения.
- **Кратко:** Регистрация с подтверждением e-mail.
- **API/Endpoints:** `POST /api/auth/register`, `POST /api/auth/verify-email`, `POST /ext-gateway/api-provider/captcha`
- **NFR hooks:** `Security-AuthN`, `InputValidation`, `RateLimiting`, `API-Contract/Errors`, `Privacy/PII`

## US-002 - Загрузка аватара/файла

- **Роль-Цель-Ценность:** Как пользователь, я хочу загрузить аватар, чтобы персонализировать профиль.
- **Кратко:** Проверка типа/размера, хранение под UUID.
- **API/Endpoints:** `POST /api/files/avatar`
- **NFR hooks:** `InputValidation`, `RateLimiting`, `Storage-Quotas`, `API-Contract/Errors`

## US-003 - Поиск по каталогу

- **Роль-Цель-Ценность:** Как пользователь, я хочу искать по полю/тегам, чтобы находить релевантные результаты.
- **Кратко:** Полнотекст/префикс, ограничение запроса.
- **API/Endpoints:** `GET /api/search?q=`
- **NFR hooks:** `Performance`, `RateLimiting`, `Timeouts/Retry`, `Observability/Logging`
