# Contoh CRUD
Berikut adalah contoh implementasi CRUD menggunakan JDBC : 

<div class="grid grid-cols-2 gap-y-10 gap-x-6 mt-8">
  <div class='flex-row'>
    

```java 
import java.sql.ResultSet;
public class Test {
  public static void main(String args[]) {
    Konektor conn = new Konektor();
    ResultSet hasil = conn.getData("SELECT * FROM `game`");

    try {
      while (select.next()) {
        System.out.println("ID : " + select.getInt(1));
        System.out.println("Name : " + select.getString(2));
        System.out.println("Genre : " + select.getString(3));
        System.out.println("Desc : " + select.getString(4));
        System.out.println();
      }
    } catch (Exception e) {
      System.out.println("Err");
    }
  }
}
```
  </div>
      
  <div class='flex-row'>
    <img src="/img/13_1.png">
  </div>
</div>