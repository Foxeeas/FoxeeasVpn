# EvanesciaVpn

<img src="icon.png" alt="EvanesciaVpn" width="128"/>

Кастомный VPN-клиент для Android на основе NekoBox (SagerNet).

## Возможности

- Поддержка всех популярных протоколов: VMess, VLESS, Shadowsocks, Trojan, Hysteria, WireGuard и другие
- Собственные градиентные обои (6 тем)
- Смена цветовой схемы (20+ цветов в Settings → Theme)
- Работа через WebSocket поверх HTTPS (обход DPI)
- Совместимость с конфигами NekoBox / SagerNet / sing-box
- Цветовая схема: #c70b33 (основной) / #eebdbc (акцент)

## Установка

1. Скачай APK из [Releases](https://github.com/Foxeeas/FoxeeasVpn/releases)
2. Установи на Android 8.0+
3. Импортируй свою конфигурацию (VMess-ссылку или JSON)

## Сборка

APK собирается из декомпилированного NekoBox с помощью APKTool:

```bash
java -jar apktool.jar b decompile -o EvanesciaVpn.apk
zipalign -p 4 EvanesciaVpn_unsigned.apk EvanesciaVpn-aligned.apk
apksigner sign --ks your.keystore --out EvanesciaVpn.apk EvanesciaVpn-aligned.apk
```

## Ссылки

- Оригинальный NekoBox: https://github.com/MatsuriDayo/NekoBoxForAndroid
