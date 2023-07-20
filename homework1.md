Homework 1 ADB.

- Скачиваем архив с ADB файлами и распаковываем.
- Подключаемся к телефону кабелем с включеной отладкой по USB в режиме разработчика.
- Заходим через PowerShell из папки распакованного архива с ADB.

1. Отобразить подключенный девайс в консоли.  
`./adb devices`
2. Вывести адрес приложения todolist в системе Android.  
`Перетягиваем скаченое приложение в окно PowerSell`
3. Установить .apk файл приложения todolist на телефон с компьютера через  ADB.  
`./adb install D:\TodoList.apk`
4. Сделать скриншот запущенного приложения todolist и сразу скопировать на компьютер в одной команде.  
`./adb shell screencap /sdcard/screen.png | .\adb pull /sdcard/screen.png`
5. Вывести в консоль логи приложения todolist.  
`./adb logcat -d | findstr com.android.todolist`
6. Скопировать логи приложения todolist на компьютер.  
`./adb logcat -d | findstr com.android.todolist > todolist_adb_logs.log`
7. Удалить приложение todolist с телефона через ADB.  
`./adb uninstall com.android.todolist`
