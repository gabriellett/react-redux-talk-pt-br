# Redux

------

<blockquote class="blockquote--wide">
  <p>"Redux is a predictable state container for JavaScript apps."</p>
</blockquote>

------

<a href="https://twitter.com/dan_abramov/status/604356871722569728"><img src="img/dan_abramov-redux.png"/></a>

------

Oi? Flux?

------

<!-- .element data-transition="fade-up none"  -->

<img src="img/flux-flow.png"/>

------

<!-- .element data-transition="none fade-up"  -->
<img src="img/flux-to-redux.png"/>

------

Gerenciar o estado é dificil

Redux ajuda a gerenciar o estado! <!-- .element class="fragment" -->

------

## Redux 

* Actions <!-- .element class="fragment" -->
* Reducers <!-- .element class="fragment" -->

------

## Actions

Decreve o que acontece ou deve acontecer, mas não como

------

## Actions

Decreve o que acontece ou deve acontecer, mas não como

&nbsp; 

<pre class="language-jsx"><code>const ADD_TODO = 'ADD_TODO'
{
  type: ADD_TODO,
  text: 'Build my first Redux app'
} </pre></code>

&nbsp; 

------

<!-- .element data-transition="slide-in fade-out"  -->

## Reducers

*Funções puras* que gerenciam as transições de estado

------

<!-- .element data-transition="fade-in none"  -->

## Reducers

*Funções puras* que gerenciam as transições de estado

&nbsp; 

<pre class="language-jsx"><code> (state, action) => state; </pre></code>

&nbsp; 

&nbsp; 

------

<!-- .element data-transition="none slide-out"  -->

## Reducers

*Funções puras* que gerenciam as transições de estado

<pre class="language-jsx"><code> (state, action) => {
  switch (action.type) {
  case ADD_TODO:
    return [...state, action.todo];
  case RESET_TODOS:
    return [];
  }
}
</pre></code>

------

## Redux dev-tools = <span class="text-red">♥</span>

<img src="img/redux-dev-tools.gif" class="big-img"/>
