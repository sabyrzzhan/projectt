import java.util.ArrayList;

public class User {
    private static int idCounter = 1;
    private int id;
    private String name;
    private int age;
    private double balance;
    private ArrayList<Ticket> orderHistory;

    public User(String name, int age, double balance) {
        this.id = idCounter++;
        this.name = name;
        this.age = age;
        this.balance = balance;
        this.orderHistory = new ArrayList<>();
    }

    public int getId() { return id; }
    public String getName() { return name; }
    public int getAge() { return age; }
    public double getBalance() { return balance; }
    public ArrayList<Ticket> getOrderHistory() { return orderHistory; }

    public void addTicket(Ticket ticket) {
        orderHistory.add(ticket);
    }

    public boolean deductBalance(double amount) {
        if (balance >= amount) {
            balance -= amount;
            return true;
        }
        System.out.println("Not enough balance.");
        return false;
    }

    public void showOrderHistory() {
        if (orderHistory.isEmpty()) {
            System.out.println("No tickets purchased.");
        } else {
            for (Ticket ticket : orderHistory) {
                System.out.println(ticket);
            }
        }
    }

    @Override
    public String toString() {
        return "User ID: " + id + ", Name: " + name + ", Age: " + age + ", Balance: $" + balance;
    }
}
