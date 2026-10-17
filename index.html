<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1, viewport-fit=cover">
<title>Simulador de Margem</title>
<style>
:root{
  box-sizing:border-box;
  padding-top:env(safe-area-inset-top,0px);
  padding-bottom:env(safe-area-inset-bottom,0px);
  --bg:#f4f6f9;--card:#fff;--text:#1c2430;--muted:#64707f;--border:#d9dfe7;
  --accent:#1f5eff;--good:#0f8a4b;--good-bg:#e3f6ec;--bad:#c62828;--bad-bg:#fde8e8;
}
@media (prefers-color-scheme:dark){
  :root:not([data-theme="light"]){
    color-scheme:dark;
    --bg:#12161c;--card:#1b212a;--text:#e8edf3;--muted:#98a3b3;--border:#2d3643;
    --accent:#6b93ff;--good:#4cd48a;--good-bg:#123424;--bad:#ff7b7b;--bad-bg:#3a1a1a;
  }
}
:root[data-theme="dark"]{
  color-scheme:dark;
  --bg:#12161c;--card:#1b212a;--text:#e8edf3;--muted:#98a3b3;--border:#2d3643;
  --accent:#6b93ff;--good:#4cd48a;--good-bg:#123424;--bad:#ff7b7b;--bad-bg:#3a1a1a;
}
*{box-sizing:border-box}
html{scroll-padding-top:env(safe-area-inset-top,0px)}
body{margin:0;background:var(--bg);color:var(--text);font-family:system-ui,-apple-system,"Segoe UI",Roboto,Arial,sans-serif;line-height:1.4}
.wrap{max-width:640px;margin:0 auto;padding:20px 16px 40px}
h1{font-size:1.4rem;margin:0 0 4px}
.sub{color:var(--muted);margin:0 0 18px;font-size:.92rem}
.card{background:var(--card);border:1px solid var(--border);border-radius:14px;padding:16px;margin-bottom:16px}
.card h2{font-size:1rem;margin:0 0 12px}
.grid{display:grid;grid-template-columns:1fr 1fr;gap:12px}
.full{grid-column:1/-1}
label{display:block;font-size:.8rem;color:var(--muted);margin-bottom:4px}
.field{position:relative}
.field span{position:absolute;left:12px;top:50%;transform:translateY(-50%);color:var(--muted);font-size:.95rem;pointer-events:none}
.field.pct span{left:auto;right:12px}
input{width:100%;padding:12px 12px 12px 38px;font-size:1.05rem;border:1px solid var(--border);border-radius:10px;background:var(--bg);color:var(--text)}
.field.pct input{padding:12px 34px 12px 12px}
input:focus{outline:2px solid var(--accent);border-color:transparent}
.result{border-radius:12px;padding:16px;text-align:center;margin-bottom:12px}
.result.good{background:var(--good-bg);color:var(--good)}
.result.bad{background:var(--bad-bg);color:var(--bad)}
.result.neutral{background:var(--bg);color:var(--muted)}
.result .big{font-size:2.2rem;font-weight:700;line-height:1.1}
.result .lbl{font-size:.85rem;opacity:.9}
.result .msg{margin-top:6px;font-size:.92rem;font-weight:600}
.rows div{display:flex;justify-content:space-between;gap:12px;padding:9px 0;border-bottom:1px solid var(--border);font-size:.95rem}
.rows div:last-child{border-bottom:0}
.rows b{font-variant-numeric:tabular-nums;text-align:right}
.hint{font-size:.85rem;color:var(--muted);margin-top:10px}
button{margin-top:4px;padding:10px 14px;border-radius:10px;border:1px solid var(--border);background:transparent;color:var(--muted);font-size:.85rem;cursor:pointer}
</style>
</head>
<body>
<div class="wrap">
  <h1>📊 Simulador de Margem</h1>
  <p class="sub">Veja como um novo pedido impacta a margem final do mês.</p>

  <div class="card">
    <h2>1. Situação atual</h2>
    <div class="grid">
      <div class="full pct field-wrap">
        <label for="meta">Meta de margem</label>
        <div class="field pct"><input id="meta" inputmode="decimal" value="2"><span>%</span></div>
      </div>
      <div>
        <label for="v1">Venda atual</label>
        <div class="field"><input id="v1" inputmode="decimal" placeholder="0,00"><span>R$</span></div>
      </div>
      <div>
        <label for="m1">Margem atual</label>
        <div class="field pct"><input id="m1" inputmode="decimal" placeholder="0,00"><span>%</span></div>
      </div>
    </div>
  </div>

  <div class="card">
    <h2>2. Simular pedido</h2>
    <div class="grid">
      <div>
        <label for="v2">Valor do pedido</label>
        <div class="field"><input id="v2" inputmode="decimal" placeholder="0,00"><span>R$</span></div>
      </div>
      <div>
        <label for="m2">Margem do pedido</label>
        <div class="field pct"><input id="m2" inputmode="decimal" placeholder="0,00"><span>%</span></div>
      </div>
    </div>
  </div>

  <div class="card">
    <h2>3. Resultado se fechar o pedido</h2>
    <div id="res" class="result neutral">
      <div class="lbl">Margem final</div>
      <div class="big">—</div>
      <div class="msg">Preencha os campos acima</div>
    </div>
    <div class="rows">
      <div><span>Venda total</span><b id="vt">—</b></div>
      <div><span>Margem atual</span><b id="ma">—</b></div>
      <div><span>Variação da margem</span><b id="var">—</b></div>
      <div><span>Lucro (margem em R$)</span><b id="lucro">—</b></div>
      <div><span>Margem mínima do pedido p/ bater a meta</span><b id="min">—</b></div>
    </div>
    <p class="hint">A margem final é a média ponderada pelo valor: (margem R$ atual + margem R$ do pedido) ÷ venda total.</p>
    <button id="limpar">Limpar pedido</button>
  </div>
</div>

<script>
const $ = id => document.getElementById(id);
const num = id => {
  let s = $(id).value.trim().replace(/\s/g,'');
  if (!s) return NaN;
  if (s.includes(',')) s = s.replace(/\./g,'').replace(',','.');
  return parseFloat(s);
};
const brl = n => n.toLocaleString('pt-BR',{style:'currency',currency:'BRL'});
const pct = n => n.toLocaleString('pt-BR',{minimumFractionDigits:2,maximumFractionDigits:2}) + '%';
const pp  = n => (n>0?'+':'') + n.toLocaleString('pt-BR',{minimumFractionDigits:2,maximumFractionDigits:2}) + ' p.p.';

function calc(){
  const meta=num('meta'), v1=num('v1'), m1=num('m1'), v2=num('v2'), m2=num('m2');
  const res=$('res');
  const ok = [meta,v1,m1,v2,m2].every(x=>!isNaN(x)) && (v1+v2)>0;
  if(!ok){
    res.className='result neutral';
    res.innerHTML='<div class="lbl">Margem final</div><div class="big">—</div><div class="msg">Preencha os campos acima</div>';
    ['vt','ma','var','lucro','min'].forEach(i=>$(i).textContent='—');
    return;
  }
  const l1=v1*m1/100, l2=v2*m2/100, vt=v1+v2, lt=l1+l2;
  const mf=lt/vt*100;
  const diff=mf-meta;
  const good=mf>=meta;
  res.className='result '+(good?'good':'bad');
  res.innerHTML='<div class="lbl">Margem final</div><div class="big">'+pct(mf)+'</div>'+
    '<div class="msg">'+(good?'✅ Acima da meta ('+pp(diff)+')':'⚠️ Abaixo da meta ('+pp(diff)+')')+'</div>';
  $('vt').textContent=brl(vt);
  $('ma').textContent=pct(m1);
  $('var').textContent=pp(mf-m1);
  $('lucro').textContent=brl(lt);
  if(v2>0){
    const mn=(meta/100*vt-l1)/v2*100;
    $('min').textContent=pct(mn);
  } else $('min').textContent='—';
}
['meta','v1','m1','v2','m2'].forEach(i=>$(i).addEventListener('input',calc));
$('limpar').addEventListener('click',()=>{$('v2').value='';$('m2').value='';calc();$('v2').focus();});
calc();
</script>
</body>
</html>
