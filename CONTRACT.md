# Контракт платёжного шлюза

## RefundResult

| Поле | Тип | С версии | Примечание |
|---|---|---|---|
| charge_id | str | 2.0 | идентификатор платежа |
| amount | Decimal | 2.4 (в плане) | сумма возврата, точная до копеек |
| status | str | 2.0 | ok / pending / declined |
| idempotency_key | str | 2.4 (в плане) | ключ операции возврата |

`amount` в 2.3 объявлен как `float` — временное расхождение с C1,
перевод на `Decimal` запланирован на 2.4.

## История контракта

- 2.3 — добавлен `GatewayClientV2.charge`; V1 помечен устаревшим.
- 2.2 — `Charge.merchant_id`.
- 2.1 — `RefundResult.status`.
