# Реестр событий Saga-хореографии оформления заказа

| Этап                               | Тип события  | Название                   |
| ---------------------------------- | ------------ | -------------------------- |
| Создание заказа                    | domain       | OrderPlaced                |
| Резервирование товаров             | domain       | InventoryReserved          |
| Ошибка резервирования              | failure      | InventoryReservationFailed |
| Успешная оплата                    | domain       | PaymentSucceeded           |
| Ошибка оплаты                      | failure      | PaymentFailed              |
| Заявка на доставку создана         | domain       | DeliveryRequested          |
| Ошибка создания заявки на доставку | failure      | DeliveryRequestFailed      |
| Заказ передан в доставку           | domain       | DeliveryShipped            |
| Заказ доставлен                    | domain       | DeliveryCompleted          |
| Снятие резерва на складе           | compensation | InventoryReleased          |
| Возврат средств                    | compensation | PaymentRefunded            |
| Отмена заказа                      | compensation | OrderCancelled             |
