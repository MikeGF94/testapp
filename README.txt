# testapp
Тестовое задание для DevOps практикума в SimbirSoft

1. Запуск приложения выполнен локально при исправлении этой части кода в файле .../scripts/forms.py
   from wtforms import Form, StringField, validators

   class LoginForm(Form):
   username = StringField('Username:', validators=[validators.required(), validators.Length(min=1, max=30)])
   password = StringField('Password:', validators=[validators.required(), validators.Length(min=1, max=30)])
   email = StringField('Email:', validators=[validators.optional(), validators.Length(min=0, max=50)])
   
   На:
   
   from wtforms import Form
   from wtforms import (StringField)
   from wtforms.validators import InputRequired, Length

   class LoginForm(Form):
   username = StringField('Username:', validators=[InputRequired(), Length(min=5, max=30)])
   password = StringField('Password:', validators=[InputRequired(), Length(min=5, max=30)])
   email = StringField('Email:', validators=[Length(min=0, max=30)])
  Данное решение найдено тут  https://github.com/anfederico/flaskex/issues/34 т.к не имею достаточно опыта в Python
  
2. Рабочий Dockerfile находится в каталоге /Flaskex-docker/Dockerfile
   Сборка и запуск контейнера:
   
 cd Flaskex-docker
 docker build ./
 docker run -d -p 5000:5000 <image id>
  
3. docker-compose.yml находится в /
   Запуск:
   
 docker-compose up -d
