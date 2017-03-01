# SoundWeather
Сценарий для "Majordomo" (majordomo.smartliving.ru) на основе данных из плагина получения информации о погоде openweather. Перед применением скрипта установить плагин "openweather"  и "API.AI". Код добавить либо в раздел "Сценарии" либо "Шаблоны поведения". Так же для успешного озвучивания у вас должен быть установлен плагин" Windows TTS" для ОС Windows. А в настройках Windows
<br>
Control Panel\Ease of Access\Speech Recognition\Text to Speech
<br>
необходимо выбрать русский синтез речи. Если у вас нерусская ОС, то вам необходимо установить дополнительно русский синтез речи, готовый не идёт по--умолчанию в нерусской ОС Windows.
<br>
Видео уроки по настройке плагинов и сценариев: https://www.youtube.com/playlist?list=PLYOYjvcehgZKWUxcNR25o37EdBGtX084E



#ExchangeRates
Сценарий для "Majordomo" (majordomo.smartliving.ru) Получает курсы валют покупки\продажи евро, доллар и рубль по отношению к гривне от API PrivatBank. А так же курсы валют евро, доллар по отношению к рублю Банка России.
Необходимо установить модуль: ExchangeRates<br>
https://github.com/Gelezako/MajorDomo-ExchangeRates<br>
И плагин API.AI<br>
После этого у объекта класса будет автоматически создано и инициализировано 6 свойств:
<br>
Rate.eurobuy<br>
Rate.eurosale<br>
Rate.usdbuy<br>
Rate.usdsale<br>
Rate.dollarrur<br>
Rate.eurorur<br>

Для того что бы данные обновлялись автоматически, необходимо в классе "Timer" открыть метод "onNewHour" и добавить в конец:
<br>
//проверяем изменение курса валют, вызываем сценарий<br>
runScript("ExchangeRates");
<br>
Название сценария должно совпадать с вызываемым в методе "onNewHour". Для хранения статистики изменения курса и построения графиков в класс "ExchangeRates" необходимо добавить свойства:<br>
eurobuy<br>
eurosale<br>
usdbuy<br>
usdsale<br>
Указать колличество дней для хранения значений курса.

Видео уроки по настройке плагинов и сценариев: https://www.youtube.com/playlist?list=PLYOYjvcehgZKWUxcNR25o37EdBGtX084E
