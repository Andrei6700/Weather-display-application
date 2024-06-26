# TemperatureConverter-APP

This project is built using C# and Universal Windows Platform (UWP)

## Appendix

It is a project made for the subject "UWP Application Development", where I chose to create an application where the user adds a city and can see the weather. 

Besides that the city can be added to a list so that the user doesn't have to write the city again and can also delete the city from the list of selected cities.


## Run Locally

Clone the project

```bash
  git clone https://github.com/Andrei6700/TemperatureConverter-APP
```

## Documentation

### MainPage.xaml

Fisierul **MainPage.xaml** interactioneaza cu elementele de UI ce sunt definite in fisierul *MainPage.xaml.cs* ,pentru a afisa vremea introdusa pentru un oras.

Clasa *MainPage* este derivata din *Page* ce contine variabilelele necesare.
Sunt definite: cheia pentru API-ul de la *OpenWeatherMap*, un container ce are ca spo stocarea setarilor aplicatiei si lista oraselor adaugate in istoric.
![alt text](image-2.png)

Constructorul initializeaza componentele din UI si incarca istoricul oraselor adaugate in lista
![alt text](image-3.png)

Fucntia LoadSearchHistory incarca lista oraslor adaugate daca exista, daca nu, nu incarca nimica. Iar elementele din lista sunt afisate una sub alta.
![alt text](image-4.png)

In functia SaveSeachHistory, se salveaza lista oraselor local, sub forma de sir de sir de caractere.
![alt text](image-5.png)

Metoda *OnShowWeatherClicked* este apelata cand userul apasa pe butonul de a arata vremea orasului selectat sau adaugat in input. In cazul in care nu este introdus sau nu este nici macar selectat un oras din lista, aplicatia va afisa un mesaj de eroare : "Please enter or select a city."
![alt text](image-6.png)

Cand utilizatorul apasa pe butonul de adaugare a unui oras, se apeleaza metoda *OnAddCityClicked* . Aceasta preaia orasul din inputul din TextBox, iar daca acesta nu a introdus nici un mesaj, ii va fi afisat un mesaj de eroare ca si cum nu ar fi adaugat un oras.
Aceasta functie adauga si salveaza orasul in lista daca nu exista deja. Si la final aceasta afiseaza vremea pentru orasul respectiv. 
![alt text](image-7.png)

Pentru a sterge un oras din lista, metoda *OnDeleteCityClicked* functioneaza sub felul urmator: utilizatorul selecteaza orasul din lista si apasa pe butonul de "Delete city" si va sterge orasul respectiv, iar daca acesta doar apasa pe butonul de stergere a unui oras va avea o eroare.
![alt text](image-8.png)

Pentru a fi afisata vremea, aplicatia initializeaza un client HTTP si trimite o cerere catre API. Daca acesta comunicarea intr API si aplicatie merge, aceasta va fi afisata vremea, iar daca nu, nu il va afisa.
![alt text](image-9.png)

### MainPage.xaml.cs
Aici este definita UI aplicatiei.
![alt text](image-10.png)


## API Reference

| Parameter | Type     | Description                |
| :-------- | :------- | :------------------------- |
| `ApiKey` | `string` | **Req3593e7c64f5424b605b43376ba0a096cuired** or Your API key |



## Screenshots

![alt text](image-1.png)