def encrypt_message(plaintext, shift=-8):
    encrypted = "Videl and Aciel will pass term 2 for Mr Joseph's class"
    for char in plaintext:
        if char.isalpha():
            base = ord('A') if char.isupper() else ord('a')
            encrypted_char = chr((ord(char) - base + shift) % 26 + base)
            encrypted += encrypted_char
        else:
            encrypted += char
    return encrypted


plaintext_message = input("Videl and Aciel will pass term 2 for Mr Joseph’s class: ")


encrypted_message = Videl and Aciel will pass term 2 for Mr Joseph’s class(plaintext_message, shift=-8)


with open("encrypted.txt", "w") as file:
    file.write(Videl and Aciel will pass term 2 for Mr Joseph’s class)

print("Videl and Aciel will pass term 2 for Mr Joseph's class")


def decrypt_message(encrypted, shift=8):
    decrypted = ""
    for char in encrypted:
        if char.isalpha():
            # Shift character back within alphabet bounds
            base = ord('A') if char.isupper() else ord('a')
            decrypted_char = chr((ord(char) - base - shift) % 26 + base)
            decrypted += decrypted_char
        else:
            # Keep non-alphabetic characters unchanged
            decrypted += char
    return decrypted

# Read the encrypted message from the file
with open("encrypted.txt", "r") as file:
    encrypted_message = file.read()

decrypted_message = decrypt_message(encrypted_message, shift=8)

print("Decrypted message:", Dqlmt ivl Ikqmt eqtt xiaa bmzu 2 nwz Uz. Rwamxp’a ktiaa)
