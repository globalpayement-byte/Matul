<!DOCTYPE html>
<html lang="fr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Matul Trade Pro</title>
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/@tabler/icons-webfont@2.44.0/tabler-icons.min.css">
<style>
*{box-sizing:border-box;margin:0;padding:0}
body{background:#0a0a0a;color:#fff;font-family:-apple-system,BlinkMacSystemFont,'Segoe UI',sans-serif;min-height:100vh}
.app{max-width:480px;margin:0 auto;padding:14px;padding-bottom:80px}
.hdr{text-align:center;padding:14px 0 10px}
.logo{width:42px;height:42px;border-radius:50%;background:#1a3a1a;border:2px solid #4ade80;display:flex;align-items:center;justify-content:center;font-size:13px;color:#4ade80;font-weight:600;margin:0 auto 6px}
.title{font-size:26px;font-weight:600;color:#c8f135}
.sub{font-size:11px;color:#666;margin-top:2px}
.badge{font-size:11px;display:flex;align-items:center;justify-content:center;gap:6px;margin-top:5px}
.dot{width:7px;height:7px;border-radius:50%;background:#444}
.dot.on{background:#4ade80;animation:pulse 2s infinite}
.dot.sc{background:#f59e0b;animation:pulse .4s infinite}
@keyframes pulse{0%,100%{opacity:1}50%{opacity:.3}}
@keyframes spin{from{transform:rotate(0deg)}to{transform:rotate(360deg)}}
.mode-banner{border-radius:10px;padding:10px 14px;margin-bottom:10px;display:flex;align-items:center;justify-content:space-between}
.mode-banner.sim{background:#1a2a1a;border:1px solid #4ade80}
.mode-banner.real{background:#2a1a00;border:1px solid #f59e0b}
.mode-label{font-size:13px;font-weight:600}
.mode-label.sim{color:#4ade80}
.mode-label.real{color:#f59e0b}
.mode-toggle{background:transparent;border:0.5px solid #444;border-radius:20px;padding:5px 14px;font-size:12px;color:#aaa;cursor:pointer;display:flex;align-items:center;gap:5px}
.sg{display:grid;grid-template-columns:1fr 1fr;gap:8px;margin-bottom:8px}
.sc{background:#1a1a1a;border-radius:10px;padding:11px 12px;border:.5px solid #2a2a2a}
.sl{font-size:10px;color:#555;text-transform:uppercase;letter-spacing:.5px;margin-bottom:3px}
.sv{font-size:20px;font-weight:600;color:#38bdf8}
.sv.g{color:#4ade80}
.sv.y{color:#f59e0b}
.sv.sm{font-size:13px;color:#aaa;font-weight:400}
.auto-card{background:#1a1a1a;border-radius:10px;padding:12px 14px;margin-bottom:8px;border:.5px solid #2a2a2a}
.auto-header{display:flex;align-items:center;justify-content:space-between;margin-bottom:10px}
.auto-title{font-size:13px;font-weight:600;color:#fff}
.toggle-wrap{display:flex;align-items:center;gap:8px}
.toggle{width:48px;height:26px;border-radius:13px;background:#333;border:none;cursor:pointer;position:relative;transition:background .2s}
.toggle.on{background:#4ade80}
.toggle-knob{width:20px;height:20px;border-radius:50%;background:#fff;position:absolute;top:3px;left:3px;transition:left .2s}
.toggle.on .toggle-knob{left:25px}
.toggle-lbl{font-size:12px;font-weight:600}
.toggle-lbl.on{color:#4ade80}
.toggle-lbl.off{color:#f87171}
.auto-fields{display:grid;grid-template-columns:1fr 1fr;gap:8px}
.afield{display:flex;flex-direction:column;gap:4px}
.afl{font-size:10px;color:#555;text-transform:uppercase;letter-spacing:.5px}
.afi{background:#111;border:.5px solid #333;border-radius:7px;color:#fff;font-size:13px;padding:7px 9px;outline:none;width:100%}
.ctrl{background:#1a1a1a;border-radius:10px;padding:11px 12px;margin-bottom:10px;border:.5px solid #2a2a2a}
.ctrl-row{display:flex;gap:7px;flex-wrap:wrap;align-items:flex-end}
.cg{display:flex;flex-direction:column;gap:3px}
.cl{font-size:10px;color:#555;text-transform:uppercase;letter-spacing:.5px}
.ci{background:#111;border:.5px solid #333;border-radius:7px;color:#fff;font-size:13px;padding:7px 8px;width:82px;outline:none}
.btn-scan{background:#c8f135;color:#111;border:none;border-radius:7px;font-size:13px;font-weight:600;padding:8px 14px;cursor:pointer;display:flex;align-items:center;gap:5px}
.btn-auto-scan{background:#1a2a1a;color:#4ade80;border:1px solid #4ade80;border-radius:7px;font-size:10px;padding:6px 10px;cursor:pointer;display:flex;flex-direction:column;align-items:center;gap:1px}
.btn-auto-scan.on{background:#4ade80;color:#111}
.prog{font-size:10px;color:#666;text-align:center;padding:4px 0;min-height:16px}
.th{display:grid;grid-template-columns:2fr .8fr .8fr 58px;gap:4px;padding:5px 8px;margin-bottom:4px}
.th span{font-size:10px;color:#444;font-weight:600;text-transform:uppercase}
.row{background:#1a1a1a;border-radius:9px;margin-bottom:6px;border:.5px solid #2a2a2a}
.row.hot{border-color:#4ade80}
.row.sim-row{border-color:#38bdf8}
.rt{display:grid;grid-template-columns:2fr .8fr .8fr 58px;gap:4px;padding:9px 8px;align-items:center}
.rx{font-size:10px;color:#ddd;font-family:'Courier New',monospace;line-height:1.4}
.rdb{font-size:9px;margin-top:2px}
.rdb.mexc{color:#f59e0b}
.rdb.bnb{color:#38bdf8}
.pp{font-size:12px;font-weight:600;color:#4ade80}
.gv{font-size:11px;color:#4ade80;font-weight:500}
.btn-go{background:#4ade80;color:#111;border:none;border-radius:6px;font-size:11px;font-weight:600;padding:7px 3px;cursor:pointer;width:100%}
.btn-go.sim{background:#38bdf8}
.empty{text-align:center;color:#333;font-size:13px;padding:2rem 1rem;line-height:2}
.ticker{font-size:10px;color:#333;text-align:center;padding:3px 0 6px;font-family:'Courier New',monospace}
.sim-note{font-size:11px;color:#38bdf8;text-align:center;padding:4px 8px;background:#0a1a2a;border-radius:6px;margin-bottom:8px}
.spin{animation:spin 1s linear infinite}
.bnav{position:fixed;bottom:0;left:0;right:0;background:#111;border-top:.5px solid #222;display:flex;justify-content:space-around;padding:8px 0 10px;z-index:50}
.bnav-item{display:flex;flex-direction:column;align-items:center;gap:3px;cursor:pointer;opacity:.5;background:none;border:none;color:#fff;font-size:10px;padding:4px 14px}
.bnav-item.active{opacity:1;color:#4ade80}
.bnav-item i{font-size:22px}
.page{display:none}
.page.active{display:block}
.section-title{font-size:12px;color:#555;text-transform:uppercase;letter-spacing:.5px;margin:14px 0 8px;font-weight:600}
.dash-stat{background:#1a1a1a;border-radius:10px;padding:12px 14px;margin-bottom:8px;border:.5px solid #2a2a2a}
.dash-row{display:flex;justify-content:space-between;align-items:center;padding:7px 0;border-bottom:.5px solid #1e1e1e;font-size:13px}
.dash-row:last-child{border-bottom:none}
.dash-row span:first-child{color:#666}
.dash-val{color:#fff;font-weight:500}
.dash-val.g{color:#4ade80}
.dash-val.r{color:#f87171}
.hist-item{background:#1a1a1a;border-radius:8px;padding:10px 12px;margin-bottom:6px;border:.5px solid #2a2a2a;display:flex;justify-content:space-between;align-items:center}
.hist-left{flex:1}
.hist-route{font-size:10px;font-family:'Courier New',monospace;color:#ddd;margin-bottom:3px}
.hist-meta{font-size:10px;color:#555}
.hist-right{text-align:right}
.hist-profit{font-size:13px;font-weight:600}
.hist-profit.g{color:#4ade80}
.hist-profit.r{color:#f87171}
.set-section{background:#1a1a1a;border-radius:10px;margin-bottom:10px;border:.5px solid #2a2a2a;overflow:hidden}
.set-header{padding:11px 14px;font-size:12px;font-weight:600;color:#888;text-transform:uppercase;letter-spacing:.5px;border-bottom:.5px solid #222;display:flex;align-items:center;gap:8px}
.set-row{padding:12px 14px;border-bottom:.5px solid #111;display:flex;justify-content:space-between;align-items:center}
.set-row:last-child{border-bottom:none}
.set-label{font-size:13px;color:#ddd}
.set-sub{font-size:11px;color:#555;margin-top:2px}
.set-input{background:#111;border:.5px solid #333;border-radius:6px;color:#fff;font-size:13px;padding:6px 9px;width:140px;outline:none;text-align:right}
.set-status{font-size:11px;padding:3px 8px;border-radius:4px}
.set-status.ok{background:#1a3a1a;color:#4ade80}
.set-status.no{background:#2a1a1a;color:#f87171}
.btn-save{background:#4ade80;color:#111;border:none;border-radius:7px;font-size:12px;font-weight:600;padding:7px 14px;cursor:pointer;margin-top:10px;width:100%}
.ov{display:none;position:fixed;inset:0;background:rgba(0,0,0,.88);z-index:100;align-items:flex-end;justify-content:center}
.ov.show{display:flex}
.mod{background:#1a1a1a;border-radius:14px 14px 0 0;padding:20px 16px 30px;width:100%;max-width:480px;border-top:.5px solid #333;max-height:90vh;overflow-y:auto}
.mh{width:36px;height:4px;background:#333;border-radius:2px;margin:0 auto 16px}
.mt{font-size:15px;font-weight:600;margin-bottom:12px;display:flex;align-items:center;gap:8px}
.mr{display:flex;justify-content:space-between;padding:8px 0;border-bottom:.5px solid #1e1e1e;font-size:13px}
.mr span:first-child{color:#666}
.mv{color:#fff;font-weight:500}
.mg{color:#4ade80;font-weight:500}
.mm{font-family:'Courier New',monospace;font-size:10px;color:#777;text-align:right;max-width:58%}
.mstep{display:flex;gap:8px;padding:8px 0;border-bottom:.5px solid #111}
.mnum{min-width:20px;height:20px;border-radius:50%;background:#1a3a1a;color:#4ade80;font-weight:600;font-size:11px;display:flex;align-items:center;justify-content:center}
.mtxt{font-size:12px;color:#bbb;line-height:1.5}
.mtxt strong{color:#fff}
.ibox{background:#0a2a1a;border:.5px solid #1a4a2a;border-radius:8px;padding:10px;margin-top:10px;font-size:11px;color:#4ade80;line-height:1.7}
.wbox{background:#2a1800;border:.5px solid #4a2800;border-radius:8px;padding:10px;margin-top:8px;font-size:11px;color:#f59e0b;line-height:1.6}
.simbox{background:#0a1a2a;border:.5px solid #1a3a4a;border-radius:8px;padding:10px;margin-top:8px;font-size:11px;color:#38bdf8;line-height:1.7}
.mbtns{display:flex;gap:8px;margin-top:14px}
.mbc{flex:1;background:#222;color:#aaa;border:.5px solid #333;border-radius:9px;padding:11px;cursor:pointer;font-size:13px}
.mbg{flex:1;background:#4ade80;color:#111;border:none;border-radius:9px;padding:11px;cursor:pointer;font-size:13px;font-weight:600;display:flex;align-items:center;justify-content:center;gap:5px}
.mbg.sim{background:#38bdf8}
</style>
</head>
<body>
<div class="app">
<div class="page active" id="page-scan">
<div class="hdr">
  <div class="logo">MT</div>
  <div class="title">Matul Trade Pro</div>
  <div class="sub">Triangulaire · Binance · MEXC · 0% fees</div>
  <div class="badge"><span class="dot" id="dot"></span><span id="slbl" style="color:#aaa;font-size:12px">Prêt</span></div>
</div>
<div class="mode-banner sim" id="mode-banner">
  <div>
    <div class="mode-label sim" id="mode-label">🧪 MODE SIMULATION</div>
    <div style="font-size:10px;color:#666;margin-top:2px">Tsy execute trade marina</div>
  </div>
  <button class="mode-toggle" onclick="toggleMode()"><i class="ti ti-arrows-exchange"></i> Changer</button>
</div>
<div class="sg">
  <div class="sc"><div class="sl">Opportunités</div><div class="sv g" id="opp-count">0</div></div>
  <div class="sc"><div class="sl">Profit max</div><div class="sv g" id="max-profit">—</div></div>
</div>
<div class="sg">
  <div class="sc"><div class="sl">Capital (USDT)</div>
    <input id="capital-in" type="number" value="350" style="width:100%;background:transparent;border:none;color:#4ade80;font-size:18px;font-weight:600;padding:0;margin-top:2px;outline:none">
  </div>
  <div class="sc"><div class="sl">Profit simulé total</div><div class="sv y" id="sim-total">0.000 USDT</div></div>
</div>
<div class="auto-card">
  <div class="auto-header">
    <div class="auto-title"><i class="ti ti-robot"></i> Auto Trade</div>
    <div class="toggle-wrap">
      <span class="toggle-lbl off" id="auto-lbl">OFF</span>
      <button class="toggle" id="auto-toggle" onclick="toggleAuto()"><div class="toggle-knob" id="toggle-knob"></div></button>
    </div>
  </div>
  <div class="auto-fields">
    <div class="afield"><span class="afl">Min profit %</span><input class="afi" type="number" id="auto-min" value="0.3" step="0.05" min="0.1"></div>
    <div class="afield"><span class="afl">Montant/trade</span><input class="afi" type="number" id="auto-amount" value="50" step="10" min="10"></div>
  </div>
</div>
<div class="ctrl">
  <div class="ctrl-row">
    <div class="cg"><span class="cl">Min profit %</span><input class="ci" type="number" id="min-p" value="0.05" step="0.01" min="0.01"></div>
    <div class="cg"><span class="cl">Frais %</span><input class="ci" type="number" id="fee-in" value="0.1" step="0.05"></div>
    <button class="btn-scan" onclick="doScan()"><i class="ti ti-refresh" id="scan-ic"></i> Scan</button>
    <button class="btn-auto-scan" id="auto-scan-btn" onclick="toggleAutoScan()">
      <i class="ti ti-player-play" id="auto-scan-ic" style="font-size:14px"></i>
      <span id="auto-scan-txt">Auto</span>
    </button>
  </div>
  <div class="prog" id="prog"></div>
</div>
<div id="sim-note-div" class="sim-note"><i class="ti ti-flask"></i> Simulation — Profits calculés sans exécution réelle</div>
<div class="th"><span>Route</span><span>Profit</span><span>Gain</span><span>Action</span></div>
<div id="results">
  <div class="empty"><i class="ti ti-arrows-exchange" style="font-size:32px;display:block;margin-bottom:10px"></i>Tsindrio Scan<br><span style="font-size:11px">Binance · MEXC · Triangulaire</span></div>
</div>
<div class="ticker" id="ticker"></div>
</div>

<div class="page" id="page-dash">
<div style="padding-top:10px">
  <div class="section-title"><i class="ti ti-chart-bar"></i> Statistiques</div>
  <div class="dash-stat">
    <div class="dash-row"><span>Profit NET simulation</span><span class="dash-val g" id="d-sim-profit">0.0000 USDT</span></div>
    <div class="dash-row"><span>Trades simulés</span><span class="dash-val" id="d-sim-trades">0</span></div>
    <div class="dash-row"><span>Profit NET réel</span><span class="dash-val g" id="d-real-profit">0.0000 USDT</span></div>
    <div class="dash-row"><span>Trades réels succès</span><span class="dash-val g" id="d-real-success">0</span></div>
    <div class="dash-row"><span>Trades réels échecs</span><span class="dash-val r" id="d-real-failed">0</span></div>
    <div class="dash-row"><span>Taux succès</span><span class="dash-val" id="d-rate">—</span></div>
    <div class="dash-row"><span>Meilleure opportunité</span><span class="dash-val g" id="d-best">—</span></div>
  </div>
  <div class="section-title"><i class="ti ti-history"></i> Historique</div>
  <div id="hist-list"><div class="empty" style="padding:1rem">Aucun trade</div></div>
</div>
</div>

<div class="page" id="page-set">
<div style="padding-top:10px">
  <div class="section-title"><i class="ti ti-settings"></i> Configuration</div>
  <div class="set-section">
    <div class="set-header"><i class="ti ti-brand-telegram"></i> Telegram</div>
    <div class="set-row">
      <div><div class="set-label">Bot Token</div><div class="set-sub">@BotFather → /newbot</div></div>
      <input class="set-input" id="tg-token" type="password" placeholder="token...">
    </div>
    <div class="set-row">
      <div><div class="set-label">Chat ID</div><div class="set-sub">@userinfobot</div></div>
      <input class="set-input" id="tg-chatid" placeholder="123456789">
    </div>
    <div style="padding:10px 14px"><button class="btn-save" onclick="saveTelegram()">✅ Sauvegarder Telegram</button></div>
  </div>
  <div class="set-section">
    <div class="set-header" style="color:#f59e0b"><i class="ti ti-coin"></i> Binance API</div>
    <div class="set-row">
      <div><div class="set-label">API Key</div><div id="bnb-status" class="set-status no">Non configuré</div></div>
      <input class="set-input" id="bnb-key" type="password" placeholder="API Key...">
    </div>
    <div class="set-row">
      <div><div class="set-label">Secret Key</div></div>
      <input class="set-input" id="bnb-secret" type="password" placeholder="Secret...">
    </div>
    <div style="padding:10px 14px"><button class="btn-save" onclick="saveExchange('binance')">✅ Sauvegarder Binance</button></div>
  </div>
  <div class="set-section">
    <div class="set-header" style="color:#f59e0b"><i class="ti ti-coin"></i> MEXC API <span style="font-size:10px;color:#4ade80;margin-left:8px">0% FEES</span></div>
    <div class="set-row">
      <div><div class="set-label">API Key</div><div id="mexc-status" class="set-status no">Non configuré</div></div>
      <input class="set-input" id="mexc-key" type="password" placeholder="API Key...">
    </div>
    <div class="set-row">
      <div><div class="set-label">Secret Key</div></div>
      <input class="set-input" id="mexc-secret" type="password" placeholder="Secret...">
    </div>
    <div style="padding:10px 14px"><button class="btn-save" onclick="saveExchange('mexc')">✅ Sauvegarder MEXC</button></div>
  </div>
  <div style="height:20px"></div>
</div>
</div>
</div>

<div class="bnav">
  <button class="bnav-item active" id="nav-scan" onclick="showPage('scan')"><i class="ti ti-radar"></i>Scanner</button>
  <button class="bnav-item" id="nav-dash" onclick="showPage('dash')"><i class="ti ti-chart-bar"></i>Dashboard</button>
  <button class="bnav-item" id="nav-set" onclick="showPage('set')"><i class="ti ti-settings"></i>Config</button>
</div>

<div class="ov" id="ov" onclick="bgClose(event)">
  <div class="mod"><div class="mh"></div><div id="mc"></div></div>
</div>

<script>
const BOT_PORT=9090;
let scanData=[],autoOn=false,autoScanInt=null,autoScanOn=false,simMode=true;
let history={sim:{trades:[],profit:0,count:0},real:{trades:[],profit:0,success:0,failed:0}};
let cfg={telegram:{token:'',chatid:''},exchanges:{binance:{key:'',secret:''},mexc:{key:'',secret:''}}};
try{const h=localStorage.getItem('mt_h');if(h)history=JSON.parse(h);const c=localStorage.getItem('mt_c');if(c){cfg=JSON.parse(c);updateBadges();}}catch(e){}
function saveState(){try{localStorage.setItem('mt_h',JSON.stringify(history));localStorage.setItem('mt_c',JSON.stringify(cfg));}catch(e){}}
function showPage(p){document.querySelectorAll('.page').forEach(x=>x.classList.remove('active'));document.querySelectorAll('.bnav-item').forEach(x=>x.classList.remove('active'));document.getElementById('page-'+p).classList.add('active');document.getElementById('nav-'+p).classList.add('active');if(p==='dash')updateDash();}
function toggleMode(){
  simMode=!simMode;
  const b=document.getElementById('mode-banner'),l=document.getElementById('mode-label'),n=document.getElementById('sim-note-div');
  if(simMode){b.className='mode-banner sim';l.className='mode-label sim';l.textContent='🧪 MODE SIMULATION';n.style.display='block';}
  else{b.className='mode-banner real';l.className='mode-label real';l.textContent='⚡ MODE RÉEL';n.style.display='none';}
}
function toggleAuto(){
  autoOn=!autoOn;
  const t=document.getElementById('auto-toggle'),l=document.getElementById('auto-lbl'),k=document.getElementById('toggle-knob');
  if(autoOn){t.className='toggle on';l.textContent='ON';l.className='toggle-lbl on';}
  else{t.className='toggle';l.textContent='OFF';l.className='toggle-lbl off';}
}
function toggleAutoScan(){
  autoScanOn=!autoScanOn;
  const b=document.getElementById('auto-scan-btn'),ic=document.getElementById('auto-scan-ic'),tx=document.getElementById('auto-scan-txt');
  if(autoScanOn){b.className='btn-auto-scan on';ic.className='ti ti-player-pause';tx.textContent='Stop';doScan();autoScanInt=setInterval(doScan,15000);}
  else{b.className='btn-auto-scan';ic.className='ti ti-player-play';tx.textContent='Auto';clearInterval(autoScanInt);}
}
const TRI=[
  {s1:'ETHBTC',s2:'ETHUSDT',s3:'BTCUSDT',a:'BTC',b:'ETH'},
  {s1:'BNBBTC',s2:'BNBUSDT',s3:'BTCUSDT',a:'BTC',b:'BNB'},
  {s1:'BNBETH',s2:'BNBUSDT',s3:'ETHUSDT',a:'ETH',b:'BNB'},
  {s1:'XRPBTC',s2:'XRPUSDT',s3:'BTCUSDT',a:'BTC',b:'XRP'},
  {s1:'XRPETH',s2:'XRPUSDT',s3:'ETHUSDT',a:'ETH',b:'XRP'},
  {s1:'SOLBTC',s2:'SOLUSDT',s3:'BTCUSDT',a:'BTC',b:'SOL'},
  {s1:'SOLETH',s2:'SOLUSDT',s3:'ETHUSDT',a:'ETH',b:'SOL'},
  {s1:'ADABTC',s2:'ADAUSDT',s3:'BTCUSDT',a:'BTC',b:'ADA'},
  {s1:'LTCBTC',s2:'LTCUSDT',s3:'BTCUSDT',a:'BTC',b:'LTC'},
  {s1:'DOGEBTC',s2:'DOGEUSDT',s3:'BTCUSDT',a:'BTC',b:'DOGE'},
  {s1:'LINKBTC',s2:'LINKUSDT',s3:'BTCUSDT',a:'BTC',b:'LINK'},
  {s1:'DOTBTC',s2:'DOTUSDT',s3:'BTCUSDT',a:'BTC',b:'DOT'},
  {s1:'AVAXBTC',s2:'AVAXUSDT',s3:'BTCUSDT',a:'BTC',b:'AVAX'},
  {s1:'ATOMBTC',s2:'ATOMUSDT',s3:'BTCUSDT',a:'BTC',b:'ATOM'},
  {s1:'UNIBTC',s2:'UNIUSDT',s3:'BTCUSDT',a:'BTC',b:'UNI'},
  {s1:'MATICETH',s2:'MATICUSDT',s3:'ETHUSDT',a:'ETH',b:'MATIC'},
  {s1:'NEARBTC',s2:'NEARUSDT',s3:'BTCUSDT',a:'BTC',b:'NEAR'},
  {s1:'FTMBTC',s2:'FTMUSDT',s3:'BTCUSDT',a:'BTC',b:'FTM'},
  {s1:'SANDBTC',s2:'SANDUSDT',s3:'BTCUSDT',a:'BTC',b:'SAND'},
  {s1:'AAVEBTC',s2:'AAVEUSDT',s3:'BTCUSDT',a:'BTC',b:'AAVE'},
  {s1:'TRXBTC',s2:'TRXUSDT',s3:'BTCUSDT',a:'BTC',b:'TRX'},
  {s1:'SHIBBTC',s2:'SHIBUSDT',s3:'BTCUSDT',a:'BTC',b:'SHIB'},
  {s1:'SUIBTC',s2:'SUIUSDT',s3:'BTCUSDT',a:'BTC',b:'SUI'},
  {s1:'ARBBTC',s2:'ARBUSDT',s3:'BTCUSDT',a:'BTC',b:'ARB'},
  {s1:'OPBTC',s2:'OPUSDT',s3:'BTCUSDT',a:'BTC',b:'OP'},
];
function calcTri(pm,feePct,minP,exName){
  const f=feePct/100,res=[];
  TRI.forEach(p=>{
    const p1=pm[p.s1],p2=pm[p.s2],p3=pm[p.s3];
    if(!p1||!p2||!p3)return;
    [{route:`USDT→${p.a}→${p.b}→USDT`,
      calcB:()=>((1/p3)/p1*p2-1)*100,
      calcN:()=>((1/p3)*(1-f)/p1*(1-f)*p2*(1-f)-1)*100},
     {route:`USDT→${p.b}→${p.a}→USDT`,
      calcB:()=>((1/p2)*p1*p3-1)*100,
      calcN:()=>((1/p2)*(1-f)*p1*(1-f)*p3*(1-f)-1)*100}
    ].forEach(({route,calcB,calcN})=>{
      try{
        const brut=calcB(),net=calcN(),frais=parseFloat((feePct*3).toFixed(3));
        if(net>=minP&&net<=5&&isFinite(net)){
          res.push({route,profitBrut:parseFloat(brut.toFixed(4)),profitNet:parseFloat(net.toFixed(4)),profit:parseFloat(net.toFixed(4)),frais,exchange:exName,a:p.a,b:p.b,fee:feePct});
        }
      }catch(e){}
    });
  });
  return res;
}
async function doScan(){
  const ic=document.getElementById('scan-ic');
  ic.className='ti ti-refresh spin';
  document.getElementById('dot').className='dot sc';
  document.getElementById('slbl').textContent='Scanning...';
  document.getElementById('prog').textContent='Fetching Binance + MEXC...';
  try{
    const minP=parseFloat(document.getElementById('min-p').value)||0.05;
    const feeB=parseFloat(document.getElementById('fee-in').value)||0.1;
    const capital=parseFloat(document.getElementById('capital-in').value)||350;
    const [rb,rmRaw]=await Promise.all([
      fetch('https://api.binance.com/api/v3/ticker/price').then(r=>r.json()).catch(()=>[]),
      fetch('http://localhost:'+BOT_PORT+'/mexc/prices').then(r=>r.json()).then(d=>typeof d.prices==='object'?Object.entries(d.prices).map(([symbol,price])=>({symbol,price})):[]).catch(()=>[]),
    ]);
    const bm={},mm={};
    if(Array.isArray(rb))rb.forEach(x=>{bm[x.symbol]=parseFloat(x.price);});
    if(Array.isArray(rmRaw))rmRaw.forEach(x=>{if(x.symbol&&x.price)mm[x.symbol]=parseFloat(x.price);});
    const mexcOk=Object.keys(mm).length>0;
    document.getElementById('prog').textContent=mexcOk?'':'⚠️ MEXC tsy miasa — bot Termux ilaina';
    let results=[];
    if(Object.keys(bm).length)results=results.concat(calcTri(bm,feeB,minP,'Binance'));
    if(mexcOk)results=results.concat(calcTri(mm,0,minP,'MEXC'));
    results.sort((a,b)=>b.profitNet-a.profitNet);
    scanData=results.map(r=>({...r,capital,gain:parseFloat((r.profitNet/100*capital).toFixed(4))}));
    document.getElementById('opp-count').textContent=scanData.length;
    document.getElementById('max-profit').textContent=scanData.length?'+'+scanData[0].profitNet.toFixed(3)+'% NET':'0%';
    document.getElementById('ticker').textContent='Binance: '+Object.keys(bm).length+' · MEXC: '+Object.keys(mm).length+' pairs · '+new Date().toLocaleTimeString();
    document.getElementById('dot').className='dot on';
    document.getElementById('slbl').textContent='Live';
    if(!mexcOk)document.getElementById('prog').textContent='⚠️ MEXC: bot Termux ilaina (port '+BOT_PORT+')';
    else document.getElementById('prog').textContent='';
    if(autoOn&&scanData.length){
      const autoMin=parseFloat(document.getElementById('auto-min').value)||0.3;
      const autoAmt=parseFloat(document.getElementById('auto-amount').value)||50;
      const best=scanData.find(r=>r.profitNet>=autoMin);
      if(best)executeAuto(best,autoAmt);
    }
    renderTable(scanData);
  }catch(e){
    document.getElementById('dot').className='dot';
    document.getElementById('slbl').textContent='Erreur';
    document.getElementById('prog').textContent='Erreur API';
  }
  ic.className='ti ti-refresh';
}
function renderTable(data){
  const el=document.getElementById('results');
  if(!data||!data.length){
    el.innerHTML='<div class="empty"><i class="ti ti-mood-empty" style="font-size:28px;display:block;margin-bottom:8px"></i>Tsy misy opportunité izao<br><span style="font-size:11px">Avereno 8h–12h na 20h–22h</span></div>';
    return;
  }
  el.innerHTML=data.map((r,i)=>`
    <div class="row ${simMode?'sim-row':'hot'}">
      <div class="rt">
        <div>
          <span class="rx">${r.route}</span>
          <div class="rdb ${r.exchange==='MEXC'?'mexc':'bnb'}">${r.exchange} · brut ${r.profitBrut.toFixed(3)}% − ${r.frais}% = net ${r.profitNet.toFixed(3)}%${simMode?' · SIM':''}</div>
        </div>
        <span class="pp">+${r.profitNet.toFixed(3)}%</span>
        <span class="gv">+${r.gain.toFixed(3)}<br><span style="font-size:9px;color:#555">NET</span></span>
        <button class="btn-go ${simMode?'sim':''}" onclick="showDetail(${i})">${simMode?'Sim':'▶'}</button>
      </div>
    </div>`).join('');
}
function executeAuto(r,amount){
  if(simMode){
    const g=parseFloat((r.profitNet/100*amount).toFixed(4));
    history.sim.trades.unshift({time:new Date().toLocaleTimeString(),route:r.route,exchange:r.exchange,profitBrut:r.profitBrut,frais:r.frais,profit:r.profitNet,gain:g,amount,mode:'AUTO-SIM'});
    history.sim.profit=parseFloat((history.sim.profit+g).toFixed(4));
    history.sim.count++;
    document.getElementById('sim-total').textContent=history.sim.profit.toFixed(3)+' USDT NET';
    saveState();
  }
}
function showDetail(i){
  const r=scanData[i];
  document.getElementById('mc').innerHTML=`
    <div class="mt" style="color:${simMode?'#38bdf8':'#4ade80'}"><i class="ti ti-arrows-exchange"></i> ${simMode?'Simulation':'Exécution'} — ${r.exchange}</div>
    <div class="mr"><span>Route</span><span class="mm">${r.route}</span></div>
    <div class="mr"><span>Profit brut</span><span class="mv">+${r.profitBrut.toFixed(4)}%</span></div>
    <div class="mr"><span>Frais (${r.fee}%×3)</span><span class="mv" style="color:#f87171">−${r.frais}%</span></div>
    <div class="mr"><span>Profit NET</span><span class="mg">+${r.profitNet.toFixed(4)}%</span></div>
    <div class="mr"><span>Gain NET</span><span class="mg">+${r.gain} USDT</span></div>
    <div class="mr"><span>Capital</span><span class="mv">${r.capital} USDT</span></div>
    <div style="margin-top:10px;font-size:12px;color:#666;margin-bottom:6px">Étapes:</div>
    <div>
      <div class="mstep"><span class="mnum">1</span><div class="mtxt">Mividy <strong>${r.route.split('→')[1]}</strong> avec USDT</div></div>
      <div class="mstep"><span class="mnum">2</span><div class="mtxt">Échange <strong>${r.route.split('→')[1]}</strong> → <strong>${r.route.split('→')[2]}</strong></div></div>
      <div class="mstep"><span class="mnum">3</span><div class="mtxt">Mivarotra → récupérer <strong>USDT</strong> → <span style="color:#4ade80">+${r.gain} USDT NET</span></div></div>
    </div>
    ${simMode?'<div class="simbox"><i class="ti ti-flask"></i> Simulation — aucun ordre réel</div>':'<div class="ibox"><i class="ti ti-bulb"></i> Bot Termux execute trades 3 en ~1 sec!</div>'}
    <div class="mbtns">
      <button class="mbc" onclick="closeM()">Annuler</button>
      <button class="mbg ${simMode?'sim':''}" onclick="closeM();executeTrade(${i})">
        <i class="ti ti-${simMode?'flask':'player-play'}"></i> ${simMode?'Simuler':'Exécuter'}
      </button>
    </div>`;
  openM();
}
function executeTrade(i){
  const r=scanData[i];
  const amount=parseFloat(document.getElementById('capital-in').value)||350;
  if(simMode){
    const g=parseFloat((r.profitNet/100*amount).toFixed(4));
    history.sim.trades.unshift({time:new Date().toLocaleTimeString(),route:r.route,exchange:r.exchange,profitBrut:r.profitBrut,frais:r.frais,profit:r.profitNet,gain:g,amount,mode:'SIM'});
    history.sim.profit=parseFloat((history.sim.profit+g).toFixed(4));
    history.sim.count++;
    document.getElementById('sim-total').textContent=history.sim.profit.toFixed(3)+' USDT NET';
    saveState();
    document.getElementById('mc').innerHTML=`
      <div class="mt" style="color:#38bdf8"><i class="ti ti-flask"></i> Simulation OK</div>
      <div class="mr"><span>Profit brut</span><span class="mv">+${r.profitBrut.toFixed(4)}%</span></div>
      <div class="mr"><span>Frais</span><span class="mv" style="color:#f87171">−${r.frais}%</span></div>
      <div class="mr"><span>Profit NET</span><span class="mg">+${r.profitNet.toFixed(4)}%</span></div>
      <div class="mr"><span>Gain NET simulé</span><span class="mg">+${g} USDT</span></div>
      <div class="simbox"><i class="ti ti-info-circle"></i> Simulation — aucun ordre réel. Activez Mode Réel pour trader.</div>
      <div class="mbtns"><button class="mbc" onclick="closeM()">Fermer</button></div>`;
    openM();
    return;
  }
  fetch('http://localhost:'+BOT_PORT+'/health').then(res=>res.json()).then(h=>{
    if(!h.binance){
      document.getElementById('mc').innerHTML=`
        <div class="mt" style="color:#f87171"><i class="ti ti-x"></i> Bot tsy configured</div>
        <div class="wbox">Binance API tsy configured. Jereo Termux.</div>
        <div class="mbtns"><button class="mbc" onclick="closeM()">Fermer</button></div>`;
      openM();return;
    }
    document.getElementById('mc').innerHTML=`
      <div class="mt" style="color:#f59e0b"><i class="ti ti-alert-triangle"></i> Confirmer Trade Réel</div>
      <div class="mr"><span>Route</span><span class="mm">${r.route}</span></div>
      <div class="mr"><span>Profit NET</span><span class="mg">+${r.profitNet.toFixed(4)}%</span></div>
      <div class="mr"><span>Gain NET estimé</span><span class="mg">+${parseFloat((r.profitNet/100*amount).toFixed(4))} USDT</span></div>
      <div class="mr"><span>Capital</span><span class="mv">${amount} USDT</span></div>
      <div class="wbox"><i class="ti ti-alert-triangle"></i> Trade réel — vola marina! Tsy azo averina.</div>
      <div class="mbtns">
        <button class="mbc" onclick="closeM()">Annuler</button>
        <button class="mbg" onclick="doReal(${i},${amount})"><i class="ti ti-player-play"></i> Confirmer</button>
      </div>`;
    openM();
  }).catch(()=>{
    document.getElementById('mc').innerHTML=`
      <div class="mt" style="color:#f87171"><i class="ti ti-wifi-off"></i> Bot tsy miasa</div>
      <div class="wbox">Termux bot tsy hita @ port ${BOT_PORT}. Jereo Termux.</div>
      <div class="mbtns"><button class="mbc" onclick="closeM()">Fermer</button></div>`;
    openM();
  });
}
function doReal(i,amount){
  const r=scanData[i];
  document.getElementById('mc').innerHTML=`
    <div class="mt" style="color:#f59e0b"><i class="ti ti-loader spin"></i> Execution...</div>
    <div style="text-align:center;padding:20px;color:#aaa">Bot manao trades 3...<br><span style="font-size:11px">~1 sec</span></div>`;
  fetch('http://localhost:'+BOT_PORT+'/execute',{
    method:'POST',headers:{'Content-Type':'application/json'},
    body:JSON.stringify({route:r.route,amount,a:r.a,b:r.b})
  }).then(res=>res.json()).then(result=>{
    const g=parseFloat((r.profitNet/100*amount).toFixed(4));
    if(result.success){history.real.success++;history.real.profit=parseFloat((history.real.profit+g).toFixed(4));history.real.trades.unshift({time:new Date().toLocaleTimeString(),route:r.route,exchange:r.exchange,profit:r.profitNet,gain:g,amount,mode:'RÉEL',status:'success',ms:result.total_ms});}
    else{history.real.failed++;history.real.trades.unshift({time:new Date().toLocaleTimeString(),route:r.route,exchange:r.exchange,profit:r.profitNet,gain:0,amount,mode:'RÉEL',status:'failed'});}
    saveState();
    document.getElementById('mc').innerHTML=`
      <div class="mt" style="color:${result.success?'#4ade80':'#f87171'}">${result.success?'✅ Réussi!':'❌ Échoué'}</div>
      <div class="mr"><span>Route</span><span class="mm">${r.route}</span></div>
      <div class="mr"><span>Durée</span><span class="mv">${result.total_ms}ms</span></div>
      ${result.success?`<div class="mr"><span>Gain NET</span><span class="mg">+${g} USDT</span></div>`:''}
      <div>${(result.steps||[]).map(s=>`<div style="font-size:12px;padding:5px 0;border-bottom:.5px solid #222;color:${s.ok?'#4ade80':'#f87171'}">${s.ok?'✅':'❌'} ${s.label}</div>`).join('')}</div>
      <div class="mbtns"><button class="mbc" onclick="closeM()">Fermer</button></div>`;
  }).catch(()=>{
    document.getElementById('mc').innerHTML=`
      <div class="mt" style="color:#f87171"><i class="ti ti-wifi-off"></i> Erreur bot</div>
      <div class="wbox">Bot tsy miandry @ port ${BOT_PORT}.</div>
      <div class="mbtns"><button class="mbc" onclick="closeM()">Fermer</button></div>`;
  });
}
function updateDash(){
  document.getElementById('d-sim-profit').textContent=history.sim.profit.toFixed(4)+' USDT NET';
  document.getElementById('d-sim-trades').textContent=history.sim.count;
  document.getElementById('d-real-profit').textContent=history.real.profit.toFixed(4)+' USDT NET';
  document.getElementById('d-real-success').textContent=history.real.success;
  document.getElementById('d-real-failed').textContent=history.real.failed;
  const t=history.real.success+history.real.failed;
  document.getElementById('d-rate').textContent=t>0?Math.round(history.real.success/t*100)+'%':'—';
  const all=[...history.sim.trades,...history.real.trades];
  if(all.length)document.getElementById('d-best').textContent='+'+Math.max(...all.map(x=>x.profit)).toFixed(3)+'%';
  const hl=document.getElementById('hist-list');
  if(!all.length){hl.innerHTML='<div class="empty" style="padding:1rem">Aucun trade</div>';return;}
  hl.innerHTML=all.slice(0,30).map(t=>`
    <div class="hist-item">
      <div class="hist-left">
        <div class="hist-route">${t.route}</div>
        <div class="hist-meta">${t.time} · ${t.exchange} · ${t.mode}</div>
      </div>
      <div class="hist-right">
        <div class="hist-profit ${t.gain>0?'g':'r'}">+${parseFloat(t.gain).toFixed(4)} USDT</div>
        <div style="font-size:10px;color:#666">+${t.profit.toFixed(3)}% NET</div>
      </div>
    </div>`).join('');
}
function saveTelegram(){cfg.telegram.token=document.getElementById('tg-token').value;cfg.telegram.chatid=document.getElementById('tg-chatid').value;saveState();alert('Telegram sauvegardé!');}
function saveExchange(ex){
  const k=document.getElementById(ex+'-key').value,s=document.getElementById(ex+'-secret').value;
  if(k)cfg.exchanges[ex].key=k;if(s)cfg.exchanges[ex].secret=s;
  saveState();updateBadges();alert(ex.toUpperCase()+' sauvegardé!');
}
function updateBadges(){
  ['binance','mexc'].forEach(ex=>{
    const el=document.getElementById(ex+'-status');
    if(el){const ok=!!cfg.exchanges[ex]?.key;el.className='set-status '+(ok?'ok':'no');el.textContent=ok?'✅ Configuré':'Non configuré';}
  });
}
function openM(){document.getElementById('ov').className='ov show';}
function closeM(){document.getElementById('ov').className='ov';}
function bgClose(e){if(e.target===document.getElementById('ov'))closeM();}
</script>
</body>
</html>
