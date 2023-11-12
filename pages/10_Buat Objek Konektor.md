# Buat objek Konektor

<div class="grid grid-cols-2 gap-y-10 gap-x-6 mt-8">
<div class='flex-row'>

Untuk membuat hubungan antara aplikasi dan database, implementasikan kode berikut : 

Tips : Agar lebih modular, sebaiknya snippet kode ini dijadikan kelasnya sendiri. 

</div>
<div class='flex-row'>

```java 
String driver = "com.mysql.cj.jdbc.Driver";
String db = "jdbc:mysql://localhost/[NAMA_DATABASE]";
String user = "root"; // Bila username berbeda, ganti baris ini
String password = ""; // Bila instance MySQL memiliki password, isi baris ini
Connection conn = NULL;
Statement state = NULL;

try{
    Class.forName(driver);
} catch(Exception e){
    System.out.println("Driver Error"); // Bila ada 
} 

try{
    conn = (Connection)DriverManager.getConnection(db, user, password);
    state = (Statement) con.createStatement();
} catch(Exception e){
    System.out.println("Connection Error");
}

System.out.println("Database Connected");
state.executeUpdate("[QUERY_MYSQL]");
```

</div>
</div>
