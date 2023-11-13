# Contoh CRUD
Berikut adalah contoh implementasi CRUD menggunakan JDBC : 

<div class="grid grid-cols-2 gap-y-10 gap-x-6 mt-8">
  <div class='flex-row'>
    <div class='text-xl'>
        ```java 
        public class Koneksi {
          public static void main(String args[]) {
            String driver = "com.mysql.cj.jdbc.Driver";
            String db = "jdbc:mysql://localhost/test_koneksi";
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
            state.executeUpdate("INSERT INTO `game` (`id`, `name`, `genre`, `description`) VALUES ('3', 'ML', 'MOBA', 'Stress'); ");
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