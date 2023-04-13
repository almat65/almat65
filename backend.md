## uvicorn
pour que ça fonctionne, on roule le service backend avec `docker-compose up backend` (il roule le backend sur 127.0.0.1:8000 et le service postgis sur 5444)

![image](https://user-images.githubusercontent.com/84472530/231776202-85bc358f-ab99-438b-8df5-e19756a0e8b8.png)

ensuite on roule en local le backend avec `uvicorn jakartowns_backend.main:app --reload` et dans le fichier `config.py` j'ai postgres_port 5432 qui doit être 5444 quand on publie ou merge
cela donne l'url pour tester le backend http://127.0.0.1:8000/docs 8000 parce que backend est sur 8000 qui est spécifié dans jakartowns_backend -> backend
