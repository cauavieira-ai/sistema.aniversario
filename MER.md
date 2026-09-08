# Modelo de Entidade e Relacionamento (MER) - 15 Anos da Rebeca



## 1. Entidades



 **Responsavel:** Representa os pais da Rebeca (organizadores e responsáveis pelo evento).

- **Festa:** Representa o evento específico da Festa de 15 Anos da Rebeca.

- **Aniversariante:** Representa a Rebeca.

- **Convidado:** Representa cada pessoa individual cadastrada para comparecer à festa.

- **Convite:** Representa o passe/credencial digital (QR Code) individual gerado para cada convidado.

- **Portaria:** Representa o registro de check-in realizado na entrada do evento.



---



## 2. Relacionamentos e Cardinalidades



- **[Responsavel] (1,1) <Organizar> (1,n) [Festa]**

&#x20; -*Explicação:* Os Pais/Responsáveis organizam o evento da festa de 15 anos.

- **[Responsavel] (1,n) <Cadastrar> (1,1) [Aniversariante]**

&#x20; - *Explicação:* Os Responsáveis cadastram a Aniversariante (Rebeca) no sistema.

- **[Festa] (1,1) <Gerar> (1,n) [Convite]**

&#x20; - *Explicação:* A festa gera múltiplos Convites individuais para distribuição aos convidados.

- **[Aniversariante] (1,1) <Convidar> (1,n) [Convidado]**

&#x20; - \*Explicação:\* A Rebeca indica a sua lista de convidados para a festa.

- **[Convidado] (1,1) <Possuir> (1,1) [Convite]**

&#x20; - *Explicação:* Cada Convidado possui exatamente 1 Convite/QR Code exclusivo, e cada Convite pertence a apenas 1 Convidado.

- **[Convite] (1,1) <Validar> (0,1) \[Portaria]**

&#x20; - *Explicação:* Cada Convite/QR Code pode ter no máximo 1 registro de entrada na Portaria, queimando o código após o uso.



---



## 3. Sugestão de Atributos



### Responsavel

- `id_responsavel` (PK)

- `nome`

- `telefone`

- `email`



### Festa

- `id_festa` (PK)

- `nome_evento` (Ex: "15 Anos da Rebeca")

- `data_hora`

- `local`



### Aniversariante

- `id_aniversariante` (PK)

- `nome` (Ex: "Rebeca")

- `data_nascimento`



### Convidado

- `id_convidado` (PK)

- `nome_completo`

- `grupo_familiar` (Ex: "Família Silva" - agrupa os parentes no sistema)

- `eh_titular` (Booleano - indica o responsável pelo grupo familiar)

- `status_rsvp` (Pendente, Confirmado, Recusado)



### Convite

- `id_convite` (PK)

- `codigo_qr` (Único para cada convidado)

- `id_convidado` (FK - Vincula diretamente ao convidado)

- `status_convite` (Ativo, Utilizado, Cancelado)



### Portaria

- `id_entrada` (PK)

- `data_hora_entrada`

- `operador_portaria`



---



## 4. Diagrama Entidade e Relacionamento (DER)

<img width="1536" height="1024" alt="image" src="https://github.com/user-attachments/assets/6283b2b2-ce96-4da1-b60d-9db6a25235dd" />



