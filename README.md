Generics em Java são um recurso que permite criar classes, interfaces e métodos que operam com tipos de dados especificados no momento da instância.
Eles ajudam a criar código mais flexível e reutilizável, além de aumentar a segurança em tempo de compilação, evitando erros de tipo.

Por que usar Generics?
Segurança de Tipo: Você pode garantir que uma coleção (como um List ou Set) contenha apenas elementos de um tipo específico.
Reutilização de Código: Generics permitem que você escreva métodos e classes que funcionem com qualquer tipo de dado.
Legibilidade e Manutenabilidade: O código se torna mais claro e mais fácil de entender.

Limitações e Uso Avançado
Generics não funcionam com tipos primitivos (como int, char, etc.). Então, você deve usar suas classes wrapper (Integer, Character, etc.).

QUAIS OS PONTOS NEGATIVOS DO USO DE GENERICS
Embora os generics em Java ofereçam muitos benefícios, como segurança de tipo e reutilização de código, eles também têm algumas limitações e desvantagens. Aqui estão alguns pontos negativos de se usar generics em Java:

1. Complexidade de Código
O uso de generics pode aumentar a complexidade do código, tornando-o mais difícil de ler e entender, especialmente para desenvolvedores que não estão familiarizados com o conceito.

2. Erasure de Tipos (Type Erasure)
Java implementa generics usando erasure de tipos, o que significa que a informação de tipo genérico é removida em tempo de compilação. Isso resulta em:

Incapacidade de Usar Tipos Primitivos: Você não pode usar tipos primitivos (como int, char) diretamente como tipos genéricos; deve usar suas classes wrapper (como Integer, Character).
Informações de Tipo Limitadas em Tempo de Execução: Você não pode obter informações de tipo genérico em tempo de execução devido ao apagamento de tipos.
3. Não Suporta Sobrecarga de Métodos
Devido ao apagamento de tipos, você não pode ter dois métodos que diferem apenas nos seus parâmetros genéricos.

4. Incompatibilidade com Arrays
Arrays e generics não se misturam bem. Por exemplo, não é permitido criar instâncias de arrays de tipos genéricos:

5. Avisos de Erro (Unchecked Warnings)
Você pode encontrar avisos de tipo não verificado em tempo de compilação ao trabalhar com tipos genéricos, especialmente ao misturar código legado com genéricos. Esses avisos indicam que o compilador não pode garantir a segurança de tipo em tempo de execução.

6. Desempenho
Embora os genéricos não adicionem overhead em termos de desempenho em tempo de execução devido ao apagamento de tipos, a conversão de tipos (casting) e o uso de classes wrapper para tipos primitivos podem introduzir alguma sobrecarga.
