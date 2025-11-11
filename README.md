<!doctype html>
<html lang="pt-BR">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Consciência Negra — Repositório Único</title>
  <meta name="description" content="Versão única (single-file) do projeto Consciência Negra para publicação no GitHub Pages. Contém HTML, CSS e JS integrados e acessíveis." />
  <meta name="author" content="Projeto Consciência Negra" />
  <meta property="og:title" content="Consciência Negra — Repositório Único" />
  <meta property="og:description" content="Material educativo e interativo sobre história, cultura e ativismo afro-brasileiro." />
  <style>
    /* ===== Reset e variáveis ===== */
    :root{
      --bg:#0b1220; --panel:#0f1724; --muted:#9aa4b2; --accent:#ffb703; --accent-2:#fb8500; --text:#e6eef6;
      --success:#2dd4bf; --danger:#ef4444; --max-width:1100px; --ui-sans: Inter, system-ui, -apple-system, 'Segoe UI', Roboto, Arial;
      --radius:12px;
    }
    *{box-sizing:border-box}
    html,body{height:100%}
    body{font-family:var(--ui-sans);margin:0;background:linear-gradient(180deg,var(--bg), #071029 160%);color:var(--text);padding:28px;display:flex;justify-content:center}
    a{color:var(--accent)}

    /* ===== Container ===== */
    .wrap{width:100%;max-width:var(--max-width);background:linear-gradient(180deg, rgba(255,255,255,0.02), rgba(255,255,255,0.01));border-radius:16px;padding:18px;box-shadow:0 12px 40px rgba(2,6,23,0.6);border:1px solid rgba(255,255,255,0.03)}

    /* ===== Header ===== */
    header{display:flex;align-items:center;justify-content:space-between;gap:12px}
    .brand{display:flex;align-items:center;gap:12px}
    .logo{width:60px;height:60px;border-radius:10px;display:flex;align-items:center;justify-content:center;font-weight:800;background:linear-gradient(135deg,var(--accent),var(--accent-2));color:#041025}
    h1{margin:0;font-size:20px}
    p.lead{margin:0;color:var(--muted);font-size:13px}
    nav.top{display:flex;gap:8px;align-items:center}
    .btn{background:transparent;border:1px solid rgba(255,255,255,0.06);padding:8px 10px;border-radius:8px;color:var(--text);cursor:pointer;font-weight:600}
    .btn.primary{background:linear-gradient(90deg,var(--accent),var(--accent-2));border:none;color:#041025}

    /* ===== Layout ===== */
    main{display:grid;grid-template-columns:1fr 360px;gap:18px;margin-top:18px}
    @media (max-width:1020px){main{grid-template-columns:1fr}}

    /* ===== Content cards ===== */
    .content{padding:12px;border-radius:12px;background:linear-gradient(180deg, rgba(255,255,255,0.01), rgba(255,255,255,0.005));border:1px solid rgba(255,255,255,0.02)}
    .card{padding:14px;border-radius:10px;background:var(--panel);margin-bottom:12px;border:1px solid rgba(255,255,255,0.02)}
    h2{margin:0 0 10px 0;font-size:18px}
    h3{margin:8px 0;font-size:15px}
    .muted{color:var(--muted);font-size:13px}

    /* ===== Sidebar ===== */
    aside .sidebar{position:sticky;top:24px;padding:14px;border-radius:12px;background:linear-gradient(180deg, rgba(255,255,255,0.01), rgba(255,255,255,0.005));border:1px solid rgba(255,255,255,0.02)}
    .stat{display:flex;align-items:center;justify-content:space-between;padding:10px;border-radius:8px}

    /* ===== Responsive helpers ===== */
    .grid-2{display:grid;grid-template-columns:1fr 1fr;gap:10px}
    @media (max-width:700px){.grid-2{grid-template-columns:1fr}}

    /* ===== Forms ===== */
    input,textarea,select{width:100%;padding:10px;border-radius:8px;border:1px solid rgba(255,255,255,0.04);background:transparent;color:var(--text);margin-top:8px}
    label{font-weight:700;font-size:13px}

    /* ===== Footer ===== */
    footer{display:flex;justify-content:space-between;gap:12px;padding-top:12px;margin-top:10px;border-top:1px dashed rgba(255,255,255,0.02)}

    /* ===== Accessibility focus ===== */
    :focus{outline:3px solid rgba(255,255,255,0.06);outline-offset:2px}

    /* ===== Misc ===== */
    .hidden{display:none}
    .kbd{font-family:monospace;background:rgba(255,255,255,0.02);padding:4px 6px;border-radius:6px}
    .quote{padding:12px;border-left:3px solid rgba(255,255,255,0.03);background:rgba(255,255,255,0.01);border-radius:8px}

    /* ===== Print ===== */
    @media print{body{background:white;color:black} .wrap{box-shadow:none;border:none}}
  </style>
</head>
<body>
  <div class="wrap" role="main">
    <header>
      <div class="brand">
        <div class="logo" aria-hidden>CN</div>
        <div>
          <h1>Consciência Negra — Versão Única</h1>
          <p class="lead">Material educativo, prático e adaptável — pronto para GitHub Pages.</p>
        </div>
      </div>
      <nav class="top" aria-label="controles principais">
        <button class="btn" id="btnSearch" title="Pesquisar (/)">🔎 Pesquisar</button>
        <button class="btn" id="toggleTheme" title="Alternar tema">🌓 Tema</button>
        <button class="btn primary" id="downloadBtn" title="Baixar arquivo">⬇️ Baixar</button>
      </nav>
    </header>

    <main>
      <section class="content" aria-labelledby="intro">
        <article id="intro" class="card">
          <h2>Apresentação</h2>
          <p class="muted">Esta é uma versão 'single-file' pensada para deploy imediato no GitHub Pages. Contém seções sobre história, personalidades, planos de aula, atividades práticas, glossário, recursos e ferramentas para professores.</p>
          <p>Use o menu lateral para navegar, a pesquisa (atalho <span class="kbd">/</span>) para encontrar termos e o botão de download para receber o arquivo pronto.</p>
        </article>

        <article id="historia" class="card">
          <h2>História</h2>
          <p class="muted">Uma síntese da presença africana no território que hoje é o Brasil, desde os primeiros contatos até o presente.</p>
          <div class="grid-2">
            <div>
              <h3>Tráfico e economia</h3>
              <p class="muted">Nos séculos XVI–XIX, milhões de africanos foram deslocados para a América; sua força de trabalho foi central para plantações e mineração.</p>
            </div>
            <div>
              <h3>Resistência</h3>
              <p class="muted">Formação de quilombos, fugas, revoltas e manifestações culturais que preservaram saberes e laços comunitários.</p>
            </div>
          </div>
        </article>

        <article id="personalidades" class="card">
          <h2>Personalidades</h2>
          <p class="muted">Perfis curtos e verificáveis de figuras que marcaram a história política, cultural e intelectual.</p>
          <ul>
            <li><strong>Zumbi dos Palmares</strong> — liderança emancipadora e símbolo nacional de resistência.</li>
            <li><strong>Luís Gama</strong> — abolicionista e operador do direito em favor de libertos.</li>
            <li><strong>Carolina Maria de Jesus</strong> — escritora que expôs a vida nas periferias urbanas.</li>
            <li><strong>Milton Santos</strong> — geógrafo e pensador crítico das cidades e desigualdades.</li>
          </ul>
        </article>

        <article id="timeline" class="card">
          <h2>Linha do Tempo (resumida)</h2>
          <ol>
            <li><strong>1500s:</strong> primeiros africanos trazidos ao território.</li>
            <li><strong>1600–1700:</strong> consolidação dos sistemas escravistas.</li>
            <li><strong>1695:</strong> morte de Zumbi dos Palmares.</li>
            <li><strong>1888:</strong> Lei Áurea — abolição formal da escravidão.</li>
            <li><strong>2003:</strong> implementação de leis de ensino obrigatório da história afro-brasileira (Lei 10.639/03).</li>
          </ol>
        </article>

        <article id="educacao" class="card">
          <h2>Educação</h2>
          <p class="muted">Instrumentos legais e pedagogias para garantir que a história e cultura afrodescendentes sejam ensinadas com qualidade.</p>
          <h3>Planos de Aula (resumo)</h3>
          <p class="muted">Sequências para ensino médio: introdução histórica, práticas culturais, projeto final e avaliação formativa.</p>
        </article>

        <article id="atividades" class="card">
          <h2>Atividades Práticas</h2>
          <p class="muted">Oficinas, feiras, rodas de leitura e projetos de memória.</p>
          <ul>
            <li>Oficina de culinária e mapa de sabores locais.</li>
            <li>Projeto de memória oral com gravação de depoimentos.</li>
            <li>Exposição de arte comunitária e ciclo de debates.</li>
          </ul>
        </article>

        <article id="glossario" class="card">
          <h2>Glossário</h2>
          <dl>
            <dt>Afrodescendente</dt>
            <dd class="muted">Pessoa com ancestralidade advinda do continente africano.</dd>
            <dt>Quilombo</dt>
            <dd class="muted">Comunidade formada por pessoas fugidas da escravidão ou descendentes.</dd>
            <dt>Racismo estrutural</dt>
            <dd class="muted">Conjunto de práticas e instituições que geram desigualdade racial.</dd>
          </dl>
        </article>

        <article id="recursos" class="card">
          <h2>Recursos e Leituras</h2>
          <p class="muted">Sugestões de livros, artigos, filmes e instituições para aprofundamento.</p>
          <ul>
            <li>Carolina Maria de Jesus — "Quarto de Despejo"</li>
            <li>Lélia Gonzalez — coletâneas e artigos</li>
            <li>Documentários e acervos digitais de memória</li>
          </ul>
        </article>

        <article id="quiz" class="card">
          <h2>Quiz Rápido</h2>
          <p class="muted">Teste seus conhecimentos com perguntas rápidas — feedback imediato.</p>
          <div id="quizArea"></div>
          <div style="margin-top:10px"><button class="btn" id="startQuiz">Iniciar Quiz</button> <button class="btn" id="showAnswers">Mostrar Respostas</button></div>
        </article>

        <article id="faq" class="card">
          <h2>Perguntas Frequentes (FAQ)</h2>
          <ul>
            <li><strong>Por que 20 de novembro?</strong> — data associada à morte de Zumbi, símbolo de resistência.</li>
            <li><strong>O que são cotas?</strong> — ações afirmativas voltadas à correção de desigualdades históricas.</li>
            <li><strong>Como acolher nas escolas?</strong> — formação docente, acervo diversificado e diálogo constante.</li>
          </ul>
        </article>

        <article id="contribua" class="card">
          <h2>Contribua</h2>
          <p class="muted">Este projeto é colaborativo. Você pode enviar sugestões, referências e materiais educativos.</p>
          <form id="contribForm">
            <label for="nome">Nome</label>
            <input id="nome" name="nome" required />
            <label for="referencia">Referência / link</label>
            <input id="referencia" name="referencia" />
            <label for="descricao">Breve descrição</label>
            <textarea id="descricao" name="descricao" rows="4"></textarea>
            <button type="submit" class="btn primary">Enviar contribuição</button>
            <p id="msgContrib" class="muted" aria-live="polite"></p>
          </form>
        </article>

      </section>

      <aside>
        <div class="sidebar card">
          <h3 class="muted">Navegação Rápida</h3>
          <nav aria-label="navegação seções">
            <ul style="list-style:none;padding:0;margin:0">
              <li><a href="#historia">História</a></li>
              <li><a href="#personalidades">Personalidades</a></li>
              <li><a href="#educacao">Educação</a></li>
              <li><a href="#atividades">Atividades</a></li>
              <li><a href="#recursos">Recursos</a></li>
              <li><a href="#contribua">Contribua</a></li>
            </ul>
          </nav>

          <div style="margin-top:12px">
            <h4 class="muted">Ferramentas</h4>
            <p class="muted">Use as ações abaixo para testar funcionalidades locais.</p>
            <div style="display:flex;gap:8px;flex-wrap:wrap;margin-top:8px">
              <button class="btn" id="btnFocusSearch">Focar pesquisa</button>
              <button class="btn" id="btnPrint">Imprimir</button>
            </div>
          </div>

          <div style="margin-top:12px">
            <h4 class="muted">Citação</h4>
            <blockquote class="quote">"Resistir é existir — reconhecer é transformar."</blockquote>
          </div>

          <div style="margin-top:12px">
            <h4 class="muted">Créditos</h4>
            <p class="muted">Projeto colaborativo — conteúdo aberto. Licença: MIT.</p>
          </div>
        </div>
      </aside>
    </main>

    <footer>
      <div class="muted">Feito para educação — adapte, cite fontes e priorize vozes negras.</div>
      <div class="muted">Versão única para GitHub Pages — pronto para commit.</div>
    </footer>
  </div>

  <script>
    /* ======================================================
       Script principal (single-file): navegação, quiz, forms
       Comentários em PT-BR para facilitar adaptações.
       ====================================================== */

    // ===== Dados (pode ser ampliado) =====
    const DATA = {
      quiz: [
        {q:'Qual a data do Dia da Consciência Negra no Brasil?', a:['13 de maio','20 de novembro','1º de maio','7 de setembro'], correct:1, explain:'20 de novembro relembra a morte de Zumbi dos Palmares.'},
        {q:'O que é um quilombo?', a:['Uma religião','Uma comunidade de resistência formada por fugidos da escravidão','Um instrumento musical','Uma obra literária'], correct:1, explain:'Quilombos eram comunidades formadas por fugidos e lugares de resistência.'}
      ]
    };

    // ===== Helpers =====
    const $ = sel => document.querySelector(sel);
    const $$ = sel => Array.from(document.querySelectorAll(sel));

    // ===== Pesquisa (filtro simples) =====
    const btnSearch = $('#btnSearch');
    btnSearch.addEventListener('click', ()=>{
      const term = prompt('Pesquisar termo (ex: Zumbi, Quilombo, Lei Áurea):');
      if(!term) return;
      const nodes = $$('section.content article, section.content article *');
      const hits = nodes.filter(n => n.textContent && n.textContent.toLowerCase().includes(term.toLowerCase()));
      if(hits.length===0) alert('Nenhum resultado para "'+term+'".');
      else{
        window.location.hash = '#'+(hits[0].closest('article').id || 'intro');
        alert(hits.length+' resultado(s) encontrado(s). Indo para a primeira ocorrência.');
      }
    });

    // atalho '/'
    document.addEventListener('keydown', (e)=>{ if(e.key === '/' && document.activeElement.tagName !== 'INPUT' && document.activeElement.tagName !== 'TEXTAREA'){ e.preventDefault(); btnSearch.click(); } });

    // ===== Tema (simples troca de CSS custom properties) =====
    const toggleTheme = $('#toggleTheme');
    let dark = true;
    toggleTheme.addEventListener('click', ()=>{
      dark = !dark;
      if(!dark){ document.body.style.background = '#f7f7f7'; document.body.style.color = '#111'; } else { document.body.style.background = ''; document.body.style.color = ''; }
      toggleTheme.textContent = dark ? '🌓 Tema' : '🌞 Tema claro';
    });

    // ===== Download do arquivo (gera um blob com o HTML atual) =====
    const downloadBtn = $('#downloadBtn');
    downloadBtn.addEventListener('click', ()=>{
      const doc = '<!doctype html>\n' + document.documentElement.outerHTML;
      const blob = new Blob([doc], {type:'text/html;charset=utf-8'});
      const url = URL.createObjectURL(blob);
      const a = document.createElement('a');
      a.href = url; a.download = 'consiencia-negra.html';
      document.body.appendChild(a); a.click(); a.remove(); URL.revokeObjectURL(url);
    });

    // ===== Formulário de contribuição (simula envio e salva no localStorage) =====
    const contribForm = $('#contribForm');
    const msgContrib = $('#msgContrib');
    contribForm.addEventListener('submit', (e)=>{
      e.preventDefault();
      const data = {nome: $('#nome').value.trim(), referencia: $('#referencia').value.trim(), descricao: $('#descricao').value.trim(), created: new Date().toISOString()};
      const prev = JSON.parse(localStorage.getItem('cn_contrib')||'[]'); prev.push(data); localStorage.setItem('cn_contrib', JSON.stringify(prev));
      msgContrib.textContent = 'Contribuição salva localmente — obrigado! (simulação)';
      contribForm.reset();
    });

    // ===== Imprimir =====
    $('#btnPrint')?.addEventListener('click', ()=> window.print());

    // ===== Quiz =====
    const quizArea = $('#quizArea');
    const startQuiz = $('#startQuiz');
    const showAnswers = $('#showAnswers');
    let userAnswers = [];
    function renderQuiz(){
      quizArea.innerHTML = '';
      DATA.quiz.forEach((q,i)=>{
        const wrap = document.createElement('div'); wrap.className='card';
        const h = document.createElement('h3'); h.textContent = (i+1)+'. '+q.q; wrap.appendChild(h);
        q.a.forEach((opt,j)=>{
          const btn = document.createElement('button'); btn.className='btn'; btn.style.display='block'; btn.style.marginTop='8px'; btn.textContent = opt;
          btn.addEventListener('click', ()=>{ userAnswers[i]=j; updateScore(); });
          wrap.appendChild(btn);
        });
        quizArea.appendChild(wrap);
      });
      const score = document.createElement('div'); score.id='quizScore'; score.className='muted'; score.textContent = 'Pontuação: 0 / '+DATA.quiz.length; quizArea.appendChild(score);
    }
    function updateScore(){
      const score = userAnswers.reduce((acc,ans,idx)=> acc + ((ans===DATA.quiz[idx].correct)?1:0), 0);
      $('#quizScore').textContent = 'Pontuação: '+score+' / '+DATA.quiz.length;
    }
    startQuiz.addEventListener('click', ()=>{ userAnswers = Array(DATA.quiz.length).fill(null); renderQuiz(); window.location.hash='#quiz'; });
    showAnswers.addEventListener('click', ()=>{
      DATA.quiz.forEach((q,i)=>{
        const card = quizArea.children[i]; if(!card) return;
        Array.from(card.querySelectorAll('button')).forEach((b,idx)=>{
          b.style.border = '1px solid rgba(255,255,255,0.04)';
          if(idx===q.correct) b.style.outline = '3px solid rgba(45,212,191,0.12)';
          if(userAnswers[i]!==undefined && userAnswers[i]!==null && userAnswers[i]!==q.correct && idx===userAnswers[i]) b.style.opacity = '0.6';
          b.title = (idx===q.correct? 'Correta. ':'') + (q.explain||'');
        });
      });
      updateScore();
    });

    // ===== Pequenos utilitários =====
    $('#btnFocusSearch')?.addEventListener('click', ()=> btnSearch.click());

    // ===== Accessibility: foco inicial =====
    window.addEventListener('load', ()=> { document.querySelector('.btn')?.focus(); });

    // ===== Instrução para deploy (console) =====
    console.info('Arquivo único pronto para commit no GitHub. Use: git add consiencia-negra.html && git commit -m "Add single-file site" && git push');

  </script>
</body>
</html>
