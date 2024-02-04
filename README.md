# OpenCart 4 payment module

[Русская версия](#Модуль-оплаты-opencart-4)

## Installation

* Backup your webstore and database
* Download from [Github releases page](https://github.com/begateway/opencart-4-payment-module/releases) the latest module archive `opencart-4-begateway-payment-extension.ocmod.zip`
* Upload `opencart-4-begateway-payment-extension.ocmod.zip` to your OpenCart or ocStore installation using the administrator menu _Extensions_ -> _Installer_
* Activate the module in payment extensions (_Extensions_ -> _Extentsions_ -> _Payments_)
* Configure the module settings:
  * Shop Id
  * Shop secret key
  * Shop public key
  * Payment page domain
  * Order statuses for successfuly processed payment and for failed one
  * Enabled the module
  * And optionally setup sort order id if you want to move the payment
    option higher level in payment method list

## Notes

Tested and developed with OpenCart v.4.0.2.3

## Troubleshooting

If the cart is not cleared after the user is redirected back to the shop following successful payment, try changing the `Session SameSite Cookie` option to `Lax`.

## Testing

You can use the following information to adjust the payment method in test mode:

  * __Shop ID:__ 361
  * __Shop Key:__ b8647b68898b084b836474ed8d61ffe117c9a01168d867f24953b776ddcb134d
  * __Payment page domain:__ checkout.begateway.com

Use the following test card to make successful test payment:

  * Card number: 4200000000000000
  * Name on card: JOHN DOE
  * Card expiry date: 01/30
  * CVC: 123

Use the following test card to make failed test payment:

  * Card number: 4005550000000019
  * Name on card: JOHN DOE
  * Card expiry date: 01/30
  * CVC: 123

## Contributing

Issue pull requests or send feature requests or open [a new issue]( https://github.com/begateway/opencart-4-payment-module/issues/new)

## Development

After installing OpenCart, execute the following command in the `db` container:

        mysql -uroot -proot opencart < /install_begateway_extension.sql

This command creates database records necessary to install the extension for development purposes.

# Модуль оплаты OpenCart 4

[English version](#opencart-4-payment-module)

## Установка

* Создайте резервную копию вашего магазина и базы данных
* Скачайте со страницы [Github релизов](https://github.com/begateway/opencart-4-payment-module/releases) архив модуля `opencart-4-begateway-payment-extension.ocmod.zip` 
* Загрузите `opencart-4-begateway-payment-extension.ocmod.zip` в ваш OpenCart или ocStore с помощью меню адиминистратора _Расширения_ -> _Установщик_
* Активируйте модуль BeGateway в модулях оплаты (_Расширения_ -> _Расширения_ -> _Оплата_)
* Задайте в настройках модуля BeGateway:
  * Id магазина
  * Ключ магазина
  * Публичный ключ магазина
  * Домен страницы оплаты
  * Статусы заказа в случае успешной и не успешной оплаты
  * Включите модуль
  * Опционально задайте идентификатор модуля для сортировки его в списке способов оплаты. Меньшее значение подымает модуль в верх списка

## Примечания

Разработано и протестировано с OpenCart v.4.0.2.3

## Устранение неполадок

Если корзина не очищается после того, как пользователь возвращается в магазин после успешной оплаты, попробуйте изменить параметр `Сессионные куки` на `Слабый`.

## Тестирование

Вы можете использовать следующие данные, чтобы настроить способ оплаты в тестовом режиме

  * __Идентификационный номер магазина:__ 361
  * __Секретный ключ магазина:__ b8647b68898b084b836474ed8d61ffe117c9a01168d867f24953b776ddcb134d
  * __Домен страницы оплаты:__ checkout.begateway.com
  * __Режим работы:__ Тестовый

Используйте следующие данные карты для успешного тестового платежа:

  * Номер карты: 4200000000000000
  * Имя на карте: JOHN DOE
  * Месяц срока действия карты: 01/30
  * CVC: 123

Используйте следующие данные карты для неуспешного тестового платежа:

  * Номер карты: 4005550000000019
  * Имя на карте: JOHN DOE
  * Месяц срока действия карты: 01/30
  * CVC: 123

## Нашли ошибку или у вас есть предложение по улучшению модуля?

Создайте [запрос](https://github.com/begateway/opencart-4-payment-module/issues/new)

## Разработка

После установки OpenCart выполните следующую команду в контейнере `db`:

        mysql -uroot -proot opencart < /install_begateway_extension.sql
        
Эта команда создает записи в базе данных, необходимые для установки расширения в целях разработки.
