AdonisJs é uma coleção de vários pacotes originais construídos em torno do [núcleo do framework](https://github.com/adonisjs/core). Sempre que você nos ouvir mencionando sobre a versão do AdonisJS, assuma que estamos falando sobre a versão do núcleo do framework.

Todos os outros pacotes como `@adonisjs/lucid` ou `@adonisjs/mail` têm suas próprias versões independentes e são livres para ter seu próprio ciclo de lançamento.

## Seguindo semver
Seguindo em frente, seguiremos estritamente o [versionamento semântico](https://semver.org/). Isso também significa que o que é o Adonis 5 hoje, pode rapidamente se tornar o Adonis 8 em alguns meses, se introduzirmos e publicarmos novas alterações não retrocompatíveis.

- Iremos aumentar a versão do patch, ao lançar **correções de bugs críticos** (ex: 5.2.0 a 5.2.1).
- A versão secundária inclui **novas funcionalidades** ou **correções de bugs não-críticos**. Além disso, descontinuaremos o uso de APIs em um lançamento de versão secundária (ex: 5.2.0 to 5.3.0).
- Ao liberar alterações não retrocompatíveis, aumentaremos a versão principal (ex: 5.2.0 to 6.0.0).

## Introduzindo mudanças não retrocompatíveis
Conforme o AdonisJS vai amadurecendo, tomaremos responsabilidade de não introduzir mudanças não retrocompatíveis periodicamente e todas as mudanças não retrocompatíveis **devem passar por uma fase de descontinuidade e uma fase RFC**

Antes de introduzir mudanças não retrocompatíveis, publicaremos um [RFC](https://github.com/adonisjs/rfcs) discutindo as motivações por trás da mudança. Se não houver um grande retrocesso, prosseguiremos com a mudança.

A fase inicial da mudança descontinuará as APIs existentes durante uma versão secundária. A execução de seu aplicativo após essa alteração terá muitos avisos, mas nada irá quebrar e continuará a funcionar como está.

Após uma fase de espera de no mínimo 4 semanas, durante o lançamento de uma próxima versão principal, removeremos as APIs descontinuadas. Remover o código antigo/morto é importante para garantir que a base de código do framework seja bem mantida e não inchada com todas as variações anteriores.

As mudanças a seguir não estão submetidas ao processo das mudanças não retrocompatíveis:

- **APIs não documentadas e estruturas de dados internas** podem ser modificadas em qualquer lançamento. Então se você depende de alguma API não documentada ou atributos privados de classes, você estará por sua conta, quando alterarmos ou restruturarmos eles.
- **Versões alpha e next do AdonisJS** podem receber mudanças não retrocompatíveis sem um aumento da versão principal. Queremos liberdade criativa para iterar rapidamente sobre nossos aprendizados no período alpha.

## Ciclo de lançamento
O AdonisJS segue um ciclo de lançamento de 8 semanas para o envio de novas funcionalidades ou publicação de mudanças não retrocompatíveis. As correções de bugs críticos e patches de segurança geralmente são lançados imediatamente.

Você pode checar nosso [roadmap no Trello](https://trello.com/b/3klaHbfP/adonisjs-roadmap) e [o que tem no próximo cartão de lançamento](https://trello.com/c/1qTLaVPl/44-may-2021) para saber sobre as mudanças futuras.
