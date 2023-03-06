<?php

class Book {
  public $id;
  public $title;
  public $author;
  public $category;

  function __construct($id, $title, $author, $category) {
    $this->id = $id;
    $this->title = $title;
    $this->author = $author;
    $this->category = $category;
  }
}

class BookManager {
  private $books = array();

  function createBook($title, $author, $category) {
    $id = uniqid(); // generate unique ID using uniqid()
    $book = new Book($id, $title, $author, $category);
    array_push($this->books, $book);
    return $id; // return ID of the newly created book
  }

  function getBooks() {
    return $this->books;
  }

  function getBookById($id) {
    foreach ($this->books as $book) {
      if ($book->id == $id) {
        return $book;
      }
    }
    return null; // book not found
  }

  function updateBook($id, $title, $author, $category) {
    foreach ($this->books as $book) {
      if ($book->id == $id) {
        $book->title = $title;
        $book->author = $author;
        $book->category = $category;
        return true; // book updated successfully
      }
    }
    return false; // book not found
  }

  function deleteBook($id) {
    foreach ($this->books as $key => $book) {
      if ($book->id == $id) {
        unset($this->books[$key]);
        return true; // book deleted successfully
      }
    }
    return false; // book not found
  }
}

// example usage
$bookManager = new BookManager();

// create new book
$bookId = $bookManager->createBook("The Lord of The Rings", "J.R.R. Tolkien", "Fantasy");

// get all books
$books = $bookManager->getBooks();
print_r($books);

// get book by ID
$book = $bookManager->getBookById($bookId);
print_r($book);

// update book
$bookManager->updateBook($bookId, "The Hobbit", "J.R.R. Tolkien", "Fantasy");
$book = $bookManager->getBookById($bookId);
print_r($book);

// delete book
$bookManager->deleteBook($bookId);
$books = $bookManager->getBooks();
print_r($books);

?>
