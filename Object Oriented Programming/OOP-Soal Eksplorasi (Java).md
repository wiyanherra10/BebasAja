import java.util.ArrayList;
import java.util.Scanner;
import java.util.UUID;

class Book {
    private UUID id;
    private String title;
    private String author;
    private String category;

    public Book(String title, String author, String category) {
        this.id = UUID.randomUUID();
        this.title = title;
        this.author = author;
        this.category = category;
    }

    public UUID getId() {
        return id;
    }

    public String getTitle() {
        return title;
    }

    public void setTitle(String title) {
        this.title = title;
    }

    public String getAuthor() {
        return author;
    }

    public void setAuthor(String author) {
        this.author = author;
    }

    public String getCategory() {
        return category;
    }

    public void setCategory(String category) {
        this.category = category;
    }

    @Override
    public String toString() {
        return "Book{" +
                "id=" + id +
                ", title='" + title + '\'' +
                ", author='" + author + '\'' +
                ", category='" + category + '\'' +
                '}';
    }
}

public class BookApp {
    private ArrayList<Book> books;
    private Scanner scanner;

    public BookApp() {
        this.books = new ArrayList<>();
        this.scanner = new Scanner(System.in);
    }

    public void createBook() {
        System.out.print("Enter book title: ");
        String title = scanner.nextLine();
        System.out.print("Enter book author: ");
        String author = scanner.nextLine();
        System.out.print("Enter book category: ");
        String category = scanner.nextLine();
        Book book = new Book(title, author, category);
        books.add(book);
        System.out.println("Book added successfully.");
    }

    public void readAllBooks() {
        if (books.isEmpty()) {
            System.out.println("No books found.");
        } else {
            for (Book book : books) {
                System.out.println(book);
            }
        }
    }

    public void readBookById() {
        System.out.print("Enter book ID: ");
        UUID id = UUID.fromString(scanner.nextLine());
        for (Book book : books) {
            if (book.getId().equals(id)) {
                System.out.println(book);
                return;
            }
        }
        System.out.println("Book not found.");
    }

    public void updateBookById() {
        System.out.print("Enter book ID: ");
        UUID id = UUID.fromString(scanner.nextLine());
        for (Book book : books) {
            if (book.getId().equals(id)) {
                System.out.print("Enter new title (press Enter to skip): ");
                String title = scanner.nextLine();
                if (!title.isEmpty()) {
                    book.setTitle(title);
                }
                System.out.print("Enter new author (press Enter to skip): ");
                String author = scanner.nextLine();
                if (!author.isEmpty()) {
                    book.setAuthor(author);
                }
                System.out.print("Enter new category (press Enter to skip): ");
                String category = scanner.nextLine();
                if (!category.isEmpty()) {
                    book.setCategory(category);
                }
                System.out.println("Book updated successfully.");
                return;
            }
        }
        System.out.println("Book not found.");
    }

    public void deleteBookById() {
        System.out.print("Enter book ID: ");
        UUID id = UUID.fromString(scanner.nextLine());
        for (int i = 0; i < books.size(); i++) {
            if (books.get(i).getId().equals(id)) {
                books.remove(i);
                System.out.println("Book deleted successfully.");
                return;
            }
        }
        System.out.println("
