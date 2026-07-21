# CONTROLE-DE-SERVI-O
CONRROLE DE SERVIÇO
[index.html.html](https://github.com/user-attachments/files/30231924/index.html.html)
<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1, maximum-scale=1, user-scalable=no">
<meta name="apple-mobile-web-app-capable" content="yes">
<meta name="apple-mobile-web-app-status-bar-style" content="black-translucent">
<meta name="mobile-web-app-capable" content="yes">
<meta name="theme-color" content="#2A1C12">
<title>Goiânia — Controle de Serviços</title>
<link href="https://fonts.googleapis.com/css2?family=Barlow+Condensed:wght@500;600;700&family=IBM+Plex+Sans:wght@400;500;600&family=IBM+Plex+Mono:wght@500;600&display=swap" rel="stylesheet">
<style>
*{box-sizing:border-box;margin:0;padding:0}
:root{
  --bg:#F4EEE8;--card:#FFFFFF;--ink:#2A1C12;--ink3:#7A6555;
  --ora:#E2570F;--ora2:#B23F06;--ora0:#FCE7D6;
  --ok:#2E7D4F;--err:#B4351F;--mute:#8A7563;--line:#E0D4C8;
  --r:10px;
  --safe-b:env(safe-area-inset-bottom,0px);
}
html{font-size:15px}
body{background:var(--bg);color:var(--ink);font-family:"IBM Plex Sans",system-ui,sans-serif;
  -webkit-text-size-adjust:100%;padding-bottom:calc(62px + var(--safe-b));min-height:100dvh}
h1,h2,h3,.hd{font-family:"Barlow Condensed","Arial Narrow",sans-serif;letter-spacing:.02em}
.mono{font-family:"IBM Plex Mono",ui-monospace,monospace;font-variant-numeric:tabular-nums}
button,input,select,textarea{font:inherit;color:inherit;border:0;background:none}
button{cursor:pointer;-webkit-tap-highlight-color:transparent}
a{color:var(--ora)}

/* HEADER */
.hdr{background:var(--ink);color:#fff;padding:12px 14px;position:sticky;top:0;z-index:20}
.hdr h1{font-size:1.2rem;font-weight:700;text-transform:uppercase}
.hdr h1 em{font-style:normal;color:var(--ora)}
.hdr small{font-size:.6rem;letter-spacing:.16em;text-transform:uppercase;color:#B9A392;display:block;margin-top:1px}

/* BOTTOM NAV */
.bnav{position:fixed;bottom:0;left:0;right:0;background:var(--ink);z-index:50;
  display:flex;justify-content:space-around;padding:5px 2px calc(5px + var(--safe-b));
  border-top:1px solid rgba(255,255,255,.1)}
.bnav button{display:flex;flex-direction:column;align-items:center;gap:2px;color:#8A7563;
  padding:4px 2px;flex:1;min-width:0}
.bnav button svg{width:20px;height:20px;flex-shrink:0}
.bnav button span{font-family:"Barlow Condensed",sans-serif;font-size:.58rem;font-weight:600;
  text-transform:uppercase;letter-spacing:.03em;white-space:nowrap}
.bnav button.on{color:var(--ora)}

/* MAIN */
main{padding:12px;max-width:900px;margin:0 auto}
.tab{display:none}.tab.on{display:block}
.sec-title{margin:4px 0 12px}
.sec-title h2{font-size:1.2rem;text-transform:uppercase}
.sec-title p{font-size:.8rem;color:var(--ink3);margin-top:2px}

/* CARDS */
.c{background:var(--card);border:1px solid var(--line);border-radius:var(--r);padding:14px;margin-bottom:10px}
.c h3{font-size:.95rem;text-transform:uppercase;margin-bottom:2px}
.c .sub{font-size:.72rem;color:var(--ink3);margin-bottom:10px}

/* KPIs */
.kpis{display:grid;grid-template-columns:repeat(2,1fr);gap:8px;margin-bottom:10px}
.kpi{background:var(--card);border:1px solid var(--line);border-radius:var(--r);padding:11px 12px;
  position:relative;overflow:hidden}
.kpi::before{content:"";position:absolute;left:0;top:0;bottom:0;width:4px;background:var(--ora)}
.kpi.ok::before{background:var(--ok)}.kpi.err::before{background:var(--err)}.kpi.m::before{background:var(--mute)}
.kpi .lb{font-size:.58rem;letter-spacing:.1em;text-transform:uppercase;color:var(--ink3)}
.kpi .vl{font-family:"Barlow Condensed",sans-serif;font-size:1.6rem;font-weight:700;line-height:1.1;margin-top:2px}
.kpi .sm{font-size:.66rem;color:var(--ink3)}

/* FORM */
.fg{display:grid;grid-template-columns:1fr 1fr;gap:10px;margin-bottom:10px}
.fg.w{grid-template-columns:1fr}
.fg label{display:block;font-size:.62rem;letter-spacing:.1em;text-transform:uppercase;color:var(--ink3);margin-bottom:4px}
.fg input,.fg select,.fg textarea{width:100%;padding:11px 10px;border:1px solid var(--line);border-radius:8px;
  background:#fff;font-size:1rem;-webkit-appearance:none;appearance:none}
.fg select{background:#fff url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='10' height='6'%3E%3Cpath d='M0 0l5 6 5-6z' fill='%237A6555'/%3E%3C/svg%3E") no-repeat right 12px center;padding-right:30px}
.fg input:focus,.fg select:focus{outline:2px solid var(--ora);border-color:var(--ora)}
.fg .full{grid-column:1/-1}
.checks{display:flex;gap:16px;flex-wrap:wrap;grid-column:1/-1;padding:2px 0}
.checks label{display:flex;align-items:center;gap:6px;font-size:.85rem;text-transform:none;letter-spacing:0;color:var(--ink)}
.checks input[type=checkbox]{width:20px;height:20px;accent-color:var(--ora)}

/* BUTTONS */
.bt{display:block;width:100%;padding:14px;border-radius:10px;font-family:"Barlow Condensed",sans-serif;
  font-size:1.05rem;font-weight:600;text-transform:uppercase;letter-spacing:.04em;text-align:center}
.bt.pr{background:var(--ora);color:#fff}.bt.pr:active{background:var(--ora2)}
.bt.sc{background:none;color:var(--ink);border:1px solid var(--line)}.bt.sc:active{background:var(--ora0)}
.bt.dn{color:var(--err);border:1px solid #EBC9BF;background:none}.bt.dn:active{background:#FBE5E0}
.btrow{display:flex;flex-direction:column;gap:8px;margin-top:12px}

/* TABLE */
.tbl-wrap{overflow-x:auto;-webkit-overflow-scrolling:touch;margin:10px -14px 0;padding:0 14px}
table{width:100%;border-collapse:collapse;font-size:.78rem;min-width:500px}
th{font-family:"Barlow Condensed",sans-serif;font-size:.72rem;text-transform:uppercase;letter-spacing:.06em;
  text-align:left;color:var(--ink3);border-bottom:1px solid var(--line);padding:7px 8px;white-space:nowrap;position:sticky;top:0;background:var(--card)}
td{padding:9px 8px;border-bottom:1px solid #F2EAE2;white-space:nowrap}
.r{text-align:right}
.tag{display:inline-block;padding:2px 7px;border-radius:99px;font-size:.65rem;font-weight:600}
.t1{background:#E1F2E8;color:var(--ok)}.t2{background:var(--ora0);color:var(--ora2)}
.t3{background:#FBE0DB;color:var(--err)}.t4{background:#F0EAE4;color:var(--ink3)}
.del{color:var(--err);font-weight:700;padding:6px 12px;font-size:1.1rem;border-radius:8px}
.del:active{background:#FBE5E0}
.del.armed{background:var(--err);color:#fff}

/* FILTERS */
.flt{display:flex;flex-direction:column;gap:8px;margin-bottom:8px}
.flt label{font-size:.62rem;letter-spacing:.1em;text-transform:uppercase;color:var(--ink3);margin-bottom:3px}
.flt input,.flt select{width:100%;padding:10px;border:1px solid var(--line);border-radius:8px;background:#fff;
  font-size:.95rem;-webkit-appearance:none;appearance:none}
.flt select{background:#fff url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='10' height='6'%3E%3Cpath d='M0 0l5 6 5-6z' fill='%237A6555'/%3E%3C/svg%3E") no-repeat right 12px center;padding-right:30px}
.flt-row{display:grid;grid-template-columns:1fr 1fr;gap:8px}

/* CRACHA */
.team{display:grid;grid-template-columns:1fr;gap:10px;margin-bottom:10px}
.badge{background:var(--card);border:1px solid var(--line);border-radius:var(--r);overflow:hidden}
.badge .stripe{height:5px;background:linear-gradient(90deg,var(--ora),var(--ora2))}
.badge .body{padding:12px}
.badge .nm{font-family:"Barlow Condensed",sans-serif;font-size:1.15rem;font-weight:700;text-transform:uppercase}
.badge .info{font-size:.65rem;letter-spacing:.1em;text-transform:uppercase;color:var(--ink3)}
.stats{display:grid;grid-template-columns:repeat(3,1fr);gap:6px;margin-top:10px;text-align:center}
.stats div{background:var(--bg);border-radius:8px;padding:7px 3px}
.stats b{display:block;font-family:"Barlow Condensed",sans-serif;font-size:1.2rem}
.stats small{font-size:.55rem;letter-spacing:.06em;text-transform:uppercase;color:var(--ink3)}
.pbar{height:6px;background:var(--bg);border-radius:99px;margin-top:10px;overflow:hidden}
.pbar i{display:block;height:100%;background:var(--ora);border-radius:99px}

/* CHARTS */
svg{display:block;max-width:100%}
.legend{display:flex;flex-wrap:wrap;gap:10px;font-size:.7rem;margin-top:6px;color:var(--ink3)}
.legend i{width:9px;height:9px;border-radius:3px;display:inline-block;margin-right:4px}
.empty{padding:20px;text-align:center;color:var(--ink3);font-size:.85rem}

.note{background:var(--ora0);border-left:4px solid var(--ora);padding:10px;border-radius:6px;font-size:.8rem;margin-bottom:12px}

/* TOAST */
#toast{position:fixed;left:10px;right:10px;bottom:calc(68px + var(--safe-b));background:var(--ink);color:#fff;
  padding:12px 16px;border-radius:12px;font-size:.85rem;text-align:center;z-index:60;
  box-shadow:0 6px 20px rgba(0,0,0,.25);display:none;animation:slideUp .25s ease}
#toast.err{background:var(--err)}
@keyframes slideUp{from{opacity:0;transform:translateY(10px)}to{opacity:1;transform:none}}

footer{text-align:center;padding:16px 10px 8px;font-size:.68rem;color:var(--ink3)}

/* DESKTOP */
@media (min-width:641px){
  html{font-size:16px}
  body{padding-bottom:0}
  .bnav{display:none}
  .hdr{padding:14px 18px}
  .hdr h1{font-size:1.45rem}
  .hdr-nav{display:flex;gap:2px;margin-top:10px}
  .hdr-nav button{color:#BCA795;padding:10px 14px;font-family:"Barlow Condensed",sans-serif;
    font-size:1rem;font-weight:600;text-transform:uppercase;letter-spacing:.05em;
    border-bottom:3px solid transparent}
  .hdr-nav button:hover{color:#fff}
  .hdr-nav button.on{color:#fff;border-bottom-color:var(--ora)}
  main{padding:18px;max-width:1100px}
  .kpis{grid-template-columns:repeat(auto-fit,minmax(155px,1fr))}
  .kpi .vl{font-size:2.1rem}
  .kpi .lb{font-size:.65rem}
  .fg{grid-template-columns:repeat(auto-fit,minmax(160px,1fr))}
  .btrow{flex-direction:row;flex-wrap:wrap}
  .bt{width:auto;padding:12px 22px}
  .flt{flex-direction:row;flex-wrap:wrap;align-items:flex-end}
  .flt>div{min-width:150px;flex:1}
  .flt-row{grid-template-columns:repeat(3,1fr)}
  .team{grid-template-columns:repeat(auto-fit,minmax(280px,1fr))}
  .tbl-wrap{margin:10px 0 0;padding:0}
  #toast{left:50%;right:auto;width:360px;transform:translateX(-50%);bottom:24px}
  .c .two{display:grid;grid-template-columns:1fr 1fr;gap:12px}
}
</style>
</head>
<body>

<header class="hdr">
  <h1>Goiânia <em>·</em> Controle de Serviços</h1>
  <small>Gestão de equipe de campo</small>
  <nav class="hdr-nav" id="topnav" style="display:none"></nav>
</header>

<main>
<!-- PAINEL -->
<div class="tab on" id="t-painel">
  <div class="sec-title">
    <h2>Painel</h2><p id="info-painel"></p>
  </div>
  <div class="flt">
    <div><label>Período</label><select id="f-mes"></select></div>
    <div><label>Técnico</label><select id="f-tec-p"></select></div>
  </div>
  <div class="kpis" id="kpis"></div>
  <div class="c"><h3>Serviços por técnico</h3><div class="sub">Total no período.</div><div id="ch-tec"></div></div>
  <div class="c"><h3>Volume diário</h3><div class="sub">Atendimentos por dia.</div><div id="ch-dia"></div></div>
  <div class="c"><h3>Tipos de serviço</h3><div class="sub">Distribuição.</div><div id="ch-tipo"></div></div>
  <div class="c"><h3>Faturamento por técnico</h3><div class="sub">Serviços com sucesso.</div><div id="ch-fat"></div></div>
  <div class="c"><h3>Taxa de sucesso</h3><div class="sub">Por técnico.</div><div id="ch-suc"></div></div>
  <div class="c"><h3>Sem sucesso — Pareto</h3><div class="sub">Onde atacar primeiro.</div><div id="ch-sem"></div></div>
</div>

<!-- LANÇAMENTOS -->
<div class="tab" id="t-lanc">
  <div class="sec-title"><h2>Lançar serviço</h2><p>Um registro por OS.</p></div>
  <div class="c">
    <div class="fg">
      <div><label>Data</label><input type="date" id="c-dt"></div>
      <div><label>Nº do serviço</label><input id="c-os" placeholder="4281093/26"></div>
      <div><label>Técnico</label><select id="c-tc"></select></div>
      <div><label>Tipo de serviço</label><select id="c-tp"></select></div>
      <div><label>Status</label><select id="c-st">
        <option>COM SUCESSO</option><option>SEM SUCESSO</option><option>RETORNO</option>
        <option>RETORNO INDEVIDO</option><option>SERVIÇO CANCELADO</option><option>APOIO</option></select></div>
      <div><label>Valor R$</label><input type="number" step="0.01" id="c-vl" inputmode="decimal" placeholder="0,00"></div>
      <div><label>A receber R$</label><input type="number" step="0.01" id="c-rc" inputmode="decimal" placeholder="0,00"></div>
      <div class="checks">
        <label><input type="checkbox" id="c-18">Após 18h</label>
        <label><input type="checkbox" id="c-fe">Feriado</label>
        <label><input type="checkbox" id="c-do">Domingo</label>
      </div>
    </div>
    <div class="btrow">
      <button class="bt pr" id="btn-save">Salvar lançamento</button>
      <button class="bt sc" id="btn-clr">Limpar</button>
    </div>
  </div>
  <div class="c">
    <h3>Lançamentos</h3>
    <div class="flt">
      <div class="flt-row">
        <div><label>Técnico</label><select id="fl-tc"></select></div>
        <div><label>Status</label><select id="fl-st"><option value="">Todos</option>
          <option>COM SUCESSO</option><option>SEM SUCESSO</option><option>RETORNO</option>
          <option>RETORNO INDEVIDO</option><option>SERVIÇO CANCELADO</option><option>APOIO</option></select></div>
      </div>
      <div><label>Buscar</label><input id="fl-q" placeholder="Nº do serviço ou tipo"></div>
    </div>
    <div class="tbl-wrap"><table><thead><tr>
      <th>Data</th><th>OS</th><th>Técnico</th><th>Tipo</th><th>Status</th>
      <th class="r">Valor</th><th class="r">Receber</th><th></th>
    </tr></thead><tbody id="tb-lanc"></tbody></table></div>
    <div class="sub" id="tb-sum" style="margin-top:8px"></div>
  </div>
</div>

<!-- RETORNOS -->
<div class="tab" id="t-ret">
  <div class="sec-title"><h2>Retornos</h2><p>Custo: VTR, hora técnica e confiança.</p></div>
  <div class="kpis" id="kpis-r"></div>
  <div class="c"><h3>Por técnico de origem</h3><div class="sub">Quem gerou o retorno.</div><div id="ch-rt"></div></div>
  <div class="c"><h3>Motivos</h3><div class="sub">Pareto dos motivos.</div><div id="ch-rm"></div></div>
  <div class="c">
    <h3>Registrar retorno</h3>
    <div class="fg">
      <div><label>Data</label><input type="date" id="r-dt"></div>
      <div><label>Nº retorno</label><input id="r-os"></div>
      <div><label>Serviço original</label><input id="r-oo"></div>
      <div><label>Tipo</label><select id="r-tp"></select></div>
      <div><label>Status original</label><select id="r-so"><option>COM SUCESSO</option><option>SEM SUCESSO</option></select></div>
      <div><label>Técnico original</label><select id="r-to"></select></div>
      <div class="full"><label>Motivo</label><input id="r-mt" placeholder="GARANTIA"></div>
      <div><label>Técnico do retorno</label><select id="r-tr"></select></div>
      <div><label>Devido/Indevido</label><select id="r-dv"><option>DEVIDO</option><option>INDEVIDO</option></select></div>
      <div><label>Resultado</label><select id="r-rs"><option>COM SUCESSO</option><option>SEM SUCESSO</option><option>PENDENTE</option></select></div>
    </div>
    <div class="btrow"><button class="bt pr" id="btn-ret">Salvar retorno</button></div>
    <div class="tbl-wrap"><table><thead><tr>
      <th>Data</th><th>Retorno</th><th>Original</th><th>Tipo</th><th>Tec. origem</th>
      <th>Motivo</th><th>Tec. ret.</th><th>Class.</th><th>Result.</th><th></th>
    </tr></thead><tbody id="tb-ret"></tbody></table></div>
  </div>
</div>

<!-- GASTOS -->
<div class="tab" id="t-gas">
  <div class="sec-title"><h2>Gastos</h2><p>Receita menos despesas.</p></div>
  <div class="kpis" id="kpis-g"></div>
  <div class="c"><h3>Por categoria</h3><div class="sub">Maior peso primeiro.</div><div id="ch-gc"></div></div>
  <div class="c">
    <h3>Lançar gasto</h3>
    <div class="fg">
      <div><label>Data</label><input type="date" id="g-dt"></div>
      <div><label>Categoria</label><select id="g-ct"></select></div>
      <div><label>Valor R$</label><input type="number" step="0.01" id="g-vl" inputmode="decimal"></div>
      <div class="full"><label>Descrição</label><input id="g-ds" placeholder="Kit embreagem"></div>
    </div>
    <div class="btrow"><button class="bt pr" id="btn-gas">Salvar gasto</button></div>
    <div class="tbl-wrap"><table><thead><tr>
      <th>Data</th><th>Categoria</th><th>Descrição</th><th class="r">Valor</th><th></th>
    </tr></thead><tbody id="tb-gas"></tbody></table></div>
  </div>
</div>

<!-- EQUIPE -->
<div class="tab" id="t-eq">
  <div class="sec-title"><h2>Equipe</h2><p>Desempenho no período do painel.</p></div>
  <div class="team" id="badges"></div>
  <div class="c">
    <h3>Cadastros</h3><div class="sub">Um item por linha.</div>
    <div class="fg w"><div><label>Técnicos</label><textarea id="lst-tc" rows="4" style="width:100%;padding:10px;border:1px solid var(--line);border-radius:8px;font-size:.95rem"></textarea></div></div>
    <div class="fg w"><div><label>Tipos de serviço</label><textarea id="lst-tp" rows="5" style="width:100%;padding:10px;border:1px solid var(--line);border-radius:8px;font-size:.95rem"></textarea></div></div>
    <div class="btrow"><button class="bt pr" id="btn-cad">Atualizar cadastros</button></div>
  </div>
</div>

<!-- DADOS -->
<div class="tab" id="t-dados">
  <div class="sec-title"><h2>Dados</h2><p>Importar, exportar, backup.</p></div>
  <div class="note">Dados ficam neste navegador. Para trocar de aparelho, use o backup JSON.</div>
  <div class="c">
    <h3>Importar planilha</h3>
    <div class="sub">Aceita o .xlsx do Controle de Serviço ou .csv.</div>
    <input type="file" id="arq" accept=".xlsx,.xls,.csv" style="margin:8px 0;font-size:.9rem">
    <label style="display:flex;align-items:center;gap:6px;font-size:.85rem;margin:6px 0">
      <input type="checkbox" id="chk-sub" checked style="width:20px;height:20px;accent-color:var(--ora)"> Substituir tudo
    </label>
    <p id="msg-imp" style="font-size:.82rem;margin-top:6px"></p>
  </div>
  <div class="c">
    <h3>Exportar</h3>
    <div class="sub">Excel com lançamentos, retornos, gastos e resumo.</div>
    <div class="btrow">
      <button class="bt pr" id="btn-xl">Baixar Excel</button>
      <button class="bt sc" id="btn-csv">Baixar CSV</button>
      <button class="bt sc" id="btn-bkp">Backup JSON</button>
      <button class="bt sc" id="btn-rest">Restaurar backup</button>
      <input type="file" id="arq-j" accept=".json" hidden>
    </div>
  </div>
  <div class="c">
    <h3>Zona perigosa</h3>
    <div class="btrow">
      <button class="bt dn" id="btn-wipe">Apagar todos os dados</button>
    </div>
  </div>
</div>
</main>

<nav class="bnav" id="bnav">
  <button data-t="painel" class="on"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><rect x="3" y="3" width="7" height="7" rx="1"/><rect x="14" y="3" width="7" height="7" rx="1"/><rect x="3" y="14" width="7" height="7" rx="1"/><rect x="14" y="14" width="7" height="7" rx="1"/></svg><span>Painel</span></button>
  <button data-t="lanc"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M12 5v14M5 12h14"/></svg><span>Lançar</span></button>
  <button data-t="ret"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><polyline points="1 4 1 10 7 10"/><path d="M3.51 15a9 9 0 1 0 2.13-9.36L1 10"/></svg><span>Retornos</span></button>
  <button data-t="gas"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><line x1="12" y1="1" x2="12" y2="23"/><path d="M17 5H9.5a3.5 3.5 0 0 0 0 7h5a3.5 3.5 0 0 1 0 7H6"/></svg><span>Gastos</span></button>
  <button data-t="eq"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M17 21v-2a4 4 0 0 0-4-4H5a4 4 0 0 0-4 4v2"/><circle cx="9" cy="7" r="4"/></svg><span>Equipe</span></button>
  <button data-t="dados"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M21 15v4a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2v-4"/><polyline points="7 10 12 15 17 10"/><line x1="12" y1="15" x2="12" y2="3"/></svg><span>Dados</span></button>
</nav>

<div id="toast"></div>
<footer>Controle de Serviços · Goiânia</footer>

<script>
var SEED_DATA = {"lancamentos": [{"id": "L000", "data": "2026-07-01", "os": "4281093/26", "tecnico": "WILSON BARBOSA", "tipo": "VENTILADOR", "valor": 159.0, "receber": 15.0, "status": "COM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L001", "data": "2026-07-01", "os": "4357747/26", "tecnico": "WILSON BARBOSA", "tipo": "HIDRÁULICO", "valor": 0.0, "receber": 0.0, "status": "SERVIÇO CANCELADO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L002", "data": "2026-07-01", "os": "4346698/26", "tecnico": "WILSON BARBOSA", "tipo": "HIDRÁULICO", "valor": 128.0, "receber": 15.0, "status": "COM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L003", "data": "2026-07-01", "os": "4303952/26", "tecnico": "WILSON BARBOSA", "tipo": "HIDRÁULICO", "valor": 128.0, "receber": 15.0, "status": "COM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L004", "data": "2026-07-01", "os": "4331530/26", "tecnico": "WILSON BARBOSA", "tipo": "ELÉTRICO", "valor": 128.0, "receber": 15.0, "status": "COM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L005", "data": "2026-07-01", "os": "4345111/26", "tecnico": "WILSON BARBOSA", "tipo": "HIDRÁULICO", "valor": 128.0, "receber": 15.0, "status": "COM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L006", "data": "2026-07-01", "os": "4341130/26", "tecnico": "EGILSON FERREIRA", "tipo": "ELÉTRICO", "valor": 232.0, "receber": 25.0, "status": "COM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L007", "data": "2026-07-01", "os": "4336511/26", "tecnico": "EGILSON FERREIRA", "tipo": "ELÉTRICO", "valor": 52.0, "receber": 0.0, "status": "SEM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L008", "data": "2026-07-01", "os": "4347192/26", "tecnico": "EGILSON FERREIRA", "tipo": "ELÉTRICO", "valor": 128.0, "receber": 15.0, "status": "COM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L009", "data": "2026-07-01", "os": "4353364/26", "tecnico": "EGILSON FERREIRA", "tipo": "ELÉTRICO", "valor": 128.0, "receber": 15.0, "status": "COM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L010", "data": "2026-07-01", "os": "4343603/26", "tecnico": "EGILSON FERREIRA", "tipo": "FIXAÇAO", "valor": 140.0, "receber": 15.0, "status": "COM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L011", "data": "2026-07-01", "os": "4178125/26", "tecnico": "WILSON BARBOSA", "tipo": "HIDRÁULICO", "valor": 128.0, "receber": 15.0, "status": "COM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L012", "data": "2026-07-01", "os": "4356515/26", "tecnico": "EGILSON FERREIRA", "tipo": "ELÉTRICO", "valor": 128.0, "receber": 15.0, "status": "COM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L013", "data": "2026-07-01", "os": "4364937/26", "tecnico": "EGILSON FERREIRA", "tipo": "ELÉTRICO", "valor": 133.82, "receber": 20.0, "status": "COM SUCESSO", "apos18": true, "feriado": false, "domingo": false}, {"id": "L014", "data": "2026-07-01", "os": "4362623/26", "tecnico": "WILSON BARBOSA", "tipo": "ELÉTRICO", "valor": 166.28, "receber": 20.0, "status": "COM SUCESSO", "apos18": true, "feriado": false, "domingo": false}, {"id": "L015", "data": "2026-07-01", "os": "4356396/26", "tecnico": "EGILSON FERREIRA", "tipo": "ELÉTRICO", "valor": 155.0, "receber": 20.0, "status": "COM SUCESSO", "apos18": true, "feriado": false, "domingo": false}, {"id": "L016", "data": "2026-07-02", "os": "4360017/26", "tecnico": "WESLEY SILVA", "tipo": "HIDRÁULICO", "valor": 52.0, "receber": 0.0, "status": "SEM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L017", "data": "2026-07-02", "os": "4369737/26", "tecnico": "EGILSON FERREIRA", "tipo": "FIXAÇAO", "valor": 88.0, "receber": 15.0, "status": "RETORNO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L018", "data": "2026-07-02", "os": "4362780/26", "tecnico": "EGILSON FERREIRA", "tipo": "ELÉTRICO", "valor": 128.0, "receber": 15.0, "status": "COM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L019", "data": "2026-07-02", "os": "4369619/26", "tecnico": "WESLEY SILVA", "tipo": "HIDRÁULICO", "valor": 128.0, "receber": 15.0, "status": "COM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L020", "data": "2026-07-02", "os": "4365593/26", "tecnico": "EGILSON FERREIRA", "tipo": "ELÉTRICO", "valor": 128.0, "receber": 15.0, "status": "COM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L021", "data": "2026-07-02", "os": "4361209/26", "tecnico": "WESLEY SILVA", "tipo": "HIDRÁULICO", "valor": 128.0, "receber": 15.0, "status": "COM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L022", "data": "2026-07-02", "os": "4371945/26", "tecnico": "EGILSON FERREIRA", "tipo": "ELÉTRICO", "valor": 232.0, "receber": 25.0, "status": "COM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L023", "data": "2026-07-02", "os": "4367158/26", "tecnico": "WESLEY SILVA", "tipo": "DESENTUPIMENTO", "valor": 153.0, "receber": 15.0, "status": "COM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L024", "data": "2026-07-02", "os": "4358795/26", "tecnico": "EGILSON FERREIRA", "tipo": "HIDRÁULICO", "valor": 145.0, "receber": 15.0, "status": "COM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L025", "data": "2026-07-02", "os": "4383046/26", "tecnico": "WESLEY SILVA", "tipo": "ELÉTRICO", "valor": 201.67, "receber": 0.0, "status": "SEM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L026", "data": "2026-07-03", "os": "4378920/26", "tecnico": "EGILSON FERREIRA", "tipo": "ELÉTRICO", "valor": 128.0, "receber": 15.0, "status": "COM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L027", "data": "2026-07-03", "os": "4390078/26", "tecnico": "WESLEY SILVA", "tipo": "OUTROS SERVIÇOS", "valor": 52.0, "receber": 0.0, "status": "SEM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L028", "data": "2026-07-03", "os": "4383396/26", "tecnico": "EGILSON FERREIRA", "tipo": "ELÉTRICO", "valor": 128.0, "receber": 15.0, "status": "COM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L029", "data": "2026-07-03", "os": "4388687/26", "tecnico": "WESLEY SILVA", "tipo": "HIDRÁULICO", "valor": 128.0, "receber": 15.0, "status": "COM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L030", "data": "2026-07-03", "os": "4389405/26", "tecnico": "WESLEY SILVA", "tipo": "HIDRÁULICO", "valor": 128.0, "receber": 15.0, "status": "COM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L031", "data": "2026-07-03", "os": "4386488/26", "tecnico": "EGILSON FERREIRA", "tipo": "ELÉTRICO", "valor": 128.0, "receber": 15.0, "status": "COM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L032", "data": "2026-07-03", "os": "4389216/26", "tecnico": "EGILSON FERREIRA", "tipo": "ELÉTRICO", "valor": 128.0, "receber": 15.0, "status": "COM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L033", "data": "2026-07-03", "os": "4390557/26", "tecnico": "WESLEY SILVA", "tipo": "DESENTUPIMENTO", "valor": 153.0, "receber": 15.0, "status": "COM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L034", "data": "2026-07-03", "os": "4393440/26", "tecnico": "WESLEY SILVA", "tipo": "OUTROS SERVIÇOS", "valor": 159.0, "receber": 15.0, "status": "COM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L035", "data": "2026-07-03", "os": "4390141/26", "tecnico": "WESLEY SILVA", "tipo": "HIDRÁULICO", "valor": 0.0, "receber": 0.0, "status": "RETORNO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L036", "data": "2026-07-04", "os": "4407518/26", "tecnico": "WESLEY SILVA", "tipo": "HIDRÁULICO", "valor": 130.82, "receber": 15.0, "status": "COM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L037", "data": "2026-07-04", "os": "4403099/26", "tecnico": "EGILSON FERREIRA", "tipo": "ELÉTRICO", "valor": 128.0, "receber": 15.0, "status": "COM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L038", "data": "2026-07-04", "os": "4407793/26", "tecnico": "EGILSON FERREIRA", "tipo": "ELÉTRICO", "valor": 52.0, "receber": 0.0, "status": "SEM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L039", "data": "2026-07-04", "os": "4386374/26", "tecnico": "EGILSON FERREIRA", "tipo": "ELÉTRICO", "valor": 52.0, "receber": 0.0, "status": "SEM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L040", "data": "2026-07-04", "os": "4412506/26", "tecnico": "EGILSON FERREIRA", "tipo": "ELÉTRICO", "valor": 284.0, "receber": 35.0, "status": "RETORNO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L041", "data": "2026-07-04", "os": "4411381/26", "tecnico": "WESLEY SILVA", "tipo": "HIDRÁULICO", "valor": 52.0, "receber": 0.0, "status": "SEM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L042", "data": "2026-07-04", "os": "4404355/26", "tecnico": "EGILSON FERREIRA", "tipo": "ELÉTRICO", "valor": 52.0, "receber": 0.0, "status": "SEM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L043", "data": "2026-07-04", "os": "4407873/26", "tecnico": "WESLEY SILVA", "tipo": "HIDRÁULICO", "valor": 232.0, "receber": 25.0, "status": "COM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L044", "data": "2026-07-04", "os": "4397621/26", "tecnico": "EGILSON FERREIRA", "tipo": "ELÉTRICO", "valor": 232.0, "receber": 25.0, "status": "COM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L045", "data": "2026-07-04", "os": "4414484/26", "tecnico": "EGILSON FERREIRA", "tipo": "ELÉTRICO", "valor": 128.0, "receber": 15.0, "status": "COM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L046", "data": "2026-07-04", "os": "4415662/26", "tecnico": "EGILSON FERREIRA", "tipo": "ELÉTRICO", "valor": 155.0, "receber": 20.0, "status": "COM SUCESSO", "apos18": true, "feriado": false, "domingo": false}, {"id": "L047", "data": "2026-07-04", "os": "4406136/26", "tecnico": "WESLEY SILVA", "tipo": "OUTROS SERVIÇOS", "valor": 233.82, "receber": 15.0, "status": "COM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L048", "data": "2026-07-04", "os": "4416228/26", "tecnico": "EGILSON FERREIRA", "tipo": "ELÉTRICO", "valor": 131.0, "receber": 20.0, "status": "COM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L049", "data": "2026-07-05", "os": "4414392/26", "tecnico": "EGILSON FERREIRA", "tipo": "FIXAÇAO", "valor": 254.7, "receber": 20.0, "status": "COM SUCESSO", "apos18": false, "feriado": false, "domingo": true}, {"id": "L050", "data": "2026-07-06", "os": "4338780/26", "tecnico": "EGILSON FERREIRA", "tipo": "VENTILADOR", "valor": 52.0, "receber": 0.0, "status": "SEM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L051", "data": "2026-07-06", "os": "4395758/26", "tecnico": "EGILSON FERREIRA", "tipo": "ELÉTRICO", "valor": 232.0, "receber": 25.0, "status": "COM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L052", "data": "2026-07-06", "os": "4426040/26", "tecnico": "EGILSON FERREIRA", "tipo": "ELÉTRICO", "valor": 128.0, "receber": 15.0, "status": "COM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L053", "data": "2026-07-06", "os": "4428752/26", "tecnico": "EGILSON FERREIRA", "tipo": "LIMPEZA DE CAIXA D'ÁGUA", "valor": 232.81, "receber": 15.0, "status": "COM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L054", "data": "2026-07-06", "os": "4435091/26", "tecnico": "EGILSON FERREIRA", "tipo": "ELÉTRICO", "valor": 104.0, "receber": 15.0, "status": "RETORNO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L055", "data": "2026-07-06", "os": "4428475/26", "tecnico": "EGILSON FERREIRA", "tipo": "ELÉTRICO", "valor": 0.0, "receber": 0.0, "status": "RETORNO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L056", "data": "2026-07-07", "os": "4448376/26", "tecnico": "EGILSON FERREIRA", "tipo": "FIXAÇAO", "valor": 52.0, "receber": 0.0, "status": "SEM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L057", "data": "2026-07-07", "os": "4457453/26", "tecnico": "WESLEY SILVA", "tipo": "ELÉTRICO", "valor": 52.0, "receber": 0.0, "status": "SEM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L058", "data": "2026-07-08", "os": "4459267/26", "tecnico": "WILSON BARBOSA", "tipo": "ELÉTRICO", "valor": 52.0, "receber": 0.0, "status": "SEM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L059", "data": "2026-07-07", "os": "4447107/26", "tecnico": "EGILSON FERREIRA", "tipo": "ELÉTRICO", "valor": 128.0, "receber": 15.0, "status": "COM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L060", "data": "2026-07-07", "os": "4438768/26", "tecnico": "WESLEY SILVA", "tipo": "ELÉTRICO", "valor": 128.0, "receber": 15.0, "status": "COM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L061", "data": "2026-07-07", "os": "4447623/26", "tecnico": "EGILSON FERREIRA", "tipo": "ELÉTRICO", "valor": 128.0, "receber": 15.0, "status": "COM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L062", "data": "2026-07-07", "os": "4441773/26", "tecnico": "WESLEY SILVA", "tipo": "HIDRÁULICO", "valor": 128.0, "receber": 15.0, "status": "COM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L063", "data": "2026-07-07", "os": "4453525/26", "tecnico": "WESLEY SILVA", "tipo": "ELÉTRICO", "valor": 232.0, "receber": 25.0, "status": "COM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L064", "data": "2026-07-07", "os": "4453742/26", "tecnico": "EGILSON FERREIRA", "tipo": "ELÉTRICO", "valor": 232.0, "receber": 25.0, "status": "COM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L065", "data": "2026-07-07", "os": "4438903/26", "tecnico": "WESLEY SILVA", "tipo": "ELÉTRICO", "valor": 128.0, "receber": 15.0, "status": "COM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L066", "data": "2026-07-07", "os": "4454626/26", "tecnico": "WESLEY SILVA", "tipo": "HIDRÁULICO", "valor": 128.0, "receber": 15.0, "status": "COM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L067", "data": "2026-07-07", "os": "4438479/26", "tecnico": "WESLEY SILVA", "tipo": "ELÉTRICO", "valor": 232.0, "receber": 25.0, "status": "COM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L068", "data": "2026-07-07", "os": "4460413/26", "tecnico": "EGILSON FERREIRA", "tipo": "ELÉTRICO", "valor": 232.0, "receber": 25.0, "status": "COM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L069", "data": "2026-07-08", "os": "4451593/26", "tecnico": "WILSON BARBOSA", "tipo": "HIDRÁULICO", "valor": 128.0, "receber": 15.0, "status": "COM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L070", "data": "2026-07-08", "os": "4458558/26", "tecnico": "WILSON BARBOSA", "tipo": "ELÉTRICO", "valor": 232.0, "receber": 25.0, "status": "COM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L071", "data": "2026-07-08", "os": "4468618/26", "tecnico": "WILSON BARBOSA", "tipo": "ELÉTRICO", "valor": 128.0, "receber": 15.0, "status": "COM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L072", "data": "2026-07-08", "os": "4444907/26", "tecnico": "WILSON BARBOSA", "tipo": "HIDRÁULICO", "valor": 128.0, "receber": 15.0, "status": "COM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L073", "data": "2026-07-08", "os": "4475554/26", "tecnico": "WILSON BARBOSA", "tipo": "HIDRÁULICO", "valor": 128.0, "receber": 15.0, "status": "COM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L074", "data": "2026-07-08", "os": "4462494/26", "tecnico": "WESLEY SILVA", "tipo": "LIMPEZA DE CALHAS", "valor": 165.64, "receber": 15.0, "status": "COM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L075", "data": "2026-07-08", "os": "4457501/26", "tecnico": "WESLEY SILVA", "tipo": "DESENTUPIMENTO", "valor": 301.97, "receber": 15.0, "status": "COM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L076", "data": "2026-07-09", "os": "4487263/26", "tecnico": "WILSON BARBOSA", "tipo": "ELÉTRICO", "valor": 52.0, "receber": 0.0, "status": "SEM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L077", "data": "2026-07-10", "os": "4449880/26", "tecnico": "WILSON BARBOSA", "tipo": "HIDRÁULICO", "valor": 52.0, "receber": 0.0, "status": "SEM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L078", "data": "2026-07-09", "os": "4490145/26", "tecnico": "WESLEY SILVA", "tipo": "HIDRÁULICO", "valor": 60.46, "receber": 0.0, "status": "SEM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L079", "data": "2026-07-09", "os": "4491618/26", "tecnico": "WESLEY SILVA", "tipo": "LIMPEZA DE CAIXA D'ÁGUA", "valor": 157.0, "receber": 15.0, "status": "COM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L080", "data": "2026-07-09", "os": "4467381/26", "tecnico": "WILSON BARBOSA", "tipo": "HIDRÁULICO", "valor": 167.0, "receber": 15.0, "status": "COM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L081", "data": "2026-07-09", "os": "4487687/26", "tecnico": "WILSON BARBOSA", "tipo": "ELÉTRICO", "valor": 128.0, "receber": 15.0, "status": "COM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L082", "data": "2026-07-09", "os": "4488557/26", "tecnico": "WILSON BARBOSA", "tipo": "ELÉTRICO", "valor": 128.0, "receber": 15.0, "status": "COM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L083", "data": "2026-07-09", "os": "4468756/26", "tecnico": "WILSON BARBOSA", "tipo": "ELÉTRICO", "valor": 128.0, "receber": 15.0, "status": "COM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L084", "data": "2026-07-10", "os": "4495481/26", "tecnico": "WESLEY SILVA", "tipo": "ELÉTRICO", "valor": 232.0, "receber": 25.0, "status": "COM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L085", "data": "2026-07-10", "os": "4494742/26", "tecnico": "WESLEY SILVA", "tipo": "DESENTUPIMENTO", "valor": 153.0, "receber": 15.0, "status": "COM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L086", "data": "2026-07-09", "os": "4497282/26", "tecnico": "WILSON BARBOSA", "tipo": "DESENTUPIMENTO", "valor": 153.0, "receber": 15.0, "status": "COM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L087", "data": "2026-07-09", "os": "4497503/26", "tecnico": "WILSON BARBOSA", "tipo": "DESENTUPIMENTO", "valor": 278.0, "receber": 15.0, "status": "COM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L088", "data": "2026-07-09", "os": "4490003/26", "tecnico": "WILSON BARBOSA", "tipo": "DESENTUPIMENTO", "valor": 153.0, "receber": 15.0, "status": "COM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L089", "data": "2026-07-09", "os": "4497934/26", "tecnico": "WESLEY SILVA", "tipo": "HIDRÁULICO", "valor": 214.94, "receber": 15.0, "status": "COM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L090", "data": "2026-07-09", "os": "4491110/26", "tecnico": "WESLEY SILVA", "tipo": "DESENTUPIMENTO", "valor": 334.4, "receber": 15.0, "status": "COM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L091", "data": "2026-07-08", "os": "4485868/26", "tecnico": "WILSON BARBOSA", "tipo": "HIDRÁULICO", "valor": 93.1, "receber": 0.0, "status": "SEM SUCESSO", "apos18": true, "feriado": false, "domingo": false}, {"id": "L092", "data": "2026-07-10", "os": "4488224/26", "tecnico": "WILSON BARBOSA", "tipo": "HIDRÁULICO", "valor": 76.0, "receber": 15.0, "status": "RETORNO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L093", "data": "2026-07-10", "os": "4501660/26", "tecnico": "WESLEY SILVA", "tipo": "FIXAÇAO", "valor": 52.0, "receber": 0.0, "status": "RETORNO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L094", "data": "2026-07-10", "os": "4493992/26", "tecnico": "WILSON BARBOSA", "tipo": "HIDRÁULICO", "valor": 52.0, "receber": 0.0, "status": "SEM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L095", "data": "2026-07-10", "os": "4515985/26", "tecnico": "WESLEY SILVA", "tipo": "INSTA COIFAS E DEPURADORES", "valor": 162.0, "receber": 20.0, "status": "COM SUCESSO", "apos18": true, "feriado": false, "domingo": false}, {"id": "L096", "data": "2026-07-10", "os": "4503679/26", "tecnico": "WILSON BARBOSA", "tipo": "HIDRÁULICO", "valor": 128.0, "receber": 15.0, "status": "COM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L097", "data": "2026-07-10", "os": "4505142/26", "tecnico": "WESLEY SILVA", "tipo": "ELÉTRICO", "valor": 232.0, "receber": 25.0, "status": "COM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L098", "data": "2026-07-10", "os": "4462533/26", "tecnico": "WESLEY SILVA", "tipo": "ELÉTRICO", "valor": 128.0, "receber": 15.0, "status": "COM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L099", "data": "2026-07-10", "os": "4487556/26", "tecnico": "WESLEY SILVA", "tipo": "ELÉTRICO", "valor": 232.0, "receber": 25.0, "status": "COM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L100", "data": "2026-07-10", "os": "4501296/26", "tecnico": "WILSON BARBOSA", "tipo": "HIDRÁULICO", "valor": 128.0, "receber": 15.0, "status": "COM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L101", "data": "2026-07-10", "os": "4506744/26", "tecnico": "WILSON BARBOSA", "tipo": "ELÉTRICO", "valor": 128.0, "receber": 15.0, "status": "COM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L102", "data": "2026-07-10", "os": "4515152/26", "tecnico": "WESLEY SILVA", "tipo": "HIDRÁULICO", "valor": 271.0, "receber": 25.0, "status": "COM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L103", "data": "2026-07-10", "os": "4519011/26", "tecnico": "WILSON BARBOSA", "tipo": "HIDRÁULICO", "valor": 133.64, "receber": 15.0, "status": "COM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L104", "data": "2026-07-10", "os": "4500508/26", "tecnico": "WILSON BARBOSA", "tipo": "HIDRÁULICO", "valor": 128.0, "receber": 15.0, "status": "COM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L105", "data": "2026-07-10", "os": "4494152/26", "tecnico": "WESLEY SILVA", "tipo": "DESENTUPIMENTO", "valor": 153.0, "receber": 15.0, "status": "COM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L106", "data": "2026-07-11", "os": "4520603/26", "tecnico": "WESLEY SILVA", "tipo": "ELÉTRICO", "valor": 128.0, "receber": 15.0, "status": "COM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L107", "data": "2026-07-11", "os": "4524726/26", "tecnico": "WILSON BARBOSA", "tipo": "HIDRÁULICO", "valor": 129.41, "receber": 15.0, "status": "COM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L108", "data": "2026-07-11", "os": "4529538/26", "tecnico": "WESLEY SILVA", "tipo": "HIDRÁULICO", "valor": 52.0, "receber": 0.0, "status": "SEM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L109", "data": "2026-07-11", "os": "4531257/26", "tecnico": "WESLEY SILVA", "tipo": "ELÉTRICO", "valor": 104.0, "receber": 10.0, "status": "COM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L110", "data": "2026-07-11", "os": "4528329/26", "tecnico": "WESLEY SILVA", "tipo": "ELÉTRICO", "valor": 208.0, "receber": 20.0, "status": "COM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L111", "data": "2026-07-11", "os": "4527768/26", "tecnico": "WILSON BARBOSA", "tipo": "APOIO OPERACIONAL", "valor": 118.0, "receber": 15.0, "status": "APOIO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L112", "data": "2026-07-11", "os": "4527570/26", "tecnico": "WILSON BARBOSA", "tipo": "ELÉTRICO", "valor": 128.0, "receber": 15.0, "status": "COM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L113", "data": "2026-07-11", "os": "4525334/26", "tecnico": "WESLEY SILVA", "tipo": "ELÉTRICO", "valor": 336.0, "receber": 35.0, "status": "COM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L114", "data": "2026-07-11", "os": "4530238/26", "tecnico": "WILSON BARBOSA", "tipo": "HIDRÁULICO", "valor": 128.0, "receber": 15.0, "status": "COM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L115", "data": "2026-07-11", "os": "4528327/26", "tecnico": "WESLEY SILVA", "tipo": "HIDRÁULICO", "valor": 128.0, "receber": 15.0, "status": "COM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L116", "data": "2026-07-11", "os": "4523651/26", "tecnico": "WILSON BARBOSA", "tipo": "HIDRÁULICO", "valor": 128.0, "receber": 15.0, "status": "COM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L117", "data": "2026-07-11", "os": "4509516/26", "tecnico": "WILSON BARBOSA", "tipo": "ELÉTRICO", "valor": 128.0, "receber": 15.0, "status": "COM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L118", "data": "2026-07-11", "os": "4532868/26", "tecnico": "WILSON BARBOSA", "tipo": "HIDRÁULICO", "valor": 185.33, "receber": 15.0, "status": "COM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L119", "data": "2026-07-11", "os": "4524969/26", "tecnico": "WESLEY SILVA", "tipo": "FIXAÇAO", "valor": 140.0, "receber": 15.0, "status": "COM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L120", "data": "2026-07-11", "os": "4525311/26", "tecnico": "WESLEY SILVA", "tipo": "FIXAÇAO", "valor": 140.0, "receber": 15.0, "status": "COM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L121", "data": "2026-07-13", "os": "4544012/26", "tecnico": "EGILSON FERREIRA", "tipo": "ELÉTRICO", "valor": 52.0, "receber": 0.0, "status": "SEM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L122", "data": "2026-07-13", "os": "4530213/26", "tecnico": "EGILSON FERREIRA", "tipo": "ELÉTRICO", "valor": 52.0, "receber": 0.0, "status": "SEM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L123", "data": "2026-07-13", "os": "4540031/26", "tecnico": "EGILSON FERREIRA", "tipo": "FIXAÇAO", "valor": 125.0, "receber": 15.0, "status": "COM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L124", "data": "2026-07-13", "os": "4544455/26", "tecnico": "EGILSON FERREIRA", "tipo": "ELÉTRICO", "valor": 128.0, "receber": 15.0, "status": "COM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L125", "data": "2026-07-13", "os": "4551370/26", "tecnico": "EGILSON FERREIRA", "tipo": "ELÉTRICO", "valor": 128.0, "receber": 15.0, "status": "COM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L126", "data": "2026-07-13", "os": "4493111/26", "tecnico": "EGILSON FERREIRA", "tipo": "ELÉTRICO", "valor": 128.0, "receber": 15.0, "status": "COM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L127", "data": "2026-07-13", "os": "4568766/26", "tecnico": "EGILSON FERREIRA", "tipo": "ELÉTRICO", "valor": 155.0, "receber": 20.0, "status": "COM SUCESSO", "apos18": true, "feriado": false, "domingo": false}, {"id": "L128", "data": "2026-07-14", "os": "4581520/26", "tecnico": "WILSON BARBOSA", "tipo": "ELÉTRICO", "valor": 0.0, "receber": 15.0, "status": "COM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L129", "data": "2026-07-14", "os": "4583340/26", "tecnico": "WILSON BARBOSA", "tipo": "HIDRÁULICO", "valor": 131.0, "receber": 0.0, "status": "COM SUCESSO", "apos18": true, "feriado": false, "domingo": false}, {"id": "L130", "data": "2026-07-14", "os": "4538206/26", "tecnico": "WILSON BARBOSA", "tipo": "HIDRÁULICO", "valor": 52.0, "receber": 0.0, "status": "SERVIÇO CANCELADO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L131", "data": "2026-07-14", "os": "4581817/26", "tecnico": "WILSON BARBOSA", "tipo": "HIDRÁULICO", "valor": 52.0, "receber": 0.0, "status": "SEM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L132", "data": "2026-07-14", "os": "4566638/26", "tecnico": "EGILSON FERREIRA", "tipo": "ELÉTRICO", "valor": 52.0, "receber": 0.0, "status": "SEM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L133", "data": "2026-07-16", "os": "4600780/26", "tecnico": "EGILSON FERREIRA", "tipo": "ELÉTRICO", "valor": 76.0, "receber": 15.0, "status": "RETORNO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L134", "data": "2026-07-14", "os": "4552866/26", "tecnico": "WILSON BARBOSA", "tipo": "DESENTUPIMENTO", "valor": 278.0, "receber": 15.0, "status": "COM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L135", "data": "2026-07-14", "os": "4557502/26", "tecnico": "EGILSON FERREIRA", "tipo": "ELÉTRICO", "valor": 128.0, "receber": 15.0, "status": "COM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L136", "data": "2026-07-14", "os": "4542722/26", "tecnico": "EGILSON FERREIRA", "tipo": "ELÉTRICO", "valor": 128.0, "receber": 15.0, "status": "COM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L137", "data": "2026-07-14", "os": "4556377/26", "tecnico": "EGILSON FERREIRA", "tipo": "ELÉTRICO", "valor": 128.0, "receber": 15.0, "status": "COM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L138", "data": "2026-07-14", "os": "4581463/26", "tecnico": "WILSON BARBOSA", "tipo": "ELÉTRICO", "valor": 128.0, "receber": 15.0, "status": "COM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L139", "data": "2026-07-14", "os": "4577062/26", "tecnico": "WILSON BARBOSA", "tipo": "HIDRÁULICO", "valor": 128.0, "receber": 15.0, "status": "COM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L140", "data": "2026-07-14", "os": "4562531/26", "tecnico": "WILSON BARBOSA", "tipo": "DESENTUPIMENTO", "valor": 278.0, "receber": 15.0, "status": "COM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L141", "data": "2026-07-14", "os": "4572487/26", "tecnico": "EGILSON FERREIRA", "tipo": "ELÉTRICO", "valor": 128.0, "receber": 15.0, "status": "COM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L142", "data": "2026-07-14", "os": "4564803/26", "tecnico": "EGILSON FERREIRA", "tipo": "ELÉTRICO", "valor": 128.0, "receber": 15.0, "status": "COM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L143", "data": "2026-07-14", "os": "4516529/26", "tecnico": "WILSON BARBOSA", "tipo": "ELÉTRICO", "valor": 232.0, "receber": 25.0, "status": "COM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L144", "data": "2026-07-14", "os": "4572682/26", "tecnico": "EGILSON FERREIRA", "tipo": "ELÉTRICO", "valor": 128.0, "receber": 15.0, "status": "COM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L145", "data": "2026-07-14", "os": "4578595/26", "tecnico": "WILSON BARBOSA", "tipo": "HIDRÁULICO", "valor": 52.0, "receber": 0.0, "status": "SEM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L146", "data": "2026-07-16", "os": "4598256/26", "tecnico": "WESLEY SILVA", "tipo": "HIDRÁULICO", "valor": 115.0, "receber": 15.0, "status": "RETORNO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L147", "data": "2026-07-14", "os": "4583694/26", "tecnico": "WILSON BARBOSA", "tipo": "HIDRÁULICO", "valor": 128.0, "receber": 15.0, "status": "COM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L148", "data": "2026-07-14", "os": "4572777/26", "tecnico": "EGILSON FERREIRA", "tipo": "ELÉTRICO", "valor": 93.0, "receber": 15.0, "status": "RETORNO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L149", "data": "2026-07-14", "os": "4586384/26", "tecnico": "WILSON BARBOSA", "tipo": "ELÉTRICO", "valor": 104.0, "receber": 10.0, "status": "COM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L150", "data": "2026-07-14", "os": "4582170/26", "tecnico": "EGILSON FERREIRA", "tipo": "ELÉTRICO", "valor": 221.46, "receber": 20.0, "status": "COM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L151", "data": "2026-07-15", "os": "4577901/26", "tecnico": "EGILSON FERREIRA", "tipo": "LIMPEZA DE CAIXA D'ÁGUA", "valor": 52.0, "receber": 0.0, "status": "SEM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L152", "data": "2026-07-15", "os": "4552131/26", "tecnico": "WILSON BARBOSA", "tipo": "HIDRÁULICO", "valor": 52.0, "receber": 0.0, "status": "SEM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L153", "data": "2026-07-17", "os": "4602336/26", "tecnico": "WESLEY SILVA", "tipo": "HIDRÁULICO", "valor": 76.0, "receber": 15.0, "status": "RETORNO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L154", "data": "2026-07-15", "os": "4589792/26", "tecnico": "WILSON BARBOSA", "tipo": "HIDRÁULICO", "valor": 128.0, "receber": 15.0, "status": "COM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L155", "data": "2026-07-15", "os": "4578953/26", "tecnico": "EGILSON FERREIRA", "tipo": "ELÉTRICO", "valor": 128.0, "receber": 15.0, "status": "COM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L156", "data": "2026-07-15", "os": "4544359/26", "tecnico": "WILSON BARBOSA", "tipo": "ELÉTRICO", "valor": 128.0, "receber": 15.0, "status": "COM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L157", "data": "2026-07-15", "os": "4609806/26", "tecnico": "WILSON BARBOSA", "tipo": "ELÉTRICO", "valor": 96.0, "receber": 0.0, "status": "SEM SUCESSO", "apos18": true, "feriado": false, "domingo": false}, {"id": "L158", "data": "2026-07-15", "os": "4584002/26", "tecnico": "EGILSON FERREIRA", "tipo": "FIXAÇAO", "valor": 140.0, "receber": 15.0, "status": "COM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L159", "data": "2026-07-15", "os": "45822200/26", "tecnico": "WILSON BARBOSA", "tipo": "IMPERMEABILIZAÇÃO DE ESTOFADOS", "valor": 52.0, "receber": 0.0, "status": "SEM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L160", "data": "2026-07-15", "os": "4592735/26", "tecnico": "EGILSON FERREIRA", "tipo": "ELÉTRICO", "valor": 232.0, "receber": 25.0, "status": "COM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L161", "data": "2026-07-15", "os": "4589574/26", "tecnico": "WILSON BARBOSA", "tipo": "HIDRÁULICO", "valor": 128.0, "receber": 15.0, "status": "COM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L162", "data": "2026-07-15", "os": "4568240/26", "tecnico": "WILSON BARBOSA", "tipo": "DESENTUPIMENTO", "valor": 278.0, "receber": 15.0, "status": "COM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L163", "data": "2026-07-15", "os": "4583583/26", "tecnico": "WILSON BARBOSA", "tipo": "ELÉTRICO", "valor": 128.0, "receber": 15.0, "status": "COM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L164", "data": "2026-07-15", "os": "4597846/26", "tecnico": "EGILSON FERREIRA", "tipo": "ELÉTRICO", "valor": 145.0, "receber": 15.0, "status": "COM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L165", "data": "2026-07-15", "os": "4584247/26", "tecnico": "EGILSON FERREIRA", "tipo": "LIMPEZA DE CAIXA D'ÁGUA", "valor": 436.22, "receber": 25.0, "status": "COM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L166", "data": "2026-07-15", "os": "4606518/26", "tecnico": "WILSON BARBOSA", "tipo": "HIDRÁULICO", "valor": 52.0, "receber": 0.0, "status": "SEM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L167", "data": "2026-07-15", "os": "4609106/26", "tecnico": "EGILSON FERREIRA", "tipo": "ELÉTRICO", "valor": 104.0, "receber": 10.0, "status": "COM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L168", "data": "2026-07-16", "os": "4599295/26", "tecnico": "EGILSON FERREIRA", "tipo": "LIMPEZA DE CAIXA D'ÁGUA", "valor": 52.0, "receber": 0.0, "status": "SEM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L169", "data": "2026-07-16", "os": "4592203/26", "tecnico": "WESLEY SILVA", "tipo": "HIDRÁULICO", "valor": 145.0, "receber": 15.0, "status": "COM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L170", "data": "2026-07-16", "os": "4601556/26", "tecnico": "WESLEY SILVA", "tipo": "HIDRÁULICO", "valor": 219.0, "receber": 25.0, "status": "RETORNO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L171", "data": "2026-07-16", "os": "4597602/26", "tecnico": "EGILSON FERREIRA", "tipo": "KIT PREGO E MARTELO", "valor": 52.0, "receber": 0.0, "status": "SEM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L172", "data": "2026-07-16", "os": "4626306/26", "tecnico": "WESLEY SILVA", "tipo": "HIDRÁULICO", "valor": 145.0, "receber": 15.0, "status": "COM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L173", "data": "2026-07-16", "os": "4620519/26", "tecnico": "EGILSON FERREIRA", "tipo": "ELÉTRICO", "valor": 76.0, "receber": 15.0, "status": "RETORNO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L174", "data": "2026-07-16", "os": "4624311/26", "tecnico": "WESLEY SILVA", "tipo": "HIDRÁULICO", "valor": 247.0, "receber": 25.0, "status": "COM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L175", "data": "2026-07-16", "os": "4624307/26", "tecnico": "WESLEY SILVA", "tipo": "ELÉTRICO", "valor": 104.0, "receber": 10.0, "status": "COM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L176", "data": "2026-07-16", "os": "4625821/26", "tecnico": "WESLEY SILVA", "tipo": "HIDRÁULICO", "valor": 128.0, "receber": 15.0, "status": "COM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L177", "data": "2026-07-16", "os": "4619913/26", "tecnico": "EGILSON FERREIRA", "tipo": "FIXAÇAO", "valor": 157.0, "receber": 15.0, "status": "COM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L178", "data": "2026-07-16", "os": "4613570/26", "tecnico": "WESLEY SILVA", "tipo": "HIDRÁULICO", "valor": 128.0, "receber": 15.0, "status": "COM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L179", "data": "2026-07-16", "os": "4629305/26", "tecnico": "WESLEY SILVA", "tipo": "ELÉTRICO", "valor": 84.5, "receber": 0.0, "status": "SEM SUCESSO", "apos18": true, "feriado": false, "domingo": false}, {"id": "L180", "data": "2026-07-17", "os": "4610039/26", "tecnico": "EGILSON FERREIRA", "tipo": "ELÉTRICO", "valor": 128.0, "receber": 15.0, "status": "COM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L181", "data": "2026-07-17", "os": "4630222/26", "tecnico": "EGILSON FERREIRA", "tipo": "ELÉTRICO", "valor": 128.0, "receber": 15.0, "status": "COM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L182", "data": "2026-07-17", "os": "4631527/26", "tecnico": "WESLEY SILVA", "tipo": "HIDRÁULICO", "valor": 52.0, "receber": 0.0, "status": "SEM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L183", "data": "2026-07-17", "os": "4629469/26", "tecnico": "EGILSON FERREIRA", "tipo": "ELÉTRICO", "valor": 52.0, "receber": 0.0, "status": "SEM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L184", "data": "2026-07-17", "os": "4631830/26", "tecnico": "WESLEY SILVA", "tipo": "HIDRÁULICO", "valor": 128.0, "receber": 15.0, "status": "COM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L185", "data": "2026-07-17", "os": "4632279/26", "tecnico": "EGILSON FERREIRA", "tipo": "ELÉTRICO", "valor": 128.0, "receber": 15.0, "status": "COM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L186", "data": "2026-07-17", "os": "4628514/26", "tecnico": "WESLEY SILVA", "tipo": "CHECK UP CASA PLUS", "valor": 52.0, "receber": 0.0, "status": "SEM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L187", "data": "2026-07-17", "os": "4628520/26", "tecnico": "WESLEY SILVA", "tipo": "ELÉTRICO", "valor": 28.0, "receber": 0.0, "status": "SEM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L188", "data": "2026-07-17", "os": "4634647/26", "tecnico": "WESLEY SILVA", "tipo": "DESENTUPIMENTO", "valor": 52.0, "receber": 0.0, "status": "SEM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L189", "data": "2026-07-17", "os": "4639142/26", "tecnico": "WESLEY SILVA", "tipo": "HIDRÁULICO", "valor": 52.0, "receber": 0.0, "status": "SEM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L190", "data": "2026-07-17", "os": "4642367/26", "tecnico": "EGILSON FERREIRA", "tipo": "ELÉTRICO", "valor": 336.0, "receber": 35.0, "status": "COM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L191", "data": "2026-07-17", "os": "4579440/26", "tecnico": "WESLEY SILVA", "tipo": "HIDRÁULICO", "valor": 128.0, "receber": 15.0, "status": "COM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L192", "data": "2026-07-17", "os": "4640433/26", "tecnico": "EGILSON FERREIRA", "tipo": "ELÉTRICO", "valor": 52.0, "receber": 0.0, "status": "SEM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L193", "data": "2026-07-17", "os": "4605396/26", "tecnico": "EGILSON FERREIRA", "tipo": "ELÉTRICO", "valor": 145.0, "receber": 15.0, "status": "COM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L194", "data": "2026-07-17", "os": "4630391/26", "tecnico": "EGILSON FERREIRA", "tipo": "ELÉTRICO", "valor": 128.0, "receber": 15.0, "status": "COM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L195", "data": "2026-07-17", "os": "4643868/26", "tecnico": "EGILSON FERREIRA", "tipo": "ELÉTRICO", "valor": 181.66, "receber": 20.0, "status": "COM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L196", "data": "2026-07-17", "os": "4651031/26", "tecnico": "WESLEY SILVA", "tipo": "HIDRÁULICO", "valor": 155.0, "receber": 20.0, "status": "COM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L197", "data": "2026-07-17", "os": "4651424/26", "tecnico": "WESLEY SILVA", "tipo": "ELÉTRICO", "valor": 155.0, "receber": 20.0, "status": "COM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L198", "data": "2026-07-17", "os": "4655022/26", "tecnico": "WESLEY SILVA", "tipo": "ELÉTRICO", "valor": 133.82, "receber": 15.0, "status": "COM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L199", "data": "2026-07-18", "os": "4644013/26", "tecnico": "EGILSON FERREIRA", "tipo": "ELÉTRICO", "valor": 128.0, "receber": 15.0, "status": "COM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L200", "data": "2026-07-18", "os": "4635865/26", "tecnico": "EGILSON FERREIRA", "tipo": "LIMPEZA DE CAIXA D'ÁGUA", "valor": 52.0, "receber": 0.0, "status": "SEM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L201", "data": "2026-07-18", "os": "4644194/26", "tecnico": "EGILSON FERREIRA", "tipo": "ELÉTRICO", "valor": 128.0, "receber": 15.0, "status": "COM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L202", "data": "2026-07-18", "os": "4655038/26", "tecnico": "EGILSON FERREIRA", "tipo": "ELÉTRICO", "valor": 128.0, "receber": 15.0, "status": "COM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L203", "data": "2026-07-18", "os": "4658885/26", "tecnico": "EGILSON FERREIRA", "tipo": "ELÉTRICO", "valor": 128.0, "receber": 15.0, "status": "COM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L204", "data": "2026-07-18", "os": "4659471/26", "tecnico": "EGILSON FERREIRA", "tipo": "ELÉTRICO", "valor": 52.0, "receber": 0.0, "status": "SEM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L205", "data": "2026-07-18", "os": "4662679/26", "tecnico": "EGILSON FERREIRA", "tipo": "ELÉTRICO", "valor": 76.0, "receber": 15.0, "status": "RETORNO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L206", "data": "2026-07-18", "os": "4660766/26", "tecnico": "EGILSON FERREIRA", "tipo": "ELÉTRICO", "valor": 128.0, "receber": 15.0, "status": "COM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L207", "data": "2026-07-18", "os": "4660480/26", "tecnico": "EGILSON FERREIRA", "tipo": "ELÉTRICO", "valor": 52.0, "receber": 0.0, "status": "SEM SUCESSO", "apos18": false, "feriado": false, "domingo": false}, {"id": "L208", "data": "2026-07-18", "os": "4664242/26", "tecnico": "EGILSON FERREIRA", "tipo": "ELÉTRICO", "valor": 206.2, "receber": 20.0, "status": "COM SUCESSO", "apos18": true, "feriado": false, "domingo": false}, {"id": "L209", "data": "2026-07-19", "os": "4668355/26", "tecnico": "EGILSON FERREIRA", "tipo": "ELÉTRICO", "valor": 269.72, "receber": 30.0, "status": "COM SUCESSO", "apos18": true, "feriado": false, "domingo": true}], "retornos": [{"id": "R021", "data": "2026-07-02", "os": "4369737/26", "osOrig": "4302395/26", "tipo": "FIXAÇAO", "statusOrig": "SEM SUCESSO", "tecOrig": "WESLEY SILVA", "motivo": "CONCLUIR O SERVIÇO", "tecResp": "EGILSON FERREIRA", "devido": "DEVIDO", "resultado": "COM SUCESSO"}, {"id": "R022", "data": "2026-07-03", "os": "4390141/26", "osOrig": "4358795/26", "tipo": "HIDRÁULICO", "statusOrig": "COM SUCESSO", "tecOrig": "EGILSON FERREIRA", "motivo": "GARANTIA", "tecResp": "WESLEY SILVA", "devido": "DEVIDO", "resultado": "COM SUCESSO"}, {"id": "R023", "data": "2026-07-04", "os": "4412506/26", "osOrig": "4386374/26", "tipo": "ELÉTRICO", "statusOrig": "SEM SUCESSO", "tecOrig": "EGILSON FERREIRA", "motivo": "CONCLUIR O SERVIÇO", "tecResp": "EGILSON FERREIRA", "devido": "DEVIDO", "resultado": "COM SUCESSO"}, {"id": "R024", "data": "2026-07-06", "os": "4435091/26", "osOrig": "4211488/26", "tipo": "ELÉTRICO", "statusOrig": "COM SUCESSO", "tecOrig": "WILSON BARBOSA", "motivo": "RETORNO INDEVIDO", "tecResp": "EGILSON FERREIRA", "devido": "INDEVIDO", "resultado": "COM SUCESSO"}, {"id": "R025", "data": "2026-07-06", "os": "4428475/26", "osOrig": "4389216/26", "tipo": "ELÉTRICO", "statusOrig": "COM SUCESSO", "tecOrig": "EGILSON FERREIRA", "motivo": "GARANTIA", "tecResp": "EGILSON FERREIRA", "devido": "DEVIDO", "resultado": "COM SUCESSO"}, {"id": "R026", "data": "2026-07-10", "os": "4488224/26", "osOrig": "4485868/26", "tipo": "HIDRÁULICO", "statusOrig": "SEM SUCESSO", "tecOrig": "WILSON BARBOSA", "motivo": "CONCLUIR O SERVIÇO", "tecResp": "WILSON BARBOSA", "devido": "DEVIDO", "resultado": "COM SUCESSO"}, {"id": "R027", "data": "2026-07-10", "os": "4501660/26", "osOrig": "4448376/26", "tipo": "FIXAÇAO", "statusOrig": "SEM SUCESSO", "tecOrig": "EGILSON FERREIRA", "motivo": "CONCLUIR O SERVIÇO", "tecResp": "WESLEY SILVA", "devido": "INDEVIDO", "resultado": "SEM SUCESSO"}, {"id": "R028", "data": "2026-07-14", "os": "4581520/26", "osOrig": "4462533/26", "tipo": "ELÉTRICO", "statusOrig": "COM SUCESSO", "tecOrig": "WESLEY SILVA", "motivo": "CONCLUIR O SERVIÇO", "tecResp": "WILSON BARBOSA", "devido": "DEVIDO", "resultado": "COM SUCESSO"}, {"id": "R029", "data": "2026-07-14", "os": "4583340/26", "osOrig": "3960978/26", "tipo": "HIDRÁULICO", "statusOrig": "COM SUCESSO", "tecOrig": "WESLEY SILVA", "motivo": "CONCLUIR O SERVIÇO", "tecResp": "WILSON BARBOSA", "devido": "INDEVIDO", "resultado": "COM SUCESSO"}, {"id": "R030", "data": "2026-07-16", "os": "4600780/26", "osOrig": "4566638/26", "tipo": "ELÉTRICO", "statusOrig": "SEM SUCESSO", "tecOrig": "EGILSON FERREIRA", "motivo": "CONCLUIR O SERVIÇO", "tecResp": "EGILSON FERREIRA", "devido": "DEVIDO", "resultado": "COM SUCESSO"}, {"id": "R031", "data": "2026-07-16", "os": "4598256/26", "osOrig": "4578595/26", "tipo": "HIDRÁULICO", "statusOrig": "SEM SUCESSO", "tecOrig": "WILSON BARBOSA", "motivo": "CONCLUIR O SERVIÇO", "tecResp": "WESLEY SILVA", "devido": "DEVIDO", "resultado": "COM SUCESSO"}, {"id": "R032", "data": "2026-07-14", "os": "4572777/26", "osOrig": "4530213/26", "tipo": "ELÉTRICO", "statusOrig": "SEM SUCESSO", "tecOrig": "EGILSON FERREIRA", "motivo": "CONCLUIR O SERVIÇO", "tecResp": "EGILSON FERREIRA", "devido": "DEVIDO", "resultado": "COM SUCESSO"}, {"id": "R033", "data": "2026-07-17", "os": "4602336/26", "osOrig": "4552131/26", "tipo": "HIDRÁULICO", "statusOrig": "SEM SUCESSO", "tecOrig": "WILSON BARBOSA", "motivo": "CONCLUIR O SERVIÇO", "tecResp": "WESLEY SILVA", "devido": "DEVIDO", "resultado": "COM SUCESSO"}, {"id": "R034", "data": "2026-07-15", "os": "4609806/26", "osOrig": "4544359/26", "tipo": "ELÉTRICO", "statusOrig": "COM SUCESSO", "tecOrig": "WILSON BARBOSA", "motivo": "GARANTIA", "tecResp": "WILSON BARBOSA", "devido": "INDEVIDO", "resultado": "SEM SUCESSO"}, {"id": "R035", "data": "2026-07-16", "os": "4601556/26", "osOrig": "4307820/26", "tipo": "HIDRÁULICO", "statusOrig": "SEM SUCESSO", "tecOrig": "WESLEY SILVA", "motivo": "CONCLUIR O SERVIÇO", "tecResp": "WESLEY SILVA", "devido": "DEVIDO", "resultado": "COM SUCESSO"}, {"id": "R036", "data": "2026-07-16", "os": "4620519/26", "osOrig": "4544012/26", "tipo": "ELÉTRICO", "statusOrig": "SEM SUCESSO", "tecOrig": "EGILSON FERREIRA", "motivo": "CONCLUIR O SERVIÇO", "tecResp": "EGILSON FERREIRA", "devido": "DEVIDO", "resultado": "COM SUCESSO"}, {"id": "R037", "data": "2026-07-18", "os": "4662679/26", "osOrig": "4659471/26", "tipo": "ELÉTRICO", "statusOrig": "SEM SUCESSO", "tecOrig": "EGILSON FERREIRA", "motivo": "CONCLUIR O SERVIÇO", "tecResp": "EGILSON FERREIRA", "devido": "DEVIDO", "resultado": "COM SUCESSO"}], "gastos": [{"id": "G000", "data": "2026-07-06", "categoria": "VIATURA E756 — MANUTENÇÃO", "descricao": "KIT EMBREAGEM", "valor": 448.0}, {"id": "G001", "data": "2026-07-06", "categoria": "VIATURA E756 — MANUTENÇÃO", "descricao": "PARAFUSO DA RODA", "valor": 18.0}, {"id": "G002", "data": "2026-07-06", "categoria": "VIATURA E756 — MANUTENÇÃO", "descricao": "JUNTA DA TAMPA DE VALVULA", "valor": 130.0}, {"id": "G003", "data": "2026-07-06", "categoria": "VIATURA E756 — MANUTENÇÃO", "descricao": "MAO DE OBRA", "valor": 500.0}, {"id": "G004", "data": "2026-07-11", "categoria": "VIATURA E35 — COMBUSTÍVEL", "descricao": "ABASTECIMENTO", "valor": 307.47}, {"id": "G005", "data": "2026-07-11", "categoria": "VIATURA E756 — COMBUSTÍVEL", "descricao": "ABASTECIMENTO", "valor": 136.8}, {"id": "G006", "data": "2026-07-11", "categoria": "VIATURA E35 — MANUTENÇÃO", "descricao": "TROCA DO CABO DE EMBREAGEM", "valor": 178.0}, {"id": "G007", "data": "2026-07-11", "categoria": "CONTADOR", "descricao": "SERVIÇO DE CONTABILIDADE DE DOIS MESES", "valor": 1510.0}, {"id": "G008", "data": "2026-07-11", "categoria": "INSS", "descricao": "INSS FUNCIONARIOS. 07.16.26182.8877585-8", "valor": 516.77}, {"id": "G009", "data": "2026-07-11", "categoria": "FGTS", "descricao": "FGTS DE FUNCIONARIO 0126070146672327-0", "valor": 344.09}, {"id": "G010", "data": "2026-07-01", "categoria": "WILSON BARBOSA — SALÁRIO", "descricao": "SALARIO MAIS PREMIO", "valor": 3825.35}, {"id": "G011", "data": "2026-07-01", "categoria": "EGILSON FERREIRA — SALÁRIO", "descricao": "SALARIO MAIS PREMIO", "valor": 2503.23}, {"id": "G012", "data": "2026-07-11", "categoria": "ÁGUA", "descricao": "DE DOIS MESES", "valor": 367.3}, {"id": "G013", "data": "2026-07-16", "categoria": "IMPOSTO", "descricao": "IMPOSTO", "valor": 2043.42}], "equipe": ["WESLEY SILVA", "WILSON BARBOSA", "EGILSON FERREIRA"], "tipos": ["APOIO OPERACIONAL", "CHECK UP CASA PLUS", "DESENTUPIMENTO", "ELÉTRICO", "FIXAÇAO", "HIDRÁULICO", "IMPERMEABILIZAÇÃO DE ESTOFADOS", "INSTA COIFAS E DEPURADORES", "KIT PREGO E MARTELO", "LIMPEZA DE CAIXA D'ÁGUA", "LIMPEZA DE CALHAS", "OUTROS SERVIÇOS", "VENTILADOR"]};

/* === STATE === */
var REG=[], RET=[], GAS=[], EQ=[], TP=[];
var CATS=['VIATURA E756 — COMBUSTÍVEL','VIATURA E756 — MANUTENÇÃO','VIATURA E35 — COMBUSTÍVEL',
 'VIATURA E35 — MANUTENÇÃO','SALÁRIO','INSS','FGTS','CONTADOR','IMPOSTO','ÁGUA','ENERGIA','MATERIAL','OUTROS'];

/* === UTIL === */
function $(s){return document.querySelector(s)}
function $$(s){return Array.from(document.querySelectorAll(s))}
function pct(a,b){return b?Math.round(a/b*1000)/10:0}
function ms(d){return(d||'').slice(0,7)}
function bd(d){if(!d)return'';var p=d.split('-');return p[2]?p[2]+'/'+p[1]+'/'+p[0]:d}
function brl(v){return'R$ '+(+v||0).toLocaleString('pt-BR',{minimumFractionDigits:2,maximumFractionDigits:2})}
function bk(v){return'R$ '+Math.round(+v||0).toLocaleString('pt-BR')}
function esc(s){return String(s==null?'':s).replace(/&/g,'&amp;').replace(/</g,'&lt;').replace(/>/g,'&gt;')}
function uid(p){return p+Date.now().toString(36)+Math.random().toString(36).slice(2,6)}
function OK(r){return r.status==='COM SUCESSO'}

var _tt;
function toast(t,e){var el=$('#toast');el.textContent=t;el.className=e?'err':'';el.style.display='block';
  clearTimeout(_tt);_tt=setTimeout(function(){el.style.display='none'},3200)}

function armed(btn,txt,norm,fn){
  if(!btn._armed){
    btn._armed=true;btn.classList.add('armed');btn.textContent=txt;
    btn._timer=setTimeout(function(){btn._armed=false;btn.classList.remove('armed');btn.textContent=norm},4500);
    return;
  }
  clearTimeout(btn._timer);btn._armed=false;btn.classList.remove('armed');btn.textContent=norm;fn();
}

/* === STORAGE (best-effort, not required) === */
function sGet(k,d){try{var v=localStorage.getItem(k);return v?JSON.parse(v):d}catch(e){return d}}
function sSet(k,v){try{localStorage.setItem(k,JSON.stringify(v))}catch(e){}}
function sDel(k){try{localStorage.removeItem(k)}catch(e){}}
var SK={r:'gy_r',t:'gy_t',g:'gy_g',e:'gy_e',p:'gy_p',i:'gy_i'};

/* === INIT === */
function init(){
  var started=sGet(SK.i,0);
  if(started){
    REG=sGet(SK.r,SEED_DATA.lancamentos||[]);
    RET=sGet(SK.t,SEED_DATA.retornos||[]);
    GAS=sGet(SK.g,SEED_DATA.gastos||[]);
    EQ=sGet(SK.e,SEED_DATA.equipe||[]);
    TP=sGet(SK.p,SEED_DATA.tipos||[]);
  }else{
    REG=SEED_DATA.lancamentos||[];
    RET=SEED_DATA.retornos||[];
    GAS=SEED_DATA.gastos||[];
    EQ=SEED_DATA.equipe||[];
    TP=SEED_DATA.tipos||[];
    save();sSet(SK.i,1);
  }
  var h=new Date().toISOString().slice(0,10);
  try{$('#c-dt').value=h;$('#r-dt').value=h;$('#g-dt').value=h}catch(e){}
  setupDesktopNav();
  render();
}

function save(){sSet(SK.r,REG);sSet(SK.t,RET);sSet(SK.g,GAS);sSet(SK.e,EQ);sSet(SK.p,TP)}

/* === DESKTOP NAV === */
function setupDesktopNav(){
  if(window.innerWidth<641)return;
  var nav=$('#topnav');nav.style.display='flex';
  var tabs=['painel','lanc','ret','gas','eq','dados'];
  var labels=['Painel','Lançamentos','Retornos','Gastos','Equipe','Dados'];
  nav.innerHTML=tabs.map(function(t,i){return '<button data-t="'+t+'"'+(i===0?' class="on"':'')+'>'+labels[i]+'</button>'}).join('');
  nav.onclick=function(e){var b=e.target.closest('[data-t]');if(b)go(b.dataset.t)};
}

/* === NAVIGATION === */
function go(id){
  $$('.tab').forEach(function(t){t.classList.toggle('on',t.id==='t-'+id)});
  $$('.bnav button,[data-t]').forEach(function(b){
    if(b.dataset.t===id){b.classList.add('on');b.setAttribute('aria-selected','true')}
    else{b.classList.remove('on');b.setAttribute('aria-selected','false')}
  });
  window.scrollTo(0,0);
}
$('#bnav').onclick=function(e){var b=e.target.closest('[data-t]');if(b)go(b.dataset.t)};

/* === PERIOD === */
function per(){
  var m=$('#f-mes').value,t=$('#f-tec-p').value;
  var fm=function(x){return m==='todos'||ms(x.data)===m};
  return{
    reg:REG.filter(function(r){return fm(r)&&(!t||r.tecnico===t)}),
    ret:RET.filter(function(r){return fm(r)&&(!t||r.tecOrig===t||r.tecResp===t)}),
    gas:GAS.filter(function(g){return fm(g)})
  };
}

/* === CHARTS === */
var PAL=['#E2570F','#B23F06','#8A7563','#2E7D4F','#C98A2E','#7A4A22','#D9A26B'];
function chBar(el,data,cor,fmt){
  if(!data.length){el.innerHTML='<div class="empty">Sem dados.</div>';return}
  cor=cor||'var(--ora)';fmt=fmt||function(v){return v};
  var mx=Math.max.apply(null,data.map(function(d){return d.v}))||1;
  var ln=28,h=data.length*ln+10;
  el.innerHTML='<svg viewBox="0 0 300 '+h+'">'+data.map(function(d,i){
    var y=i*ln+4,w=Math.max(2,d.v/mx*130);
    return '<text x="0" y="'+(y+13)+'" font-size="10" fill="var(--ink3)" font-family="IBM Plex Sans">'+esc(d.n).slice(0,16)+'</text>'+
      '<rect x="120" y="'+(y+2)+'" width="'+w+'" height="14" rx="3" fill="'+cor+'"/>'+
      '<text x="'+(124+w)+'" y="'+(y+14)+'" font-size="10" font-weight="600" fill="var(--ink)" font-family="IBM Plex Mono">'+fmt(d.v)+'</text>';
  }).join('')+'</svg>';
}
function chCol(el,data){
  if(!data.length){el.innerHTML='<div class="empty">Sem dados.</div>';return}
  var mx=Math.max.apply(null,data.map(function(d){return d.v}))||1,W=300,H=130,w=W/data.length;
  el.innerHTML='<svg viewBox="0 0 '+W+' '+(H+18)+'">'+
    '<line x1="0" y1="'+H+'" x2="'+W+'" y2="'+H+'" stroke="var(--line)"/>'+
    data.map(function(d,i){var h2=d.v/mx*(H-12);
      return '<rect x="'+(i*w+w*.15)+'" y="'+(H-h2)+'" width="'+(w*.7)+'" height="'+h2+'" rx="2" fill="var(--ora)"/>'+
        (data.length<=20?'<text x="'+(i*w+w/2)+'" y="'+(H+12)+'" font-size="7.5" text-anchor="middle" fill="var(--ink3)" font-family="IBM Plex Mono">'+d.n+'</text>':'')
    }).join('')+'</svg>';
}
function chDonut(el,data){
  if(!data.length||!data.reduce(function(s,d){return s+d.v},0)){el.innerHTML='<div class="empty">Sem dados.</div>';return}
  var total=data.reduce(function(s,d){return s+d.v},0),ang=-Math.PI/2,arcs='';
  data.forEach(function(d,i){
    var a=d.v/total*Math.PI*2,f=ang+a,R=58,r2=36,cx=70,cy=70,big=a>Math.PI?1:0;
    arcs+='<path d="M'+(cx+R*Math.cos(ang))+' '+(cy+R*Math.sin(ang))+' A'+R+' '+R+' 0 '+big+' 1 '+(cx+R*Math.cos(f))+' '+(cy+R*Math.sin(f))+' L'+(cx+r2*Math.cos(f))+' '+(cy+r2*Math.sin(f))+' A'+r2+' '+r2+' 0 '+big+' 0 '+(cx+r2*Math.cos(ang))+' '+(cy+r2*Math.sin(ang))+' Z" fill="'+PAL[i%7]+'"/>';
    ang=f;
  });
  el.innerHTML='<svg viewBox="0 0 140 140" style="margin:0 auto;max-width:160px">'+arcs+
    '<text x="70" y="67" text-anchor="middle" font-size="20" font-weight="700" font-family="Barlow Condensed" fill="var(--ink)">'+total+'</text>'+
    '<text x="70" y="80" text-anchor="middle" font-size="7" fill="var(--ink3)">SERVIÇOS</text></svg>'+
    '<div class="legend">'+data.map(function(d,i){return '<span><i style="background:'+PAL[i%7]+'"></i>'+esc(d.n)+' · '+d.v+'</span>'}).join('')+'</div>';
}
function chPareto(el,data,empty){
  if(!data.length){el.innerHTML='<div class="empty">'+(empty||'Sem dados.')+'</div>';return}
  var tot=data.reduce(function(s,d){return s+d.v},0),mx=data[0].v,W=300,H=130,w=W/data.length;
  var ac=0,pts=data.map(function(d,i){ac+=d.v;return(i*w+w/2)+','+(H-ac/tot*(H-14)).toFixed(1)});
  el.innerHTML='<svg viewBox="0 0 '+W+' '+(H+22)+'">'+
    '<line x1="0" y1="'+H+'" x2="'+W+'" y2="'+H+'" stroke="var(--line)"/>'+
    data.map(function(d,i){var h2=d.v/mx*(H-14);
      return '<rect x="'+(i*w+w*.15)+'" y="'+(H-h2)+'" width="'+(w*.7)+'" height="'+h2+'" rx="2" fill="var(--ora)"/>'+
        '<text x="'+(i*w+w/2)+'" y="'+(H+14)+'" font-size="7.5" text-anchor="middle" fill="var(--ink3)">'+esc(d.n).slice(0,10)+'</text>'
    }).join('')+
    '<polyline points="'+pts.join(' ')+'" fill="none" stroke="var(--ink)" stroke-width="1.5"/>'+
    pts.map(function(p){var xy=p.split(',');return '<circle cx="'+xy[0]+'" cy="'+xy[1]+'" r="2.3" fill="var(--ink)"/>'}).join('')+
    '</svg><div class="legend"><span><i style="background:var(--ora)"></i>Qtd</span><span><i style="background:var(--ink)"></i>% acum.</span></div>';
}

/* === SELECTS === */
function fillSel(){
  var ot=EQ.map(function(t){return '<option>'+esc(t)+'</option>'}).join('');
  var op=TP.map(function(t){return '<option>'+esc(t)+'</option>'}).join('');
  ['#c-tc','#r-to','#r-tr'].forEach(function(s){$(s).innerHTML=ot});
  ['#c-tp','#r-tp'].forEach(function(s){$(s).innerHTML=op});
  ['#fl-tc','#f-tec-p'].forEach(function(s){$(s).innerHTML='<option value="">Todos</option>'+ot});
  $('#g-ct').innerHTML=CATS.map(function(c){return '<option>'+esc(c)+'</option>'}).join('');
  $('#lst-tc').value=EQ.join('\n');
  $('#lst-tp').value=TP.join('\n');
}
function fillMes(){
  var mm={};REG.forEach(function(r){if(r.data)mm[ms(r.data)]=1});
  var meses=Object.keys(mm).sort().reverse();
  var sel=$('#f-mes'),cur=sel.value;
  var nms=['jan','fev','mar','abr','mai','jun','jul','ago','set','out','nov','dez'];
  sel.innerHTML='<option value="todos">Todos</option>'+meses.map(function(m){
    return '<option value="'+m+'">'+nms[+m.slice(5,7)-1]+'/'+m.slice(0,4)+'</option>'}).join('');
  if(cur&&sel.querySelector('[value="'+cur+'"]'))sel.value=cur;else sel.value=meses[0]||'todos';
}

/* === RENDER === */
function render(){
  fillMes();fillSel();dashboard();tblLanc()
}
function dashboard(){
  var p=per(),L=p.reg,R=p.ret,G=p.gas;
  var suc=L.filter(OK),sem=L.filter(function(r){return r.status==='SEM SUCESSO'});
  var retL=L.filter(function(r){return r.status==='RETORNO'});
  var retInd=L.filter(function(r){return r.status==='RETORNO INDEVIDO'});
  var canc=L.filter(function(r){return r.status==='SERVIÇO CANCELADO'});
  var apos=L.filter(function(r){return r.apos18});
  var prodTotal=L.reduce(function(s,r){return s+r.valor},0);
  var rec=L.reduce(function(s,r){return s+r.receber},0);
  var desp=G.reduce(function(s,g){return s+g.valor},0);
  var txSuc=L.length?pct(suc.length,L.length):0;

  $('#info-painel').textContent=REG.length?L.length+' serviço(s) · '+brl(prodTotal)+' produzidos':'Nenhum lançamento — importe na aba Dados.';

  $('#kpis').innerHTML=[
    ['Serviços lançados',L.length,'','m'],
    ['Com sucesso',suc.length,pct(suc.length,L.length)+'% do total','ok'],
    ['Sem sucesso',sem.length,pct(sem.length,L.length)+'% do total','err'],
    ['Retorno',retL.length,retInd.length+' indevido(s)','err'],
    ['Valor total produção',bk(prodTotal),'todos os serviços',''],
    ['A pagar técnicos',bk(rec),pct(rec,prodTotal)+'% da produção','m'],
    ['Após 18h',apos.length,canc.length+' cancelado(s)','m'],
    ['% Sucesso geral',(txSuc)+'%',suc.length+' de '+L.length,'ok'],
    ['Resultado',bk(prodTotal-desp),'desp. '+bk(desp),prodTotal-desp>=0?'ok':'err']
  ].map(function(x){return '<div class="kpi '+x[3]+'"><div class="lb">'+x[0]+'</div><div class="vl mono">'+x[1]+'</div><div class="sm">'+x[2]+'</div></div>'}).join('');

  chBar($('#ch-tec'),EQ.map(function(t){return{n:t,v:L.filter(function(r){return r.tecnico===t}).length}}).filter(function(d){return d.v}).sort(function(a,b){return b.v-a.v}));
  var dias={};L.forEach(function(r){if(r.data)dias[r.data]=(dias[r.data]||0)+1});
  chCol($('#ch-dia'),Object.keys(dias).sort().map(function(d){return{n:d.slice(8),v:dias[d]}}));
  var tipos={};L.forEach(function(r){var t=r.tipo||'OUTROS';tipos[t]=(tipos[t]||0)+1});
  chDonut($('#ch-tipo'),Object.keys(tipos).map(function(n){return{n:n,v:tipos[n]}}).sort(function(a,b){return b.v-a.v}).slice(0,7));
  chBar($('#ch-fat'),EQ.map(function(t){return{n:t,v:Math.round(L.filter(function(r){return r.tecnico===t}).reduce(function(s,r){return s+r.valor},0))}}).filter(function(d){return d.v}).sort(function(a,b){return b.v-a.v}),'var(--ora2)',bk);
  chBar($('#ch-suc'),EQ.map(function(t){var l=L.filter(function(r){return r.tecnico===t});return{n:t,v:l.length?pct(l.filter(OK).length,l.length):0}}).filter(function(d){return d.v}).sort(function(a,b){return b.v-a.v}),'var(--ok)',function(v){return v+'%'});
  var ss={};sem.forEach(function(r){ss[r.tipo]=(ss[r.tipo]||0)+1});
  chPareto($('#ch-sem'),Object.keys(ss).map(function(n){return{n:n,v:ss[n]}}).sort(function(a,b){return b.v-a.v}).slice(0,7),'Nenhum sem sucesso!');

  badges(L,R);retPainel(L,R);gasPainel(L,G);
}

function badges(L,R){
  var el=$('#badges');if(!EQ.length){el.innerHTML='<div class="empty">Cadastre a equipe.</div>';return}
  var mxF=Math.max(1,Math.max.apply(null,EQ.map(function(t){return L.filter(function(r){return r.tecnico===t}).reduce(function(s,r){return s+r.valor},0)})));
  el.innerHTML=EQ.map(function(t){
    var l=L.filter(function(r){return r.tecnico===t}),s=l.filter(OK);
    var f=l.reduce(function(a,r){return a+r.valor},0),c=l.reduce(function(a,r){return a+r.receber},0);
    var rt=R.filter(function(r){return r.tecOrig===t&&r.devido==='DEVIDO'}).length;
    return '<article class="badge"><div class="stripe"></div><div class="body">'+
      '<div class="nm">'+esc(t)+'</div><div class="info">'+l.length+' serviços · '+rt+' ret. devido(s)</div>'+
      '<div class="stats"><div><b class="mono">'+s.length+'</b><small>Sucesso</small></div>'+
      '<div><b class="mono">'+pct(s.length,l.length)+'%</b><small>Taxa</small></div>'+
      '<div><b class="mono">'+bk(c)+'</b><small>Receber</small></div></div>'+
      '<div class="pbar"><i style="width:'+((f/mxF*100).toFixed(0))+'%"></i></div>'+
      '<p style="margin:5px 0 0;font-size:.75rem;color:var(--ink3)">Produziu '+brl(f)+'</p></div></article>';
  }).join('');
}

function retPainel(L,R){
  var suc=L.filter(OK),dev=R.filter(function(r){return r.devido==='DEVIDO'}).length;
  var ind=R.filter(function(r){return r.devido==='INDEVIDO'}).length;
  var pend=R.filter(function(r){return!r.resultado||r.resultado==='PENDENTE'}).length;
  $('#kpis-r').innerHTML=[
    ['Total',R.length,pct(R.length,suc.length)+'% dos ok','err'],
    ['Devidos',dev,'falha/incompleto','err'],
    ['Indevidos',ind,'não era da equipe','m'],
    ['Pendentes',pend,'sem resultado','']
  ].map(function(x){return '<div class="kpi '+x[3]+'"><div class="lb">'+x[0]+'</div><div class="vl mono">'+x[1]+'</div><div class="sm">'+x[2]+'</div></div>'}).join('');
  chBar($('#ch-rt'),EQ.map(function(t){return{n:t,v:R.filter(function(r){return r.tecOrig===t}).length}}).filter(function(d){return d.v}).sort(function(a,b){return b.v-a.v}),'var(--ora2)');
  var mv={};R.forEach(function(r){var m=r.motivo||'N/I';mv[m]=(mv[m]||0)+1});
  chPareto($('#ch-rm'),Object.keys(mv).map(function(n){return{n:n,v:mv[n]}}).sort(function(a,b){return b.v-a.v}).slice(0,7),'Nenhum retorno.');
  $('#tb-ret').innerHTML=R.length?R.slice().sort(function(a,b){return(b.data||'').localeCompare(a.data||'')}).map(function(r){
    var cls=r.devido==='INDEVIDO'?'t4':'t3';
    return '<tr><td class="mono">'+bd(r.data)+'</td><td class="mono">'+esc(r.os)+'</td><td class="mono">'+esc(r.osOrig)+'</td>'+
      '<td>'+esc(r.tipo)+'</td><td>'+esc(r.tecOrig)+'</td><td>'+esc(r.motivo)+'</td><td>'+esc(r.tecResp)+'</td>'+
      '<td><span class="tag '+cls+'">'+esc(r.devido)+'</span></td><td>'+esc(r.resultado)+'</td>'+
      '<td><button class="del" data-k="ret" data-id="'+r.id+'">×</button></td></tr>'}).join('')
    :'<tr><td colspan="10" class="empty">Nenhum retorno.</td></tr>';
}

function gasPainel(L,G){
  var prodTotal=L.reduce(function(s,r){return s+r.valor},0);
  var desp=G.reduce(function(s,g){return s+g.valor},0);
  var viat=G.filter(function(g){return g.categoria.indexOf('VIATURA')>=0}).reduce(function(s,g){return s+g.valor},0);
  $('#kpis-g').innerHTML=[
    ['Receita',bk(prodTotal),'produção total','ok'],
    ['Despesas',bk(desp),G.length+' lançamento(s)','err'],
    ['Resultado',bk(prodTotal-desp),prodTotal?'margem '+pct(prodTotal-desp,prodTotal)+'%':'—',prodTotal-desp>=0?'ok':'err'],
    ['Viaturas',bk(viat),pct(viat,desp)+'% das desp.','']
  ].map(function(x){return '<div class="kpi '+x[3]+'"><div class="lb">'+x[0]+'</div><div class="vl mono">'+x[1]+'</div><div class="sm">'+x[2]+'</div></div>'}).join('');
  var cat={};G.forEach(function(g){var c=g.categoria||'OUTROS';cat[c]=(cat[c]||0)+g.valor});
  chBar($('#ch-gc'),Object.keys(cat).map(function(n){return{n:n,v:Math.round(cat[n])}}).sort(function(a,b){return b.v-a.v}).slice(0,10),'var(--ora2)',bk);
  $('#tb-gas').innerHTML=G.length?G.slice().sort(function(a,b){return(b.data||'').localeCompare(a.data||'')}).map(function(g){
    return '<tr><td class="mono">'+bd(g.data)+'</td><td>'+esc(g.categoria)+'</td><td>'+esc(g.descricao)+'</td>'+
      '<td class="r mono">'+brl(g.valor)+'</td><td><button class="del" data-k="gas" data-id="'+g.id+'">×</button></td></tr>'}).join('')
    :'<tr><td colspan="5" class="empty">Nenhum gasto.</td></tr>';
}

function tblLanc(){
  var m=$('#f-mes').value,t=$('#fl-tc').value,s=$('#fl-st').value,q=($('#fl-q').value||'').toLowerCase();
  var L=REG.filter(function(r){
    return(m==='todos'||ms(r.data)===m)&&(!t||r.tecnico===t)&&(!s||r.status===s)&&
      (!q||(r.os+' '+r.tipo).toLowerCase().indexOf(q)>=0)
  }).sort(function(a,b){return(b.data||'').localeCompare(a.data||'')});
  var tb=$('#tb-lanc');
  tb.innerHTML=L.length?L.map(function(r){
    var cls=r.status==='COM SUCESSO'?'t1':r.status==='SEM SUCESSO'?'t2':r.status.indexOf('RETORNO')>=0?'t3':'t4';
    var ad=[r.apos18?'18h':'',r.feriado?'Fer':'',r.domingo?'Dom':''].filter(Boolean).join(' ');
    return '<tr><td class="mono">'+bd(r.data)+'</td><td class="mono">'+esc(r.os)+'</td><td>'+esc(r.tecnico)+'</td>'+
      '<td>'+esc(r.tipo)+'</td><td><span class="tag '+cls+'">'+esc(r.status)+'</span></td>'+
      '<td class="r mono">'+brl(r.valor)+'</td><td class="r mono">'+brl(r.receber)+'</td>'+
      '<td><button class="del" data-k="reg" data-id="'+r.id+'">×</button></td></tr>'
  }).join(''):'<tr><td colspan="8" class="empty">Sem lançamentos.</td></tr>';
  var ft=L.reduce(function(s2,r){return s2+r.valor},0);
  $('#tb-sum').textContent=L.length?L.length+' linha(s) · '+brl(ft)+' produção total · '+brl(L.reduce(function(s2,r){return s2+r.receber},0))+' a receber':'';
}

/* === EVENTS === */
$('#f-mes').onchange=$('#f-tec-p').onchange=function(){dashboard();tblLanc()};
$('#fl-tc').onchange=$('#fl-st').onchange=$('#fl-q').oninput=tblLanc;

$('#btn-save').onclick=function(){
  if(!$('#c-dt').value){toast('Informe a data.',1);return}
  REG.push({id:uid('L'),data:$('#c-dt').value,os:$('#c-os').value.trim(),tecnico:$('#c-tc').value,
    tipo:$('#c-tp').value,valor:+$('#c-vl').value||0,receber:+$('#c-rc').value||0,
    status:$('#c-st').value,apos18:$('#c-18').checked,feriado:$('#c-fe').checked,domingo:$('#c-do').checked});
  save();$('#c-os').value=$('#c-vl').value=$('#c-rc').value='';
  $('#c-18').checked=$('#c-fe').checked=$('#c-do').checked=false;
  render();toast('Salvo!');
};
$('#btn-clr').onclick=function(){$('#c-os').value=$('#c-vl').value=$('#c-rc').value='';$('#c-18').checked=$('#c-fe').checked=$('#c-do').checked=false};

$('#btn-ret').onclick=function(){
  if(!$('#r-dt').value){toast('Informe a data.',1);return}
  RET.push({id:uid('R'),data:$('#r-dt').value,os:$('#r-os').value.trim(),osOrig:$('#r-oo').value.trim(),
    tipo:$('#r-tp').value,statusOrig:$('#r-so').value,tecOrig:$('#r-to').value,
    motivo:($('#r-mt').value||'').trim().toUpperCase(),tecResp:$('#r-tr').value,
    devido:$('#r-dv').value,resultado:$('#r-rs').value});
  save();$('#r-os').value=$('#r-oo').value=$('#r-mt').value='';
  render();toast('Retorno salvo!');
};

$('#btn-gas').onclick=function(){
  if(!$('#g-dt').value||!(+$('#g-vl').value)){toast('Data e valor obrigatórios.',1);return}
  GAS.push({id:uid('G'),data:$('#g-dt').value,categoria:$('#g-ct').value,
    descricao:($('#g-ds').value||'').trim(),valor:+$('#g-vl').value});
  save();$('#g-ds').value=$('#g-vl').value='';
  render();toast('Gasto salvo!');
};

document.addEventListener('click',function(e){
  var b=e.target.closest('.del');if(!b)return;
  armed(b,'Excluir?','×',function(){
    var k=b.dataset.k,id=b.dataset.id;
    if(k==='reg')REG=REG.filter(function(x){return x.id!==id});
    if(k==='ret')RET=RET.filter(function(x){return x.id!==id});
    if(k==='gas')GAS=GAS.filter(function(x){return x.id!==id});
    save();render();toast('Excluído.');
  });
});

$('#btn-cad').onclick=function(){
  EQ=$('#lst-tc').value.split('\n').map(function(s){return s.trim()}).filter(Boolean);
  TP=$('#lst-tp').value.split('\n').map(function(s){return s.trim()}).filter(Boolean);
  save();render();toast('Cadastros atualizados.');
};

/* === IMPORT === */
function dISO(v){
  if(v==null||v==='')return'';
  if(v instanceof Date)return new Date(v.getTime()-v.getTimezoneOffset()*6e4).toISOString().slice(0,10);
  if(typeof v==='number')return new Date(Date.UTC(1899,11,30)+v*864e5).toISOString().slice(0,10);
  var s=String(v).trim();if(/^\d{4}-\d{2}-\d{2}/.test(s))return s.slice(0,10);
  var m=s.match(/^(\d{1,2})[\/\-](\d{1,2})[\/\-](\d{2,4})/);
  if(m)return(m[3].length===2?'20'+m[3]:m[3])+'-'+('0'+m[2]).slice(-2)+'-'+('0'+m[1]).slice(-2);
  return '';
}
function nn(v){var n=parseFloat(String(v==null?'':v).replace(/[^\d,.\-]/g,'').replace(/\.(?=\d{3}\b)/g,'').replace(',','.'));return isFinite(n)?n:0}
function SIM(v){return String(v||'').trim().toUpperCase()==='SIM'}
function abaRows(wb,nome,cab){
  var ws=wb.Sheets[nome];if(!ws)return[];
  var m=XLSX.utils.sheet_to_json(ws,{header:1,defval:'',raw:false,cellDates:true});
  var idx=-1;
  for(var i=0;i<Math.min(10,m.length);i++){if(String(m[i][0]||'').toLowerCase().indexOf(cab)>=0){idx=i;break}}
  if(idx<0)return[];
  var hdr=m[idx].map(function(x){return String(x).trim()});
  return m.slice(idx+1).filter(function(l){return l.some(function(c){return c!==''})}).map(function(l){
    var o={};hdr.forEach(function(k,j){o[k]=l[j]});return o});
}
$('#arq').onchange=function(e){
  var f=e.target.files[0];if(!f)return;var msg=$('#msg-imp');
  if(/\.csv$/i.test(f.name)){doImport(f,msg)}
  else{loadXLSX(function(){doImport(f,msg)})}
};
function doImport(f,msg){
  var reader=new FileReader();
  reader.onload=function(ev){
    try{
      var nl=[],nr=[],ng=[];
      if(/\.csv$/i.test(f.name)){
        var txt=ev.target.result;var l0=txt.split('\n')[0];
        var sep=(l0.match(/;/g)||[]).length>(l0.match(/,/g)||[]).length?';':',';
        var parts=txt.split(/\r?\n/).filter(function(x){return x.trim()});
        var hdr=parts[0].split(sep).map(function(x){return x.replace(/^"|"$/g,'').trim()});
        nl=parts.slice(1).map(function(l){var c=l.split(sep);var o={};hdr.forEach(function(k,i){o[k]=(c[i]||'').replace(/^"|"$/g,'').trim()});return o});
      }else{
        var wb=XLSX.read(ev.target.result,{cellDates:true});
        nl=abaRows(wb,'LANÇAMENTOS','data');
        nr=abaRows(wb,'RETORNOS','data do retorno');
        ng=abaRows(wb,'LANÇAMENTO DE GASTOS','data');
        if(!nl.length){nl=XLSX.utils.sheet_to_json(wb.Sheets[wb.SheetNames[0]],{defval:''})}
      }
      var lanc=nl.map(function(o){
        var recKey=Object.keys(o).filter(function(k){return /receber/i.test(k)})[0];
        return{id:uid('L'),data:dISO(o['Data']),os:String(o['Nº do Serviço']||o['OS']||'').trim(),
          tecnico:String(o['Técnico']||'').trim().toUpperCase(),
          tipo:String(o['Tipo de Serviço']||'OUTROS SERVIÇOS').trim().toUpperCase(),
          valor:nn(o['Valor do Serviço (R$)']||o['Valor']),
          receber:nn(recKey?o[recKey]:0),
          status:String(o['Status']||'COM SUCESSO').trim().toUpperCase(),
          apos18:SIM(o['Após 18h']),feriado:SIM(o['Feriado']),domingo:SIM(o['Domingo'])}
      }).filter(function(r){return r.data||r.os});
      var rets=nr.map(function(o){
        var trKey=Object.keys(o).filter(function(k){return /responsável|responsavel/i.test(k)})[0];
        return{id:uid('R'),data:dISO(o['Data do Retorno']),os:String(o['Nº do Retorno']||'').trim(),
          osOrig:String(o['Nº do Serviço Original']||'').trim(),tipo:String(o['Tipo de Serviço']||'').trim().toUpperCase(),
          statusOrig:String(o['Status do Serviço Original']||'').trim().toUpperCase(),
          tecOrig:String(o['Técnico do Serviço Original']||'').trim().toUpperCase(),
          motivo:String(o['Motivo do Retorno']||'').trim().toUpperCase(),
          tecResp:String(trKey?o[trKey]:'').trim().toUpperCase(),
          devido:String(o['Retorno Devido/Indevido']||'DEVIDO').trim().toUpperCase(),
          resultado:String(o['Resultado do Retorno']||'').trim().toUpperCase()}
      }).filter(function(r){return r.data||r.os});
      var gas=ng.map(function(o){
        return{id:uid('G'),data:dISO(o['Data']),categoria:String(o['Categoria']||'OUTROS').trim(),
          descricao:String(o['Descrição']||'').trim(),valor:nn(o['Valor (R$)']||o['Valor'])}
      }).filter(function(g){return g.data&&g.valor});
      if(!lanc.length&&!rets.length&&!gas.length)throw new Error('Nenhuma linha válida encontrada.');
      var sub=$('#chk-sub').checked;
      REG=sub?lanc:REG.concat(lanc);
      if(rets.length||sub)RET=sub?rets:RET.concat(rets);
      if(gas.length||sub)GAS=sub?gas:GAS.concat(gas);
      lanc.forEach(function(r){if(r.tecnico&&EQ.indexOf(r.tecnico)<0)EQ.push(r.tecnico)});
      lanc.forEach(function(r){if(r.tipo&&TP.indexOf(r.tipo)<0)TP.push(r.tipo)});
      save();sSet(SK.i,1);
      msg.style.color='var(--ok)';msg.textContent=lanc.length+' lanç, '+rets.length+' ret, '+gas.length+' gastos importados.';
      render();
    }catch(err){msg.style.color='var(--err)';msg.textContent=err.message}
  };
  if(/\.csv$/i.test(f.name))reader.readAsText(f);else reader.readAsArrayBuffer(f);
  e.target.value='';
};

/* === EXPORT === */
function dl(name,content,type){var a=document.createElement('a');a.href=URL.createObjectURL(new Blob([content],{type:type}));a.download=name;a.click();URL.revokeObjectURL(a.href)}
function flat(){return REG.map(function(r){return{Data:bd(r.data),'Nº do Serviço':r.os,Técnico:r.tecnico,'Tipo de Serviço':r.tipo,'Valor (R$)':r.valor,'A Receber (R$)':r.receber,Status:r.status,'Após 18h':r.apos18?'SIM':'NÃO',Feriado:r.feriado?'SIM':'NÃO',Domingo:r.domingo?'SIM':'NÃO'}})}
$('#btn-csv').onclick=function(){
  var d=flat();if(!d.length)return toast('Nada para exportar.',1);
  var k=Object.keys(d[0]);
  var csv=k.join(';')+'\n'+d.map(function(o){return k.map(function(c){return'"'+String(o[c]).replace(/"/g,'""')+'"'}).join(';')}).join('\n');
  dl('lancamentos-goiania.csv','\ufeff'+csv,'text/csv;charset=utf-8');
};
$('#btn-xl').onclick=function(){
  loadXLSX(function(){
    if(!REG.length&&!GAS.length)return toast('Nada para exportar.',1);
  var wb=XLSX.utils.book_new();
  XLSX.utils.book_append_sheet(wb,XLSX.utils.json_to_sheet(flat()),'LANCAMENTOS');
  XLSX.utils.book_append_sheet(wb,XLSX.utils.json_to_sheet(RET.map(function(r){return{'Data':bd(r.data),'Nº Retorno':r.os,'Serviço Original':r.osOrig,Tipo:r.tipo,'Status Original':r.statusOrig,'Téc. Original':r.tecOrig,Motivo:r.motivo,'Téc. Retorno':r.tecResp,Classificação:r.devido,Resultado:r.resultado}})),'RETORNOS');
  XLSX.utils.book_append_sheet(wb,XLSX.utils.json_to_sheet(GAS.map(function(g){return{Data:bd(g.data),Categoria:g.categoria,Descrição:g.descricao,'Valor (R$)':g.valor}})),'GASTOS');
  XLSX.utils.book_append_sheet(wb,XLSX.utils.json_to_sheet(EQ.map(function(t){
    var l=REG.filter(function(r){return r.tecnico===t}),s=l.filter(OK);
    return{Técnico:t,Serviços:l.length,'Com sucesso':s.length,'Taxa %':l.length?pct(s.length,l.length):0,
      'Produzido (R$)':+s.reduce(function(a,r){return a+r.valor},0).toFixed(2),
      'A Receber (R$)':+l.reduce(function(a,r){return a+r.receber},0).toFixed(2),
      'Ret. devidos':RET.filter(function(r){return r.tecOrig===t&&r.devido==='DEVIDO'}).length}
  })),'RESUMO');
  XLSX.writeFile(wb,'controle-goiania.xlsx');
  });
};
$('#btn-bkp').onclick=function(){dl('backup-goiania.json',JSON.stringify({lancamentos:REG,retornos:RET,gastos:GAS,equipe:EQ,tipos:TP},null,1),'application/json')};
$('#btn-rest').onclick=function(){$('#arq-j').click()};
$('#arq-j').onchange=function(e){
  var f=e.target.files[0];if(!f)return;
  var rd=new FileReader();
  rd.onload=function(ev){
    try{var o=JSON.parse(ev.target.result);
      REG=o.lancamentos||[];RET=o.retornos||[];GAS=o.gastos||[];
      EQ=o.equipe||EQ;TP=o.tipos||TP;
      save();sSet(SK.i,1);render();toast('Backup restaurado!');
    }catch(err){toast('Arquivo inválido.',1)}
  };rd.readAsText(f);e.target.value='';
};
$('#btn-wipe').onclick=function(){
  var self=this;
  armed(self,'Confirmar: apagar tudo','Apagar todos os dados',function(){
    REG=[];RET=[];GAS=[];
    sDel(SK.r);sDel(SK.t);sDel(SK.g);sSet(SK.r,[]);sSet(SK.t,[]);sSet(SK.g,[]);sSet(SK.i,1);
    render();toast('Tudo apagado.');
  });
};

/* === START === */
/* Carrega XLSX só quando precisar (não bloqueia a página) */
var _xlsxLoaded=false;
function loadXLSX(cb){
  if(_xlsxLoaded||typeof XLSX!=='undefined'){_xlsxLoaded=true;if(cb)cb();return}
  var s=document.createElement('script');
  s.src='https://cdn.jsdelivr.net/npm/xlsx@0.18.5/dist/xlsx.full.min.js';
  s.onload=function(){_xlsxLoaded=true;if(cb)cb()};
  s.onerror=function(){toast('Sem internet para carregar biblioteca Excel.',1)};
  document.head.appendChild(s);
}
init();
</script>
</body>
</html>
