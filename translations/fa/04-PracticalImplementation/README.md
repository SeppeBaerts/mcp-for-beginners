<!--
CO_OP_TRANSLATOR_METADATA:
{
  "original_hash": "bb1ab5c924f58cf75ef1732d474f008a",
  "translation_date": "2025-07-14T17:05:02+00:00",
  "source_file": "04-PracticalImplementation/README.md",
  "language_code": "fa"
}
-->
# پیاده‌سازی عملی

پیاده‌سازی عملی جایی است که قدرت پروتکل مدل کانتکست (MCP) به صورت ملموس نمایان می‌شود. در حالی که درک نظریه و معماری پشت MCP اهمیت دارد، ارزش واقعی زمانی آشکار می‌شود که این مفاهیم را به کار ببرید تا راه‌حل‌هایی بسازید، آزمایش کنید و مستقر کنید که مشکلات دنیای واقعی را حل می‌کنند. این فصل فاصله بین دانش مفهومی و توسعه عملی را پر می‌کند و شما را در فرآیند زنده کردن برنامه‌های مبتنی بر MCP راهنمایی می‌کند.

چه در حال توسعه دستیارهای هوشمند باشید، چه در حال ادغام هوش مصنوعی در جریان‌های کاری کسب‌وکار، یا ساخت ابزارهای سفارشی برای پردازش داده‌ها، MCP پایه‌ای انعطاف‌پذیر فراهم می‌کند. طراحی مستقل از زبان آن و SDKهای رسمی برای زبان‌های برنامه‌نویسی محبوب، دسترسی به آن را برای طیف گسترده‌ای از توسعه‌دهندگان ممکن می‌سازد. با استفاده از این SDKها، می‌توانید به سرعت نمونه اولیه بسازید، تکرار کنید و راه‌حل‌های خود را در پلتفرم‌ها و محیط‌های مختلف مقیاس دهید.

در بخش‌های بعدی، مثال‌های عملی، کد نمونه و استراتژی‌های استقرار را خواهید دید که نشان می‌دهند چگونه MCP را در C#، Java، TypeScript، JavaScript و Python پیاده‌سازی کنید. همچنین یاد می‌گیرید چگونه سرورهای MCP خود را اشکال‌زدایی و تست کنید، APIها را مدیریت کنید و راه‌حل‌ها را با استفاده از Azure به فضای ابری منتقل کنید. این منابع عملی برای تسریع یادگیری شما طراحی شده‌اند و به شما کمک می‌کنند با اطمینان برنامه‌های MCP مقاوم و آماده تولید بسازید.

## مرور کلی

این درس بر جنبه‌های عملی پیاده‌سازی MCP در چند زبان برنامه‌نویسی تمرکز دارد. ما بررسی خواهیم کرد چگونه از SDKهای MCP در C#، Java، TypeScript، JavaScript و Python برای ساخت برنامه‌های مقاوم، اشکال‌زدایی و تست سرورهای MCP و ایجاد منابع، پرامپت‌ها و ابزارهای قابل استفاده مجدد استفاده کنیم.

## اهداف یادگیری

تا پایان این درس، قادر خواهید بود:
- راه‌حل‌های MCP را با استفاده از SDKهای رسمی در زبان‌های مختلف برنامه‌نویسی پیاده‌سازی کنید
- سرورهای MCP را به صورت سیستماتیک اشکال‌زدایی و تست کنید
- ویژگی‌های سرور (منابع، پرامپت‌ها و ابزارها) را ایجاد و استفاده کنید
- جریان‌های کاری مؤثر MCP را برای وظایف پیچیده طراحی کنید
- پیاده‌سازی‌های MCP را برای عملکرد و قابلیت اطمینان بهینه کنید

## منابع SDK رسمی

پروتکل مدل کانتکست SDKهای رسمی برای چند زبان ارائه می‌دهد:

- [C# SDK](https://github.com/modelcontextprotocol/csharp-sdk)
- [Java SDK](https://github.com/modelcontextprotocol/java-sdk) 
- [TypeScript SDK](https://github.com/modelcontextprotocol/typescript-sdk)
- [Python SDK](https://github.com/modelcontextprotocol/python-sdk)
- [Kotlin SDK](https://github.com/modelcontextprotocol/kotlin-sdk)

## کار با SDKهای MCP

این بخش مثال‌های عملی از پیاده‌سازی MCP در چند زبان برنامه‌نویسی را ارائه می‌دهد. می‌توانید کد نمونه را در دایرکتوری `samples` که بر اساس زبان سازماندهی شده است، پیدا کنید.

### نمونه‌های موجود

مخزن شامل [نمونه‌های پیاده‌سازی](../../../04-PracticalImplementation/samples) در زبان‌های زیر است:

- [C#](./samples/csharp/README.md)
- [Java](./samples/java/containerapp/README.md)
- [TypeScript](./samples/typescript/README.md)
- [JavaScript](./samples/javascript/README.md)
- [Python](./samples/python/README.md)

هر نمونه مفاهیم کلیدی MCP و الگوهای پیاده‌سازی مربوط به آن زبان و اکوسیستم را نشان می‌دهد.

## ویژگی‌های اصلی سرور

سرورهای MCP می‌توانند هر ترکیبی از این ویژگی‌ها را پیاده‌سازی کنند:

### منابع  
منابع زمینه و داده‌هایی را برای استفاده کاربر یا مدل هوش مصنوعی فراهم می‌کنند:
- مخازن اسناد
- پایگاه‌های دانش
- منابع داده ساختاریافته
- سیستم‌های فایل

### پرامپت‌ها  
پرامپت‌ها پیام‌ها و جریان‌های کاری قالب‌بندی شده برای کاربران هستند:
- قالب‌های مکالمه از پیش تعریف شده
- الگوهای تعامل هدایت شده
- ساختارهای گفتگوی تخصصی

### ابزارها  
ابزارها توابعی هستند که مدل هوش مصنوعی می‌تواند اجرا کند:
- ابزارهای پردازش داده
- ادغام با APIهای خارجی
- قابلیت‌های محاسباتی
- عملکرد جستجو

## نمونه پیاده‌سازی: C#

مخزن رسمی SDK زبان C# شامل چندین نمونه پیاده‌سازی است که جنبه‌های مختلف MCP را نشان می‌دهد:

- **کلاینت پایه MCP**: نمونه ساده‌ای که نشان می‌دهد چگونه یک کلاینت MCP بسازید و ابزارها را فراخوانی کنید
- **سرور پایه MCP**: پیاده‌سازی حداقلی سرور با ثبت ابزارهای پایه
- **سرور پیشرفته MCP**: سرور کامل با ثبت ابزار، احراز هویت و مدیریت خطا
- **ادغام با ASP.NET**: مثال‌هایی که ادغام با ASP.NET Core را نشان می‌دهند
- **الگوهای پیاده‌سازی ابزار**: الگوهای مختلف برای پیاده‌سازی ابزارها با سطوح پیچیدگی متفاوت

SDK زبان C# در حالت پیش‌نمایش است و APIها ممکن است تغییر کنند. ما این بلاگ را به‌روزرسانی خواهیم کرد تا با تکامل SDK هماهنگ باشد.

### ویژگی‌های کلیدی  
- [C# MCP Nuget ModelContextProtocol](https://www.nuget.org/packages/ModelContextProtocol)

- ساخت [اولین سرور MCP خود](https://devblogs.microsoft.com/dotnet/build-a-model-context-protocol-mcp-server-in-csharp/).

برای نمونه‌های کامل پیاده‌سازی C# به [مخزن نمونه‌های رسمی SDK C#](https://github.com/modelcontextprotocol/csharp-sdk) مراجعه کنید.

## نمونه پیاده‌سازی: Java

SDK زبان Java گزینه‌های قدرتمندی برای پیاده‌سازی MCP با ویژگی‌های سطح سازمانی ارائه می‌دهد.

### ویژگی‌های کلیدی

- ادغام با Spring Framework
- ایمنی نوع قوی
- پشتیبانی از برنامه‌نویسی واکنشی
- مدیریت جامع خطا

برای نمونه کامل پیاده‌سازی Java، به [نمونه Java](samples/java/containerapp/README.md) در دایرکتوری نمونه‌ها مراجعه کنید.

## نمونه پیاده‌سازی: JavaScript

SDK زبان JavaScript رویکردی سبک و انعطاف‌پذیر برای پیاده‌سازی MCP ارائه می‌دهد.

### ویژگی‌های کلیدی

- پشتیبانی از Node.js و مرورگر
- API مبتنی بر Promise
- ادغام آسان با Express و فریم‌ورک‌های دیگر
- پشتیبانی از WebSocket برای استریمینگ

برای نمونه کامل پیاده‌سازی JavaScript، به [نمونه JavaScript](samples/javascript/README.md) در دایرکتوری نمونه‌ها مراجعه کنید.

## نمونه پیاده‌سازی: Python

SDK زبان Python رویکردی پایتونیک برای پیاده‌سازی MCP با ادغام‌های عالی با فریم‌ورک‌های یادگیری ماشین ارائه می‌دهد.

### ویژگی‌های کلیدی

- پشتیبانی از async/await با asyncio
- ادغام با FastAPI
- ثبت ساده ابزارها
- ادغام بومی با کتابخانه‌های محبوب یادگیری ماشین

برای نمونه کامل پیاده‌سازی Python، به [نمونه Python](samples/python/README.md) در دایرکتوری نمونه‌ها مراجعه کنید.

## مدیریت API

Azure API Management پاسخ مناسبی برای چگونگی ایمن‌سازی سرورهای MCP است. ایده این است که یک نمونه Azure API Management را جلوی سرور MCP خود قرار دهید و اجازه دهید ویژگی‌هایی که احتمالاً نیاز دارید را مدیریت کند، مانند:

- محدودیت نرخ درخواست
- مدیریت توکن
- نظارت
- تعادل بار
- امنیت

### نمونه Azure

در اینجا یک نمونه Azure وجود دارد که دقیقاً همین کار را انجام می‌دهد، یعنی [ساخت یک سرور MCP و ایمن‌سازی آن با Azure API Management](https://github.com/Azure-Samples/remote-mcp-apim-functions-python).

نحوه انجام جریان احراز هویت را در تصویر زیر ببینید:

![APIM-MCP](https://github.com/Azure-Samples/remote-mcp-apim-functions-python/blob/main/mcp-client-authorization.gif?raw=true) 

در تصویر بالا، موارد زیر اتفاق می‌افتد:

- احراز هویت/مجوز با استفاده از Microsoft Entra انجام می‌شود.
- Azure API Management به عنوان دروازه عمل می‌کند و با استفاده از سیاست‌ها ترافیک را هدایت و مدیریت می‌کند.
- Azure Monitor تمام درخواست‌ها را برای تحلیل‌های بعدی ثبت می‌کند.

#### جریان احراز هویت

بیایید نگاهی دقیق‌تر به جریان احراز هویت بیندازیم:

![Sequence Diagram](https://github.com/Azure-Samples/remote-mcp-apim-functions-python/blob/main/infra/app/apim-oauth/diagrams/images/mcp-client-auth.png?raw=true)

#### مشخصات احراز هویت MCP

اطلاعات بیشتر درباره [مشخصات احراز هویت MCP](https://modelcontextprotocol.io/specification/2025-03-26/basic/authorization#2-10-third-party-authorization-flow) را بیاموزید.

## استقرار سرور MCP راه دور در Azure

بیایید ببینیم آیا می‌توانیم نمونه‌ای که قبلاً ذکر کردیم را مستقر کنیم:

1. مخزن را کلون کنید

    ```bash
    git clone https://github.com/Azure-Samples/remote-mcp-apim-functions-python.git
    cd remote-mcp-apim-functions-python
    ```

1. ارائه‌دهنده منابع `Microsoft.App` را ثبت کنید.
    * اگر از Azure CLI استفاده می‌کنید، دستور `az provider register --namespace Microsoft.App --wait` را اجرا کنید.
    * اگر از Azure PowerShell استفاده می‌کنید، دستور `Register-AzResourceProvider -ProviderNamespace Microsoft.App` را اجرا کنید. سپس پس از مدتی با دستور `(Get-AzResourceProvider -ProviderNamespace Microsoft.App).RegistrationState` بررسی کنید که ثبت کامل شده است یا خیر.

2. این دستور [azd](https://aka.ms/azd) را اجرا کنید تا سرویس مدیریت API، برنامه فانکشن (با کد) و سایر منابع مورد نیاز Azure را فراهم کند

    ```shell
    azd up
    ```

    این دستور باید تمام منابع ابری را در Azure مستقر کند.

### تست سرور خود با MCP Inspector

1. در یک **پنجره ترمینال جدید**، MCP Inspector را نصب و اجرا کنید

    ```shell
    npx @modelcontextprotocol/inspector
    ```

    باید رابطی مشابه زیر ببینید:

    ![Connect to Node inspector](/03-GettingStarted/01-first-server/assets/connect.png) 

1. با نگه داشتن کلید CTRL روی URL نمایش داده شده توسط برنامه کلیک کنید تا وب‌اپ MCP Inspector بارگذاری شود (مثلاً http://127.0.0.1:6274/#resources)
1. نوع انتقال را روی `SSE` تنظیم کنید
1. URL را به نقطه انتهایی SSE مدیریت API خود که پس از اجرای `azd up` نمایش داده شده است، تنظیم کنید و **اتصال** را بزنید:

    ```shell
    https://<apim-servicename-from-azd-output>.azure-api.net/mcp/sse
    ```

5. **لیست ابزارها**. روی یک ابزار کلیک کنید و **اجرای ابزار** را انتخاب کنید.

اگر همه مراحل به درستی انجام شده باشد، اکنون باید به سرور MCP متصل شده باشید و توانسته باشید یک ابزار را فراخوانی کنید.

## سرورهای MCP برای Azure

[Remote-mcp-functions](https://github.com/Azure-Samples/remote-mcp-functions-dotnet): این مجموعه مخازن قالب شروع سریع برای ساخت و استقرار سرورهای سفارشی MCP راه دور با استفاده از Azure Functions با Python، C# .NET یا Node/TypeScript است.

نمونه‌ها راه‌حلی کامل ارائه می‌دهند که به توسعه‌دهندگان امکان می‌دهد:

- ساخت و اجرای محلی: توسعه و اشکال‌زدایی سرور MCP روی ماشین محلی
- استقرار در Azure: استقرار آسان در فضای ابری با یک دستور ساده azd up
- اتصال از کلاینت‌ها: اتصال به سرور MCP از کلاینت‌های مختلف از جمله حالت عامل Copilot در VS Code و ابزار MCP Inspector

### ویژگی‌های کلیدی:

- امنیت از ابتدا: سرور MCP با استفاده از کلیدها و HTTPS ایمن شده است
- گزینه‌های احراز هویت: پشتیبانی از OAuth با احراز هویت داخلی و/یا مدیریت API
- جداسازی شبکه: امکان جداسازی شبکه با استفاده از شبکه‌های مجازی Azure (VNET)
- معماری بدون سرور: استفاده از Azure Functions برای اجرای مقیاس‌پذیر و رویدادمحور
- توسعه محلی: پشتیبانی کامل از توسعه و اشکال‌زدایی محلی
- استقرار ساده: فرآیند استقرار ساده و روان به Azure

مخزن شامل تمام فایل‌های پیکربندی لازم، کد منبع و تعاریف زیرساخت است تا به سرعت با پیاده‌سازی سرور MCP آماده تولید شروع کنید.

- [Azure Remote MCP Functions Python](https://github.com/Azure-Samples/remote-mcp-functions-python) - نمونه پیاده‌سازی MCP با استفاده از Azure Functions و Python

- [Azure Remote MCP Functions .NET](https://github.com/Azure-Samples/remote-mcp-functions-dotnet) - نمونه پیاده‌سازی MCP با استفاده از Azure Functions و C# .NET

- [Azure Remote MCP Functions Node/Typescript](https://github.com/Azure-Samples/remote-mcp-functions-typescript) - نمونه پیاده‌سازی MCP با استفاده از Azure Functions و Node/TypeScript.

## نکات کلیدی

- SDKهای MCP ابزارهای مخصوص زبان برای پیاده‌سازی راه‌حل‌های مقاوم MCP فراهم می‌کنند
- فرآیند اشکال‌زدایی و تست برای برنامه‌های قابل اعتماد MCP حیاتی است
- قالب‌های پرامپت قابل استفاده مجدد تعاملات یکنواخت با هوش مصنوعی را ممکن می‌سازند
- جریان‌های کاری خوب طراحی شده می‌توانند وظایف پیچیده را با استفاده از چند ابزار هماهنگ کنند
- پیاده‌سازی راه‌حل‌های MCP نیازمند توجه به امنیت، عملکرد و مدیریت خطا است

## تمرین

یک جریان کاری عملی MCP طراحی کنید که یک مشکل واقعی در حوزه کاری شما را حل کند:

1. ۳ تا ۴ ابزار که برای حل این مشکل مفید هستند را شناسایی کنید
2. نمودار جریان کاری ایجاد کنید که نشان دهد این ابزارها چگونه با هم تعامل دارند
3. نسخه پایه‌ای از یکی از ابزارها را با زبان مورد علاقه خود پیاده‌سازی کنید
4. قالب پرامپتی بسازید که به مدل کمک کند ابزار شما را به طور مؤثر استفاده کند

## منابع اضافی


---

بعدی: [موضوعات پیشرفته](../05-AdvancedTopics/README.md)

**سلب مسئولیت**:  
این سند با استفاده از سرویس ترجمه هوش مصنوعی [Co-op Translator](https://github.com/Azure/co-op-translator) ترجمه شده است. در حالی که ما در تلاش برای دقت هستیم، لطفاً توجه داشته باشید که ترجمه‌های خودکار ممکن است حاوی خطاها یا نواقصی باشند. سند اصلی به زبان بومی خود باید به عنوان منبع معتبر در نظر گرفته شود. برای اطلاعات حیاتی، ترجمه حرفه‌ای انسانی توصیه می‌شود. ما مسئول هیچ گونه سوءتفاهم یا تفسیر نادرستی که از استفاده این ترجمه ناشی شود، نیستیم.