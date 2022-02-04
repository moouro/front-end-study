# Entenda a existência do Staging Area

É mais como um recurso do que uma obrigação de uso no Git.

É perfeitamente possível trabalhar com o Git sem nunca usar o Staging Area, e não há nenhum problema em abrir mão dela no seu dia-a-dia de desenvolvedor. Mas ela pode ser bem útil se souber como usá-la.

1. O principal uso dela é fazer com que você tenha mais controle de quais alterações quer commitar por vez, permitindo commits menores sem muito esforço extra para isto.

Imagine que você tenha feito uma porção de alterações em vários arquivos do seu projeto: script de banco de dados, arquivos de configuração, arquivos fonte, novas imagens inseridas, etc. É claro que você poderia fazer um único commit com tudo

`git commit -am "Funcionalidade XYZ` 

implementada. Imagens inseridas,  arquivos de configuração alterados, HTML de criar,  editar e excluir criados. 

- Scripts SQL inseridos para os novos parâmetros" Bem, será um senhor commit com uma senhora mensagem de commit.

- Talvez você gostaria de separar melhor os arquivos enviados a cada commit, deixando mais organizada as alterações feitas:

`git add config/application.yml`
`git commit -m "Configurações alteradas"`

`git add images/imagem1.jpg images/imagem2.jpg` 
`git commit -m "Novas imagens"`

e assim por diante.

Sem o Staging Area, você teria muito trabalho para fazer a mesma coisa: precisaria fazer um diff das alterações para salvar o que fez, deixar apenas o quer quer enviar no commit atual, salvar os arquivos binários em outro local até fazer o commit no qual elas vão, etc.
O Staging Area também pode ser usado em situações mais específicas, como quando você está no meio de uma implementação no código e surge algum bug que precisa ser corrigido antes. Você pode simplesmente corrigir o bug no arquivo, fazer um git add apenas do arquivo alterado e fazer o git push, sem se preocupar com as outras alterações.
