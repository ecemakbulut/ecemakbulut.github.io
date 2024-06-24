import tkinter as tk
from tkinter import messagebox

# Dummy-Daten für Genre und Künstler
genres = ["Renaissance", "Barock", "Kubismus", "Impressionismus"]
kuenstler = ["Leonardo da Vinci", "Rembrandt", "Pablo Picasso", "Vincent van Gogh"]

class ArtHubApp:
    def __init__(self, root):
        self.root = root
        self.root.title("ArtHub")
        self.root.geometry("800x700")
        self.root.configure(bg="black")  # Hintergrundfarbe auf schwarz setzen
        
        # Inhaltsverzeichnis auf der linken Seite
        self.frame_menu = tk.Frame(self.root, bg="black")
        self.frame_menu.pack(side=tk.LEFT, fill=tk.Y)

        self.label_title = tk.Label(self.frame_menu, text="Web App ArtHub", font=("Helvetica", 16, "bold"), bg="black", fg="white")
        self.label_title.pack(pady=10)

        self.label_home = tk.Label(self.frame_menu, text="Home", font=("Helvetica", 14), bg="black", fg="white", cursor="hand2")
        self.label_home.pack(pady=5)
        self.label_home.bind("<Button-1>", lambda e: self.show_home())

        self.label_value_prop = tk.Label(self.frame_menu, text="Value Proposition", font=("Helvetica", 14), bg="black", fg="white", cursor="hand2")
        self.label_value_prop.pack(pady=5)
        self.label_value_prop.bind("<Button-1>", lambda e: self.show_value_prop())

        self.label_tech_docs = tk.Label(self.frame_menu, text="Technical Docs", font=("Helvetica", 14), bg="black", fg="white", cursor="hand2")
        self.label_tech_docs.pack(pady=5)
        self.label_tech_docs.bind("<Button-1>", lambda e: self.show_tech_docs())

        self.label_team_eval = tk.Label(self.frame_menu, text="Team Evaluation", font=("Helvetica", 14), bg="black", fg="white", cursor="hand2")
        self.label_team_eval.pack(pady=5)
        self.label_team_eval.bind("<Button-1>", lambda e: self.show_team_eval())
        
        # Rahmen für den Hauptinhalt
        self.frame_content = tk.Frame(self.root, bg="black")
        self.frame_content.pack(side=tk.LEFT, fill=tk.BOTH, expand=True)

        # Genre und Künstler Buttons in der Mitte
        self.button_genre = tk.Button(self.frame_content, text="Genre", font=("Helvetica", 25), command=self.show_genres, width=20, height=3, bg="white", fg="black")
        self.button_genre.pack(pady=30)

        self.button_artist = tk.Button(self.frame_content, text="Künstler", font=("Helvetica", 25), command=self.show_artists, width=20, height=3, bg="white", fg="black")
        self.button_artist.pack(pady=30)
        
        # Suchleiste mit Lupe-Symbol
        self.entry_search = tk.Entry(self.frame_content, font=("Helvetica", 14), bg="white", fg="black")
        self.entry_search.pack(pady=20)
        
        # Rahmen für die Such- und Favoriten-Buttons unten
        frame_bottom_buttons = tk.Frame(self.frame_content, bg="black")
        frame_bottom_buttons.pack(side=tk.BOTTOM, pady=40)
        
        # Button für die Suche (Lupe-Symbol)
        self.button_search = tk.Button(frame_bottom_buttons, text="🔍", font=("Helvetica", 16), command=self.search, width=10, height=2, bg="white", fg="black")
        self.button_search.grid(row=0, column=0, padx=5)

        # Button für Favoriten (Herz-Symbol)
        self.button_favorites = tk.Button(frame_bottom_buttons, text="❤️", font=("Helvetica", 16), command=self.show_favorites, width=10, height=2, bg="white", fg="black")
        self.button_favorites.grid(row=0, column=1, padx=5)
        
        # Rahmen für die Favoritenliste
        frame_favorites = tk.Frame(self.frame_content, bg="black")
        frame_favorites.pack(pady=20)
        
        # Favoritenliste mit Herz-Symbol
        self.label_favorites = tk.Label(frame_favorites, text="Favoriten", font=("Helvetica", 16, "bold"), bg="black", fg="white")
        self.label_favorites.grid(row=0, column=0, padx=10)
        
        self.favorite_listbox = tk.Listbox(frame_favorites, width=40, height=5, font=("Helvetica", 12), bg="white", fg="black")
        self.favorite_listbox.grid(row=1, column=0, padx=10)
        
        # Beispiel: Eintrag zur Favoritenliste hinzufügen (Dummy-Daten)
        self.add_to_favorites("Mona Lisa")
        self.add_to_favorites("Starry Night")

    def show_home(self):
        messagebox.showinfo("Home", "Web App ArtHub\n---\nHome\n\n# ArtHub\n\nDie ArtHub App ist eine innovative Plattform...")

    def show_value_prop(self):
        messagebox.showinfo("Value Proposition", "Web App ArtHub\n---\nValue Proposition\n\n# Description\n\n+ Die ArtHub App ist eine informative Kunst App...")

    def show_tech_docs(self):
        messagebox.showinfo("Technical Docs", "Web App ArtHub\n---\nTechnical Docs\n\n# Technical Documentation\n\nHier könnte die technische Dokumentation stehen...")

    def show_team_eval(self):
        messagebox.showinfo("Team Evaluation", "Web App ArtHub\n---\nTeam Evaluation\n\n# Team members\n\n### Ecem Akbulut\n\nAbout\n: 21-jährige Wirtschaftsinformatik Studentin aus Köpenick...")

    def show_genres(self):
        # Dummy-Funktion, um Genres anzuzeigen
        messagebox.showinfo("Genres", "\n".join(genres))
        
    def show_artists(self):
        # Dummy-Funktion, um Künstler anzuzeigen
        messagebox.showinfo("Künstler", "\n".join(kuenstler))
        
    def search(self):
        # Dummy-Funktion für die Suchfunktion
        query = self.entry_search.get().strip().lower()
        if query:
            messagebox.showinfo("Suchergebnisse", f"Suche nach: {query}")
        else:
            messagebox.showwarning("Fehler", "Bitte geben Sie einen Suchbegriff ein.")
    
    def show_favorites(self):
        # Dummy-Funktion, um Favoriten anzuzeigen
        favorites = self.favorite_listbox.get(0, tk.END)
        if favorites:
            messagebox.showinfo("Favoritenliste", "\n".join(favorites))
        else:
            messagebox.showinfo("Favoritenliste", "Keine Favoriten gespeichert.")
    
    def add_to_favorites(self, item):
        self.favorite_listbox.insert(tk.END, item)
    
# Hauptprogramm
if __name__ == "__main__":
    root = tk.Tk()
    app = ArtHubApp(root)
    root.mainloop()
