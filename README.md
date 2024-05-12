# אלגוריתמים על גרפים

## תיאור הפרוייקט
מימוש מחלקה לייצוג גרף בלתי מכוונים עם משקלים שליליים ואלגוריתמים הפועלים עליה. מיועד לכל מתכנת שרוצה להשתמש בגרפים בשביל לפתור בעיות.

## מימוש
מחלקת הגרף ממומשת בקובץ `Graph.cpp`, והצהרותיה מופיעות ב`Graph.hpp`. האלגוריתמים ממומשים בקובץ `Algorithms.cpp`, והצהרותם והצהרות פונקציות העזר שלהם מופיעות ב`Algorithms.hpp`. ישנו קובץ `Test.cpp` שמשתמש ב`doctest.h` בשביל להריץ טסטים בצורה אוטומטית. מחלקת `Graph` מאפשרת לטעון את הגרף בעזרת מטריצת שכנויות (`vector<vector<int>>`), בנוסף ניתן להפעיל את הפונקציה `getReversedGraph` שמחזירה את הגרף הנוכחי אבל הפוך בצלעות, ולא משנה את המקור. מחלקת `Algorithms` מאפשרת לגשת למגוון אלגוריתמים כגון: בדיקת קשירות לגרף, מציאת מסלול קל ביותר ממקור ליעד, מציאת מעגל, מציאת מעגל שלילי ומציאת חלוקת הגרף במידה והוא דו צדדי.

## דגשים על האלגוריתמים
1. כאשר מכניסים לפונ' `isConnected` גרף לא מכוון היא תחזיר true כאשר הוא קשיר. כאשר מכניסים אלייה גרף לא מכוון, היא תחזיר true רק כאשר הוא קשיר חזק.
2. כאשר מכניסים לפונ' `shortestPath` גרף עם מעגל שלילי היא זורקת שגיאה. זאת משום שאם יש מעגל שלילי בגרף, ישנם קודקודים שאין בינהם מסלול קצר ביותר.
3. כאשר מכניסים לפונ' `isContainsCycle` גרף לא מכוון, היא תחזיר true רק כאשר יש מעגל בגודל 3 ומעלה (לא טריוואלי). כאשר מכניסים לה גרף מכוון, היא תחזיר true גם אם יש מעגל בגודל 2 (bidirectional edge).
4. לפונ' `getNegativeCycle` יש התנהגות זהה ל`isContainsCycle` לגבי גדלי המעגלים.

## שם הכותב
נועם סיידה