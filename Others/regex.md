## Expressões regulares

 Também conhecidas como regex são padrões que descrevem um conjunto de cadeias de caracteres. Na programação, as expressões regulares são usadas para verificar se uma determinada string (cadeia de caracteres) está em conformidade com um determinado padrão.

Uma expressão regular é composta de caracteres literais e metacaracteres que definem o padrão a ser correspondido. Por exemplo, um metacaracteres como o ponto (.) corresponde a qualquer caractere único, enquanto um conjunto de colchetes ([ ]) corresponde a qualquer caractere dentro do conjunto. As expressões regulares são usadas em muitas linguagens de programação, incluindo Java.

Aqui está um exemplo de função de validação de CPF em Java que utiliza expressões regulares:

```Java
public static boolean validarCPF(String cpf) {
    String regex = "\\d{3}\\.\\d{3}\\.\\d{3}\\-\\d{2}"; // padrão de CPF com pontos e hífen
    if (!cpf.matches(regex)) { // verifica se a string cpf corresponde ao padrão regex
        return false;
    }
    // mais código para verificar se o CPF é válido de acordo com o algoritmo do CPF
    return true;
}
```
Neste exemplo, a expressão regular é representada pela string \\d{3}\\.\\d{3}\\.\\d{3}\\-\\d{2}. Esta expressão regular representa um CPF formatado com pontos e hífen, onde \d corresponde a um dígito numérico e {3} significa que o padrão deve se repetir três vezes. O ponto e o hífen são caracteres literais que devem ser correspondidos exatamente. A função matches é usada para verificar se a string cpf corresponde ao padrão regex. Se não corresponder, a função retorna false. Caso contrário, a função continua a verificar se o CPF é válido de acordo com o algoritmo do CPF e retorna true ou false dependendo do resultado da verificação.

Em resumo, as expressões regulares são uma poderosa ferramenta de programação que permitem a correspondência de padrões em strings. Elas são amplamente usadas em validação de dados, busca e substituição de texto, filtragem de dados, entre outras tarefas.