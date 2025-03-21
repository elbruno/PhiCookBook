# به افزونه VS Code خود خوش آمدید

## محتوای پوشه

* این پوشه شامل تمام فایل‌های لازم برای افزونه شما است.
* `package.json` - این فایل مانیفست است که در آن افزونه و دستورات خود را تعریف می‌کنید.
  * افزونه نمونه یک دستور را ثبت کرده و عنوان و نام دستور آن را تعریف می‌کند. با این اطلاعات، VS Code می‌تواند دستور را در پنل دستورات نمایش دهد. هنوز نیازی به بارگذاری افزونه نیست.
* `src/extension.ts` - این فایل اصلی است که در آن پیاده‌سازی دستور خود را ارائه می‌دهید.
  * این فایل یک تابع به نام `activate` را صادر می‌کند که اولین بار هنگام فعال شدن افزونه شما فراخوانی می‌شود (در این مورد با اجرای دستور). داخل تابع `activate` ما `registerCommand` را فراخوانی می‌کنیم.
  * تابعی که پیاده‌سازی دستور را شامل می‌شود به عنوان پارامتر دوم به `registerCommand` ارسال می‌شود.

## راه‌اندازی

* افزونه‌های پیشنهادی را نصب کنید (amodio.tsl-problem-matcher, ms-vscode.extension-test-runner, و dbaeumer.vscode-eslint).

## سریع شروع به کار کنید

* دکمه `F5` را فشار دهید تا یک پنجره جدید با افزونه شما بارگذاری شود.
* دستور خود را از پنل دستورات اجرا کنید با فشردن (`Ctrl+Shift+P` یا `Cmd+Shift+P` در مک) و تایپ `Hello World`.
* نقاط توقف (breakpoints) را در کد خود داخل `src/extension.ts` تنظیم کنید تا افزونه خود را دیباگ کنید.
* خروجی افزونه خود را در کنسول دیباگ پیدا کنید.

## ایجاد تغییرات

* می‌توانید پس از تغییر کد در `src/extension.ts`، افزونه را دوباره از نوار ابزار دیباگ اجرا کنید.
* همچنین می‌توانید پنجره VS Code را با افزونه خود بازنشانی کنید (`Ctrl+R` یا `Cmd+R` در مک) تا تغییرات شما بارگذاری شود.

## کاوش در API

* می‌توانید مجموعه کامل API ما را با باز کردن فایل `node_modules/@types/vscode/index.d.ts` مشاهده کنید.

## اجرای تست‌ها

* [Extension Test Runner](https://marketplace.visualstudio.com/items?itemName=ms-vscode.extension-test-runner) را نصب کنید.
* وظیفه "watch" را از طریق دستور **Tasks: Run Task** اجرا کنید. اطمینان حاصل کنید که این در حال اجرا است، در غیر این صورت تست‌ها ممکن است شناسایی نشوند.
* نمای تست را از نوار فعالیت باز کنید و روی دکمه "Run Test" کلیک کنید، یا از کلید میانبر `Ctrl/Cmd + ; A` استفاده کنید.
* خروجی نتایج تست را در نمای نتایج تست مشاهده کنید.
* تغییراتی در `src/test/extension.test.ts` ایجاد کنید یا فایل‌های تست جدیدی داخل پوشه `test` ایجاد کنید.
  * اجراکننده تست ارائه شده فقط فایل‌هایی را که با الگوی نام `**.test.ts` مطابقت دارند در نظر می‌گیرد.
  * می‌توانید پوشه‌هایی داخل پوشه `test` ایجاد کنید تا تست‌های خود را به هر شکلی که می‌خواهید سازماندهی کنید.

## پیشروی بیشتر

* اندازه افزونه را کاهش دهید و زمان راه‌اندازی را با [بسته‌بندی افزونه خود](https://code.visualstudio.com/api/working-with-extensions/bundling-extension) بهبود دهید.
* [افزونه خود را منتشر کنید](https://code.visualstudio.com/api/working-with-extensions/publishing-extension) در بازار افزونه‌های VS Code.
* با تنظیم [یکپارچگی مداوم](https://code.visualstudio.com/api/working-with-extensions/continuous-integration) ساخت‌ها را خودکار کنید.

**سلب مسئولیت**:  
این سند با استفاده از خدمات ترجمه ماشینی مبتنی بر هوش مصنوعی ترجمه شده است. در حالی که ما برای دقت تلاش می‌کنیم، لطفاً توجه داشته باشید که ترجمه‌های خودکار ممکن است شامل اشتباهات یا نواقصی باشند. سند اصلی به زبان اصلی آن باید به عنوان منبع معتبر در نظر گرفته شود. برای اطلاعات حساس یا حیاتی، ترجمه حرفه‌ای انسانی توصیه می‌شود. ما هیچ مسئولیتی در قبال سوء تفاهم‌ها یا تفسیرهای نادرست ناشی از استفاده از این ترجمه نداریم.