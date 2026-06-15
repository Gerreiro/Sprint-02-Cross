# Como rodar o GrassWatch

## Pré-requisitos
- Node.js 18+
- npm ou yarn
- Expo Go instalado no celular (App Store / Play Store)

## Passos

```bash
# 1. Entrar na pasta do projeto
cd grasswatch

# 2. Instalar dependências
npm install

# 3. Iniciar o servidor Expo
npx expo start
```

Depois de iniciar, escaneie o QR code com o **Expo Go** no celular.

## Estrutura do projeto

```
grasswatch/
├── App.tsx                          ← Raiz: estado global + navegação
├── src/
│   ├── types/
│   │   └── Ocorrencia.ts            ← Tipagem TypeScript
│   ├── data/
│   │   └── ocorrenciasMock.ts       ← Dados simulados (Motiva)
│   ├── components/
│   │   ├── OcorrenciaCard.tsx       ← Card da lista
│   │   ├── RiscoBadge.tsx           ← Badge baixo/médio/alto
│   │   └── SensorBanner.tsx         ← Alerta do sensor IoT
│   └── screens/
│       ├── ListaScreen.tsx          ← Tela 1: lista + filtros
│       ├── CadastroScreen.tsx       ← Tela 2: cadastrar ocorrência
│       └── DetalheScreen.tsx        ← Tela 3: visualizar detalhe
```

## Fluxo funcional

1. App abre na **Lista** com 4 ocorrências mockadas
2. Toque em qualquer card → vai para o **Detalhe**
3. Toque no **+** (FAB ou header) → vai para o **Cadastro**
4. Preencha os campos e toque em "Registrar" → salva no estado e volta para a Lista
5. A nova ocorrência aparece no topo da lista
