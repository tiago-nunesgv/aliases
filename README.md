<h1 align="center">
Para navegar de forma confortavel pelos diretorios 
</h1>

Os usuários do Linux geralmente precisam usar um comando repetidamente. Digitar ou copiar o mesmo comando repetidamente reduz sua produtividade e o distrai do que você está realmente fazendo.

Você pode economizar algum tempo criando aliases para os comandos mais usados. Os aliases são como atalhos personalizados usados para representar um comando (ou conjunto de comandos) executado com ou sem opções personalizadas. Provavelmente, você já está usando aliases no seu sistema Linux.


* Exemplo:

|comando|resultado|
|-------|----------|
|alias docs="cd ~/Documentos"|docs|

* Neste exemplo criamos um apelido para o comando de cd ~/Documentos, sempre que quisermos acessar a pasta Ducumentos é so digitar docs .

> sempre qui tiver que fazer o mesmo comando por varias veses é bom criar aliases.

* caso queira remover um ou todos os aliases execute os comandos abaixo:
```
$ unalias alias_name [remove um alias]

$ unalias -a  [remove todos os alias]

-----
