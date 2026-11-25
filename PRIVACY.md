# Privacy / حریم خصوصی

## Data handling
RTL PRO processes visible DOM text and eligible editable text locally to infer direction. The extension has no telemetry, analytics, account requirement, backend API, or automatic network transmission of page text in its current source. The popup's GitHub author link opens an external website only when clicked. Custom CSS is user-provided; its filter is not a complete network or security boundary.

## Local storage
`chrome.storage.local` stores defaults, theme and per-hostname settings (`site:<hostname>`), including CSS and selected DOM selectors. These settings are not synced by the extension. JSON export contains these settings, potentially revealing visited/configured hostnames and custom rules; do not share backups without reviewing them. Clearing extension data or uninstalling removes local settings, subject to browser behavior. Reset Site removes the selected hostname override.

## Permissions
- `storage`: retain settings locally.
- `scripting`: insert/remove custom CSS on the current document.
- `activeTab`: current-tab interaction.
- HTTP/HTTPS host access: automatic text direction on regular websites and access to the active tab URL. Content scripts run even on domains disabled in settings, but the transformation is disabled there.

No access to browser history, cookies or downloads APIs is requested. Broad host access is used by design; use only if you trust the source. Fonts are resolved from the local system, not fetched by the extension.

## فارسی
پردازش متن و ذخیره تنظیمات روی مرورگر انجام می‌شود. بکاپ JSON ممکن است نام دامنه‌ها و CSS اختصاصی را در بر داشته باشد؛ آن را بدون بررسی منتشر نکنید. دسترسی به صفحات وب عادی برای فعال‌سازی خودکار لازم است. فیلتر CSS ضمانت امنیت کامل نیست.

Contact: [mdazadeh](https://github.com/mdazadeh).
