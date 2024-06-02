# Simulador De Automatos

## Sobre
-
Projeto realizado para a disciplina de Teoria Da Computação, orientado pelo professor Wellington Della Mura, pela discente da Universidade Estadual Norte Do Paraná(UENP)
Simulador projetado em Python, sendo necessários 3 arquivos, "arqFile.aut" (arquivo em JSON com o automato definido), "arqTeste.in"(arquivo em CSV com as entradas definidas), e "arqSaida.out" (arquivo para receber as saídas, sendo elas 0 ou 1)
### Arquivo JSON
```json
{
  "initial": 0,
  "final": [3],
  "transitions": [
    {"from": 0, "read": "a", "to": 1},
    {"from": 1, "read": "b", "to": 2},
    {"from": 2, "read": "c", "to": 3},
    {"from": 3, "read": "a", "to": 1}, 
    {"from": 3, "read": "b", "to": 0},
    {"from": 3, "read": "c", "to": 0}
  ]
}
```
### Arquivo CSV: 
-
```CSV
abc;1
aabc;1
ababc;1
abcd;1
aabcc;0
ab;0
cabc;1
abcabc;1
abccba;0
```
### Arquivo De Saída:
-
```CSV
abc;1;1;0.0
aabc;1;0;0.0
ababc;1;0;0.0
abcd;1;0;0.0
aabcc;0;0;0.0
ab;0;0;0.0
cabc;1;0;0.0
abcabc;1;1;0.0
abccba;0;0;0.0
```
### Funcionamento
#### Para compilar, não utilizamos a interface digital, compilamos pelo CMD(prompt de comando), entretanto, para acessar foi necessário incluir o caminho da pasta onde está incluso todos os arquivos. Com o seguinte comando:
```bash
 C:\Windows\system32>cd C:\Users\End User\OneDrive\Área de Trabalho\automatos
```
#### Após o caminho da pasta, é necessário incluir o comando para acessar o código pelo CMD:
```bash
python main.py arqFile.aut arqTeste.in arqSaida.out
```

