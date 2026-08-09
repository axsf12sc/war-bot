# جنگ جهانی ریات — ربات تلگرام

## اجرای محلی
```bash
pip install -r requirements.txt
cp .env.example .env
# BOT_TOKEN و ADMIN_IDS را در .env پر کن
python bot.py
```

## استقرار روی Railway
1. پروژه را به GitHub بفرست
2. در Railway از GitHub Deploy کن
3. Variables:
   - `BOT_TOKEN` = توکن ربات
   - `ADMIN_IDS` = آیدی عددی ادمین (مثلاً 7767354117)
   - `CHANNEL_ID` = آیدی کانال گزارش یا 0
   - `DB_PATH` = `/data/game.db` (اگر Volume ساختی)
4. یک Volume بساز و روی `/data` mount کن تا دیتابیس پاک نشود
5. Start Command: `python bot.py`

## دستورات
- `/start` شروع / ثبت کشور
- `/menu` منوی اصلی
- `/admin` پنل ادمین
- در گروه: `/attack` `/profile` `/rank`
