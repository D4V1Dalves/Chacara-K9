# Chácara K-9 — site estático

O index.html contém o site, as fontes e as quatro mídias incorporadas. Não precisa de instalação ou compilação. A reconstrução adapta a estrutura de apresentação do BASE (capa, apresentação, experiências, treinamento e contato), com laranja como cor secundária e verde escuro como cor principal. Não é uma cópia exata: o BASE depende de serviços e imagens externos ausentes no ZIP.

## Publicar no GitHub Pages

1. Extraia este ZIP e envie index.html e .nojekyll para a raiz do repositório.
2. No GitHub, abra Settings → Pages e selecione a publicação pela branch, pasta raiz.
3. Use o endereço HTTPS fornecido pelo GitHub Pages.

## Editar mídias

Com o site em foco, pressione Ctrl + Shift + D. Se o navegador capturar o atalho, use Administração no rodapé. Use exatamente o usuário e a senha fornecidos no pedido original (diferencia maiúsculas e minúsculas).

Cada uma das quatro imagens do site pode ser substituída por PNG, JPG, WebP, GIF animado ou MP3, até 15 MB por arquivo. MP3 substitui a imagem por um player com controles; não reproduz automaticamente. A marca e os elementos decorativos são texto/CSS, não PNGs.

“Salvar neste navegador” guarda um rascunho criptografado em IndexedDB. Ele só aparece após login no mesmo navegador e endereço. Não altera o GitHub nem o site de outros visitantes. “Exportar index.html” baixa um HTML completo com as alterações incorporadas; envie esse arquivo ao GitHub substituindo o anterior para publicar para todos. Guarde cópias dos HTMLs para recuperar versões. Navegação privada ou limpeza dos dados pode eliminar rascunhos.

## Segurança e limites

Não há usuário ou senha em texto simples no código entregue. O verificador usa PBKDF2-HMAC-SHA-256, 600.000 iterações e salt aleatório de 256 bits. O rascunho local usa AES-256-GCM com IV aleatório e chave derivada separadamente. As chaves ficam apenas em memória durante a sessão. Há saída após 15 minutos de inatividade.

Isso NÃO cria autenticação segura de servidor: qualquer visitante pode inspecionar/modificar o JavaScript, contornar o painel local ou atacar o verificador offline. O atraso entre tentativas também é apenas local. GitHub Pages só serve arquivos estáticos. Para impedir acessos de verdade e publicar edições automaticamente, é necessário um backend com autenticação, autorização e armazenamento. As mídias publicadas são públicas. Não reutilize essa senha em outros serviços. O HTML não contém tokens GitHub.

## Conteúdo e imagens

Fonte de informações: https://share.google/snMjamKXPLbA118ee — perfil Google da Chácara K-9, consultado em 15/10/2026. Foram utilizados nome, categoria, descrição empresarial, endereço e telefone. Não foram inventados preços, horários fixos ou condições de hospedagem.

As quatro fotos vieram de scroll.zip e são identificadas no site como ilustrativas; não são fotos verificadas da Chácara K-9. Substitua por imagens próprias/autorizadas antes da publicação. A fonte Circular veio do BASE; confirme os direitos de uso dos arquivos fornecidos.

Rolagem: o scroll.zip usa SmoothScroll com duração de 600 ms e passo de 50, e âncoras com 1000 ms. A implementação independente reproduz esses parâmetros, preserva a rolagem nativa de toque/trackpad e respeita a preferência por movimento reduzido. Não foram incluídos rastreadores nem scripts legados dos ZIPs.

## Verificação
Sintaxe JavaScript, correspondência do verificador de senha, rejeição de senha incorreta, integridade das quatro mídias e ciclo de criptografia/descriptografia AES-GCM verificados. A prévia no navegador não conectou ao servidor local; layout, login, upload, persistência e download ainda precisam de verificação interativa no navegador.

## Atualização: textos, ícones e solicitação de hospedagem

O painel Ctrl + Shift + D agora inclui “Textos do site” e “Ícones e símbolos”. Edite o conteúdo pelos campos de texto; os ícones de texto podem ser trocados por caracteres Unicode ou emojis. Não se aceita HTML ou JavaScript nesses campos. Textos, símbolos e mídias são salvos juntos no rascunho criptografado e no index.html exportado. Os links e a estrutura do site permanecem definidos no código.

O botão “Conversar sobre adestramento” abre exatamente o link solicitado, com a mensagem “Olá! Vim pelo link e gostaria de mais informações.”.

A seção Hospedagem coleta nome do responsável, telefone, CPF, endereço, nome e raça do cachorro, entrada, saída e opção de buscar o pet. A quantidade de diárias é calculada pela diferença entre as datas; saída deve ser posterior à entrada. Isso é uma solicitação de possível hospedagem, sem confirmar disponibilidade ou reserva. Transporte, valores e horários são combinados com a equipe.

Após consentimento, o botão abre https://wa.me/5518997212241 com os campos organizados na mensagem. O visitante precisa confirmar o envio no próprio WhatsApp. Não é envio automático via API. O site não grava esses dados em IndexedDB, localStorage ou servidor. Os dados são incluídos no link aberto no WhatsApp, que passa a recebê-los. O formulário não é incluído com valores pessoais ao exportar o site.

Foram verificados CPF válido/inválido, conteúdo e codificação da mensagem, destino WhatsApp, consentimento obrigatório e caminhos de persistência/exportação dos textos. A verificação interativa de layout, upload, login e navegação permanece pendente pela indisponibilidade da prévia do navegador.
