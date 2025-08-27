> DEV >>> VM022330.detran.reders 
> 
> HML >>> VM022331.detran.reders
> 
> sinara charlie2018


> clear       limpa tela
> 
> pwd         mostra  o diretório
> 
> cd          vai para o home
> 
> cd /        vai para a raiz
> 
> ls          mostra conteudo 
> 
> ls ./ideias  mostra o conteudo do diretorio ideias
> 
> ls -al     estamos somando as opções de exibição de todos os arquivos, inclusive os ocultos, e a exibição de mais  
>              algumas informações, como as permissões de cada um desses itens que estão dentro desse diretório.

--- 
A letra d indica que esse primeiro é o diretório,

O xr se refere as permissões de grupo, o x são outras permissões. Depois, o primeiro sinara se refere a pessoa proprietária, que no caso é a pessoa usuária que criou, e o segundo sinara ao grupo. 

O 4096 parece um número aleatório, mas nada mais é do que o tamanho desse item em bytes. Por fim, temos a data de modificação deles.
--- 

## cria diretório 

mkdir dir1    cria diretório 

mkdir dir1 dir3/sub3 dir4 dir5  correto  mkdir -p, dir3/sub3   

O -p faz exatamente o que mencionamos: se a estrutura não existir, ele cria para nós.



touch a1.txt a2.txt a3.txt     O comando touch cria um arquivo vazio. 

echo teste > a10.txt     

Isso só está aqui para comprovar o que fizemos: touch cria arquivo vazio; echo cria arquivo com conteúdo.

Qual é o conteúdo? Nós já podemos usar o comando cat, que exibe o conteúdo de arquivos de texto: cat a10.txt

## mv diretorio novonomediretorio

Descobriremos como renomear um diretório ou um arquivo no ambiente Linux. O que faremos é usar o comando referente a move, o mv. Mas, ao invés de especificarmos um caminho para o qual esse diretório ou arquivo vai, especificaremos o nome atual e o nome que desejamos renomear.