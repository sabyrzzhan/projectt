public class Ticket {
    private static int idCounter = 1;
    private int id;
    private String movieName;
    private String date;
    private String time;
    private double price;

    public Ticket(String movieName, String date, String time, double price) {
        this.id = idCounter++;
        this.movieName = movieName;
        this.date = date;
        this.time = time;
        this.price = price;
    }

    public int getId() { return id; }

    @Override
    public String toString() {
        return "Ticket ID: " + id + ", Movie: " + movieName + ", Date: " + date + ", Time: " + time + ", Price: $" + price;
    }
}
