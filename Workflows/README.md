# n8n Workflows

תיקייה זו מרכזת את חומרי ה-Workflows של n8n בפרויקט IQRAA — צילומי מסך ותיאור קצר לכל אחד מ-10 ה-Workflows הפעילים במערכת. לתיאור המלא (כולל קישורים) ראו [תיואר הוורקפלוז.docx](<תיואר הוורקפלוז.docx>). לתמונה כללית על מקום כל Workflow בתהליך העסקי ראו את [README הראשי](../README.md#-workflows).

## תוכן

### [IQRAA - New Lead](https://kholod-khadeja.app.n8n.cloud/workflow/qtTTVeTKQNcXIVWA)

Webhook שמקבל ליד חדש מדף הנחיתה ויוצר עבורו רשומה חדשה בטבלת Leads ב-Airtable, בסטטוס New Lead.

![IQRAA - New Lead](<IQRAA - New Lead.png>)

### [IQRAA - Email Agent ](https://kholod-khadeja.app.n8n.cloud/workflow/idtPLov1J8z18cOF)

וורקפלו אוטומטי לניהול מחזור החיים הראשוני של לידים ב־IQRAA. הוורקפלו מאתר לידים חדשים ב־Airtable, שולח מייל אישור הכולל קישור לקביעת פגישת ייעוץ וקישור לבוט המידע של IQRAA בטלגרם, ולאחר שליחה מוצלחת מעדכן את הסטטוס ל־Processing. בנוסף, הוא בודק תגובות של לידים ומעדכן ל־Meeting Booking כאשר קיימת בקשה ברורה לקביעת פגישה.

![IQRAA - Lead Lifecycle Agent](<IQRAA - Lead Lifecycle Agent.png>)

### [IQRAA - Updating Status to "BOOK MEETING" via email](https://kholod-khadeja.app.n8n.cloud/workflow/x4CFW0rWiCXzVwpO)

Webhook שמופעל בלחיצה על כפתור "קביעת פגישת ייעוץ" במייל שהתקבל, ומעדכן את סטטוס הליד ב-Airtable ל-Meeting Booking.

![IQRAA - Updating Status to BOOK MEETING via email](<IQRAA - Updating Status to BOOK MEETING via email.png>)

### [IQRAA - Invoice Validation & Preparation](https://kholod-khadeja.app.n8n.cloud/workflow/RRa3OH3hcHw4YPr7)

קולט חשבונית חדשה מהאפליקציה, מאתר את הלקוח, יוצר רשומת חשבונית, מאמת תקינות ומחשב מע"מ 18% — ומסמן כ-Validated או Invalid בהתאם.

![IQRAA - Invoice Validation & Preparation](<IQRAA - Invoice Validation & Preparation.png>)

### [IQRAA - Invoice File Creation](https://kholod-khadeja.app.n8n.cloud/workflow/E6y1TnTQMPNUhQWo)

הרצה מתוזמנת שמאתרת חשבוניות מאומתות (Validated) ללא קובץ, מפיקה עבורן מסמך ומעלה אותו ל-Google Drive.

![IQRAA - Invoice File Creation](<IQRAA - Invoice File Creation.png>)

### [IQRAA - Payments Webhook](https://kholod-khadeja.app.n8n.cloud/workflow/0VGrtCT1fmueYpgx)

מקבל בקשת תשלום מהאפליקציה, מאמת נתונים ומעדכן את סטטוס התשלום והחשבונית המתאימים ב-Airtable.

![IQRAA - Payments Webhook](<IQRAA - Payments Webhook.png>)

### [IQRAA - New Client + New Project](https://kholod-khadeja.app.n8n.cloud/workflow/i6ygYglievi9989i)

הרצה מתוזמנת שמאתרת ליד ששילם תשלום ראשון, יוצרת עבורו לקוח ופרויקט חדשים ב-Airtable (או פרויקט נוסף ללקוח קיים).

![IQRAA - New Client + New Project](<IQRAA - New Client+New Project.png>)

### [IQRAA - Admin Telegram Bot](https://t.me/Iqraa_AdminBot)

סוכן ניהולי ב-Telegram שעונה בזמן אמת על שאלות עסקיות של הבעלים, בעזרת שליפת נתונים מטבלאות Invoices, Projects ו-Leads.

![IQRAA - Admin Telegram Bot](<IQRAA - Admin Telegram Bot.png>)

### [IQRAA Workflow 3: Telegram Customer Service Agent](https://kholod-khadeja.app.n8n.cloud/workflow/JEmAyi3maq4Nf3Os)

סוכן שירות לקוחות ב-Telegram שמאתר מידע רשמי של IQRAA באמצעות RAG, שומר הקשר שיחה ומשיב ללקוח בשפתו.

![Telegram Customer Service Agent](<Telegram Customer Service Agent.png>)

### [IQRAA - RAG Ingestion Policies and catalog](https://kholod-khadeja.app.n8n.cloud/workflow/nOAu9zc5KiuWEFHn)

קולט קבצי ידע, יוצר עבורם Embeddings ושומר אותם ב-Qdrant, עבור בסיס הידע של סוכני ה-AI (Telegram Customer Service ו-Admin Bot).

![IQRAA - RAG Ingestion Policies and catalog](<IQRAA - RAG Ingestion Policies and catalog.png>)

---

📌 **הערה:** הקובץ `IQRAA - Email Agent.png` הוא צילום מסך מוקדם יותר של אותו Workflow המופיע למעלה תחת "IQRAA - Lead Lifecycle Agent" (זהה ב-n8n, כולל אותו מזהה Workflow) — לכן לא הוצג כפריט נפרד, כדי לשמור על 10 פריטים התואמים ל-10 ה-Workflows הפעילים בפועל.
