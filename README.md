# Mini Portfolio in Python - Für die Bewerbung bei U-Glow

def zeige_bewerbung():
    name = "Dein Name"
    beruf = "Angehender Softwareentwickler"
    skills = ["Python (Anfänger)", "Teamarbeit", "Lernbereitschaft"]
    motivation = "Ich möchte bei U-Glow arbeiten, weil ich motiviert bin und gern im Tech-Bereich wachse."

    print(" Hallo, mein Name ist:", name)
    print(" Berufsziel:", beruf)
    print(" Meine Fähigkeiten:")
    for skill in skills:
        print("-", skill)
    print("📝 Warum U-Glow?")
    print(motivation)

zeige_bewerbung()

