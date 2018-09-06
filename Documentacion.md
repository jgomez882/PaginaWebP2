# Proyecto 1 2018-2<h1>
# Tópicos especiales en telemática <h2>

### 1. Ruby on Rails:
Es un framework para crear aplicaciones web y esta escrito en ruby.
* __Importante:__ ActiveRecord permite trabajar con las tablas 
es decir cosas de la base datos.

ERB es acceso a html en el cual puede llevar codigo ruby

Migracion son archivos que se encargan de hacer modificaciones ala bd

form_for es un formulario


```Codigo ruby
<%= imprime en la pagina web>
<% evalua el codigo de la pagina %>

Aplication controller es el controlador del framework

<% [1,2,3,4].each do |number| %>
<p>Numero: <%= number %>
<%end%>

```
* __Patron:__ Usa MVC

* __Promueve:__ buenas practicas de desarrollo

### 2. PASOS
* __Paso 1:__ para crear el proyecto rails new webrails

* __Paso 2:__ rails server arranca un servidor  que arranca con WEBrick que es el que nos va a permitir visualizar la web.

* __Paso 3:__ para generar un controlador es rails generate controller welcome index y el index es un metodo que crea en ese controlador.

* __Paso 4:__ descargar un flexbox y ponerlo en stylesheet


* __Paso 5:__ Generador de modelos rails generate model Article title:string body:text visits_count:integer

* __Paso 6:__ cuando instale una gema debo hacer bundle install y creo la bd con rake db:create

     rake db:migrate RAILS_ENV=development para corregir problema de migraciones

    rake db:rollback hace operaciones inversas ala tabla es decir eliminar la tabla y las mofidicaciones delos campos y despues de eso escribo rake:db migrate 

```Modelo
=> la tabla => articles
=> campos => article.title() devuelve el titulo del articulos o cualquier otra tabla

```

* __Paso 7:__ abro la consola de ruby con rails console

  nombre modelo.all ---> select
```ModeloBD
  SELECT "geolocations".* FROM "geolocations"
  GET pongo en routes post y en index.html.erb pongo <%= link_to "Recurso con POST","/welcome/index", method: :post %>
  COLOR #15959F
  POST
  PATCH
  PUT
  DELETE
```

* __Paso8:__ para pasar datos ala vista desde el controlador utilizamos variables de clase @
y sin el @ significa que solo se quedan en el controlador

* __Paso9:__ ActiveRecord es una interfaz que mapea la bd y nos permite comunicarnos con ella atravez de objetos en lugar de utilizar SQL

     *  + Rojo ya que nos podemos pasar facilmente a otras bd

* __Paso10:__ Vistas parciales son las que tienen como formato _.form.html.erb, es decir layout que  se comparte en todas las paginas web

* __Paso11:__ Cuandos se quiere instalar una gema se va a rubygem y luego a documentacion y de ahi siempre que se ponga una gema se debe hacer bundle install

* __Paso12:__ rails g devise:install
y luego en layout aplication.html.erb depues de generar el devise se tiene que generar el modelo
rails g devise User

 luego se añade en la migracion nueva creada t.string :name
 t.string :permission_level
y se procede a migrar la bd rake db:migrate

* __Paso13:__ 

hago rails g devise:views
### 3. 