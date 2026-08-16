# سایت Borhan Trading — راهنمای فارسی

## ساختار
- `index.html` و بقیه‌ی فایل‌های ریشه → نسخه‌ی آلمانی (زبان اصلی)
- `en/` → نسخه‌ی انگلیسی
- `css/style.css` → استایل مشترک همه‌ی صفحات
- `CNAME` → برای اتصال دامنه‌ی www.borhan.at به GitHub Pages (دست نزنید)

## قبل از انتشار — موارد TODO
1. `kontakt.html` و `en/contact.html` → شماره تلفن واقعی
2. `impressum.html` → شماره UID و GISA/Firmenbuch (طبق قانون اتریش الزامی است)

## افزودن دسته‌ی محصول جدید
1. در `css/style.css` یک متغیر رنگ جدید در `:root` اضافه کنید
2. در صفحه‌ی produkte.html (و en/products.html) یک بلوک
   `<article class="cat" style="border-top-color: var(--رنگ);">` کپی کنید
3. در `.spectrum` (نوار رنگی بالای سایت) هم می‌توانید یک `<span>` جدید اضافه کنید

## انتشار روی GitHub Pages
1. ریپازیتوری Public بسازید و همه‌ی این فایل‌ها را در ریشه آپلود کنید
2. Settings → Pages → Branch: main، پوشه: / (root)
3. Custom domain: www.borhan.at → بعد Enforce HTTPS را تیک بزنید
4. در DNS دامنه (پنل internex):
   - CNAME برای www → username.github.io
   - چهار رکورد A برای @ → 185.199.108.153 / 185.199.109.153 / 185.199.110.153 / 185.199.111.153
   - به رکوردهای MX دست نزنید (ایمیل قطع می‌شود!)
