# JOp-Forca-game
A final project where the creation of a chess game was requested.

Documentação - Jogo da Forca
Manual de Uso
Requisitos:
- Java JDK 17 ou superior instalado
Como Executar:
1. Compile os arquivos:
 javac br\edu\unoesc\jogo\*.java
2. Gere o arquivo .jar:
 jar cfe jogo-da-forca.jar br.edu.unoesc.jogo.Main br\edu\unoesc\jogo\*.class
3. Execute o jogo:
 java -jar jogo-da-forca.jar
Modelagem de Fluxo
1. Início
2. Sort realiza sorteio da palavra
3. Loop principal:
 - Usuário digita letra
 - Se letra já foi tentada -> volta
 - Se letra correta -> adiciona
 - Se todas adivinhadas -> vitória
 - Se errada -> adiciona
 - Se nº de erros > 6 -> derrota
4. Fim
Diagrama de Sequência (texto)
Main --> Sort: sortear()
Sort --> Main: retorna palavra
loop até ganhar/perder
 Main --> InterfaceJogo: perguntarLetra()
 InterfaceJogo --> Main: retorna letra
Documentação - Jogo da Forca
 alt letra correta
 Main: adiciona letra a corretas
 else
 Main: adiciona letra a erradas
 Main: exibirEstadoAtual()
end
Diagrama de Classes (texto)
+------------------+
| Sort |
+------------------+
| - palavras[] |
+------------------+
| +sortear():String|
+------------------+
+---------------------------+
| InterfaceJogo |
+---------------------------+
| +mostrarMensagem() |
| +perguntarLetra():String |
+---------------------------+
+--------------------------+
| Main |
+--------------------------+
| - palavraSecreta:String |
| - letrasCorretas:Set |
| - letrasErradas:Set |
+--------------------------+
| +main(String[]):void |
| -exibirEstadoAtual(...) |
| -todasLetrasAdivinhadas()|
Documentação - Jogo da Forca
+--------------------------+
