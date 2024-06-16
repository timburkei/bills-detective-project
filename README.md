# container-et

Damit das Projekt ausgeführt werden kann, müssen drei Repos geclonet werden. Zudem muss eine aktuelle Docker Version auf dem Devices laufen

## backend
```
git clone https://gitlab.mi.hdm-stuttgart.de/expense-tracker/backend.git
```

## frontend
```
git clone https://gitlab.mi.hdm-stuttgart.de/expense-tracker/frontend-et.git
```

## ai-logic
```
git clone https://gitlab.mi.hdm-stuttgart.de/expense-tracker/ai-logic-et.git
```
```
cd ai-logic-et
git checkout master
```
Wenn Sie bereits ein .env File mit API Key besitzen, fügen Sie es im Directory: `SecurityGuard` ein.<br>
Andernfalls rstellen Sie ein .env Files mit Secret:
```
touch SecurityGuard/.env
python SecurityGuard/KeyGenerator.py
```
## env files
Anschließend muss jeweils in das Repo frontend und backend die jeweilige .env Datei. Im Frontend muss die Datei auth_config.json hinterlegt werden. Das ist Teil des Sicherheitskonzeptes. Ansonten kann das Projekt nicht gestartet werden.

## docker-compose ausführen
```
cd ..
docker-compose up
```
