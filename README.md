Оборудование:
- Материнская плата AsRock z490m itx/ac
- Процессор Intel i7 10700
- Видеокарта AMD Radeon RX 6600 XT 8 ГБ
- Монитор с разрешением 2560x1080

ПО:
- OpenCore 0.8.8
- Monterey 12.6.2 (не тестировалось на Ventura)

Работает:
- WiFi (встроенный в материнскую плату)
- Bluetooth
- USB порты (задние и передние)
- Сон
- iCloud, AppStore
- iMessage, Facetime
- Звук по 3.5 и HDMI
- DRM

Версия 1.1
- Фикс iServices

Версия 1.2
- Обновил OpenCore до версии 0.6.7
- Обновил Lilu, WhateverGreen, VirtualSMC, SMCSuperIO и SMCProcessor до актуальных на 31 марта 2021 версий
- Добавил графический интерфейс в загрузчик, скрыл лишние элементы меню (recovery, reset nvram, etc)

Версия 1.3
- Обновил AirportItlwm до версии 1.3. Скорость по Wi-Fi больше не режется до 40 мбит/с.

Версия 1.4
- Удалил Usbinjectall
- Добавил Usbmap
- Установил xhciportlimit = false для совместимости с Big Sur 11.3 и выше

Версия 1.5
- Обновил OpenCore до версии 0.7.2
- Обновил AirportItlwm, AppleALC, Lilu, NVMeFix, SMCProcessor, SMCSuperIO, VirtualSMC, WhateverGreen до актуальных на 13 августа 2021 версий

Версия 1.6
- Удалил FakePCIID и FakePCIID_Intel_HDMI_Audio.kext из-за конфликтов с Monterey
- Обновил AirportItlwm, AppleALC, Lilu, WhateverGreen, VirtualSMC, SMCSuperIO и SMCProcessor до актуальных на 7 мая 2022 версий
- Добавил IntelBluetoothFirmware для фикса Bluetooth (неудачно)
- Конфиг переписан с нуля для избежания проблем с обновлением до Monterey

Версия 1.6.1
- Добавил BlueToolFixup, теперь Bluetooth работает

Версия 1.6.2
- Добавил FakePCIID и FakePCIID_Intel_HDMI_Audio для восстановления звука из репозитория
https://github.com/mbarbierato/OS-X-Fake-PCI-ID/releases/tag/v1.3.16

Версия 1.7
- Обновил OpenCore до версии 0.8.8
- Добавил поддержку внешней видеокарты RX 6600XT
- Обновил AppleALC, Lilu, NVMeFix, WhateverGreen, VirtualSMC, SMCSuperIO и SMCProcessor до актуальных на 3 января 2023 версий

Версия 1.7.1
- Удалил FakePCIID и FakePCIID_Intel_HDMI_Audio.kext, аудио теперь работает нативно
- Удалил NullEthernet
- Устранил проблемы с DRM, для активации необходимо выполнить команду в терминале

``defaults write com.apple.AppleGVA gvaForceAMDKE -boolean yes``

SMBIOS удален, нужно сгенерировать серийные номера

Конфигурация выложена в ознакомительных/образовательных целях. Я не гарантирую работоспособность на оборудовании, отличном от моего.
