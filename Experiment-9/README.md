## Experiment-9
## Experiment-9a
## Source Code
```
import java.sql.*;
import java.util.Scanner;

class DBConnection {

    public static Connection getConnection() throws Exception {

        String url = "jdbc:oracle:thin:@localhost:1521:xe";
        String username = "system";
        String password = "newpassword";

        Class.forName("oracle.jdbc.driver.OracleDriver");

        Connection con = DriverManager.getConnection(url, username, password);

        return con;
    }
}

class FetchData {

    public static void displayStudentsRecords() {

        try (
            Connection con = DBConnection.getConnection();
            PreparedStatement ps = con.prepareStatement("SELECT * FROM StudentRecords");
            ResultSet rs = ps.executeQuery();
        ) {

            System.out.println("Student Records:");
            System.out.println("-----------------------");

            while (rs.next()) {

                int id = rs.getInt("ID");
                String name = rs.getString("NAME");
                int age = rs.getInt("AGE");

                System.out.println("ID: " + id + " Name: " + name + " Age: " + age);
            }

        } catch (Exception e) {
            System.out.println("Error: " + e);
        }
    }
}

public class DatabaseConnectionExample {

    public static void main(String[] args) {

        System.out.println("Connecting to database...");

        FetchData.displayStudentsRecords();

        System.out.println("Operation completed successfully.");
    }
}
```
## Output

<img width="1920" height="952" alt="exp9a" src="https://github.com/user-attachments/assets/2b7f40e9-8101-4ae5-adf5-77ef8a809f9c" />



## Experiment-9b
## source Code
```
import java.sql.*;
import java.util.Scanner;

class DBConnectionInsert {

    public static Connection getConnection() throws Exception {

        String url = "jdbc:oracle:thin:@localhost:1521:xe";
        String username = "system";
        String password = "newpassword";

        Class.forName("oracle.jdbc.driver.OracleDriver");

        return DriverManager.getConnection(url, username, password);
    }
}

class InsertStudent {

    public static void insertData() {

        Scanner sc = new Scanner(System.in);

        try {

            Connection con = DBConnectionInsert.getConnection();

            String query = "INSERT INTO StudentRecords VALUES(?,?,?)";

            PreparedStatement ps = con.prepareStatement(query);

            System.out.print("Enter Student ID: ");
            int id = sc.nextInt();

            System.out.print("Enter Student Name: ");
            String name = sc.next();

            System.out.print("Enter Student Age: ");
            int age = sc.nextInt();

            ps.setInt(1, id);
            ps.setString(2, name);
            ps.setInt(3, age);

            int rows = ps.executeUpdate();

            if (rows > 0) {
                System.out.println("Record Inserted Successfully");
            }

            ps.close();
            con.close();

        } catch (Exception e) {
            System.out.println(e);
        }
    }
}

public class InsertDataExample {

    public static void main(String[] args) {

        InsertStudent.insertData();
    }
}

```
## Output
<img width="1920" height="941" alt="Screenshot 2026-03-07 160859" src="https://github.com/user-attachments/assets/f41996c7-0c3d-461b-997d-9e3f4e876f42" />



## Experiment-9c
## Source Code
```import java.sql.*;
import java.util.Scanner;

class DBConnectionDelete {

    public static Connection getConnection() throws Exception {

        String url = "jdbc:oracle:thin:@localhost:1521:xe";
        String username = "system";
        String password = "newpassword";

        Class.forName("oracle.jdbc.driver.OracleDriver");

        return DriverManager.getConnection(url, username, password);
    }
}

class DeleteStudent {

    public static void deleteRecord() {

        Scanner sc = new Scanner(System.in);

        try {

            Connection con = DBConnectionDelete.getConnection();

            String query = "DELETE FROM StudentRecords WHERE id=?";

            PreparedStatement ps = con.prepareStatement(query);

            System.out.print("Enter Student ID to delete: ");
            int id = sc.nextInt();

            ps.setInt(1, id);

            int rows = ps.executeUpdate();

            if (rows > 0) {
                System.out.println("Record Deleted Successfully");
            } else {
                System.out.println("No record found with this ID");
            }

            ps.close();
            con.close();

        } catch (Exception e) {
            System.out.println(e);
        }
    }
}

public class DeleteDataExample {

    public static void main(String[] args) {

        DeleteStudent.deleteRecord();
    }
}

```
## Output
<img width="1920" height="962" alt="Screenshot 2026-03-07 161245" src="https://github.com/user-attachments/assets/e39e2a3f-52d3-40ab-864f-27661a708d11" />


