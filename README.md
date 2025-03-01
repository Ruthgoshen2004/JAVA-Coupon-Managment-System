# מערכת ניהול קופונים

## סקירה כללית

פרויקט זה הוא **מערכת ניהול קופונים** שנכתבה ב-**Java Spring Boot**. המערכת נועדה לאפשר לחברות להשיק קופונים ולקוחות לרכוש אותם. הפרויקט עושה שימוש בטכנולוגיות מרכזיות כמו **JWT (JSON Web Tokens)** לאימות משתמשים, **DAO (Data Access Object)** לגישה לבסיסי נתונים, והמערכת בנויה לפי עקרונות **OOP (תכנות מונחה עצמים)**.

המרכיבים העיקריים של המערכת הם:
- **Controller**: מטפל בבקשות HTTP ומחזיר תגובות.
- **Entity**: מגדיר את האובייקטים העסקיים המרכזיים (כגון `Coupon`, `Company`, `Customer`).
- **Service**: מכיל את הלוגיקה העסקית של המערכת.
- **Repository**: מבצע גישה לבסיסי נתונים ומספק גישה לאובייקטים.
- **JWT**: מנהל את האימות והנפקת הטוקנים.
- **Login**: מטפל בפונקציות של כניסת משתמש ואימות טוקן.

---

## תכונות

- **יצירת קופונים**: חברות יכולות ליצור קופונים חדשים ולשייך אותם לחשבונות שלהן.
- **רכישת קופונים**: לקוחות יכולים לעיין בקופונים זמינים ולרכוש אותם.
- **אימות**: האימות של המשתמשים נעשה באמצעות JWT, כך שהגישה למערכת מוגבלת למשתמשים מורשים בלבד.
- **תמיכה ב multi-threads**: המערכת תומכת בעיבוד בקשות בצורה יעילה בעזרת multi-threads.
- **שכבת DAO**: המערכת משתמשת בדפוס DAO (Data Access Object) כדי לאנדקס את לוגיקת הגישה לנתונים מתוך הלוגיקה העסקית.

---

## טכנולוגיות בשימוש

- **Java Spring Boot**: ליצירת ה-API ה-RESTful של השרת.
- **JWT**: לאימות והסמכת משתמשים בצורה מאובטחת.
- **DAO**: לאיבוד הגישה לנתונים בצורה מנותקת מהלוגיקה העסקית.
- **OOP**: תכנות מונחה עצמים לשמירה על קוד מסודר ותחזוקתי.
- **MySQL/PostgreSQL**: בסיס נתונים רלציוני לשמירת מידע על קופונים, חברות ולקוחות.

---

## מבנה הפרויקט

הפרויקט בנוי בתיקיות הבאות:

- `controller/`: מכילה את בקרי ה-REST שמטפלים בבקשות HTTP.
- `entity/`: מכילה את מחלקות ה-Entity המייצגות את האובייקטים העסקיים (כגון Coupon, Company, Customer).
- `service/`: מכילה את מחלקות השירות שמבצעות את הלוגיקה העסקית.
- `repository/`: מכילה את הממשקים של המאגר לגישה לבסיס הנתונים.
- `JWT/`: מכילה את המחלקות האחראיות על ניהול אימות ה-JWT.
- `Login/`: אחראית על טיפול בפונקציות ההתחברות ואימות טוקן.

