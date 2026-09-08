# Sistema de Controle de Acesso - Aniversário de 15 Anos da Rebeca

## Descrição do Minimundo
Organizar a festa de 15 anos da Rebeca envolve o controle rigoroso da lista de convidados para garantir a segurança, o conforto dos presentes e evitar a entrada de acompanhantes não autorizados ou penetras. O sistema automatiza a emissão de convites digitais com QR Code individual para cada membro da família e realiza a validação nominal na portaria do evento.

## Contexto da Aplicação
O sistema será utilizado por três perfis de usuários:
- **Pais/Responsáveis:** Administram o evento e aprovam a lista final de convidados.
- **Aniversariante (Rebeca):** Define a lista de amigos e familiares convidados para o evento.
- **Portaria / Recepção:** Realiza o check-in dos convidados no dia da festa de 15 anos através da leitura do QR Code individual.

## Regras de Negócio
1. Os Pais/Responsáveis organizam a festa de 15 anos da Rebeca.
2. Cada convidado (seja titular ou familiar/acompanhante) possui o seu próprio **Convite e QR Code individual e exclusivo**.
3. A entrada no evento é liberada exclusivamente mediante a leitura do QR Code individual e validação do nome cadastrado no RSVP.
4. O registro de check-in é único por QR Code, invalidando o código imediatamente após o primeiro uso para impedir a entrada em duplicidade ou reuso por terceiros.

## Principais Processos
- **Cadastro do Evento:** Registro dos dados da festa de 15 anos (data, horário e local).
- **Gerenciamento de Convites:** Emissão de QR Codes individuais para cada membro cadastrado na família.
- **Confirmação de Presença (RSVP):** Coleta e validação do nome completo de cada convidado.
- **Controle de Portaria:** Leitura do QR Code, validação nominal na lista e registro da data/hora de entrada.
