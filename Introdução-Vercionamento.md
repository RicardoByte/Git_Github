# O que é controle de versionamento

Controle de versionamento é o método utilizado para controle de um projeto onde há mais de um colaborador fazendo modificações dentre outras contribuições ao um mesmo arquivo/projeto, ou seja, surgiu como uma solução mais simples para o gerenciamento de projetos fazendo com que problemas como incompatibilidade de versões sejam contornados.

## Importância do controle versionamento

O software de controle de versão facilita a coordenação, o compartilhamento e a colaboração entre toda a equipe de desenvolvimento de software. Ele permite que as equipes trabalhem em ambientes distribuídos e assíncronos, gerenciem alterações e versões de código e artefatos, além de resolverem conflitos de merge e anomalias relacionadas.

--------------------------------------------------------------------------

# Tipos de sistemas de controle de versionamento

Os sistemas de controle de versionamento se dividem em dois grupos os centralizados e os distribuídos:

### VCS (Version Control System) Centralizado :

Estes controles tem como característica o compartilhamento simultâneo de um mesmo repositório de em um servidor central, usando controle de fonte centralizado, cada usuário faz commits diretamente no branch principal. Por isso, esse tipo de controle de versão costuma funcionar bem para equipes pequenas, pois os membros da equipe podem se comunicar rapidamente, evitando que dois desenvolvedores trabalhem no mesmo trecho de código ao mesmo tempo.

### Funcionamento

Sistemas de controle de versão centralizado, como CVS, Perforce e SVN, exigem que os usuários façam pull da versão mais recente do servidor para baixar uma cópia local em sua máquina. Depois disso, os colaboradores enviam por push os commits para o servidor e resolvem qualquer conflito de merge no repositório principal.

Importante salientar que ele permite o bloqueio de arquivos, de modo que qualquer parte do código que esteja sendo editada não fique acessível para outras pessoas, garantindo que apenas um desenvolvedor possa contribuir com o código por vez ( impossibilitando conflito em branches e ou commits de um ou mais desenvolvedores ). Os membros da equipe usam branches para contribuir com o repositório central, e o servidor desbloqueará os arquivos após os merges.

### Exemplos de VCS centralizados:

Os sistemas de controle de versão centralizados mais comuns são o Concurrent Versions System (CVS), o Perforce e o Subversion (SVN). Há também o Microsoft Team Foundation Server (TFS), que agora é conhecido como Azure DevOps Server.


--------------------------------------------------------------------------
# Vantagens:

### Funciona bem com arquivos binários[](https://about.gitlab.com/pt-br/topics/version-control/what-is-centralized-version-control-system/#funciona-bem-com-arquivos-binrios)

Arquivos binários, como recursos gráficos e arquivos de texto, exigem uma grande quantidade de espaço, por isso os desenvolvedores de software recorrem a sistemas de controle de versão centralizados para armazenar esses dados. Com um servidor centralizado, as equipes podem extrair algumas linhas de código sem precisar salvar todo o histórico na máquina local.

### Oferece visibilidade total[](https://about.gitlab.com/pt-br/topics/version-control/what-is-centralized-version-control-system/#oferece-visibilidade-total)

Com uma localização centralizada, todos os membros da equipe têm visibilidade total sobre em que código estão trabalhando atualmente e quais alterações foram feitas. Um sistema de controle de versão centralizado tem apenas dois repositórios de dados que os usuários precisam monitorar: a cópia local e o servidor central.

### Diminui a curva de aprendizado[](https://about.gitlab.com/pt-br/topics/version-control/what-is-centralized-version-control-system/#diminui-a-curva-de-aprendizado)

O controle de versão centralizado é fácil de entender e usar, então desenvolvedores de qualquer nível de habilidade podem enviar mudanças e começar a contribuir para a base de código rapidamente.


# Desvantagens

### Um único ponto de falha coloca os dados em risco[](https://about.gitlab.com/pt-br/topics/version-control/what-is-centralized-version-control-system/#um-nico-ponto-de-falha-coloca-os-dados-em-risco)

A maior desvantagem é o ponto único de falha presente no [servidor centralizado](https://git-scm.com/book/en/v2/Getting-Started-About-Version-Control). Se o servidor remoto ficar indisponível, ninguém poderá trabalhar no código ou enviar alterações. A falta de acesso offline significa que qualquer interrupção pode prejudicar significativamente o desenvolvimento do código e até resultar na perda dele. Todo o projeto e a equipe são interrompidos durante uma falha. 
### A velocidade lenta atrasa o desenvolvimento[](https://about.gitlab.com/pt-br/topics/version-control/what-is-centralized-version-control-system/#a-velocidade-lenta-atrasa-o-desenvolvimento)

A criação de branches se torna uma tarefa demorada que possibilita o surgimento de conflitos de merge, pois os desenvolvedores não conseguem enviar suas alterações para o repositório central rápido o suficiente para que outras pessoas possam consultá-las. Se os membros da equipe tiverem uma conexão de rede lenta, o processo de desenvolvimento de código se tornará ainda mais demorado ao tentarem se conectar com o servidor remoto.

### Poucos momentos estáveis para enviar alterações por push[](https://about.gitlab.com/pt-br/topics/version-control/what-is-centralized-version-control-system/#poucos-momentos-estveis-para-enviar-alteraes-por-push)

Um fluxo de trabalho centralizado pode ser ótimo para equipes pequenas, mas apresenta limitações quando equipes maiores tentam colaborar. Quando vários desenvolvedores querem trabalhar no mesmo trecho de código, fica difícil encontrar um momento estável para enviar por push as alterações. 

