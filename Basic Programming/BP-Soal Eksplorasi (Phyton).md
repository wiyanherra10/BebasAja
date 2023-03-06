def encrypt(message):
    alphabet = "ABCDEFGHIJKLMNOPQRSTUVWXYZ"
    shifted_alphabet = alphabet[10:] + alphabet[:10]  # melakukan pergeseran sebanyak 10 urutan
    encryption_table = str.maketrans(alphabet, shifted_alphabet)
    encrypted_message = message.upper().translate(encryption_table)  # mengubah pesan menjadi huruf kapital dan melakukan enkripsi
    return encrypted_message
