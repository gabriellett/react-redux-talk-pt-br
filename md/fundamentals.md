# Como funciona?

------

Declarativo<!-- .element class="fragment" -->

Baseado em Componentes<!-- .element class="fragment" -->

One-way data flow<!-- .element class="fragment" -->

------

## Declarativo

O que eu quero

e não como eu quero<!-- .element class="fragment highlight-red" -->

------

<div class="split">
	<div class="split-col-50">
		Imperativo
		<pre class="language-javascript"><code>
var onChange = function(){
  text = $(input).val();
  $("div text").text(text);
});

$("input").on('change', onChange);
		</pre></code>
	</div>
	<div><!-- .element class="fragment split-col-50" -->
		Declarativo
		<pre class="language--clean  language-jsx"><code>
&lt;div className="text"></span>
  {text}
&lt;/div>
		</pre></code>
	</div>
</div>

------

O React faz o trabalho de atualizar a interface pra você

É uma interface REATIVA <img class="fragment gotcha" src="img/gotcha.gif"/>


------

## Componentes

Componentes everywhere

------

<pre class="language-jsx"><code>
class HelloMessage extends React.Component {
  render() {
    return &lt;div>Hello {this.props.name}&lt;/div>;
  }
}

ReactDOM.render(&lt;HelloMessage name="Jane" />, mountNode);
</pre></code>

------

Aaaaaaa mas como assim Javascript junto com HTML que loucura!

Calma, vai passar <!-- .element class="fragment highlight-green" -->

prometo <!-- .element class="fragment highlight-green" -->

------

### Sim, JS + HTML!
ou
### JSX

------

#<a href="https://twitter.com/iamdevloper/status/598435575662813184"><img src="img/iamdeveloper-jsx.png"/></a>

------

Componentes de React com JSX permitem você construir pedaços de negócio, e não pedaços de bibliotecas

mas como que o browser renderiza? <!-- .element class="fragment highlight-green" -->

no final, tudo compila pra JavaScript mesmo :) <!-- .element class="fragment" -->

maaas, se não quiser não precisa usar JSX, é opcional <!-- .element class="fragment" -->

------

## Estado

Componentes podem ter estado!

<code>this.state</code> <!-- .element class="fragment" -->

------

## Ciclo de vida

* Mounting<!-- .element class="fragment" -->
* Updating<!-- .element class="fragment" -->
* Unmounting<!-- .element class="fragment" -->


------

<div class="split">
  <div class="split-col-70">
    <pre data-line="1,4,7" class="language-jsx language--clean language--small"><code>
class Timer extends React.Component {
  constructor(props) {
    super(props);
    this.state = {secondsElapsed: 0};
  }
  tick() {
    this.setState((prevState) => ({
      secondsElapsed: prevState.secondsElapsed + 1
    }));
  }
    </pre></code>
  </div>
  <div class="split-col-30">
    <p>1. Cria o componente</p>
    <p>4. Inicia o estado</p>
    <p>7. Atualiza o estado</p>
  </div>
</div>

------

<div class="split">
  <div class="split-col-70">
    <pre data-line="1,5" class="language-jsx language--clean language--small"><code>
  componentDidMount() {
    this.interval = setInterval(() => this.tick(), 1000);
  }

  componentWillUnmount() {
    clearInterval(this.interval);
  }
    </pre></code>
  </div>
  <div class="split-col-30">
    <p>1. Executa quando o componente renderiza no DOM<p>
    <p>5. Executa antes do componente ser destruido
  </div>
</div>

------

<div class="split">
  <div class="split-col-70">
    <pre data-line="3,8" class="language-jsx language--clean language--small"><code>
  render() {
    return (
      &lt;div>Seconds Elapsed: {this.state.secondsElapsed}&lt;/div>
    );
  }
}

ReactDOM.render(&lt;Timer />, mountNode);
    </code></pre>
  </div>
  <div class="split-col-30">
    <p>3. Obtem o valor do estado
    <p>8. Efetivamente renderiza o componente
  </div>
</div>

------

## One-way data flow

------

<img src="img/fundamentals_data_flow.png"/>


