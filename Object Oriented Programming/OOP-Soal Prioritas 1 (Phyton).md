class Product:
    def __init__(self, name, description, price, stock):
        self.__name = name
        self.__description = description
        self.__price = price
        self.__stock = stock

    def getName(self):
        return self.__name

    def getDescription(self):
        return self.__description

    def getPrice(self):
        return self.__price

    def getStock(self):
        return self.__stock

    def setName(self, name):
        self.__name = name

    def setDescription(self, description):
        self.__description = description

    def setPrice(self, price):
        self.__price = price

    def setStock(self, stock):
        self.__stock = stock

    def getInfo(self):
        print("Nama produk:", self.__name)
        print("Deskripsi:", self.__description)
        print("Harga:", self.__price)
        print("Stok:", self.__stock)
