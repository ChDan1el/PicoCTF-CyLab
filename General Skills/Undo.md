##### [Link do Desafio](https://learn.cylabacademy.org/library/766?page=1&category=5)

## Passo a Passo

### Passo 1
Ao conectar com o desafio recebemos a seguinte string codificada em base64:
> KTBxcDI0bnIwLWZhMDFnQHplMHNmYTRlRy1nazNnLXRhMWZlcmlyRShTR1BicHZj

Para decodificar uma string base64 no terminal linux usamos o seguinte comando:
```bash
echo 'stringbase64' | base64 -d
```

Então o comando a ser usado é o `base64 -d`

<img width="627" height="228" alt="image" src="https://github.com/user-attachments/assets/976b1346-bc37-472d-a87a-21099e984e58" />

### Passo 2 
Agora temos uma string que devemos inverter a ordem dos caracteres:
> )0qp24nr0-fa01g@ze0sfa4eG-gk3g-ta1ferirE(SGPbpvc

O comando padrão é:
```bash
echo 'stringrev' | rev
```
Então usaremos o comando `rev`

<img width="503" height="88" alt="image" src="https://github.com/user-attachments/assets/964d11ca-ddad-4a5d-8973-55aace24186a" />

### Passo 3

Nesse momente precisamos substituir os '-' por '_' na string:
> cvpbPGS(Eriref1at-g3kg-Ge4afs0ez@g10af-0rn42pq0)

O comando padrão é:
```bash
echo 'string' | tr 'antigo' 'novo'
```

Então o comando é : `tr '-' '_'`

<img width="516" height="91" alt="image" src="https://github.com/user-attachments/assets/b40f3fa7-a488-43df-826c-311a9d90af85" />

### Passo 4

Devemos agora substituir os '()' por '{}'

Então o comando fica o seguinte: `tr '()' '{}'`

<img width="507" height="86" alt="image" src="https://github.com/user-attachments/assets/0a940520-4b34-4416-9bdd-05a68485459a" />

### Passo 5

Por fim para obtermos a flag, devemos transladar os caracteres da string 13x para a direita, ou seja, aplicar ROT13

O comando padrão é:
```bash
echo 'string' | tr 'A-Za-z' 'N-ZA-Mn-za-m'
```

<img width="531" height="129" alt="Captura de tela 2026-07-23 191931" src="https://github.com/user-attachments/assets/d19432a6-e079-4fc6-95d3-ec3813bd3ce7" />


## FLAG: picoCTF{Revers1ng_t3xt_Tr4nsf0rm@t10ns_0ea42cd0}
