Создайте Init commit с папкой abobryashova:

git clone git@github.com:Anastasiya-Bobryashova/jedi.bigdata.1  abobryashova
cd abobryashova

Заберите код из https://github.com/apache/airflow (v-1-8-stable) в свой репрозиторий и сделайте коммит ""Add airflow"":

git remote add airflow git@github.com:apache/airflow.git
git pull airflow v1-8-stable
git checkout -b v1-8-stable airflow/v1-8-stable
git checkout main
git read-tree --prefix=abobryashova/airflow -u v1-8-stable
git commit -am "Add airflow"
git push origin HEAD

Возьмите ветку v-1-8-stable(https://github.com/apache/airflow) и добавьте свой коммит с названием ""WIP: Testing working with git"" в коммите нужно внести любые изменения в любые 10 файлов:

git checkout -b v1-8-stable airflow/v1-8-stable

echo "какой-то текст\nещё что-то" > tox.ini
echo "какой-то текст\nещё что-то" > setup.py
echo "какой-то текст\nещё что-то" > UPDATING.md
echo "какой-то текст\nещё что-то" > TODO.md
echo "какой-то текст\nещё что-то" > README.md
echo "какой-то текст\nещё что-то" > MANIFEST.in
echo "какой-то текст\nещё что-то" > CHANGELOG.txt
echo "какой-то текст\nещё что-то" > CONTRIBUTING.md
echo "какой-то текст\nещё что-то" > setup.cfg
echo "какой-то текст\nещё что-то" > run_tox.sh
git add -A
git commit -m "WIP: Testing working with git"


Создайте еще одну ветку fix которая будет идентична предыдущий вашей ветке main:

git checkout main
git branch fix
git checkout fix

И удалите из нее все коммиты от Jun 16, 2017:

-

Создайте SOLUTION.md файл со списком комманд как вы выполняли все задания и тоже закоммитьте этот файл в main ветку:

cat > SOLUTION.md
git add SOLUTION.md
git commit -m "Commands"








-------------------------------------------------------------------------------------------------
Не рабочее

git remote add airflow git@github.com:apache/airflow.git
git pull airflow v1-8-stable
git checkout -b v1-8-stable airflow v1-8-stable
touch .gitpeek
git add -A
git commit -m "Add airflow"
git push origin HEAD

