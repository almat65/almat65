## uvicorn
pour que ça fonctionne, on build backend avec `5444:5432` sur docker-compose et `5432` dans `config.py` de jakartowns_backend. ensuite on roule backend et nginx, modifie le port pour 5444 dans config et lance  `uvicorn jakartowns_backend.main:app --reload`.

le service backend (avec `docker-compose up backend`) roule sur 127.0.0.1:8000 et le service postgis sur 5444

![image](https://user-images.githubusercontent.com/84472530/231776202-85bc358f-ab99-438b-8df5-e19756a0e8b8.png)

pour travailler en dev on modifie dans `config.py` pour 5432

cela donne l'url pour tester le backend http://127.0.0.1:8000/docs 8000 parce que backend est sur 8000 qui est spécifié dans jakartowns_backend -> backend
