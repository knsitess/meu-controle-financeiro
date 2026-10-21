# Meu Controle Financeiro

Aplicação web em português para registrar receitas e despesas, acompanhar saldo disponível e reserva separadamente, e gerenciar metas mensais e futuras.

## Executar localmente
```bash
npm install
npm run dev
```

## Build de produção
```bash
npm run build
npm run preview
```

## Persistência atual
Os dados ficam no armazenamento local do navegador (`localStorage`) deste dispositivo e navegador. Eles não sincronizam entre dispositivos e não substituem um banco de dados remoto. Antes de usar com dados sensíveis ou publicar para uso multi-dispositivo, configure autenticação e banco de dados (por exemplo, Supabase) com políticas de acesso por usuário.

## Regras financeiras
- Receitas aumentam o saldo disponível.
- Despesas reduzem o saldo disponível e contam uma única vez.
- Transferências entre saldo disponível e reserva não são despesas.
- Depósitos e retiradas são considerados no cálculo da reserva.
- Metas não alteram saldo por si só; registre o movimento financeiro correspondente separadamente.
