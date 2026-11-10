# ◈ MindVault

Uma aplicação independente de microaprendizagem, gratuita, sem anúncios, sem subscrições e criada para instalar no iPhone ou Android como PWA.

## Funcionalidades
- 70 ideias **originais** em português de Portugal, em 10 temas
- Feed personalizado pelos interesses selecionados
- Explorar e pesquisar por tema, título e texto
- Guardar ideias sem limites artificiais
- Histórico de leitura, objetivo diário, sequência de dias
- Revisão ativa com perguntas de escolha múltipla
- Notas pessoais por ideia
- Leitura áudio usando as vozes do dispositivo (Web Speech API; o suporte a pt-PT varia)
- Partilha nativa e cópia de texto
- Offline depois da primeira visita online (service worker)
- Exportação/importação de backup JSON
- Design responsivo e instalação no ecrã principal

## Publicar gratuitamente no GitHub Pages
1. Cria um repositório GitHub, por exemplo `mindvault`.
2. Carrega **todos os ficheiros desta pasta**, mantendo as subpastas `.github/workflows` e `assets`.
3. Certifica-te de que a branch se chama `main`.
4. Abre **Settings → Pages → Build and deployment → Source → GitHub Actions**.
5. Abre **Actions** e verifica que a execução `Publish MindVault to GitHub Pages` termina com sucesso.
6. A tua app ficará acessível em `https://TEU-UTILIZADOR.github.io/mindvault/` (substitui o nome de utilizador e repositório pelos teus).
7. Abre o endereço no telemóvel e adiciona-o ao ecrã principal.

Não precisas de Node.js, npm, base de dados, API nem chave de acesso. Usa apenas HTML, CSS e JavaScript.

## Instalar no telemóvel
- **iPhone (Safari):** abrir o link → Partilhar → Adicionar ao ecrã principal → Adicionar.
- **Android (Chrome):** abrir o link → menu ⋮ → Instalar aplicação ou Adicionar ao ecrã principal.

## Testar no computador
Podes abrir `index.html` para testar a maioria das funções. Para testar a instalação PWA e offline usa um servidor local:

```bash
python -m http.server 8000
```

Abre http://localhost:8000 (service workers requerem HTTPS ou localhost).

## Conteúdos e direitos
Os textos incluídos são originais e foram escritos para esta aplicação. Não se copiou a interface, a marca ou o conteúdo proprietário da Deepstash. Conceitos gerais são apresentados em texto próprio; não são resumos oficiais de obras citadas. Se adicionares material de terceiros, respeita a licença e atribuição correspondentes.

Para adicionar conteúdo, edita o array `window.IDEAS` em `data.js` no formato `[tema, título, explicação, exercício, conceito]`. Mantém os IDs existentes estáveis para não corromper referências da biblioteca pessoal quando atualizares a app.

## Limitações honestas
- Os dados ficam no `localStorage` deste browser/dispositivo. **Não existe sincronização entre telemóvel e computador.** Usa Exportar/Importar para mudar de dispositivo.
- Limpar dados do browser pode apagar o progresso. Faz backups.
- O áudio depende das vozes disponíveis no sistema; pode não funcionar offline em todos os dispositivos.
- As notificações automáticas e resumos gerados por IA não estão incluídos, pois exigiriam serviços adicionais ou integração externa.
- O catálogo inicial tem 70 ideias, não os milhares de ideias da Deepstash. Pode crescer através de conteúdo original adicional.
- O quiz é uma primeira versão de recuperação ativa, não um algoritmo clínico ou científico avançado de repetição espaçada.

## Licença
Código distribuído sob licença MIT — vê `LICENSE`. Os conteúdos originais em `data.js` são disponibilizados para este projeto, sem autorização para os fazer passar por conteúdos oficiais da Deepstash.
