# Einfache Aufgabenverwaltung (To-Do-Liste) in Python

aufgaben = []

def aufgabe_hinzufuegen(aufgabe):
    aufgaben.append(aufgabe)
    print(f"Aufgabe '{aufgabe}' wurde hinzugefügt.")

def aufgaben_anzeigen():
    if not aufgaben:
        print("Keine Aufgaben vorhanden.")
    else:
        print("Deine Aufgaben:")
        for index, aufgabe in enumerate(aufgaben, start=1):
            print(f"{index}. {aufgabe}")

def aufgabe_entfernen(index):
    if 0 < index <= len(aufgaben):
        entfernte = aufgaben.pop(index - 1)
        print(f"Aufgabe '{entfernte}' wurde entfernt.")
    else:
        print("Ungültiger Index.")

def hauptmenue():
    while True:
        print("\n--- Aufgabenverwaltung ---")
        print("1. Aufgabe hinzufügen")
        print("2. Aufgaben anzeigen")
        print("3. Aufgabe entfernen")
        print("4. Beenden")
        wahl = input("Bitte wähle (1-4): ")

        if wahl == "1":
            aufgabe = input("Gib eine neue Aufgabe ein: ")
            aufgabe_hinzufuegen(aufgabe)
        elif wahl == "2":
            aufgaben_anzeigen()
        elif wahl == "3":
            aufgaben_anzeigen()
            try:
                index = int(input("Welche Aufgabe soll entfernt werden (Nummer)? "))
                aufgabe_entfernen(index)
            except ValueError:
                print("Bitte gib eine gültige Zahl ein.")
        elif wahl == "4":
            print("Auf Wiedersehen!")
            break
        else:
            print("Ungültige Auswahl. Bitte nochmal.")

# Starte das Programm
hauptmenue()


