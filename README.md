# python



### **סיכום SQL – שאילתות נפוצות**
הטבלה בתמונה מציגה דוגמאות לשימוש ב-SQL לניהול מסדי נתונים.  
להלן הסבר על כל שאילתה וכיצד משתמשים בה:

---

## **📌 שליפת נתונים (`SELECT`)**
שאילתה לשליפת נתונים ממסד הנתונים:
```sql
SELECT * FROM Customers;
```
🔹 **מציגה את כל הנתונים מהטבלה `Customers`**.

#### **שליפת נתונים עם תנאי (`WHERE`)**
```sql
SELECT * FROM Orders WHERE customer_id=4;
```
🔹 **מציגה רק את ההזמנות שבהן `customer_id = 4`**.

```sql
SELECT * FROM Shippings WHERE customer=1 OR customer=2;
```
🔹 **מציגה את כל המשלוחים של `customer=1` או `customer=2`**.

---

## **📌 הכנסת נתונים (`INSERT`)**
כדי להוסיף רשומה חדשה לטבלה:
```sql
INSERT INTO Orders VALUES (10, 'Monitor', 100, 3);
```
🔹 **מוסיף רשומה חדשה לטבלת `Orders` עם:**
- `order_id = 10`
- `item = 'Monitor'`
- `amount = 100`
- `customer_id = 3`

```sql
INSERT INTO Shippings VALUES (6, 'Delivered', 3);
```
🔹 **מוסיף רשומה חדשה לטבלת `Shippings` עם:**
- `shipping_id = 6`
- `status = 'Delivered'`
- `customer_id = 3`

---

## **📌 מחיקת נתונים (`DELETE`)**
```sql
DELETE FROM Orders WHERE customer_id=4;
```
🔹 **מוחק את כל ההזמנות של `customer_id = 4`**.

```sql
DELETE FROM Customers WHERE age<30;
```
🔹 **מוחק את כל הלקוחות שהגיל שלהם קטן מ-30**.

⚠ **זהירות:** בלי `WHERE` השאילתה תמחק את כל הנתונים בטבלה!

---

## **📌 עדכון נתונים (`UPDATE`)**
כדי לעדכן רשומות קיימות בטבלה:
```sql
UPDATE Orders SET amount = 100;
```
🔹 **מעדכן את כל ההזמנות ושם את הכמות (`amount`) על 100**.

```sql
UPDATE Customers SET first_name='Noam' WHERE first_name='Robert';
```
🔹 **מעדכן את שם המשתמשים מ-'Robert' ל-'Noam'` בטבלת `Customers`**.

---

## **📌 טיפים חשובים**
1. **תמיד להשתמש ב-`WHERE` עם `UPDATE` או `DELETE`** כדי לא לעדכן/למחוק את כל הטבלה בטעות.
2. **`SELECT * FROM table_name;`** – הדרך הכי פשוטה לראות את כל הנתונים בטבלה.
3. **`INSERT` מוסיף שורות חדשות, `UPDATE` משנה נתונים קיימים, `DELETE` מוחק נתונים**.

---

### **🔹 סיכום קצר**
| פעולה | פקודה |
|------|------|
| **שליפת כל הנתונים** | `SELECT * FROM Customers;` |
| **שליפת נתונים עם תנאי** | `SELECT * FROM Orders WHERE customer_id=4;` |
| **הוספת רשומה לטבלה** | `INSERT INTO Orders VALUES (10, 'Monitor', 100, 3);` |
| **מחיקת נתונים** | `DELETE FROM Orders WHERE customer_id=4;` |
| **עדכון נתונים** | `UPDATE Orders SET amount = 100;` |

אם את רוצה הרחבה על משהו מסוים או דוגמאות נוספות, תגידי לי! 😊
