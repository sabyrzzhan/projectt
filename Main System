import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        CinemaSystem system = new CinemaSystem();
        Scanner scanner = new Scanner(System.in);

        while (true) {
            System.out.println("\nChoose an option:");
            System.out.println("1) Add a new movie");
            System.out.println("2) Show all available movies");
            System.out.println("3) Add a new user");
            System.out.println("4) Buy a ticket");
            System.out.println("5) Cancel a ticket purchase");
            System.out.println("6) Exit");

            int choice = scanner.nextInt();
            scanner.nextLine();

            switch (choice) {
                case 1:
                    System.out.println("Enter movie name:");
                    String name = scanner.nextLine();
                    System.out.println("Enter movie genre:");
                    String genre = scanner.nextLine();
                    System.out.println("Enter age restriction:");
                    int ageRestriction = scanner.nextInt();
                    scanner.nextLine();
                    system.addMovie(name, genre, ageRestriction);
                    break;
                case 2:
                    system.showMovies();
                    break;
                case 3:
                    System.out.println("Enter user name:");
                    String userName = scanner.nextLine();
                    System.out.println("Enter user age:");
                    int age = scanner.nextInt();
                    System.out.println("Enter user balance:");
                    double balance = scanner.nextDouble();
                    scanner.nextLine();
                    system.addUser(userName, age, balance);
                    break;
                case 4:
                    System.out.println("Enter user ID:");
                    int userId = scanner.nextInt();
                    scanner.nextLine();
                    System.out.println("Enter movie name:");
                    String movieName = scanner.nextLine();
                    System.out.println("Enter date (dd/mm/yyyy):");
                    String date = scanner.nextLine();
                    System.out.println("Enter time (hh:mm):");
                    String time = scanner.nextLine();
                    System.out.println("Enter ticket price:");
                    double price = scanner.nextDouble();
                    scanner.nextLine();
                    system.buyTicket(userId, movieName, date, time, price);
                    break;
                case 5:
                    System.out.println("Enter user ID:");
                    int cancelUserId = scanner.nextInt();
                    System.out.println("Enter ticket ID:");
                    int ticketId = scanner.nextInt();
                    system.cancelTicket(cancelUserId, ticketId);
                    break;
                case 6:
                    System.out.println("Exiting...");
                    return;
                default:
                    System.out.println("Invalid choice. Try again.");
            }
        }
    }
}
