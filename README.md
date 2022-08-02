Configurazione per creare i servizi necessari per l'applicazione.
Sono presenti 4 servizi:
  - nginx: per il web server
  - php: per l'applicazione Laravel
  - postgres: per il database
  - exchange: per il servizio di exchange

Per avviare i servizi eseguire il seguente comando:
```
docker-compose up --remove-orphans --build
```
Il quale creerà i contenitori per ogni servizio ed inizializzerà le applicazioni e il database con dei dati di partenza.