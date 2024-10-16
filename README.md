def read_file(file_path):
    try:
        with open(file_path, 'r', encoding='utf-8') as file:
            content = file.read()
            print(content)
    except FileNotFoundError:
        print(f"A megadott fájl nem található: {file_path}")
    except Exception as e:
        print(f"Hiba történt a fájl olvasása során: {e}")

if __name__ == "__main__":
    file_path = input("Add meg a fájl elérési útját: ")
    read_file(file_path)
