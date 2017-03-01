# Melhores Praticas

------

<ul>
  <li class="fragment"> *PropTypes* </li>
  <li class="fragment"> *Presentational Components* e *Container Components* </li>
  <li class="fragment"> *ECMA6* </li>
  <li class="fragment"> *ESLint* </li>
</ul>

------

## PropTypes

Typechecking === menos bugs :)

------

<pre class="language-jsx"><code>
class HelloMessage extends React.Component {
  render() {
    return &lt;div>Hello {this.props.name}&lt;/div>;
  }
}
</pre></code>

------

<pre class="language-jsx"><code>
class HelloMessage extends React.Component {
  render() {
    return &lt;div>Hello {this.props.name}&lt;/div>;
  }
}

HelloMessage.propTypes = {
  name: React.PropTypes.string.isRequired
};
</pre></code>

------

<pre class="language-jsx"><code>
MyComponent.propTypes = {
  // You can declare that a prop is a specific JS primitive. By default, these
  // are all optional.
  optionalArray: React.PropTypes.array,
  optionalBool: React.PropTypes.bool,
  optionalFunc: React.PropTypes.func,
  optionalNumber: React.PropTypes.number
  //...
</pre></code>

Lista completa [aqui](https://facebook.github.io/react/docs/typechecking-with-proptypes.html)

------

## Presentational Components
## e
## Container Components

------

### Presentational Components

<ul>
  <li class="fragment"> Como as coisas vão ser exibidas </li>
  <li class="fragment"> Não depende de actions e stores </li>
  <li class="fragment"> Não trabalha com a manipulação dos dados </li>
  <li class="fragment"> Dificilmente tem seu proprio estado </li>
  <li class="fragment"> São escritos geralmente como componentes funcionais </li>
</ul>

<div>Por exemplo: *SideBar, Link, List* </div><!-- .element class="fragment" -->

------

## Container Components

<ul>
  <li class="fragment"> Como as coisas vão funcionar </li>
  <li class="fragment"> Disponibilizam os dados para outros componentes </li>
  <li class="fragment"> Chama actions e gerencia callbacks </li>
  <li class="fragment"> Normlmanete possuem estado </li>
</ul>

<div>Por exemplo: *GoogleSideBar, CompanyPage, ItemsList* </div><!-- .element class="fragment" -->

------

### Beneficios

<ul>
  <li class="fragment"> Melhor componentização e reuso </li>
  <li class="fragment"> Logica separada da view </li>
</ul>

------

## ECMA6

<ul>
  <li class="fragment"> <code>class</code> </li>
  <li class="fragment"> <code>{ ...objectSpread }</code> </li>
  <li class="fragment"> <code>() => returnValue</code> </li>
  <li class="fragment"> etc </li>
</ul>
