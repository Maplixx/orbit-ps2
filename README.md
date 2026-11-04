# ORBIT PS2

ORBIT PS2 é uma bancada de emulação local para navegador, com visual inspirado em superfícies translúcidas e controles glass. A interface é responsiva para PC, Android e iOS, e foi pensada para publicação estática no GitHub Pages.

## O que já funciona

- Biblioteca local com busca, ordenação e persistência dos metadados no `localStorage`.
- Importação de arquivos locais por seletor ou arrastar e soltar; os arquivos não são enviados a um servidor.
- Sessão de demonstração com canvas animado, estados de espera, execução, pausa, retomada, reinício e encerramento.
- Controles virtuais touch, teclado, suporte a gamepad conectado e tela cheia.
- Ajustes de vídeo, áudio, scanlines, tema e preferências de interface.
- Layout responsivo com navegação lateral no desktop e tab bar inferior em telas pequenas.

## Rodar localmente

```bash
python3 -m http.server 3000
```

Abra `http://localhost:3000`.

## GitHub Pages

O workflow em `.github/workflows/pages.yml` publica o conteúdo estático a cada push em `main`. No GitHub, confirme em **Settings → Pages** que a fonte está configurada para **GitHub Actions**.

## Nota sobre emulação real

Esta entrega implementa a bancada, o fluxo de importação local e o runtime visual de demonstração. Um core PS2 real exige um módulo WASM dedicado, compatibilidade de navegador, BIOS fornecida pelo usuário e uma estratégia de distribuição compatível com licenças. Por isso o produto sinaliza claramente a cena demo em vez de afirmar que uma ROM PS2 está sendo executada sem esse core conectado.
