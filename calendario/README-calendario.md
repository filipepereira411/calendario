# GitHub × Google Calendar

Dashboard HTML estático que sincroniza:

- issues e pull requests abertos via GitHub API;
- milestones com prazo via GitHub API;
- eventos dos próximos 30 dias através de um URL ICS público do Google Calendar;
- conflitos no mesmo dia entre GitHub e Calendar.

## Usar

1. Publique ou partilhe o calendário no Google Calendar.
2. Copie o **endereço secreto no formato iCal** (`.ics`).
3. Abra `index.html` num servidor local ou GitHub Pages.
4. Preencha o URL ICS e clique em **Sincronizar**.

A página atualiza automaticamente a cada 15 minutos. As configurações ficam no `localStorage` do navegador.

## Nota de segurança

O HTML não inclui OAuth nem credenciais privadas. Para calendários privados, o URL ICS secreto ficará exposto no navegador; para uso em produção, substitua o ICS por um backend/Worker com OAuth e mantenha os segredos no servidor.
