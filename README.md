# PapaJohns


Сидели мы с ребятами в общежитии, гладили пустые животы. Пришла идея заказать пиццу. Беглый поиск показал нам одноименную пиццерию. Основной ее особенностью является 
возможность использовать промо-коды для получения дополнительных ништяков. 

После детального изучения сайта, стало понятно, что технологически он весьма грустный.
Благодаря средствам разработчика в браузере, стало понятно, что ввод промо-кода происходит путем отправки POST-запроса, в ответ на который 
прилетает JSON ответ о том, что не комильфо вводить неправильный промокод, либо производится переход на страницу активированного промокода.

Был произведена серия гугл-запросов для выяснения стандартной маски автосгенерированного промокода. Промокод состоит из 7 символов алфавита и цифр.


В итоге был написан простенький генератор строки (class Brutforce).

В классе getAnswer реализован механизм POST-запроса.

В классе main реализована обработка ответа и сбор итоговых промокодов. 

Так как есть два возможных ответа: JSON и непосредственно веб-страница, то был организован блок try catch, где в блоке try происходила попытка обработать
ответ библиотекой парсинга. В случае, если ответ представляет из себя веб-страницу, то парсинг выдает exeption, следовательно это наш случай.

Программа писалась на коленке в голодном состоянии и не является удовлетворительным продуктом. 
Результаты данной программы не были использованы в корыстных целях. Данный проект был произведен в рамках самообучения и только с этой целью.
