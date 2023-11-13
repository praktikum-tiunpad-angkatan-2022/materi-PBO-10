# Buat objek Konektor

<div class="grid grid-cols-2 gap-y-10 gap-x-6 mt-8">
<div class='flex-row'>

Untuk membuat hubungan antara aplikasi dan database, implementasikan kode berikut : 

Tips : Agar lebih modular, sebaiknya snippet kode ini dijadikan kelasnya sendiri. 

</div>
<div class='flex-row'>

```java 
import java.sql.*;
public class Test{
    public static void main(String[] args) {
        String driver = "com.mysql.cj.jdbc.Driver";
        String db = "jdbc:mysql://localhost/NAMA_DATABASE"; // Bila ada yang instance mysqlnya pindah port, tuliskan menjadi 'localhost:PORT/NAMA_DATABASE'
        String user = "root"; // Bila username berbeda, ganti baris ini
        String password = ""; // Bila instance MySQL memiliki password, isi baris ini
        Connection conn = null;
        Statement state = null;

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
        try{ 
            state.executeUpdate("MYSQL QUERY");
        } catch(Exception e){
            System.out.println("Error");
        }
    }
}
```

</div>
</div>
