# Análise de Desempenho Criptográfico
Desenvolva um programa (java) que utiliza a criptografia de chave pública e simétrica conforme requisitos abaixo:

Desenvolva um programa (java) que utiliza a criptografia de chave pública e simétrica conforme requisitos abaixo:

1. O programa deve cifrar o texto: “RSA é um algoritmo que deve o seu nome a três professores do MIT: Ronald Rivest, Adi Shamir e Leonard Adleman”.

2. O programa deve cifrar o texto utilizando as seguintes técnicas:
a. Utilizando o algoritmo RSA com chave pública de 1024 bits.
b. Utilizando o algoritmo RSA com chave privada de 1024 bits.
c. Utilizando o algoritmo RSA com chave pública de 2048 bits.
d. Utilizando o algoritmo RSA com chave privada de 2048 bits.
e. Utilizando o algoritmo RSA com chave pública de 4096 bits.
f. Utilizando o algoritmo RSA com chave privada de 4096 bits.
g. Utilizando o algoritmo RSA com chave pública de 8192 bits.
h. Utilizando o algoritmo RSA com chave privada de 8192 bits.
i. Utilizando o algoritmo AES com chave de 16 bytes.
3. O programa deve calcular o tempo de execução do experimento, incluindo a geração de chaves.

4. Cada uma das técnicas deve ser executada pelo menos três vezes. É recomendado que o processo não seja automatizado, para que o resultado não utilize cache.

5. Finalmente, cifre o texto utilizando o algoritmo RSA com chave de 512 bits.

Desenvolva um relatório descrevendo o experimento executado. O relatório deve descrever o resultado das execuções, realizando uma análise do tempo de resposta das diversas técnicas. Adicionalmente, deve ser entregue o código fonte.

## Resultado da análise criptográfica
|descrição|1ª execução|2ª execução|3ª execução|
|-|-|-|-|
|RSA com chave pública de 1024 bits|360 milisegundos|171 milisegundos|174 milisegundos|
|RSA com chave privada de 1024 bits|310 milisegundos|173 milisegundos|175 milisegundos|
|RSA com chave pública de 2048 bits|496 milisegundos|190 milisegundos|186 milisegundos|
|RSA com chave privada de 2048 bits|553 milisegundos|190 milisegundos|186 milisegundos|
|RSA com chave pública de 4096 bits|1869 milisegundos|263 milisegundos|241 milisegundos|
|RSA com chave privada de 4096 bits|1262 milisegundos|245 milisegundos|252 milisegundos|
|RSA com chave pública de 8192 bits|20480 milisegundos|435 milisegundos|443 milisegundos|
|RSA com chave privada de 8192 bits|25203 milisegundos|442 milisegundos|442 milisegundos|
|AES com chave de 16 bytes|64 milisegundos|66 milisegundos|62 milisegundos|
|RSA com chave pública de 512 bits|Impossível realizar tal operação, texto é muito grande, ultrapassa 53 bytes|
|RSA com chave privada de 512 bits|Impossível realizar tal operação, texto é muito grande, ultrapassa 53 bytes|

**Relátorio**: A maior diferença nas contagens está na primeira execução, pois o computador leva um certo tempo para gerar e gravar a chave, uma vez gravada ela é usada muito mais rapidamente pelas outras execuções, claro que a mudança de computador para um melhor ou pior do que esse que foi feito o teste, trará mudanças significativas para os tempos vistos, já a ultima encriptação não pode ser feita pois o texto é muito maior do que o método RSA de 512 bits pode suportar, para fins de comparação fiz um teste tentando encriptar a frase "Teste" e obtive sucesso com um tempo estimado de 174 milisegundos.
