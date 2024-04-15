package Apr15;

import java.sql.*;

public class InsertData {
    public static void main(String[] args){
        try(Connection c = MySQLConnection.getConnection();
            PreparedStatement statement = c.prepareStatement(
                    "INSERT INTO users (name, email) VALUES (?, ?)")) {
            String name = "Charuzu Darney Hudar";
            String email = "charuzudarney@cit.edu";
            statement.setString(1, name);
            statement.setString(2, email);
            int rowsInserted = statement.executeUpdate();

            if(rowsInserted > 0){
                System.out.println("Data Inserted Successfully!");
            }
        } catch (SQLException e){
            e.printStackTrace();
        }
    }
}
