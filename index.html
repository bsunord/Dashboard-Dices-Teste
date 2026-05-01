<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Dashboard — Gestão Documental DICES</title>
<link href="https://fonts.googleapis.com/css2?family=DM+Sans:wght@300;400;500;600&family=DM+Mono:wght@400;500&display=swap" rel="stylesheet">
<script src="https://cdnjs.cloudflare.com/ajax/libs/Chart.js/4.4.1/chart.umd.js"></script>
<style>
  :root {
    --bg: #F5F3EF;
    --surface: #FFFFFF;
    --surface2: #EFEDE8;
    --border: rgba(0,0,0,0.08);
    --border-strong: rgba(0,0,0,0.14);
    --text: #1A1916;
    --text-muted: #6B6860;
    --text-faint: #A09D97;
    --green: #3B6D11;
    --green-bg: #EAF3DE;
    --green-mid: #639922;
    --amber: #633806;
    --amber-bg: #FAEEDA;
    --amber-mid: #BA7517;
    --blue: #0C447C;
    --blue-bg: #E6F1FB;
    --blue-mid: #378ADD;
    --red: #791F1F;
    --red-bg: #FCEBEB;
    --accent: #1A1916;
    --radius: 12px;
    --radius-sm: 8px;
    font-family: 'DM Sans', sans-serif;
  }

  * { box-sizing: border-box; margin: 0; padding: 0; }

  body {
    background: var(--bg);
    color: var(--text);
    min-height: 100vh;
    padding: 2rem 2.5rem;
    font-size: 14px;
    line-height: 1.5;
  }

  /* Header */
  .header {
    display: flex;
    align-items: flex-start;
    justify-content: space-between;
    margin-bottom: 2rem;
    padding-bottom: 1.5rem;
    border-bottom: 1px solid var(--border-strong);
  }
  .header-left h1 {
    font-size: 24px;
    font-weight: 600;
    letter-spacing: -0.02em;
    color: var(--text);
    margin-bottom: 2px;
  }
  .header-left p {
    font-size: 13px;
    color: var(--text-muted);
  }
  .header-right {
    display: flex;
    align-items: center;
    gap: 8px;
    font-size: 12px;
    color: var(--text-muted);
    font-family: 'DM Mono', monospace;
    background: var(--surface2);
    padding: 6px 14px;
    border-radius: 100px;
    border: 1px solid var(--border);
  }
  .dot-live { width: 7px; height: 7px; border-radius: 50%; background: var(--green-mid); }

  /* Metrics */
  .metrics {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    gap: 12px;
    margin-bottom: 1.5rem;
  }
  .metric {
    background: var(--surface);
    border-radius: var(--radius);
    padding: 18px 20px;
    border: 1px solid var(--border);
  }
  .metric-label {
    font-size: 11px;
    font-weight: 500;
    color: var(--text-faint);
    text-transform: uppercase;
    letter-spacing: 0.06em;
    margin-bottom: 8px;
  }
  .metric-value {
    font-size: 32px;
    font-weight: 600;
    letter-spacing: -0.03em;
    line-height: 1;
    margin-bottom: 4px;
  }
  .metric-sub { font-size: 12px; color: var(--text-muted); }
  .mv-default { color: var(--text); }
  .mv-green { color: var(--green-mid); }
  .mv-amber { color: var(--amber-mid); }
  .mv-blue { color: var(--blue-mid); }

  /* Progress bar global */
  .progress-track {
    height: 6px;
    background: var(--surface2);
    border-radius: 99px;
    overflow: hidden;
    margin-top: 10px;
  }
  .progress-fill { height: 100%; border-radius: 99px; transition: width 0.6s ease; }

  /* Two col layout */
  .two-col { display: grid; grid-template-columns: 1fr 1fr; gap: 12px; margin-bottom: 12px; }
  .three-col { display: grid; grid-template-columns: 1.4fr 1fr 1fr; gap: 12px; margin-bottom: 12px; }

  /* Card */
  .card {
    background: var(--surface);
    border-radius: var(--radius);
    padding: 20px;
    border: 1px solid var(--border);
  }
  .card-title {
    font-size: 11px;
    font-weight: 600;
    color: var(--text-faint);
    text-transform: uppercase;
    letter-spacing: 0.07em;
    margin-bottom: 16px;
  }

  /* Chart wrapper */
  .chart-wrap { position: relative; width: 100%; }

  /* Phase bars */
  .phase-list { display: flex; flex-direction: column; gap: 14px; }
  .phase-item {}
  .phase-header { display: flex; justify-content: space-between; align-items: baseline; margin-bottom: 6px; }
  .phase-name { font-size: 13px; font-weight: 500; color: var(--text); }
  .phase-pct { font-size: 12px; font-family: 'DM Mono', monospace; color: var(--text-muted); }
  .phase-sub { font-size: 11px; color: var(--text-faint); margin-bottom: 4px; }

  /* Team grid */
  .team-grid { display: flex; flex-wrap: wrap; gap: 8px; }
  .member {
    display: flex; align-items: center; gap: 8px;
    background: var(--surface2);
    border-radius: 100px;
    padding: 5px 12px 5px 6px;
    font-size: 12px;
    font-weight: 500;
    color: var(--text);
    border: 1px solid var(--border);
  }
  .avatar {
    width: 24px; height: 24px; border-radius: 50%;
    display: flex; align-items: center; justify-content: center;
    font-size: 9px; font-weight: 600;
  }
  .av-blue { background: var(--blue-bg); color: var(--blue); }
  .av-teal { background: #E1F5EE; color: #085041; }
  .av-amber { background: var(--amber-bg); color: var(--amber); }
  .av-purple { background: #EEEDFE; color: #3C3489; }
  .av-green { background: var(--green-bg); color: var(--green); }

  /* Locations */
  .location-list { display: flex; flex-direction: column; gap: 8px; }
  .location-item {
    display: flex; align-items: center; gap: 10px;
    padding: 8px 12px;
    border-radius: var(--radius-sm);
    background: var(--surface2);
    border: 1px solid var(--border);
    font-size: 12px;
  }
  .loc-dot { width: 8px; height: 8px; border-radius: 50%; flex-shrink: 0; }
  .loc-name { font-weight: 500; color: var(--text); flex: 1; }
  .loc-type { font-size: 11px; color: var(--text-faint); }

  /* Table */
  .task-table { width: 100%; border-collapse: collapse; }
  .task-table thead tr { border-bottom: 1px solid var(--border-strong); }
  .task-table th {
    text-align: left; padding: 8px 10px;
    font-size: 11px; font-weight: 600;
    color: var(--text-faint);
    text-transform: uppercase;
    letter-spacing: 0.06em;
  }
  .task-table td { padding: 9px 10px; border-bottom: 1px solid var(--border); font-size: 13px; vertical-align: middle; }
  .task-table tr:last-child td { border-bottom: none; }
  .task-table tbody tr:hover { background: var(--surface2); }
  .sem-tag {
    font-size: 10px; font-family: 'DM Mono', monospace;
    background: var(--surface2); color: var(--text-muted);
    padding: 2px 7px; border-radius: 4px;
    border: 1px solid var(--border);
    white-space: nowrap;
  }
  .date-tag { font-size: 12px; font-family: 'DM Mono', monospace; color: var(--text-muted); white-space: nowrap; }

  /* Badges */
  .badge {
    display: inline-block; font-size: 11px; font-weight: 500;
    padding: 3px 10px; border-radius: 100px; white-space: nowrap;
  }
  .badge-completo { background: var(--green-bg); color: var(--green); }
  .badge-andamento { background: var(--amber-bg); color: var(--amber); }
  .badge-iniciar { background: var(--blue-bg); color: var(--blue); }

  /* Legend */
  .legend { display: flex; flex-wrap: wrap; gap: 14px; margin-bottom: 12px; }
  .legend-item { display: flex; align-items: center; gap: 5px; font-size: 11px; color: var(--text-muted); }
  .legend-swatch { width: 10px; height: 10px; border-radius: 2px; }

  /* Edital tags */
  .edital-list { display: flex; flex-direction: column; gap: 6px; }
  .edital-item {
    display: flex; align-items: center; gap: 10px;
    padding: 8px 12px; border-radius: var(--radius-sm);
    background: var(--surface2); border: 1px solid var(--border);
    font-size: 12px;
  }
  .edital-num { font-family: 'DM Mono', monospace; font-weight: 500; color: var(--text); width: 80px; flex-shrink: 0; }
  .edital-desc { color: var(--text-muted); flex: 1; }
  .edital-year { font-family: 'DM Mono', monospace; font-size: 11px; color: var(--text-faint); }

  /* Footer */
  .footer {
    margin-top: 2rem;
    padding-top: 1rem;
    border-top: 1px solid var(--border);
    display: flex;
    justify-content: space-between;
    align-items: center;
  }
  .footer p { font-size: 11px; color: var(--text-faint); font-family: 'DM Mono', monospace; }

  @media print {
    body { padding: 1rem; background: white; }
    .card { break-inside: avoid; }
  }

  @media (max-width: 900px) {
    body { padding: 1rem; }
    .metrics { grid-template-columns: repeat(2, 1fr); }
    .two-col, .three-col { grid-template-columns: 1fr; }
  }
</style>
</head>
<body>

<div class="header">
  <div class="header-left">
    <h1>Resgate Documental — DICES</h1>
    <p>Diretoria de Concursos e Seleções · Prefeitura Municipal de Fortaleza · Plano Emergencial de Gestão Documental</p>
  </div>
  <div class="header-right">
    <div class="dot-live"></div>
    Atualizado em Abril / 2026
  </div>
</div>

<!-- Metrics -->
<div class="metrics">
  <div class="metric">
    <div class="metric-label">Tarefas totais</div>
    <div class="metric-value mv-default">22</div>
    <div class="metric-sub">Semanas 1 a 4</div>
    <div class="progress-track"><div class="progress-fill" style="width:100%; background: var(--surface2);"></div></div>
  </div>
  <div class="metric">
    <div class="metric-label">Concluídas</div>
    <div class="metric-value mv-green">14</div>
    <div class="metric-sub">64% do total</div>
    <div class="progress-track"><div class="progress-fill" style="width:64%; background: var(--green-mid);"></div></div>
  </div>
  <div class="metric">
    <div class="metric-label">Em andamento</div>
    <div class="metric-value mv-amber">3</div>
    <div class="metric-sub">14% do total</div>
    <div class="progress-track"><div class="progress-fill" style="width:14%; background: var(--amber-mid);"></div></div>
  </div>
  <div class="metric">
    <div class="metric-label">A iniciar</div>
    <div class="metric-value mv-blue">5</div>
    <div class="metric-sub">23% do total</div>
    <div class="progress-track"><div class="progress-fill" style="width:23%; background: var(--blue-mid);"></div></div>
  </div>
</div>

<!-- Charts row -->
<div class="two-col">
  <div class="card">
    <div class="card-title">Status das tarefas</div>
    <div class="legend">
      <div class="legend-item"><div class="legend-swatch" style="background:#639922;"></div>Completo (14)</div>
      <div class="legend-item"><div class="legend-swatch" style="background:#BA7517;"></div>Em andamento (3)</div>
      <div class="legend-item"><div class="legend-swatch" style="background:#378ADD;"></div>A iniciar (5)</div>
    </div>
    <div class="chart-wrap" style="height:200px;">
      <canvas id="statusChart" role="img" aria-label="Gráfico de pizza: 14 completas, 3 em andamento, 5 a iniciar"></canvas>
    </div>
  </div>

  <div class="card">
    <div class="card-title">Tarefas por semana</div>
    <div class="legend">
      <div class="legend-item"><div class="legend-swatch" style="background:#639922;"></div>Completo</div>
      <div class="legend-item"><div class="legend-swatch" style="background:#BA7517;"></div>Em andamento</div>
      <div class="legend-item"><div class="legend-swatch" style="background:#378ADD;"></div>A iniciar</div>
    </div>
    <div class="chart-wrap" style="height:200px;">
      <canvas id="weekChart" role="img" aria-label="Barras de tarefas por semana"></canvas>
    </div>
  </div>
</div>

<!-- Phases + Team -->
<div class="three-col">
  <div class="card">
    <div class="card-title">Fases do projeto</div>
    <div class="phase-list">
      <div class="phase-item">
        <div class="phase-header">
          <div class="phase-name">Fase 1 — Contenção e infraestrutura</div>
          <div class="phase-pct">75%</div>
        </div>
        <div class="phase-sub">Resgate emergencial, EPIs, estantes, caixas-box</div>
        <div class="progress-track"><div class="progress-fill" style="width:75%; background:#639922;"></div></div>
      </div>
      <div class="phase-item">
        <div class="phase-header">
          <div class="phase-name">Fase 2 — Planejamento técnico e jurídico</div>
          <div class="phase-pct">40%</div>
        </div>
        <div class="phase-sub">Plano de classificação, tabela de temporalidade</div>
        <div class="progress-track"><div class="progress-fill" style="width:40%; background:#BA7517;"></div></div>
      </div>
      <div class="phase-item">
        <div class="phase-header">
          <div class="phase-name">Fase 3 — Triagem e organização física</div>
          <div class="phase-pct">15%</div>
        </div>
        <div class="phase-sub">Higienização, triagem, acondicionamento, etiquetagem</div>
        <div class="progress-track"><div class="progress-fill" style="width:15%; background:#378ADD;"></div></div>
      </div>
      <div class="phase-item">
        <div class="phase-header">
          <div class="phase-name">Fase 4 — Digitalização</div>
          <div class="phase-pct">0%</div>
        </div>
        <div class="phase-sub">Digitalização e armazenamento dos arquivos digitais</div>
        <div class="progress-track"><div class="progress-fill" style="width:2%; background:#D85A30;"></div></div>
      </div>
    </div>
  </div>

  <div class="card">
    <div class="card-title">Equipe</div>
    <div class="team-grid">
      <div class="member"><div class="avatar av-blue">BR</div>Bruno</div>
      <div class="member"><div class="avatar av-teal">GE</div>George</div>
      <div class="member"><div class="avatar av-amber">NE</div>Neto</div>
      <div class="member"><div class="avatar av-purple">TM</div>Tom</div>
      <div class="member"><div class="avatar av-green">AN</div>Anita</div>
      <div class="member"><div class="avatar av-blue">DA</div>Daiana</div>
      <div class="member"><div class="avatar av-teal">AR</div>Artur</div>
      <div class="member"><div class="avatar av-amber">EV</div>Evonildes</div>
      <div class="member"><div class="avatar av-purple">HO</div>Homero</div>
    </div>
  </div>

  <div class="card">
    <div class="card-title">Locais do acervo</div>
    <div class="location-list">
      <div class="location-item">
        <div class="loc-dot" style="background:#639922;"></div>
        <div class="loc-name">DICES</div>
        <div class="loc-type">Arquivo corrente</div>
      </div>
      <div class="location-item">
        <div class="loc-dot" style="background:#378ADD;"></div>
        <div class="loc-name">Anexo da Logística</div>
        <div class="loc-type">Arquivo intermediário 01</div>
      </div>
      <div class="location-item">
        <div class="loc-dot" style="background:#BA7517;"></div>
        <div class="loc-name">Anexo DICES</div>
        <div class="loc-type">Arquivo intermediário 02</div>
      </div>
      <div class="location-item">
        <div class="loc-dot" style="background:#D85A30;"></div>
        <div class="loc-name">Depósito compartilhado</div>
        <div class="loc-type">Depósito temporário</div>
      </div>
    </div>
  </div>
</div>

<!-- Editais prioritários -->
<div class="two-col" style="margin-bottom:12px;">
  <div class="card">
    <div class="card-title">Editais prioritários</div>
    <div class="edital-list">
      <div class="edital-item">
        <div class="edital-num">108/2022</div>
        <div class="edital-desc">Professor de Áreas Específicas</div>
        <div class="edital-year">2022</div>
      </div>
      <div class="edital-item">
        <div class="edital-num">109/2022</div>
        <div class="edital-desc">Professor Pedagogo</div>
        <div class="edital-year">2022</div>
      </div>
      <div class="edital-item">
        <div class="edital-num">165/2024</div>
        <div class="edital-desc">PGM</div>
        <div class="edital-year">2024</div>
      </div>
      <div class="edital-item">
        <div class="edital-num">166/2024</div>
        <div class="edital-desc">ACFor</div>
        <div class="edital-year">2024</div>
      </div>
      <div class="edital-item">
        <div class="edital-num">168/2024</div>
        <div class="edital-desc">CGM</div>
        <div class="edital-year">2024</div>
      </div>
    </div>
  </div>

  <div class="card">
    <div class="card-title">Aquisições necessárias</div>
    <div class="location-list">
      <div class="location-item" style="align-items:flex-start; flex-direction:column; gap:2px;">
        <div style="font-weight:500; font-size:12px;">EPIs</div>
        <div class="loc-type">Luvas, máscaras, óculos, jalecos descartáveis</div>
      </div>
      <div class="location-item" style="align-items:flex-start; flex-direction:column; gap:2px;">
        <div style="font-weight:500; font-size:12px;">Estantes metálicas</div>
        <div class="loc-type">Revestimento a base de esmalte por fosfatação (padrão arquivo)</div>
      </div>
      <div class="location-item" style="align-items:flex-start; flex-direction:column; gap:2px;">
        <div style="font-weight:500; font-size:12px;">Caixas-box</div>
        <div class="loc-type">Polionda ou papelão — 14cm × 36cm × 24cm</div>
      </div>
    </div>
  </div>
</div>

<!-- Full table -->
<div class="card">
  <div class="card-title">Cronograma detalhado de atividades</div>
  <table class="task-table">
    <thead>
      <tr>
        <th style="width:80px;">Semana</th>
        <th style="width:95px;">Data</th>
        <th>Atividade</th>
        <th style="width:120px;">Status</th>
      </tr>
    </thead>
    <tbody>
      <tr><td><span class="sem-tag">Sem. 1</span></td><td><span class="date-tag">09/04</span></td><td>Reunião de alinhamento do projeto e definição de atividades</td><td><span class="badge badge-completo">Completo</span></td></tr>
      <tr><td></td><td><span class="date-tag">10/04</span></td><td>Vistoria do Anexo da Logística (futuro Arquivo Intermediário DICES 01)</td><td><span class="badge badge-completo">Completo</span></td></tr>
      <tr><td><span class="sem-tag">Sem. 2</span></td><td><span class="date-tag">14/04</span></td><td>Segunda reunião de alinhamento do projeto e definição de atividades</td><td><span class="badge badge-completo">Completo</span></td></tr>
      <tr><td></td><td><span class="date-tag">15/04</span></td><td>Identificação, localização e agrupamento dos documentos na DICES</td><td><span class="badge badge-completo">Completo</span></td></tr>
      <tr><td></td><td><span class="date-tag">15/04</span></td><td>Preenchimento do Canvas do Projeto de Gestão Documental</td><td><span class="badge badge-completo">Completo</span></td></tr>
      <tr><td></td><td><span class="date-tag">15/04</span></td><td>Criação de etiquetas no padrão do Arquivo Central para identificação dos documentos</td><td><span class="badge badge-completo">Completo</span></td></tr>
      <tr><td></td><td><span class="date-tag">16–17/04</span></td><td>Remanejamento de materiais da logística do Anexo (Artur e Evonildes) + continuidade da organização</td><td><span class="badge badge-completo">Completo</span></td></tr>
      <tr><td><span class="sem-tag">Sem. 3</span></td><td><span class="date-tag">20/04</span></td><td>Reunião de alinhamento + continuidade da identificação e localização dos documentos na DICES</td><td><span class="badge badge-completo">Completo</span></td></tr>
      <tr><td></td><td><span class="date-tag">20/04</span></td><td>Retomada do preenchimento do Canvas do Projeto de Gestão Documental</td><td><span class="badge badge-andamento">Em andamento</span></td></tr>
      <tr><td></td><td><span class="date-tag">22/04</span></td><td>Início da transformação do Anexo da Logística em Arquivo Intermediário 01 da DICES</td><td><span class="badge badge-iniciar">A iniciar</span></td></tr>
      <tr><td></td><td><span class="date-tag">23/04</span></td><td>Elaboração do checklist de documentos produzidos pela DICES</td><td><span class="badge badge-completo">Completo</span></td></tr>
      <tr><td><span class="sem-tag">Sem. 4</span></td><td><span class="date-tag">28/04</span></td><td>Reunião de alinhamento do projeto</td><td><span class="badge badge-completo">Completo</span></td></tr>
      <tr><td></td><td><span class="date-tag">29/04</span></td><td>Transformação estrutural do Anexo da Logística em Arquivo Intermediário 01</td><td><span class="badge badge-iniciar">A iniciar</span></td></tr>
      <tr><td></td><td><span class="date-tag">29/04</span></td><td>Mapeamento dos documentos disponíveis em formato digital (com Homero)</td><td><span class="badge badge-iniciar">A iniciar</span></td></tr>
      <tr><td></td><td><span class="date-tag">30/04</span></td><td>Início da transferência dos documentos para o Arquivo Intermediário 01</td><td><span class="badge badge-iniciar">A iniciar</span></td></tr>
      <tr><td></td><td><span class="date-tag">30/04</span></td><td>Início da confecção do relatório do projeto</td><td><span class="badge badge-andamento">Em andamento</span></td></tr>
      <tr><td><span class="sem-tag">Próx.</span></td><td><span class="date-tag">Maio+</span></td><td>Realização de relatórios semanais e quinzenais</td><td><span class="badge badge-andamento">Em andamento</span></td></tr>
      <tr><td></td><td><span class="date-tag">Maio+</span></td><td>Investigação dos cartões-resposta</td><td><span class="badge badge-iniciar">A iniciar</span></td></tr>
      <tr><td></td><td><span class="date-tag">Maio+</span></td><td>Mapeamento de recursos</td><td><span class="badge badge-iniciar">A iniciar</span></td></tr>
    </tbody>
  </table>
</div>

<div class="footer">
  <p>DICES · Prefeitura Municipal de Fortaleza</p>
  <p>Plano Emergencial de Resgate do Arquivo · Abril 2026</p>
</div>

<script>
new Chart(document.getElementById('statusChart'), {
  type: 'doughnut',
  data: {
    labels: ['Completo', 'Em andamento', 'A iniciar'],
    datasets: [{
      data: [14, 3, 5],
      backgroundColor: ['#639922', '#BA7517', '#378ADD'],
      borderWidth: 2,
      borderColor: '#FFFFFF',
      hoverOffset: 6
    }]
  },
  options: {
    responsive: true,
    maintainAspectRatio: false,
    cutout: '62%',
    plugins: { legend: { display: false }, tooltip: {
      callbacks: { label: ctx => ` ${ctx.label}: ${ctx.raw} tarefa${ctx.raw > 1 ? 's' : ''}` }
    }}
  }
});

new Chart(document.getElementById('weekChart'), {
  type: 'bar',
  data: {
    labels: ['Semana 1', 'Semana 2', 'Semana 3', 'Semana 4'],
    datasets: [
      { label: 'Completo', data: [2, 5, 5, 2], backgroundColor: '#639922', borderRadius: 3, borderSkipped: false },
      { label: 'Em andamento', data: [0, 0, 2, 1], backgroundColor: '#BA7517', borderRadius: 3, borderSkipped: false },
      { label: 'A iniciar', data: [0, 0, 2, 3], backgroundColor: '#378ADD', borderRadius: 3, borderSkipped: false }
    ]
  },
  options: {
    responsive: true,
    maintainAspectRatio: false,
    plugins: { legend: { display: false } },
    scales: {
      x: { stacked: true, grid: { display: false }, ticks: { font: { size: 11, family: "'DM Sans'" } } },
      y: { stacked: true, beginAtZero: true, ticks: { stepSize: 2, font: { size: 11 } }, grid: { color: 'rgba(0,0,0,0.05)' } }
    }
  }
});
</script>

</body>
</html>
