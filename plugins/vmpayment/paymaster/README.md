**Инструкция по установке и настройке модуля  Joomla v3.3+VirtueMart 3.0.3 и выше**

**Установка:**
1. В Joomla Administrator -> Расширения -> Менеджер расширений 
ваш_сайт.ру/administrator/index.php?option=com_installer 

1.1	Установить скачанный  архив с сайта Paymaster.

1.2	 В способах оплаты добавить способ и выбрать Paymaster.
ваш_сайт.ру/administrator/index.php?option=com_virtuemart&view=paymentmethod

1.3	 Нажимаете кнопку создать и создаете новый метод оплаты.

В названии — вводите PayMaster

Псевдоним — paymaster

Способ оплаты — выбираете Paymaster


В разделе VirtueMart выбираете способы оплаты
ваш_сайт.ру/administrator/index.php?option=com_virtuemart&view=paymentmethod

Выбираете созданный метод PayMaster

И переходите во вкладку конфигурация.
 
Введите в поля Merchant ID и Secret Key свои данные из  личного кабинета PayMaster. А затем выберете метод проверке хеша (среди md5, sha1 или sha256). 
Также необходимо установить ставку НДС (если только необходимо); 

Пропишите обратные вызовы по примеру:

Payment  notification POST запрос: 

http://ВАШСАЙТ.ru/index.php?option=com_virtuemart&view=pluginresponse&task=pluginresponsereceived&action=paymaster_result

Success redirect POST запрос:

http://ВАШСАЙТ.ru/index.php?option=com_virtuemart&view=pluginresponse&task=pluginresponsereceived&action=paymaster_success

Failure redirect POST запрос:

http://ВАШСАЙТ.ru/index.php?option=com_virtuemart&view=pluginresponse&task=pluginUserPaymentCancel

Но можно обратные вызовы и не прописывать, а просто отметить опцию в интерфейсе личного кабинета мерчанта Paymaster что можно устанавливать подмененные url. 

1.	Для работы с онлайн-кассой: правильно устанавливаем ставку НДС для продуктов и отдельно для доставки, если этого не сделать ставка НДС будет по умолчанию (без НДС). 
2.	Правильно прописываем способ валидации HASH они должны совпадать с тем методом что у вас выбран в интерфейсе мерчанта личного кабинета PayMaster.
3.	Выбираем правильно логотип системы оплаты. 
4.	Включаем модуль Paymaster