# [re]gene compradores

------

* React + Redux + Rails ?<!-- .element class="fragment" -->
* Organização<!-- .element class="fragment" -->
* Testes<!-- .element class="fragment" -->
* Caching<!-- .element class="fragment" -->

------

### Queremos usar react

<ul>
  <li>novo backend só pra compradores é *over engineering*</li><!-- .element class="fragment" -->
  <li class="fragment">Deve ter uma gem...
    <ul>
      <li>react-rails</li><!-- .element class="fragment" -->
      <li>react_on_rails</li><!-- .element class="fragment highlight-green" -->
    </ul>
  </li>
</ul>


------

### React on Rails

* Webpack<!-- .element class="fragment" -->
* Babel<!-- .element class="fragment" -->
* React<!-- .element class="fragment" -->
* Redux<!-- .element class="fragment" -->
<li> *React-Router*</li><!-- .element class="fragment" -->
* Não depende de jQuery<!-- .element class="fragment" -->
* Menor acoplamento<!-- .element class="fragment" -->

------

### Organização

<img src="img/regene-structure.png" class="big-img"/>

------

### Organização

* Gulp<!-- .element class="fragment" -->
  * Linting
  * Watching
* nested package.json <!-- .element class="fragment" -->
  * build
  * test
  * run
* Webpack<!-- .element class="fragment" -->
  * *compilar* o client
* Foreman<!-- .element class="fragment" -->
  * Rodar rails + watch do webpack junto

------

### Testes

* Mocha<!-- .element class="fragment" -->
* Chai<!-- .element class="fragment" -->
* Nock<!-- .element class="fragment" -->

------

### Caching do carrinho

* Redis + Middleware<!-- .element class="fragment" -->
<li>redux-storage + [redux-storage-engine-remoteendpoint](https://github.com/Bionexo/redux-storage-engine-remoteendpoint)</li><!-- .element class="fragment" -->

------

### Demo!

------

# Perguntas?

------

# Obrigado :)
