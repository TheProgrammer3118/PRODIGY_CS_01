import string


def caesar_cipher(message, shift, mode):
    """Encrypt or decrypt a message using Caesar cipher."""
    shift %= 26
    if mode == "decrypt":
        shift = -shift

    result = []
    for char in message:
        if char in string.ascii_letters:
            base = ord("A") if char.isupper() else ord("a")
            new_char = chr(base + (ord(char) - base + shift) % 26)
            result.append(new_char)
        else:
            result.append(char)
    return "".join(result)


def display_menu():
    print("\nCaesar Cipher Program")
    print("1. Encrypt a message")
    print("2. Decrypt a message")
    print("3. Exit")


def main():
    while True:
        display_menu()
        choice = input("Choose an option (1-3): ")

        if choice == "1":
            message = input("Enter the message to encrypt: ")
            shift = int(input("Enter the shift value (integer): "))
            encrypted_message = caesar_cipher(message, shift, "encrypt")
            print("Encrypted message:", encrypted_message)

        elif choice == "2":
            message = input("Enter the message to decrypt: ")
            shift = int(input("Enter the shift value (integer): "))
            decrypted_message = caesar_cipher(message, shift, "decrypt")
            print("Decrypted message:", decrypted_message)

        elif choice == "3":
            print("Exiting the program.")
            break

        else:
            print("Invalid choice. Please select a valid option.")


if __name__ == "__main__":
    main()

