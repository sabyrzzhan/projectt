import java.util.ArrayList;

public class CinemaSystem {
    private ArrayList<User> users = new ArrayList<>();
    private ArrayList<Movie> movies = new ArrayList<>();

    public void addUser(String name, int age, double balance) {
        User newUser = new User(name, age, balance);
        users.add(newUser);
        System.out.println("User added successfully: " + newUser);
    }

    public void addMovie(String name, String genre, int ageRestriction) {
        Movie newMovie = new Movie(name, genre, ageRestriction);
        movies.add(newMovie);
        System.out.println("Movie added successfully: " + newMovie);
    }

    public void showMovies() {
        if (movies.isEmpty()) {
            System.out.println("No movies available.");
        } else {
            for (Movie movie : movies) {
                System.out.println(movie);
            }
        }
    }

    public void buyTicket(int userId, String movieName, String date, String time, double price) {
        User user = findUserById(userId);
        Movie movie = findMovieByName(movieName);

        if (user != null && movie != null) {
            if (user.getAge() < movie.getAgeRestriction()) {
                System.out.println("User does not meet the age restriction for this movie.");
                return;
            }
            if (user.deductBalance(price)) {
                Ticket ticket = new Ticket(movieName, date, time, price);
                user.addTicket(ticket);
                System.out.println("Ticket purchased successfully: " + ticket);
            }
        }
    }

    public void cancelTicket(int userId, int ticketId) {
        User user = findUserById(userId);
        if (user != null) {
            user.getOrderHistory().removeIf(ticket -> ticket.getId() == ticketId);
            System.out.println("Ticket with ID " + ticketId + " canceled successfully.");
        }
    }

    private User findUserById(int userId) {
        for (User user : users) {
            if (user.getId() == userId) {
                return user;
            }
        }
        System.out.println("User with ID " + userId + " not found.");
        return null;
    }

    private Movie findMovieByName(String movieName) {
        for (Movie movie : movies) {
            if (movie.getName().equalsIgnoreCase(movieName)) {
                return movie;
            }
        }
        System.out.println("Movie with name '" + movieName + "' not found.");
        return null;
    }
}
