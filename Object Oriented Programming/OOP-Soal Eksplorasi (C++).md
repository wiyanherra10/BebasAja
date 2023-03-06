#include <iostream>
#include <vector>
#include <algorithm>
#include <string>
#include <cstdlib>
#include <ctime>
#include <iomanip>
#include <sstream>

using namespace std;

class Book {
    private:
        string id;
        string title;
        string author;
        string category;
    public:
        Book() {
            this->id = generateUUID();
            this->title = "";
            this->author = "";
            this->category = "";
        }
        Book(string title, string author, string category) {
            this->id = generateUUID();
            this->title = title;
            this->author = author;
            this->category = category;
        }
        string getId() const {
            return id;
        }
        string getTitle() const {
            return title;
        }
        void setTitle(string title) {
            this->title = title;
        }
        string getAuthor() const {
            return author;
        }
        void setAuthor(string author) {
            this->author = author;
        }
        string getCategory() const {
            return category;
        }
        void setCategory(string category) {
            this->category = category;
        }
        string toString() const {
            stringstream ss;
            ss << left << setw(40) << title << left << setw(30) << author << left << setw(20) << category << left << setw(40) << id;
            return ss.str();
        }
    private:
        string generateUUID() {
            srand((unsigned) time(0));
            stringstream ss;
            for(int i = 0; i < 8; i++) {
                int r = rand() % 16;
                ss << hex << r;
            }
            ss << "-";
            for(int i = 0; i < 4; i++) {
                int r = rand() % 16;
                ss << hex << r;
            }
            ss << "-4";
            for(int i = 0; i < 3; i++) {
                int r = rand() % 16;
                ss << hex << r;
            }
            ss << "-a";
            for(int i = 0; i < 3; i++) {
                int r = rand() % 16;
                ss << hex << r;
            }
            ss << "-";
            for(int i = 0; i < 12; i++) {
                int r = rand() % 16;
                ss << hex << r;
            }
            return ss.str();
        }
};

vector<Book> books;

void createBook() {
    string title, author, category;
    cout << "Enter book title: ";
    getline(cin, title);
    cout << "Enter book author: ";
    getline(cin, author);
    cout << "Enter book category: ";
    getline(cin, category);
    Book book(title, author, category);
    books.push_back(book);
    cout << "Book added successfully!" << endl;
}

void readAllBooks() {
    if(books.empty()) {
        cout << "There are no books in the library." << endl;
    } else {
        cout << left << setw(40) << "Title" << left << setw(30) << "Author" << left << setw(20) << "Category" << left << setw(40) << "ID" << endl;
        for(int i = 0; i < books.size(); i++) {
            cout << books[i].toString() << endl;
        }
    }
}

void readBookById() {
    if(books.empty()) {
        cout << "There are no books
