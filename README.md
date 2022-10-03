# cwiczenia_16_SqLite

# Przykładowy kod

## Czytanie z bazy

```java
public ArrayList<HashMap<String, String>> GetOrders(){
        SQLiteDatabase db = this.getReadableDatabase();
        ArrayList<HashMap<String, String>> orderList = new ArrayList<>();

        String query = "SELECT name, price, date, suite, mouse, keyboard, camera FROM "+ DbContract.FeedEntry.TABLE_NAME;
        Log.d("HWA","qwery="+query);
        Cursor cursor = db.rawQuery(query,null);

        while (cursor.moveToNext()){
            HashMap<String,String> order = new HashMap<>();
            //
          String dat = cursor.getString(cursor.getColumnIndex(DbContract.FeedEntry.COLUMN_DATE));
 ```
