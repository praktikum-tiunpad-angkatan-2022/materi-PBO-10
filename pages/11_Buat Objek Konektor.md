# Buat objek Konektor

<div class="grid grid-cols-2 gap-y-10 gap-x-6 mt-8">
<div class='flex-row'>

Contoh implementasi objek konektor : 

```java
import java.sql.*;
public class Konektor{
    private String driver = "com.mysql.cj.jdbc.Driver";
    private String db = "jdbc:mysql://localhost/NAMA_DATABASE"; 
    // Bila ada yang instance mysqlnya pindah port, tuliskan menjadi 'localhost:PORT/NAMA_DATABASE'
    private String user = "root"; // Bila username berbeda, ganti baris ini
    private String password = ""; // Bila instance MySQL memiliki password, isi baris ini
    private Connection conn = null;
    private Statement state = null;
    private ResultSet rs = null;

    ...
}

        
```

</div>
<div class='flex-row'>

```java 
    // Constructor 
    public void Konektor() {

        try{
            Class.forName(driver);
        } catch(Exception e){
            System.out.println("Driver Error"); 
        } 

        try{
            conn = (Connection)DriverManager.getConnection(db, user, password);
            state = (Statement) conn.createStatement();
        } catch(Exception e){
            System.out.println("Connection Error");
        }

        System.out.println("Database Connected");
    }
```

</div>
</div>
