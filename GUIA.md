# Labamba Studio: como colocar o site no ar e editar

Tempo total: cerca de 30 minutos, mais a espera do domínio (até 24 h).
Custo: só o domínio (um .com.br custa cerca de R$ 40 por ano). GitHub, Netlify e Pages CMS são grátis.

Como as peças se encaixam:

- **GitHub** guarda os arquivos do site.
- **Netlify** publica o site e atualiza sozinha sempre que algo muda no GitHub.
- **Pages CMS** é o seu painel: formulários para editar contatos, logos, cases e imagens. Cada vez que você salva, ele grava no GitHub, e a Netlify atualiza o site em cerca de 1 minuto.

---

## 1. Subir os arquivos no GitHub

1. Crie uma conta grátis em https://github.com
2. Clique em **New repository** (botão verde ou no "+" do canto superior direito).
3. Nome: `labamba-site`. Pode deixar como **Private**. Clique em **Create repository**.
4. Na página que abrir, clique no link **uploading an existing file**.
5. Abra esta pasta no seu computador, selecione **tudo o que está dentro dela** (index.html, content.json, netlify.toml, a pasta img e este guia) e arraste para a página. Clique em **Commit changes**.
6. Confira se o arquivo **.pages.yml** subiu. Ele começa com ponto, e por isso o Mac e o Windows costumam escondê-lo:
   - Se ele não aparecer na lista do GitHub, clique em **Add file > Create new file**.
   - No nome, digite `.pages.yml`.
   - Abra o arquivo `.pages.yml` desta pasta num editor de texto (no Mac, aperte Cmd + Shift + . no Finder para ver arquivos ocultos), copie todo o conteúdo e cole no GitHub.
   - Clique em **Commit changes**.

## 2. Publicar na Netlify

1. Entre em https://app.netlify.com e crie a conta usando **Sign up with GitHub**.
2. Clique em **Add new site > Import an existing project > GitHub**.
3. Autorize e escolha o repositório `labamba-site`.
4. Deixe **Build command** vazio e **Publish directory** vazio (ou um ponto: `.`). Clique em **Deploy**.
5. Em cerca de 1 minuto o site está no ar num endereço provisório, tipo `nome-aleatorio.netlify.app`. Em **Site configuration > Change site name** você pode trocar para `labamba.netlify.app`, se estiver livre.

Esse link provisório já funciona e já pode ser enviado.

## 3. Conectar o domínio próprio

1. Compre o domínio em https://registro.br (por exemplo, `labambastudio.com.br`).
2. Na Netlify, abra o site e vá em **Domain management > Add a domain**. Digite o domínio e confirme.
3. Escolha **Set up Netlify DNS**. A Netlify vai mostrar **4 endereços de servidores DNS** (algo como `dns1.p01.nsone.net`).
4. No Registro.br, entre no domínio, clique em **Alterar servidores DNS** e cole os 4 endereços. Salve.
5. Aguarde a propagação, que normalmente leva de 1 a 24 horas. O cadeado de segurança (HTTPS) é ativado sozinho pela Netlify.

## 4. Ativar o painel (Pages CMS)

1. Entre em https://app.pagescms.org e clique em **Sign in with GitHub**.
2. Instale o app do Pages CMS e dê acesso ao repositório `labamba-site`.
3. Abra o repositório. No menu da esquerda vai aparecer **Site Labamba**.
4. Pronto: é só editar e clicar em **Save**. Em cerca de 1 minuto a mudança aparece no site.

### O que dá para editar no painel

- **Contatos:** e-mail, WhatsApp (número do botão e como aparece escrito), link do LinkedIn e o selo "Agenda aberta".
- **Sua foto.**
- **Marcas atendidas:** adicionar, remover e reordenar logos do carrossel.
- **Portfólio:** cada case com categoria, cliente, título, capa, desafio, solução, entregas e galeria, em português e espanhol.
- **Imagens do site:** a faixa de imagens e as imagens dos cards Agências e Empresas.
- **Serviços:** nome, descrição e imagem de cada serviço.

Os textos das seções (títulos, chamadas, a história do nome) ficam no código para não quebrar a diagramação. Para mudá-los, é só pedir ao Claude e substituir o `index.html` no GitHub.

### Dicas para as imagens

- Faixa: vertical 4:5 (por exemplo, 800 x 1000 px).
- Cards Agências e Empresas: horizontal 16:9 (1200 x 675 px).
- Serviços e capas de case: 4:3 (800 x 600 px).
- Logos: PNG com fundo transparente ou SVG, em branco ou claro.
- Prefira JPG com até 300 KB por imagem para o site continuar rápido.
