# Contoh CRUD
Berikut adalah contoh implementasi CRUD menggunakan JDBC : 

<div class="grid grid-cols-2 gap-y-10 gap-x-6 mt-8">
  <div class='flex-row'>
    <div class='text-xl'>

```java 
public class Test {
  public static void main(String args[]) {
    Konektor conn = new Konektor();
    conn.query("INSERT INTO `game` (`id`, `name`, `genre`, `description`) VALUES ('5', 'Huniepop', 'Puzzle', 'Candy crush + Anime');");
  }
}
```
        
  </div>
  <br>
  <div class='flex-row'>
    <img src="/img/11_1.png">
  </div>
  </div>
</div>