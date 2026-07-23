## Passo a Passo

### Passo 1

Aqui temos um input que retorna o comando ping para somente o IP 8.8.8.8

<img width="626" height="181" alt="image" src="https://github.com/user-attachments/assets/f804026f-1c82-42d6-b7a4-731aa9738898" />

Vamos testar então se o input está devidamente sanitizado. Usaremos um Command Injection para isso, o comando fica assim:
```bash
8.8.8.8 ; ls
```

<img width="628" height="220" alt="image" src="https://github.com/user-attachments/assets/0fe83e72-e33c-4a0a-ac8c-b76e865ce65b" />

É retornado o resultado do ping, mas também é voltado o comando `ls`, ou seja, a aplicação é vulnerável a commando injection

### Passo 2

Agora que sabemos a vulnerabilidade, vamos explora-la.

O comando `ls` retornou dois arquivos, o primeiro é `flag.txt` e o segundo é `script.sh`. Então vamos ler o primeiro arquivo com o seguinte input:
```bash
8.8.8.8 ; cat flag.txt
```

<img width="624" height="202" alt="Captura de tela 2026-07-23 193634" src="https://github.com/user-attachments/assets/2663360d-9bda-4456-9022-0a26bc2474a5" />

E com isso conseguimos a flag do desafio

### FLAG: picoCTF{p1nG_c0mm@nd_3xpL0it_su33essFuL_e003709d}
