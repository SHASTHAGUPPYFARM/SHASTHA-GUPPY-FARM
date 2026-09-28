[index-2.html](https://github.com/user-attachments/files/32739161/index-2.html)
[index.html](https://github.com/user-attachments/files/32738961/index.html)
<!DOCTYPE html>
<html lang="en">
<head><!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1, viewport-fit=cover">
<title>Shastha Guppy Farm</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Baloo+2:wght@500;600;700&family=Karla:wght@400;500;700&display=swap" rel="stylesheet">
<style>
  :root{
    --ink:#F4E7C9;         /* warm parchment text on dark */
    --paper:#0B0906;       /* near-black, matches logo background */
    --panel:#161209;       /* slightly lifted panel over the black */
    --violet:#C79A3D;      /* muted gold, used for secondary accents */
    --magenta:#E3A83B;     /* warm amber accent */
    --gold:#D4AF37;        /* classic metallic gold, the hero accent */
    --teal:#8C6A2F;        /* deep bronze, used sparingly */
    --line:#2B2313;        /* dark bronze hairline */
    --radius:14px;
  }
  *{box-sizing:border-box;}
  html{scroll-behavior:smooth;}
  body{
    margin:0; background:var(--paper); color:var(--ink);
    font-family:'Karla',sans-serif; line-height:1.55;
    padding-bottom:env(safe-area-inset-bottom,0px);
  }
  h1,h2,h3,.brand,.tagline{font-family:'Baloo 2',sans-serif;}

  header{
    position:sticky; top:0; z-index:30; background:var(--paper);
    border-bottom:2px solid var(--line);
    padding:calc(env(safe-area-inset-top,0px) + 12px) 20px 12px;
    display:flex; align-items:center; justify-content:space-between; gap:12px;
  }
  .brand{display:flex; align-items:center; gap:10px; font-size:1.2rem; font-weight:700; color:var(--ink);}
  .brand .fin{
    width:40px;height:40px;border-radius:50%;
    object-fit:cover; flex-shrink:0; background:#000;
  }
  .cart-btn{
    background:var(--ink); color:var(--paper); border:none; border-radius:999px;
    padding:10px 18px; font-family:'Karla'; font-weight:700; font-size:.88rem;
    cursor:pointer; display:flex; align-items:center; gap:8px;
  }
  .cart-count{background:var(--gold); color:var(--ink); border-radius:999px; padding:1px 9px; font-size:.78rem; font-weight:700;}

  .hero{
    padding:52px 20px 40px; max-width:920px; margin:0 auto;
    display:flex; flex-direction:column; gap:14px;
  }
  .tagline{
    font-size:.85rem; letter-spacing:.02em; color:var(--teal); font-weight:600;
    text-transform:lowercase;
  }
  .hero h1{
    font-size:clamp(2.1rem,6vw,3.2rem); margin:0; font-weight:700; line-height:1.08;
    max-width:16ch;
  }
  .hero h1 .accent{color:var(--magenta);}
  .hero p{max-width:52ch; font-size:1.05rem; margin:2px 0 0; color:#D8C79A;}
  .tail-row{display:flex; gap:10px; margin-top:6px; font-size:1.6rem;}

  main{max-width:1000px; margin:0 auto; padding:0 20px 90px;}
  .tabs{display:flex; gap:10px; overflow-x:auto; padding:4px 0 26px;}
  .tab{
    border:2px solid var(--ink); background:transparent; color:var(--ink);
    padding:9px 18px; border-radius:999px; font-size:.9rem; font-weight:700;
    cursor:pointer; white-space:nowrap; font-family:'Karla';
  }
  .tab[aria-selected="true"]{background:var(--ink); color:var(--paper);}

  .grid{display:grid; grid-template-columns:repeat(auto-fill,minmax(220px,1fr)); gap:20px;}
  .card{
    background:var(--panel); border-radius:var(--radius); overflow:hidden;
    display:flex; flex-direction:column;
    box-shadow:0 1px 0 var(--line);
    border:1px solid var(--line);
  }
  .media{
    width:100%; aspect-ratio:4/3; background:linear-gradient(160deg,#241C0D,#171207);
    display:flex; align-items:center; justify-content:center; font-size:1.1rem; letter-spacing:.08em; color:#7A6636; font-weight:700;
    position:relative; overflow:hidden;
  }
  .media img, .media video{width:100%; height:100%; object-fit:cover;}
  .media .play-badge{
    position:absolute; bottom:8px; right:8px; background:rgba(27,16,53,.75); color:#fff;
    font-size:.7rem; padding:3px 8px; border-radius:999px; font-weight:700;
  }
  .card-body{padding:14px 14px 16px; display:flex; flex-direction:column; gap:6px; flex:1;}
  .card-body .cat{font-size:.72rem; font-weight:700; color:var(--violet); text-transform:lowercase;}
  .card-body h3{margin:0; font-size:1.05rem; font-weight:600; color:var(--ink);}
  .card-body .price{font-weight:700; margin-top:auto; font-size:1.05rem;}
  .qty-row{display:flex; align-items:center; gap:10px; margin-top:4px;}
  .qty-row button{
    width:30px; height:30px; border-radius:8px; border:2px solid var(--ink);
    background:var(--paper); color:var(--ink); font-size:1rem; cursor:pointer; font-weight:700;
  }
  .add-btn{
    background:var(--violet); color:#fff; border:none; border-radius:8px;
    padding:10px; font-weight:700; cursor:pointer; font-family:'Karla'; font-size:.92rem;
    margin-top:4px;
  }
  .add-btn:active{background:var(--magenta);}

  .overlay{position:fixed; inset:0; background:rgba(27,16,53,.45); z-index:40; display:none;}
  .overlay.open{display:block;}
  .drawer{
    position:fixed; top:0; right:0; bottom:0; width:min(400px,92vw);
    background:var(--panel); z-index:41; transform:translateX(105%);
    transition:transform .25s ease; display:flex; flex-direction:column;
    padding-top:env(safe-area-inset-top,0px); padding-bottom:env(safe-area-inset-bottom,0px);
  }
  .drawer.open{transform:translateX(0);}
  .drawer-head{padding:18px 20px; border-bottom:2px solid var(--line); display:flex; justify-content:space-between; align-items:center;}
  .drawer-head h2{margin:0; font-size:1.25rem;}
  .drawer-head button{background:none; border:none; font-size:1.3rem; cursor:pointer; color:var(--ink);}
  .drawer-items{flex:1; overflow-y:auto; padding:14px 20px;}
  .line{display:flex; justify-content:space-between; align-items:center; gap:8px; padding:12px 0; border-bottom:1px solid var(--line);}
  .line-name{font-size:.92rem; font-weight:600;}
  .line-qty{display:flex; align-items:center; gap:6px;}
  .line-qty button{width:26px;height:26px;border-radius:6px;border:2px solid var(--ink);background:var(--paper);cursor:pointer;font-weight:700;}
  .drawer-foot{padding:18px 20px; border-top:2px solid var(--line);}
  .total-row{display:flex; justify-content:space-between; font-weight:700; margin-bottom:14px; font-size:1.1rem;}
  .checkout-btn{
    width:100%; background:#25D366; color:#062A16; border:none; border-radius:10px;
    padding:14px; font-weight:700; font-size:1rem; cursor:pointer; font-family:'Karla';
    display:flex; align-items:center; justify-content:center; gap:8px;
  }
  .empty-note{color:var(--violet); opacity:.85; font-size:.92rem; padding:24px 0; text-align:center;}
  footer{text-align:center; padding:26px 20px 40px; font-size:.82rem; opacity:.6;}

  .add-btn[disabled]{background:#3a3220;color:#8a7a52;cursor:not-allowed;}
  #adminPanel{position:fixed;inset:0;z-index:60;background:var(--paper);overflow-y:auto;padding:calc(env(safe-area-inset-top,0px) + 16px) 16px 60px;}
  #adminPanel[hidden]{display:none;}
  .ad-head{display:flex;justify-content:space-between;align-items:center;gap:8px;flex-wrap:wrap;}
  .ad-head h2{margin:0;}
  .ad-save,.ad-x,.ad-add{border:none;border-radius:8px;padding:10px 14px;font-weight:700;cursor:pointer;font-family:'Karla';}
  .ad-save{background:var(--gold);color:#0B0906;} .ad-x{background:var(--line);color:var(--ink);}
  .ad-add{background:var(--panel);color:var(--gold);border:2px dashed var(--gold);width:100%;margin-top:14px;}
  .ad-note{font-size:.85rem;opacity:.75;}
  .ad-wa{display:block;font-size:.85rem;margin:8px 0 14px;}
  .ad-wa input,.ad-row input,.ad-row select{background:var(--panel);color:var(--ink);border:1px solid var(--line);border-radius:6px;padding:8px;font-family:'Karla';font-size:.9rem;width:100%;}
  .ad-row{display:grid;grid-template-columns:2fr 1fr 1fr;gap:6px;background:var(--panel);border:1px solid var(--line);border-radius:10px;padding:10px;margin-bottom:8px;}
  .ad-row .full{grid-column:1/-1;display:flex;justify-content:space-between;align-items:center;font-size:.85rem;}
  .ad-row .del{background:none;border:none;color:#e0705a;font-weight:700;cursor:pointer;}

  /* ---------- product detail popup ---------- */
  .card{cursor:pointer;}
  .detail-overlay{
    position:fixed; inset:0; background:rgba(0,0,0,.72); z-index:60;
    display:flex; align-items:flex-end; justify-content:center;
    opacity:0; pointer-events:none; transition:opacity .28s ease;
  }
  .detail-overlay.open{opacity:1; pointer-events:auto;}
  @media (min-width:720px){ .detail-overlay{align-items:center;} }
  .detail-card{
    background:var(--panel); border:2px solid var(--line); border-radius:20px 20px 0 0;
    width:100%; max-width:560px; max-height:88vh; overflow-y:auto;
    padding:0 0 26px; position:relative;
    transform:translateY(28px) scale(.97); opacity:0;
    transition:transform .32s cubic-bezier(.2,.9,.25,1.1), opacity .28s ease;
  }
  .detail-overlay.open .detail-card{transform:translateY(0) scale(1); opacity:1;}
  @media (min-width:720px){ .detail-card{border-radius:20px;} }
  .detail-close{
    position:absolute; top:14px; right:14px; z-index:2;
    background:rgba(11,9,6,.75); color:var(--ink); border:1px solid var(--line);
    border-radius:999px; width:36px; height:36px; font-size:1.1rem; cursor:pointer;
  }
  .detail-media{width:100%; aspect-ratio:1/1; background:#000; overflow:hidden; border-radius:20px 20px 0 0;}
  .detail-media img, .detail-media video{width:100%; height:100%; object-fit:cover; display:block;
    animation:detailZoom .5s ease;}
  @keyframes detailZoom{from{transform:scale(1.08); opacity:.4;} to{transform:scale(1); opacity:1;}}
  .detail-media .media{height:100%; border-radius:0;}
  .detail-body{padding:20px 22px 4px;}
  .detail-body .cat{display:block; margin-bottom:4px;}
  .detail-body h2{margin:2px 0 8px; font-size:1.5rem;}
  .detail-body .price{font-size:1.2rem; font-weight:700; color:var(--gold); display:block; margin-bottom:16px;}
  .detail-actions{display:flex; gap:10px;}
</style>
</head>
<body>

<header>
  <div class="brand"><img class="fin" src="data:image/jpeg;base64,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" alt="Shastha Guppy Farm logo">Shastha Guppy Farm</div>
  <button class="cart-btn" id="editBtn" hidden style="background:var(--gold);color:#0B0906;margin-left:auto">Edit shop</button>
  <button class="cart-btn" id="cartOpenBtn">Order <span class="cart-count" id="cartCount">0</span></button>
</header>

<div class="hero">
  <div class="tagline">fifty plus guppy varieties, bred and raised here</div>
  <h1>Colour that <span class="accent">swims</span></h1>
  <p>Live guppies in every colour and tail shape we raise, plus the food that keeps them thriving. Pick your favourites and send the order straight to us on WhatsApp.</p>
</div>

<main>
  <div class="tabs" id="tabs"></div>
  <div class="grid" id="grid"></div>
</main>

<footer>Shastha Guppy Farm &mdash; orders confirmed over WhatsApp.</footer>


<section id="adminPanel" hidden>
  <div class="ad-head"><h2>Edit shop</h2><div><button id="adSave" class="ad-save">Save changes</button> <button id="adClose" class="ad-x">Close</button></div></div>
  <p class="ad-note">Only you see this screen. Changes go live for all customers after you press Save.</p>
  <label class="ad-wa">WhatsApp number (country code first, no + or spaces)<input id="adWa" inputmode="numeric"></label>
  <div id="adminList"></div>
  <button id="adAdd" class="ad-add">+ Add new item</button>
</section>
<div class="overlay" id="overlay"></div>
<aside class="drawer" id="drawer">
  <div class="drawer-head"><h2>Your order</h2><button id="drawerClose" aria-label="Close">X</button></div>
  <div class="drawer-items" id="drawerItems"></div>
  <div class="drawer-foot">
    <div class="total-row"><span>Total</span><span id="totalAmt">Rs. 0</span></div>
    <button class="checkout-btn" id="checkoutBtn">Send order on WhatsApp</button>
  </div>
</aside>

<div class="detail-overlay" id="detailOverlay">
  <div class="detail-card" id="detailCard">
    <button class="detail-close" id="detailClose" aria-label="Close">X</button>
    <div class="detail-media" id="detailMedia"></div>
    <div class="detail-body">
      <span class="cat" id="detailCat"></span>
      <h2 id="detailName"></h2>
      <span class="price" id="detailPrice"></span>
      <div class="detail-actions" id="detailActions"></div>
    </div>
  </div>
</div>

<script type="application/json" id="state">{"whatsapp": "918088820799", "products": [{"id": "g1", "name": "Albino Platinum White Guppy (pair)", "cat": "Guppies", "price": 300, "inStock": true}, {"id": "g2", "name": "Albino Redlace Guppy (pair)", "cat": "Guppies", "price": 250, "inStock": true}, {"id": "g3", "name": "Albino Silvarado Red Ear Guppy (pair)", "cat": "Guppies", "price": 240, "inStock": true}, {"id": "g4", "name": "AFR Guppy (pair)", "cat": "Guppies", "price": 230, "inStock": true}, {"id": "g5", "name": "Masco Blue Guppy (pair)", "cat": "Guppies", "price": 220, "inStock": true}, {"id": "g6", "name": "Black Guppy (pair)", "cat": "Guppies", "price": 180, "inStock": true}, {"id": "g7", "name": "Platinum White Dumbo Guppy (pair)", "cat": "Guppies", "price": 450, "inStock": true}, {"id": "g8", "name": "Silvarado Mosaic Guppy (pair)", "cat": "Guppies", "price": 180, "inStock": true}, {"id": "g9", "name": "White Texido Guppy (pair)", "cat": "Guppies", "price": 180, "inStock": true}, {"id": "g10", "name": "Japanese Blue Guppy (pair)", "cat": "Guppies", "price": 250, "inStock": true}, {"id": "g11", "name": "Platinum Big Ear Guppy (pair)", "cat": "Guppies", "price": 250, "inStock": true}, {"id": "g12", "name": "Chilli Mosaic Dumbo Guppy (pair)", "cat": "Guppies", "price": 205, "inStock": true}, {"id": "g13", "name": "Gold Guppy (pair)", "cat": "Guppies", "price": 250, "inStock": true}, {"id": "g14", "name": "Gold Ribbon Guppy (pair)", "cat": "Guppies", "price": 500, "inStock": true}, {"id": "g15", "name": "Red Granite Guppy (pair)", "cat": "Guppies", "price": 215, "inStock": true}, {"id": "g16", "name": "Blue Panda Guppy (pair)", "cat": "Guppies", "price": 230, "inStock": true}, {"id": "g17", "name": "Purple Burry Guppy (pair)", "cat": "Guppies", "price": 250, "inStock": true}, {"id": "g18", "name": "Tiger HM Guppy (pair)", "cat": "Guppies", "price": 180, "inStock": true}, {"id": "g19", "name": "Yellow Pingu Guppy (pair)", "cat": "Guppies", "price": 215, "inStock": true}, {"id": "g20", "name": "Lazuli Blue Guppy (pair)", "cat": "Guppies", "price": 190, "inStock": true}, {"id": "g21", "name": "Black Bar Endler Guppy (pair)", "cat": "Guppies", "price": 200, "inStock": true}, {"id": "g22", "name": "Red Scarlet Endler Guppy (pair)", "cat": "Guppies", "price": 200, "inStock": true}, {"id": "g23", "name": "Ivory Purple Guppy (pair)", "cat": "Guppies", "price": 250, "inStock": true}, {"id": "g24", "name": "Red Coral Endler Guppy (pair)", "cat": "Guppies", "price": 250, "inStock": true}, {"id": "g25", "name": "Zee Through Koi Guppy (pair)", "cat": "Guppies", "price": 250, "inStock": true}, {"id": "g26", "name": "Santha Clause SB Guppy (pair)", "cat": "Guppies", "price": 400, "inStock": true}, {"id": "g27", "name": "Wildred Guppy (pair)", "cat": "Guppies", "price": 210, "inStock": true}, {"id": "g28", "name": "Albino Metal Redlace Guppy (pair)", "cat": "Guppies", "price": 230, "inStock": true}, {"id": "g29", "name": "Red Dragon HM Guppy (pair)", "cat": "Guppies", "price": 250, "inStock": true}, {"id": "f1", "name": "Guppy Flake Food 100g", "cat": "Food", "price": 120, "inStock": true}, {"id": "f2", "name": "Live Daphnia Culture", "cat": "Food", "price": 80, "inStock": true}, {"id": "f3", "name": "Baby Guppy Fry Food", "cat": "Food", "price": 100, "inStock": true}]}</script>
<script>
let state = JSON.parse(document.getElementById('state').textContent);
let PRODUCTS = state.products;
const CATS = ['All','Guppies','Food'];
let cart = {}, activeCat = 'All';
const $ = id => document.getElementById(id);
const money = n => '\u20b9' + Number(n).toLocaleString('en-IN');
const esc = s => String(s).replace(/[&<>"']/g, c => ({'&':'&amp;','<':'&lt;','>':'&gt;','"':'&quot;',"'":'&#39;'}[c]));
const find = id => PRODUCTS.find(p => p.id === id);

function renderTabs(){
  $('tabs').innerHTML = '';
  CATS.forEach(c => {
    const b = document.createElement('button');
    b.className = 'tab'; b.textContent = c;
    b.setAttribute('aria-selected', c === activeCat ? 'true' : 'false');
    b.onclick = () => { activeCat = c; renderTabs(); renderGrid(); };
    $('tabs').appendChild(b);
  });
}
function mediaHtml(p){
  if(p.video) return '<div class="media"><video src="'+p.video+'" '+(p.photo?'poster="'+p.photo+'" ':'')+'controls preload="none" playsinline></video></div>';
  if(p.photo) return '<div class="media"><img src="'+p.photo+'" alt="'+esc(p.name)+'" loading="lazy"></div>';
  return '<div class="media">'+(p.cat==='Guppies'?'GUPPY':'FOOD')+'</div>';
}
function renderGrid(){
  const grid = $('grid'); grid.innerHTML = '';
  PRODUCTS.filter(p => activeCat === 'All' || p.cat === activeCat).forEach(p => {
    const q = cart[p.id] || 0;
    const action = !p.inStock ? '<button class="add-btn" disabled>Sold out</button>'
      : q === 0 ? '<button class="add-btn" data-add="'+p.id+'">Add to order</button>'
      : '<div class="qty-row"><button data-dec="'+p.id+'">-</button><span>'+q+'</span><button data-inc="'+p.id+'">+</button></div>';
    const card = document.createElement('div'); card.className = 'card';
    card.innerHTML = mediaHtml(p)+'<div class="card-body"><span class="cat">'+esc(p.cat)+'</span><h3>'+esc(p.name)+'</h3><span class="price">'+money(p.price)+'</span>'+action+'</div>';
    card.addEventListener('click', (ev) => { if(ev.target.closest('button')) return; openDetail(p.id); });
    grid.appendChild(card);
  });
  bind(grid);
}

function openDetail(id){
  const p = find(id); if(!p) return;
  $('detailMedia').innerHTML = mediaHtml(p);
  const vid = $('detailMedia').querySelector('video');
  if(vid){ vid.muted = true; vid.autoplay = true; vid.loop = true; vid.play().catch(()=>{}); }
  $('detailCat').textContent = p.cat;
  $('detailName').textContent = p.name;
  $('detailPrice').textContent = money(p.price);
  const q = cart[p.id] || 0;
  $('detailActions').innerHTML = !p.inStock ? '<button class="add-btn" disabled>Sold out</button>'
    : q === 0 ? '<button class="add-btn" data-add="'+p.id+'">Add to order</button>'
    : '<div class="qty-row"><button data-dec="'+p.id+'">-</button><span>'+q+'</span><button data-inc="'+p.id+'">+</button></div>';
  bind($('detailActions'));
  $('detailOverlay').classList.add('open');
}
function closeDetail(){ $('detailOverlay').classList.remove('open'); }
$('detailClose').onclick = closeDetail;
$('detailOverlay').onclick = (ev) => { if(ev.target === $('detailOverlay')) closeDetail(); };
function bind(root){
  root.querySelectorAll('[data-add]').forEach(b => b.onclick = () => { cart[b.dataset.add] = 1; renderAll(); });
  root.querySelectorAll('[data-inc]').forEach(b => b.onclick = () => { cart[b.dataset.inc]++; renderAll(); });
  root.querySelectorAll('[data-dec]').forEach(b => b.onclick = () => { const id = b.dataset.dec; if(--cart[id] <= 0) delete cart[id]; renderAll(); });
}
const cartTotal = () => Object.entries(cart).reduce((s,[id,q]) => s + (find(id)?.price||0)*q, 0);
const cartCount = () => Object.values(cart).reduce((a,b) => a+b, 0);
function renderDrawer(){
  $('cartCount').textContent = cartCount();
  const w = $('drawerItems'), e = Object.entries(cart).filter(([id]) => find(id));
  w.innerHTML = e.length ? e.map(([id,q]) => { const p = find(id);
    return '<div class="line"><div><div class="line-name">'+esc(p.name)+'</div><div style="font-size:.82rem;opacity:.65">'+money(p.price)+' x '+q+'</div></div><div class="line-qty"><button data-dec="'+id+'">-</button><span>'+q+'</span><button data-inc="'+id+'">+</button></div></div>'; }).join('')
    : '<p class="empty-note">Your order is empty.<br>Add guppies or food from the catalog.</p>';
  bind(w);
  $('totalAmt').textContent = money(cartTotal());
}
function renderAll(){ renderGrid(); renderDrawer(); refreshDetailActions(); }
function refreshDetailActions(){
  if(!$('detailOverlay').classList.contains('open')) return;
  const id = $('detailActions').querySelector('[data-add],[data-inc],[data-dec]');
  if(!id) return;
  const pid = id.dataset.add || id.dataset.inc || id.dataset.dec;
  const p = find(pid); if(!p) return;
  const q = cart[p.id] || 0;
  $('detailActions').innerHTML = !p.inStock ? '<button class="add-btn" disabled>Sold out</button>'
    : q === 0 ? '<button class="add-btn" data-add="'+p.id+'">Add to order</button>'
    : '<div class="qty-row"><button data-dec="'+p.id+'">-</button><span>'+q+'</span><button data-inc="'+p.id+'">+</button></div>';
  bind($('detailActions'));
}
const setDrawer = on => { $('overlay').classList.toggle('open', on); $('drawer').classList.toggle('open', on); };
$('cartOpenBtn').onclick = () => setDrawer(true);
$('drawerClose').onclick = $('overlay').onclick = () => setDrawer(false);

$('checkoutBtn').onclick = () => {
  const e = Object.entries(cart).filter(([id]) => find(id));
  if(!e.length){ alert('Add at least one item to your order first.'); return; }
  let msg = "Hello Shastha Guppy Farm, I'd like to order:\n\n";
  e.forEach(([id,q]) => { const p = find(id); msg += '- '+p.name+' x'+q+' = '+money(p.price*q)+'\n'; });
  msg += '\nTotal: '+money(cartTotal())+'\n\nPlease confirm availability and delivery.';
  window.open('https://wa.me/'+state.whatsapp+'?text='+encodeURIComponent(msg), '_blank');
};

/* ---------- owner-only edit mode ---------- */
let draft;
function buildDoc(s){
  const c = document.documentElement.cloneNode(true);
  ['grid','tabs','drawerItems','adminList','detailMedia','detailActions'].forEach(id => { const e = c.querySelector('#'+id); if(e) e.innerHTML = ''; });
  c.querySelector('#state').textContent = JSON.stringify(s).replace(/</g,'\\u003c');
  c.querySelectorAll('.open').forEach(e => e.classList.remove('open'));
  c.querySelector('#editBtn').setAttribute('hidden','');
  c.querySelector('#adminPanel').setAttribute('hidden','');
  c.querySelector('#cartCount').textContent = '0';
  c.querySelector('#totalAmt').textContent = money(0);
  return '<!DOCTYPE html>\n' + c.outerHTML;
}
function readData(f){ return new Promise((res,rej)=>{ const r=new FileReader(); r.onload=()=>res(r.result); r.onerror=rej; r.readAsDataURL(f); }); }
async function shrink(f){
  const img = new Image(); img.src = await readData(f); await img.decode();
  const s = Math.min(1, 640/img.width), c = document.createElement('canvas');
  c.width = Math.round(img.width*s); c.height = Math.round(img.height*s);
  c.getContext('2d').drawImage(img,0,0,c.width,c.height);
  return c.toDataURL('image/jpeg',0.72);
}
function renderAdmin(){
  $('adminList').innerHTML = draft.products.map((p,i) =>
    '<div class="ad-row"><input data-f="name" data-i="'+i+'" value="'+esc(p.name)+'"><input data-f="price" data-i="'+i+'" inputmode="numeric" value="'+p.price+'"><select data-f="cat" data-i="'+i+'"><option'+(p.cat==='Guppies'?' selected':'')+'>Guppies</option><option'+(p.cat==='Food'?' selected':'')+'>Food</option></select>'
    +'<div class="full"><span>Photo: '+(p.photo?'added <button class="del" data-rmp="'+i+'">remove</button>':'<input type="file" accept="image/*" data-photo="'+i+'" style="width:auto">')+'</span></div>'
    +'<div class="full"><span>Video: '+(p.video?'added <button class="del" data-rmv="'+i+'">remove</button>':'<input type="file" accept="video/*" data-video="'+i+'" style="width:auto">')+'</span></div>'
    +'<div class="full"><label><input type="checkbox" style="width:auto" data-f="inStock" data-i="'+i+'"'+(p.inStock?' checked':'')+'> In stock</label><button class="del" data-del="'+i+'">Delete</button></div></div>').join('');
  const L = $('adminList');
  L.querySelectorAll('[data-f]').forEach(el => el.onchange = () => {
    const p = draft.products[el.dataset.i], f = el.dataset.f;
    p[f] = f==='inStock' ? el.checked : f==='price' ? (Number(el.value)||0) : el.value.trim();
  });
  L.querySelectorAll('[data-photo]').forEach(el => el.onchange = async () => { const f = el.files[0]; if(!f) return; draft.products[el.dataset.photo].photo = await shrink(f); renderAdmin(); });
  L.querySelectorAll('[data-video]').forEach(el => el.onchange = async () => {
    const f = el.files[0]; if(!f) return;
    if(f.size > 2*1048576){ alert('This video is '+(f.size/1048576).toFixed(1)+' MB. Please compress it under 2 MB first.'); el.value=''; return; }
    draft.products[el.dataset.video].video = await readData(f); renderAdmin();
  });
  L.querySelectorAll('[data-rmp]').forEach(b => b.onclick = () => { delete draft.products[b.dataset.rmp].photo; renderAdmin(); });
  L.querySelectorAll('[data-rmv]').forEach(b => b.onclick = () => { delete draft.products[b.dataset.rmv].video; renderAdmin(); });
  L.querySelectorAll('[data-del]').forEach(b => b.onclick = () => { if(confirm('Delete this item?')){ draft.products.splice(b.dataset.del,1); renderAdmin(); } });
}
const OWNER_PASSWORD = 'shastha2026'; // change this to any password you like

function initAdmin(){
  $('editBtn').hidden = false;
  $('editBtn').onclick = () => {
    if(!sessionStorage.getItem('ownerOk')){
      const pw = prompt('Enter shop owner password:');
      if(pw !== OWNER_PASSWORD){ if(pw !== null) alert('Wrong password.'); return; }
      sessionStorage.setItem('ownerOk','1');
    }
    draft = JSON.parse(JSON.stringify(state)); $('adWa').value = draft.whatsapp; renderAdmin(); $('adminPanel').hidden = false;
  };
  $('adClose').onclick = () => { $('adminPanel').hidden = true; };
  $('adAdd').onclick = () => { draft.products.unshift({id:'n'+Date.now(), name:'New guppy (pair)', cat:'Guppies', price:0, inStock:true}); renderAdmin(); };
  $('adSave').onclick = () => {
    draft.whatsapp = $('adWa').value.replace(/\D/g,'') || draft.whatsapp;
    if(JSON.stringify(draft).length > 12e6){ alert('Too much photo/video data for one page (limit about 12 MB). Remove a few videos.'); return; }
    state = draft;
    localStorage.setItem('shasthaState', JSON.stringify(state));
    const blob = new Blob([buildDoc(state)], {type:'text/html'});
    const url = URL.createObjectURL(blob);
    const a = document.createElement('a');
    a.href = url; a.download = 'index.html';
    document.body.appendChild(a); a.click(); a.remove();
    URL.revokeObjectURL(url);
    $('adminPanel').hidden = true;
    renderTabs(); renderAll();
    alert('Saved! A file named index.html was downloaded. Upload it to your GitHub repository (replacing the old one) to publish these changes live. Your changes are also kept in this browser for now.');
  };
}
initAdmin();

(() => {
  try {
    const saved = localStorage.getItem('shasthaState');
    if(saved){ state = JSON.parse(saved); }
  } catch(e){}
})();

renderTabs(); renderAll();
</script>
</body>
</html>

<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1, viewport-fit=cover">
<title>Shastha Guppy Farm</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Baloo+2:wght@500;600;700&family=Karla:wght@400;500;700&display=swap" rel="stylesheet">
<style>
  :root{
    --ink:#F4E7C9;         /* warm parchment text on dark */
    --paper:#0B0906;       /* near-black, matches logo background */
    --panel:#161209;       /* slightly lifted panel over the black */
    --violet:#C79A3D;      /* muted gold, used for secondary accents */
    --magenta:#E3A83B;     /* warm amber accent */
    --gold:#D4AF37;        /* classic metallic gold, the hero accent */
    --teal:#8C6A2F;        /* deep bronze, used sparingly */
    --line:#2B2313;        /* dark bronze hairline */
    --radius:14px;
  }
  *{box-sizing:border-box;}
  html{scroll-behavior:smooth;}
  body{
    margin:0; background:var(--paper); color:var(--ink);
    font-family:'Karla',sans-serif; line-height:1.55;
    padding-bottom:env(safe-area-inset-bottom,0px);
  }
  h1,h2,h3,.brand,.tagline{font-family:'Baloo 2',sans-serif;}

  header{
    position:sticky; top:0; z-index:30; background:var(--paper);
    border-bottom:2px solid var(--line);
    padding:calc(env(safe-area-inset-top,0px) + 12px) 20px 12px;
    display:flex; align-items:center; justify-content:space-between; gap:12px;
  }
  .brand{display:flex; align-items:center; gap:10px; font-size:1.2rem; font-weight:700; color:var(--ink);}
  .brand .fin{
    width:40px;height:40px;border-radius:50%;
    object-fit:cover; flex-shrink:0; background:#000;
  }
  .cart-btn{
    background:var(--ink); color:var(--paper); border:none; border-radius:999px;
    padding:10px 18px; font-family:'Karla'; font-weight:700; font-size:.88rem;
    cursor:pointer; display:flex; align-items:center; gap:8px;
  }
  .cart-count{background:var(--gold); color:var(--ink); border-radius:999px; padding:1px 9px; font-size:.78rem; font-weight:700;}

  .hero{
    padding:52px 20px 40px; max-width:920px; margin:0 auto;
    display:flex; flex-direction:column; gap:14px;
  }
  .tagline{
    font-size:.85rem; letter-spacing:.02em; color:var(--teal); font-weight:600;
    text-transform:lowercase;
  }
  .hero h1{
    font-size:clamp(2.1rem,6vw,3.2rem); margin:0; font-weight:700; line-height:1.08;
    max-width:16ch;
  }
  .hero h1 .accent{color:var(--magenta);}
  .hero p{max-width:52ch; font-size:1.05rem; margin:2px 0 0; color:#D8C79A;}
  .tail-row{display:flex; gap:10px; margin-top:6px; font-size:1.6rem;}

  main{max-width:1000px; margin:0 auto; padding:0 20px 90px;}
  .tabs{display:flex; gap:10px; overflow-x:auto; padding:4px 0 26px;}
  .tab{
    border:2px solid var(--ink); background:transparent; color:var(--ink);
    padding:9px 18px; border-radius:999px; font-size:.9rem; font-weight:700;
    cursor:pointer; white-space:nowrap; font-family:'Karla';
  }
  .tab[aria-selected="true"]{background:var(--ink); color:var(--paper);}

  .grid{display:grid; grid-template-columns:repeat(auto-fill,minmax(220px,1fr)); gap:20px;}
  .card{
    background:var(--panel); border-radius:var(--radius); overflow:hidden;
    display:flex; flex-direction:column;
    box-shadow:0 1px 0 var(--line);
    border:1px solid var(--line);
  }
  .media{
    width:100%; aspect-ratio:4/3; background:linear-gradient(160deg,#241C0D,#171207);
    display:flex; align-items:center; justify-content:center; font-size:1.1rem; letter-spacing:.08em; color:#7A6636; font-weight:700;
    position:relative; overflow:hidden;
  }
  .media img, .media video{width:100%; height:100%; object-fit:cover;}
  .media .play-badge{
    position:absolute; bottom:8px; right:8px; background:rgba(27,16,53,.75); color:#fff;
    font-size:.7rem; padding:3px 8px; border-radius:999px; font-weight:700;
  }
  .card-body{padding:14px 14px 16px; display:flex; flex-direction:column; gap:6px; flex:1;}
  .card-body .cat{font-size:.72rem; font-weight:700; color:var(--violet); text-transform:lowercase;}
  .card-body h3{margin:0; font-size:1.05rem; font-weight:600; color:var(--ink);}
  .card-body .price{font-weight:700; margin-top:auto; font-size:1.05rem;}
  .qty-row{display:flex; align-items:center; gap:10px; margin-top:4px;}
  .qty-row button{
    width:30px; height:30px; border-radius:8px; border:2px solid var(--ink);
    background:var(--paper); color:var(--ink); font-size:1rem; cursor:pointer; font-weight:700;
  }
  .add-btn{
    background:var(--violet); color:#fff; border:none; border-radius:8px;
    padding:10px; font-weight:700; cursor:pointer; font-family:'Karla'; font-size:.92rem;
    margin-top:4px;
  }
  .add-btn:active{background:var(--magenta);}

  .overlay{position:fixed; inset:0; background:rgba(27,16,53,.45); z-index:40; display:none;}
  .overlay.open{display:block;}
  .drawer{
    position:fixed; top:0; right:0; bottom:0; width:min(400px,92vw);
    background:var(--panel); z-index:41; transform:translateX(105%);
    transition:transform .25s ease; display:flex; flex-direction:column;
    padding-top:env(safe-area-inset-top,0px); padding-bottom:env(safe-area-inset-bottom,0px);
  }
  .drawer.open{transform:translateX(0);}
  .drawer-head{padding:18px 20px; border-bottom:2px solid var(--line); display:flex; justify-content:space-between; align-items:center;}
  .drawer-head h2{margin:0; font-size:1.25rem;}
  .drawer-head button{background:none; border:none; font-size:1.3rem; cursor:pointer; color:var(--ink);}
  .drawer-items{flex:1; overflow-y:auto; padding:14px 20px;}
  .line{display:flex; justify-content:space-between; align-items:center; gap:8px; padding:12px 0; border-bottom:1px solid var(--line);}
  .line-name{font-size:.92rem; font-weight:600;}
  .line-qty{display:flex; align-items:center; gap:6px;}
  .line-qty button{width:26px;height:26px;border-radius:6px;border:2px solid var(--ink);background:var(--paper);cursor:pointer;font-weight:700;}
  .drawer-foot{padding:18px 20px; border-top:2px solid var(--line);}
  .total-row{display:flex; justify-content:space-between; font-weight:700; margin-bottom:14px; font-size:1.1rem;}
  .checkout-btn{
    width:100%; background:#25D366; color:#062A16; border:none; border-radius:10px;
    padding:14px; font-weight:700; font-size:1rem; cursor:pointer; font-family:'Karla';
    display:flex; align-items:center; justify-content:center; gap:8px;
  }
  .empty-note{color:var(--violet); opacity:.85; font-size:.92rem; padding:24px 0; text-align:center;}
  footer{text-align:center; padding:26px 20px 40px; font-size:.82rem; opacity:.6;}

  .add-btn[disabled]{background:#3a3220;color:#8a7a52;cursor:not-allowed;}
  #adminPanel{position:fixed;inset:0;z-index:60;background:var(--paper);overflow-y:auto;padding:calc(env(safe-area-inset-top,0px) + 16px) 16px 60px;}
  #adminPanel[hidden]{display:none;}
  .ad-head{display:flex;justify-content:space-between;align-items:center;gap:8px;flex-wrap:wrap;}
  .ad-head h2{margin:0;}
  .ad-save,.ad-x,.ad-add{border:none;border-radius:8px;padding:10px 14px;font-weight:700;cursor:pointer;font-family:'Karla';}
  .ad-save{background:var(--gold);color:#0B0906;} .ad-x{background:var(--line);color:var(--ink);}
  .ad-add{background:var(--panel);color:var(--gold);border:2px dashed var(--gold);width:100%;margin-top:14px;}
  .ad-note{font-size:.85rem;opacity:.75;}
  .ad-wa{display:block;font-size:.85rem;margin:8px 0 14px;}
  .ad-wa input,.ad-row input,.ad-row select{background:var(--panel);color:var(--ink);border:1px solid var(--line);border-radius:6px;padding:8px;font-family:'Karla';font-size:.9rem;width:100%;}
  .ad-row{display:grid;grid-template-columns:2fr 1fr 1fr;gap:6px;background:var(--panel);border:1px solid var(--line);border-radius:10px;padding:10px;margin-bottom:8px;}
  .ad-row .full{grid-column:1/-1;display:flex;justify-content:space-between;align-items:center;font-size:.85rem;}
  .ad-row .del{background:none;border:none;color:#e0705a;font-weight:700;cursor:pointer;}

  /* ---------- product detail popup ---------- */
  .card{cursor:pointer;}
  .detail-overlay{
    position:fixed; inset:0; background:rgba(0,0,0,.72); z-index:60;
    display:flex; align-items:flex-end; justify-content:center;
    opacity:0; pointer-events:none; transition:opacity .28s ease;
  }
  .detail-overlay.open{opacity:1; pointer-events:auto;}
  @media (min-width:720px){ .detail-overlay{align-items:center;} }
  .detail-card{
    background:var(--panel); border:2px solid var(--line); border-radius:20px 20px 0 0;
    width:100%; max-width:560px; max-height:88vh; overflow-y:auto;
    padding:0 0 26px; position:relative;
    transform:translateY(28px) scale(.97); opacity:0;
    transition:transform .32s cubic-bezier(.2,.9,.25,1.1), opacity .28s ease;
  }
  .detail-overlay.open .detail-card{transform:translateY(0) scale(1); opacity:1;}
  @media (min-width:720px){ .detail-card{border-radius:20px;} }
  .detail-close{
    position:absolute; top:14px; right:14px; z-index:2;
    background:rgba(11,9,6,.75); color:var(--ink); border:1px solid var(--line);
    border-radius:999px; width:36px; height:36px; font-size:1.1rem; cursor:pointer;
  }
  .detail-media{width:100%; aspect-ratio:1/1; background:#000; overflow:hidden; border-radius:20px 20px 0 0;}
  .detail-media img, .detail-media video{width:100%; height:100%; object-fit:cover; display:block;
    animation:detailZoom .5s ease;}
  @keyframes detailZoom{from{transform:scale(1.08); opacity:.4;} to{transform:scale(1); opacity:1;}}
  .detail-media .media{height:100%; border-radius:0;}
  .detail-body{padding:20px 22px 4px;}
  .detail-body .cat{display:block; margin-bottom:4px;}
  .detail-body h2{margin:2px 0 8px; font-size:1.5rem;}
  .detail-body .price{font-size:1.2rem; font-weight:700; color:var(--gold); display:block; margin-bottom:16px;}
  .detail-actions{display:flex; gap:10px;}
</style>
</head>
<body>

<header>
  <div class="brand"><img class="fin" src="data:image/jpeg;base64,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" alt="Shastha Guppy Farm logo">Shastha Guppy Farm</div>
  <button class="cart-btn" id="editBtn" hidden style="background:var(--gold);color:#0B0906;margin-left:auto">Edit shop</button>
  <button class="cart-btn" id="cartOpenBtn">Order <span class="cart-count" id="cartCount">0</span></button>
</header>

<div class="hero">
  <div class="tagline">fifty plus guppy varieties, bred and raised here</div>
  <h1>Colour that <span class="accent">swims</span></h1>
  <p>Live guppies in every colour and tail shape we raise, plus the food that keeps them thriving. Pick your favourites and send the order straight to us on WhatsApp.</p>
</div>

<main>
  <div class="tabs" id="tabs"></div>
  <div class="grid" id="grid"></div>
</main>

<footer>Shastha Guppy Farm &mdash; orders confirmed over WhatsApp.</footer>


<section id="adminPanel" hidden>
  <div class="ad-head"><h2>Edit shop</h2><div><button id="adSave" class="ad-save">Save changes</button> <button id="adClose" class="ad-x">Close</button></div></div>
  <p class="ad-note">Only you see this screen. Changes go live for all customers after you press Save.</p>
  <label class="ad-wa">WhatsApp number (country code first, no + or spaces)<input id="adWa" inputmode="numeric"></label>
  <div id="adminList"></div>
  <button id="adAdd" class="ad-add">+ Add new item</button>
</section>
<div class="overlay" id="overlay"></div>
<aside class="drawer" id="drawer">
  <div class="drawer-head"><h2>Your order</h2><button id="drawerClose" aria-label="Close">X</button></div>
  <div class="drawer-items" id="drawerItems"></div>
  <div class="drawer-foot">
    <div class="total-row"><span>Total</span><span id="totalAmt">Rs. 0</span></div>
    <button class="checkout-btn" id="checkoutBtn">Send order on WhatsApp</button>
  </div>
</aside>

<div class="detail-overlay" id="detailOverlay">
  <div class="detail-card" id="detailCard">
    <button class="detail-close" id="detailClose" aria-label="Close">X</button>
    <div class="detail-media" id="detailMedia"></div>
    <div class="detail-body">
      <span class="cat" id="detailCat"></span>
      <h2 id="detailName"></h2>
      <span class="price" id="detailPrice"></span>
      <div class="detail-actions" id="detailActions"></div>
    </div>
  </div>
</div>

<script type="application/json" id="state">{"whatsapp": "919999999999", "products": [{"id": "g1", "name": "Albino Platinum White Guppy (pair)", "cat": "Guppies", "price": 300, "inStock": true}, {"id": "g2", "name": "Albino Redlace Guppy (pair)", "cat": "Guppies", "price": 250, "inStock": true}, {"id": "g3", "name": "Albino Silvarado Red Ear Guppy (pair)", "cat": "Guppies", "price": 240, "inStock": true}, {"id": "g4", "name": "AFR Guppy (pair)", "cat": "Guppies", "price": 230, "inStock": true}, {"id": "g5", "name": "Masco Blue Guppy (pair)", "cat": "Guppies", "price": 220, "inStock": true}, {"id": "g6", "name": "Black Guppy (pair)", "cat": "Guppies", "price": 180, "inStock": true}, {"id": "g7", "name": "Platinum White Dumbo Guppy (pair)", "cat": "Guppies", "price": 450, "inStock": true}, {"id": "g8", "name": "Silvarado Mosaic Guppy (pair)", "cat": "Guppies", "price": 180, "inStock": true}, {"id": "g9", "name": "White Texido Guppy (pair)", "cat": "Guppies", "price": 180, "inStock": true}, {"id": "g10", "name": "Japanese Blue Guppy (pair)", "cat": "Guppies", "price": 250, "inStock": true}, {"id": "g11", "name": "Platinum Big Ear Guppy (pair)", "cat": "Guppies", "price": 250, "inStock": true}, {"id": "g12", "name": "Chilli Mosaic Dumbo Guppy (pair)", "cat": "Guppies", "price": 205, "inStock": true}, {"id": "g13", "name": "Gold Guppy (pair)", "cat": "Guppies", "price": 250, "inStock": true}, {"id": "g14", "name": "Gold Ribbon Guppy (pair)", "cat": "Guppies", "price": 500, "inStock": true}, {"id": "g15", "name": "Red Granite Guppy (pair)", "cat": "Guppies", "price": 215, "inStock": true}, {"id": "g16", "name": "Blue Panda Guppy (pair)", "cat": "Guppies", "price": 230, "inStock": true}, {"id": "g17", "name": "Purple Burry Guppy (pair)", "cat": "Guppies", "price": 250, "inStock": true}, {"id": "g18", "name": "Tiger HM Guppy (pair)", "cat": "Guppies", "price": 180, "inStock": true}, {"id": "g19", "name": "Yellow Pingu Guppy (pair)", "cat": "Guppies", "price": 215, "inStock": true}, {"id": "g20", "name": "Lazuli Blue Guppy (pair)", "cat": "Guppies", "price": 190, "inStock": true}, {"id": "g21", "name": "Black Bar Endler Guppy (pair)", "cat": "Guppies", "price": 200, "inStock": true}, {"id": "g22", "name": "Red Scarlet Endler Guppy (pair)", "cat": "Guppies", "price": 200, "inStock": true}, {"id": "g23", "name": "Ivory Purple Guppy (pair)", "cat": "Guppies", "price": 250, "inStock": true}, {"id": "g24", "name": "Red Coral Endler Guppy (pair)", "cat": "Guppies", "price": 250, "inStock": true}, {"id": "g25", "name": "Zee Through Koi Guppy (pair)", "cat": "Guppies", "price": 250, "inStock": true}, {"id": "g26", "name": "Santha Clause SB Guppy (pair)", "cat": "Guppies", "price": 400, "inStock": true}, {"id": "g27", "name": "Wildred Guppy (pair)", "cat": "Guppies", "price": 210, "inStock": true}, {"id": "g28", "name": "Albino Metal Redlace Guppy (pair)", "cat": "Guppies", "price": 230, "inStock": true}, {"id": "g29", "name": "Red Dragon HM Guppy (pair)", "cat": "Guppies", "price": 250, "inStock": true}, {"id": "f1", "name": "Guppy Flake Food 100g", "cat": "Food", "price": 120, "inStock": true}, {"id": "f2", "name": "Live Daphnia Culture", "cat": "Food", "price": 80, "inStock": true}, {"id": "f3", "name": "Baby Guppy Fry Food", "cat": "Food", "price": 100, "inStock": true}]}</script>
<script>
let state = JSON.parse(document.getElementById('state').textContent);
let PRODUCTS = state.products;
const CATS = ['All','Guppies','Food'];
let cart = {}, activeCat = 'All';
const $ = id => document.getElementById(id);
const money = n => '\u20b9' + Number(n).toLocaleString('en-IN');
const esc = s => String(s).replace(/[&<>"']/g, c => ({'&':'&amp;','<':'&lt;','>':'&gt;','"':'&quot;',"'":'&#39;'}[c]));
const find = id => PRODUCTS.find(p => p.id === id);

function renderTabs(){
  $('tabs').innerHTML = '';
  CATS.forEach(c => {
    const b = document.createElement('button');
    b.className = 'tab'; b.textContent = c;
    b.setAttribute('aria-selected', c === activeCat ? 'true' : 'false');
    b.onclick = () => { activeCat = c; renderTabs(); renderGrid(); };
    $('tabs').appendChild(b);
  });
}
function mediaHtml(p){
  if(p.video) return '<div class="media"><video src="'+p.video+'" '+(p.photo?'poster="'+p.photo+'" ':'')+'controls preload="none" playsinline></video></div>';
  if(p.photo) return '<div class="media"><img src="'+p.photo+'" alt="'+esc(p.name)+'" loading="lazy"></div>';
  return '<div class="media">'+(p.cat==='Guppies'?'GUPPY':'FOOD')+'</div>';
}
function renderGrid(){
  const grid = $('grid'); grid.innerHTML = '';
  PRODUCTS.filter(p => activeCat === 'All' || p.cat === activeCat).forEach(p => {
    const q = cart[p.id] || 0;
    const action = !p.inStock ? '<button class="add-btn" disabled>Sold out</button>'
      : q === 0 ? '<button class="add-btn" data-add="'+p.id+'">Add to order</button>'
      : '<div class="qty-row"><button data-dec="'+p.id+'">-</button><span>'+q+'</span><button data-inc="'+p.id+'">+</button></div>';
    const card = document.createElement('div'); card.className = 'card';
    card.innerHTML = mediaHtml(p)+'<div class="card-body"><span class="cat">'+esc(p.cat)+'</span><h3>'+esc(p.name)+'</h3><span class="price">'+money(p.price)+'</span>'+action+'</div>';
    card.addEventListener('click', (ev) => { if(ev.target.closest('button')) return; openDetail(p.id); });
    grid.appendChild(card);
  });
  bind(grid);
}

function openDetail(id){
  const p = find(id); if(!p) return;
  $('detailMedia').innerHTML = mediaHtml(p);
  const vid = $('detailMedia').querySelector('video');
  if(vid){ vid.muted = true; vid.autoplay = true; vid.loop = true; vid.play().catch(()=>{}); }
  $('detailCat').textContent = p.cat;
  $('detailName').textContent = p.name;
  $('detailPrice').textContent = money(p.price);
  const q = cart[p.id] || 0;
  $('detailActions').innerHTML = !p.inStock ? '<button class="add-btn" disabled>Sold out</button>'
    : q === 0 ? '<button class="add-btn" data-add="'+p.id+'">Add to order</button>'
    : '<div class="qty-row"><button data-dec="'+p.id+'">-</button><span>'+q+'</span><button data-inc="'+p.id+'">+</button></div>';
  bind($('detailActions'));
  $('detailOverlay').classList.add('open');
}
function closeDetail(){ $('detailOverlay').classList.remove('open'); }
$('detailClose').onclick = closeDetail;
$('detailOverlay').onclick = (ev) => { if(ev.target === $('detailOverlay')) closeDetail(); };
function bind(root){
  root.querySelectorAll('[data-add]').forEach(b => b.onclick = () => { cart[b.dataset.add] = 1; renderAll(); });
  root.querySelectorAll('[data-inc]').forEach(b => b.onclick = () => { cart[b.dataset.inc]++; renderAll(); });
  root.querySelectorAll('[data-dec]').forEach(b => b.onclick = () => { const id = b.dataset.dec; if(--cart[id] <= 0) delete cart[id]; renderAll(); });
}
const cartTotal = () => Object.entries(cart).reduce((s,[id,q]) => s + (find(id)?.price||0)*q, 0);
const cartCount = () => Object.values(cart).reduce((a,b) => a+b, 0);
function renderDrawer(){
  $('cartCount').textContent = cartCount();
  const w = $('drawerItems'), e = Object.entries(cart).filter(([id]) => find(id));
  w.innerHTML = e.length ? e.map(([id,q]) => { const p = find(id);
    return '<div class="line"><div><div class="line-name">'+esc(p.name)+'</div><div style="font-size:.82rem;opacity:.65">'+money(p.price)+' x '+q+'</div></div><div class="line-qty"><button data-dec="'+id+'">-</button><span>'+q+'</span><button data-inc="'+id+'">+</button></div></div>'; }).join('')
    : '<p class="empty-note">Your order is empty.<br>Add guppies or food from the catalog.</p>';
  bind(w);
  $('totalAmt').textContent = money(cartTotal());
}
function renderAll(){ renderGrid(); renderDrawer(); refreshDetailActions(); }
function refreshDetailActions(){
  if(!$('detailOverlay').classList.contains('open')) return;
  const id = $('detailActions').querySelector('[data-add],[data-inc],[data-dec]');
  if(!id) return;
  const pid = id.dataset.add || id.dataset.inc || id.dataset.dec;
  const p = find(pid); if(!p) return;
  const q = cart[p.id] || 0;
  $('detailActions').innerHTML = !p.inStock ? '<button class="add-btn" disabled>Sold out</button>'
    : q === 0 ? '<button class="add-btn" data-add="'+p.id+'">Add to order</button>'
    : '<div class="qty-row"><button data-dec="'+p.id+'">-</button><span>'+q+'</span><button data-inc="'+p.id+'">+</button></div>';
  bind($('detailActions'));
}
const setDrawer = on => { $('overlay').classList.toggle('open', on); $('drawer').classList.toggle('open', on); };
$('cartOpenBtn').onclick = () => setDrawer(true);
$('drawerClose').onclick = $('overlay').onclick = () => setDrawer(false);

$('checkoutBtn').onclick = () => {
  const e = Object.entries(cart).filter(([id]) => find(id));
  if(!e.length){ alert('Add at least one item to your order first.'); return; }
  let msg = "Hello Shastha Guppy Farm, I'd like to order:\n\n";
  e.forEach(([id,q]) => { const p = find(id); msg += '- '+p.name+' x'+q+' = '+money(p.price*q)+'\n'; });
  msg += '\nTotal: '+money(cartTotal())+'\n\nPlease confirm availability and delivery.';
  window.open('https://wa.me/'+state.whatsapp+'?text='+encodeURIComponent(msg), '_blank');
};

/* ---------- owner-only edit mode ---------- */
let draft;
function buildDoc(s){
  const c = document.documentElement.cloneNode(true);
  ['grid','tabs','drawerItems','adminList','detailMedia','detailActions'].forEach(id => { const e = c.querySelector('#'+id); if(e) e.innerHTML = ''; });
  c.querySelector('#state').textContent = JSON.stringify(s).replace(/</g,'\\u003c');
  c.querySelectorAll('.open').forEach(e => e.classList.remove('open'));
  c.querySelector('#editBtn').setAttribute('hidden','');
  c.querySelector('#adminPanel').setAttribute('hidden','');
  c.querySelector('#cartCount').textContent = '0';
  c.querySelector('#totalAmt').textContent = money(0);
  return '<!DOCTYPE html>\n' + c.outerHTML;
}
function readData(f){ return new Promise((res,rej)=>{ const r=new FileReader(); r.onload=()=>res(r.result); r.onerror=rej; r.readAsDataURL(f); }); }
async function shrink(f){
  const img = new Image(); img.src = await readData(f); await img.decode();
  const s = Math.min(1, 640/img.width), c = document.createElement('canvas');
  c.width = Math.round(img.width*s); c.height = Math.round(img.height*s);
  c.getContext('2d').drawImage(img,0,0,c.width,c.height);
  return c.toDataURL('image/jpeg',0.72);
}
function renderAdmin(){
  $('adminList').innerHTML = draft.products.map((p,i) =>
    '<div class="ad-row"><input data-f="name" data-i="'+i+'" value="'+esc(p.name)+'"><input data-f="price" data-i="'+i+'" inputmode="numeric" value="'+p.price+'"><select data-f="cat" data-i="'+i+'"><option'+(p.cat==='Guppies'?' selected':'')+'>Guppies</option><option'+(p.cat==='Food'?' selected':'')+'>Food</option></select>'
    +'<div class="full"><span>Photo: '+(p.photo?'added <button class="del" data-rmp="'+i+'">remove</button>':'<input type="file" accept="image/*" data-photo="'+i+'" style="width:auto">')+'</span></div>'
    +'<div class="full"><span>Video: '+(p.video?'added <button class="del" data-rmv="'+i+'">remove</button>':'<input type="file" accept="video/*" data-video="'+i+'" style="width:auto">')+'</span></div>'
    +'<div class="full"><label><input type="checkbox" style="width:auto" data-f="inStock" data-i="'+i+'"'+(p.inStock?' checked':'')+'> In stock</label><button class="del" data-del="'+i+'">Delete</button></div></div>').join('');
  const L = $('adminList');
  L.querySelectorAll('[data-f]').forEach(el => el.onchange = () => {
    const p = draft.products[el.dataset.i], f = el.dataset.f;
    p[f] = f==='inStock' ? el.checked : f==='price' ? (Number(el.value)||0) : el.value.trim();
  });
  L.querySelectorAll('[data-photo]').forEach(el => el.onchange = async () => { const f = el.files[0]; if(!f) return; draft.products[el.dataset.photo].photo = await shrink(f); renderAdmin(); });
  L.querySelectorAll('[data-video]').forEach(el => el.onchange = async () => {
    const f = el.files[0]; if(!f) return;
    if(f.size > 2*1048576){ alert('This video is '+(f.size/1048576).toFixed(1)+' MB. Please compress it under 2 MB first.'); el.value=''; return; }
    draft.products[el.dataset.video].video = await readData(f); renderAdmin();
  });
  L.querySelectorAll('[data-rmp]').forEach(b => b.onclick = () => { delete draft.products[b.dataset.rmp].photo; renderAdmin(); });
  L.querySelectorAll('[data-rmv]').forEach(b => b.onclick = () => { delete draft.products[b.dataset.rmv].video; renderAdmin(); });
  L.querySelectorAll('[data-del]').forEach(b => b.onclick = () => { if(confirm('Delete this item?')){ draft.products.splice(b.dataset.del,1); renderAdmin(); } });
}
const OWNER_PASSWORD = 'shastha2026'; // change this to any password you like

function initAdmin(){
  $('editBtn').hidden = false;
  $('editBtn').onclick = () => {
    if(!sessionStorage.getItem('ownerOk')){
      const pw = prompt('Enter shop owner password:');
      if(pw !== OWNER_PASSWORD){ if(pw !== null) alert('Wrong password.'); return; }
      sessionStorage.setItem('ownerOk','1');
    }
    draft = JSON.parse(JSON.stringify(state)); $('adWa').value = draft.whatsapp; renderAdmin(); $('adminPanel').hidden = false;
  };
  $('adClose').onclick = () => { $('adminPanel').hidden = true; };
  $('adAdd').onclick = () => { draft.products.unshift({id:'n'+Date.now(), name:'New guppy (pair)', cat:'Guppies', price:0, inStock:true}); renderAdmin(); };
  $('adSave').onclick = () => {
    draft.whatsapp = $('adWa').value.replace(/\D/g,'') || draft.whatsapp;
    if(JSON.stringify(draft).length > 12e6){ alert('Too much photo/video data for one page (limit about 12 MB). Remove a few videos.'); return; }
    state = draft;
    localStorage.setItem('shasthaState', JSON.stringify(state));
    const blob = new Blob([buildDoc(state)], {type:'text/html'});
    const url = URL.createObjectURL(blob);
    const a = document.createElement('a');
    a.href = url; a.download = 'index.html';
    document.body.appendChild(a); a.click(); a.remove();
    URL.revokeObjectURL(url);
    $('adminPanel').hidden = true;
    renderTabs(); renderAll();
    alert('Saved! A file named index.html was downloaded. Upload it to your GitHub repository (replacing the old one) to publish these changes live. Your changes are also kept in this browser for now.');
  };
}
initAdmin();

(() => {
  try {
    const saved = localStorage.getItem('shasthaState');
    if(saved){ state = JSON.parse(saved); }
  } catch(e){}
})();

renderTabs(); renderAll();
</script>
</body>
</html>
