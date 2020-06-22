# Studing React-Context

- Utiliza-se **Context** quando se quer ter o _compartilhamento_ de um determinado componente disponível para todo o escopo do projeto (_globalmente_).

- Ele _não_ precisa ser gerado no _componente pai_, pode ser gerado em _qualquer componente filho_ e _qualquer outro componente filho_ poderá utilizá-lo, mesmo havendo alguns componentes que _não irão fazer uso dele_

Não é interessante manter o _context_ no componente _pai_, pois a medida que a aplicação vai crescendo a dificuldade para lidar com ele vai aumentando, o mais recomendado é criar um local que contêm todos os componentes que serão compartilhados.

- o **Provider** vai basicamente repassar para o componente pai e todos os seus filhos quais componentes serão compartilhados, então todo o conteúdo compartilhado deve sempre estar dentro de um **Provider**.

- De forma simples você consegue compartilhar estados da aplicação sem ter muitos problemas

### Verificações

- É sempre recomendável também haver uma verificação para saber se o componente está dentro de um **context**

```js
if (!context) {
  throw new Error("useCount must be used within a CountProvider");
} // Verifica se não existe um contexto, provavelmente se não existir, é porque não existe um **Provider** por volta do **App**
```
