# Разработка лидара без движущихся частей

[CopterHack-2022](copterhack2022.md), команда **SolidEye**.

## Информация о команде

Состав команды:

* Галкин Иван, @feanor_gg, ivan.galkin5066@gmail.com, программист.

## Описание проекта

Была реализована идея создания лидара без движущихся элементов для использования его через платформу ROS. Лидар позволяет получать панорамную карту препятствий в плоскости с поперечным углом от 5 до 27 градусов. Это позволит БПЛА ориентироваться в замкнутом пространстве, строить карты помещений.

Лидар представляет из себя печатную плату круглой формы, содержащую микроконтроллер STM32F411CE и 18 датчиков VL53L1CB от компании STMicroelectronics.

Соединение с Raspberry на борту коптера обеспечивается посредством кабеля.

### Идея проекта

Идея заключается в создании устройства, представляющего собой лидар, не содержащий движущихся элементов и обладающий низким энергопотреблением.

Такое устройство может быть использовано в негабаритных коптерах в течение длительного времени, так как, во-первых, не вносит вклад в геометрию движения (в отличие от лидаров с вращающимися элементами), во-вторых, отличается низким энергопотреблением (средний ток потребления прототипа составляет 200 мА), в-третьих, масса устройства также невелика (44.3 грамма - масса прототипа).

### Планируемые результаты

В качестве результата я планирую представить чертежи и исходные коды устройства. Предполагаемые характеристики лидара:

* Дальность действия: 4 метра.
* Частота работы: 10+ Гц.
* Вертикальное FoV: до 27 градусов.
* Горизонтальное FoV: 360 градусов.
* Формат получаемых данных: Совместим с rviz (массив расстояний).
* Ток потребления: не превышает 500 мА.
* Масса устройства: не превышает 50 грамм.

### Использование платформы "Клевер"

Платформа "Клевер" будет использоваться для тестирования разработанного устройства. Оно будет подключаться к Raspberry на борту коптера, что позволит продемонстрировать различные применения устройства, например - построение карты помещения или перемещение с повышенной точностью по известной локации.

### Дополнительная информация по желанию участников

Я - Галкин Иван, ученик 11 класса ГБОУ "Лицея "Вторая школа". Занимаюсь робототехникой в течение 7 лет. Имею опыт работы над проектами в Сириусе ("Большие Вызовы" 2021), занимаюсь разработкой ПО для проекта, получившего грант на акселераторе SberZ в 2021 году.

Проект был представлен на конкурсах "Инженеры будущего" и "Большие вызовы" в 2021 году, в обоих конкурсах получен диплом победителя.

Имеется техническое описание проекта, далее привожу ссылку на Google Drive: https://drive.google.com/drive/folders/1ElGUSOP4B7EvlwnueIqEFiv8VGPkNK_Y?usp=sharing.