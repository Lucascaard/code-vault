## API Fetch

A API Fetch é uma interface JavaScript moderna para recuperar recursos da rede. Ela fornece uma maneira fácil de buscar e enviar dados.

### Uso básico

```javascript
    fetch(url)
    .then(response => response.json())
    .then(data => console.log(data))
    .catch(error => console.error(error));
```

Neste exemplo, fetch é usada para buscar dados de uma URL. A chamada fetch(url) retorna uma promessa que resolve em um objeto Response. O método json() é chamado no objeto Response para analisar o corpo da resposta como JSON e retornar uma promessa que resolve em um objeto JavaScript. Finalmente, then é usado para imprimir o objeto JavaScript no console e catch é usado para lidar com quaisquer erros.

### Opções

A API Fetch oferece muitas opções para personalizar as solicitações de rede. Algumas das opções incluem:

method: O método HTTP a ser usado para a solicitação (GET, POST, etc.).
headers: Os cabeçalhos HTTP para serem incluídos na solicitação.
body: O corpo da solicitação, geralmente usado com o método POST.

```javaScript
    fetch(url, {
        method: 'POST',
        headers: {
            'Content-Type': 'application/json'
        },
        body: JSON.stringify(data)
    })
        .then(response => response.json())
        .then(data => console.log(data))
        .catch(error => console.error(error));

```

Neste exemplo, fetch é usada para enviar dados para uma URL usando o método POST. As opções são definidas como um objeto que é passado como o segundo argumento para fetch. O cabeçalho Content-Type é definido como application/json e o corpo da solicitação é convertido em uma string JSON usando JSON.stringify().

### Suporte do navegador

A API Fetch é suportada em todos os principais navegadores, incluindo Chrome, Firefox, Safari e Edge. No entanto, alguns recursos podem não estar disponíveis em todos os navegadores.