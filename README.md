# mdlp
1. Запустить .\stunnel\stunnel-msspi.exe (криптотуннель для ГОСТ 2012, прописаны порты 28080, 38080).
https://www.cryptopro.ru/products/other/stunnel-msspi

2. Запустить mdlp.exe (сервер подписи и отправки в МДЛП, порт 2222, должен работать там где стоит криптопро и сертификат подписи, иметь доступ до stunnel).
Написан на Golang, выполняет роль промежуточного сервера для учетного софта.

3. Открыть Тест_МДЛП_ГГГГ_ММ_ДД_ХХ.ert в любой конфе 1С 7.7, там есть комментарии в тексте (адрес и порт mdlp, пользователь, отпечаток сертификата подписи и т.д.).

Все собрано под Windows x86, можно сделать варианты под x86_64 и linux.
Обработка 1С 7.7 для работы требует WinHTTP 5.1 и MSXML (лучше поставить 6 для Windows старее Vista).
https://www.microsoft.com/ru-ru/download/details.aspx?id=6276
