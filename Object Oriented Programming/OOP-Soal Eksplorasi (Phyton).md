import uuid

class Book:
    def __init__(self, title, author, category):
        self.id = uuid.uuid4()
        self.title = title
        self.author = author
        self.category = category

class Library:
    def __init__(self):
        self.books = []

    def create_book(self):
        title = input("Masukkan judul buku: ")
        author = input("Masukkan penulis buku: ")
        category = input("Masukkan kategori buku: ")
        book = Book(title, author, category)
        self.books.append(book)
        print("Buku berhasil ditambahkan!")

    def read_all_books(self):
        if len(self.books) == 0:
            print("Tidak ada buku yang tersimpan.")
        else:
            for book in self.books:
                print(f"ID: {book.id}\nJudul: {book.title}\nPenulis: {book.author}\nKategori: {book.category}\n")

    def read_book_by_id(self):
        id = input("Masukkan ID buku yang ingin dilihat: ")
        for book in self.books:
            if str(book.id) == id:
                print(f"ID: {book.id}\nJudul: {book.title}\nPenulis: {book.author}\nKategori: {book.category}\n")
                return
        print("Buku dengan ID tersebut tidak ditemukan.")

    def update_book(self):
        id = input("Masukkan ID buku yang ingin diubah: ")
        for book in self.books:
            if str(book.id) == id:
                book.title = input("Masukkan judul baru: ")
                book.author = input("Masukkan penulis baru: ")
                book.category = input("Masukkan kategori baru: ")
                print("Buku berhasil diubah!")
                return
        print("Buku dengan ID tersebut tidak ditemukan.")

    def delete_book(self):
        id = input("Masukkan ID buku yang ingin dihapus: ")
        for book in self.books:
            if str(book.id) == id:
                self.books.remove(book)
                print("Buku berhasil dihapus!")
                return
        print("Buku dengan ID tersebut tidak ditemukan.")

library = Library()

while True:
    print("Selamat datang di perpustakaan!\nPilih operasi yang ingin dilakukan:")
    print("1. Tambah buku")
    print("2. Lihat semua buku")
    print("3. Cari buku berdasarkan ID")
    print("4. Ubah data buku")
    print("5. Hapus buku")
    print("6. Keluar")

    choice = input("Masukkan pilihan Anda: ")

    if choice == "1":
        library.create_book()
    elif choice == "2":
        library.read_all_books()
    elif choice == "3":
        library.read_book_by_id()
    elif choice == "4":
        library.update_book()
    elif choice == "5":
        library.delete_book()
    elif choice == "6":
        print("Terima kasih telah menggunakan layanan perpustakaan.")
        break
    else:
        print("Pilihan tidak valid. Silakan coba lagi.")
