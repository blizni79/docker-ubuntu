Dockerfile

Zdecydowaną większość z kroków wymienionych w poprzednim rozdziale wykonamy za pomocą tzw. Dockerfile. 
Jest to zwykły plik tekstowy o nazwie Dockerfile (brak rozszerzeń, sama nazwa), który zawiera szereg instrukcji, 
dzięki którym damy radę stworzyć w pełni funkcjonalny obraz. Obraz ten będzie zawierał wszystko, co jest
 nam potrzebne do uruchomienia opisanej aplikacji.

Dockerfile składa się z par "instrukcja ↔ argumenty dla instrukcji". Opisuje on dokładnie, 
z jakich elementów powinno składać się środowisko wykonawcze dla umieszczonej w obrazie aplikacji. 
Zobaczmy teraz, jak może wyglądać przykładowy prosty plik Dockerfile:

# Obraz bazowy
FROM node:alpine

# Instalacja paczek
RUN npm i -g serve

# Domyślna komenda startowa
CMD ["serve", "--help"]


# Obraz bazowy
FROM
Obraz bazowy możemy traktować jak swego rodzaju system operacyjny dla tworzonego przez nas obrazu. Jest to baza, do której będziemy dodawać kolejne aplikacje (np. biblioteki) oraz nasz własny kod. To od nas zależy, z jakiego punktu zaczniemy tworzenie naszego obrazu właśnie poprzez określenie obrazu bazowego.


# Instalacje paczek




echo "this-is-my-secret" > secret.txt
docker secret list
docker secret create password-secret secret.txt


docker run –env-file .env mysql:latest
docker service create --name test-service --secret password-secret mysql:latest


docker volume inspect \{nazwa\}