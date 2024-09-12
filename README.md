# github_api
Автоматический тест для проверки работы с GitHub API на языке Python.
Скрипт использует API GitHub для выполнения следующих операций:
- создание нового публичного репозитория;
- проверка списка репозиториев для подтверждения создания;
- удаление репозитория.

### Запуск проекта на локальной машине:

Клонировать репозиторий:
```
git clone https://github.com/Anton-Kim/github_api.git
```
Сгенерировать свой персональный API-токен на GitHub:
1. Клик по своему аватару (правый верхний угол) -> Settings (https://github.com/settings/profile);
2. Слева раздел Developer Settings -> Personal Access Tokens -> Fine-grained tokens -> Generate new token;
3. Задать название, срок действия, в разделе Repository access выбрать All repositories, в разделе Permissions в Repository permissions в строке Administration выставить права Read and write;
4. Нажать зеленую кнопку Generate token для завершения процедуры.

Заполнить файл .env своими данными вручную или через (Ctrl+O - сохранить, Ctrl+X - выйти из редактора):
```
nano .env
```
```
GITHUB_USERNAME=<ваш username на GitHub>
TOKEN_API=<ваш API-токен на GitHub>
REPO_NAME=effectivemobile_test_repo
```
Cоздать виртуальное окружение:
```
python -m venv venv
```
Активировать виртуальное окружение:
```
source venv/scripts/activate
```
Установить зависимости из файла requirements.txt:
```
python -m pip install --upgrade pip
```
```
pip install -r requirements.txt
```
Запустить скрипт любым удобным способом:
```
python test_api.py
```