# Abiim App 📱

اپلیکیشن اندروید برای سایت [abiim.com](https://abiim.com)

---

## ساختار پروژه

```
abiim_app/
├── lib/
│   └── main.dart              # کد اصلی اپ
├── android/
│   └── app/src/main/
│       └── AndroidManifest.xml
├── .github/
│   └── workflows/
│       └── build-apk.yml      # ساخت خودکار APK
├── pubspec.yaml
└── README.md
```

## ویژگی‌ها

- نمایش سایت abiim.com داخل اپ
- پشتیبانی از دکمه بازگشت
- نوار پیشرفت هنگام بارگذاری
- صفحه خطا هنگام قطع اینترنت
- پشتیبانی از حالت افقی و عمودی

---

## گرفتن APK با GitHub Actions

### مرحله ۱ — ساخت ریپو در GitHub

1. به [github.com](https://github.com) برو
2. روی **New repository** کلیک کن
3. نام بذار: `abiim-app`
4. روی **Create repository** کلیک کن

### مرحله ۲ — آپلود فایل‌ها

```bash
git init
git add .
git commit -m "Initial commit"
git branch -M main
git remote add origin https://github.com/USERNAME/abiim-app.git
git push -u origin main
```

> **USERNAME** رو با نام کاربری GitHub خودت عوض کن

### مرحله ۳ — دانلود APK

1. بعد از push، بری به ریپوی GitHub
2. روی تب **Actions** کلیک کن
3. روی آخرین workflow کلیک کن
4. صبر کن تا تموم بشه (حدود ۵-۱۰ دقیقه)
5. پایین صفحه قسمت **Artifacts** → روی `abiim-release-apk` کلیک کن

---

## اجرا روی کامپیوتر (پیش‌نمایش)

### نیاز داری به:
- [Flutter SDK](https://flutter.dev/docs/get-started/install)
- [Android Studio](https://developer.android.com/studio) یا VS Code

### دستورات:

```bash
# نصب dependencies
flutter pub get

# اجرا روی شبیه‌ساز یا موبایل متصل
flutter run

# ساخت APK به صورت دستی
flutter build apk --release
```

APK ساخته شده در این مسیر قرار می‌گیره:
```
build/app/outputs/flutter-apk/app-release.apk
```
