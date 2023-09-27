package library;

import java.util.ArrayList;
import java.util.List;

class Book {
    private int bookId;
    private String title;
    private boolean isIssued;

    public Book(int bookId, String title) {
        this.bookId = bookId;
        this.title = title;
        this.isIssued = false;
    }

    public int getBookId() {
        return bookId;
    }

    public String getTitle() {
        return title;
    }

    public boolean isIssued() {
        return isIssued;
    }

    public void setIssued(boolean issued) {
        isIssued = issued;
    }
}

class Library {
    private List<Book> books;

    public Library() {
        this.books = new ArrayList<>();
    }

    public void addBook(Book book) {
        books.add(book);
    }

    public void issueBook(int bookId) {
        for (Book book : books) {
            if (book.getBookId() == bookId) {
                if (!book.isIssued()) {
                    book.setIssued(true);
                    System.out.println("Book with ID " + bookId + " has been issued.");
                    return;
                } else {
                    System.out.println("Book with ID " + bookId + " is already issued.");
                    return;
                }
            }
        }
        System.out.println("Book with ID " + bookId + " not found in the library.");
    }

    public void returnBook(int bookId) {
        for (Book book : books) {
            if (book.getBookId() == bookId) {
                if (book.isIssued()) {
                    book.setIssued(false);
                    System.out.println("Book with ID " + bookId + " has been returned.");
                    return;
                } else {
                    System.out.println("Book with ID " + bookId + " is not issued.");
                    return;
                }
            }
        }
        System.out.println("Book with ID " + bookId + " not found in the library.");
    }
}

public class libraryreturn{
    public static void main(String[] args) {
        Library library = new Library();

        // Adding books to the library
        library.addBook(new Book(1, "Java Programming"));
        library.addBook(new Book(2, "Python Programming"));
        library.addBook(new Book(3, "Data Structures and Algorithms"));

        // Issuing and returning books
        library.issueBook(1);
        library.issueBook(2);
        library.returnBook(1);
        library.issueBook(3);
        library.issueBook(1);
    }
}
