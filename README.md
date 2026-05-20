# Sonkoy.com
Pagina de venta de artesanías 
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>SONKOY | Orfebrería y Joyería de Autor</title>
  <link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,300;0,400;0,500;0,600;1,300;1,400&display=swap" rel="stylesheet">
<style>
*{box-sizing:border-box;margin:0;padding:0}
:root{--crema:#faf8f3;--blanco:#ffffff;--negro:#1a1a1a;--gris:#5a5040;--dorado:#c9a227;--teal:#2e7d6e;--bordo:#8b2020;--borde:#e0d5c0}
html{scroll-behavior:smooth}
body{font-family:'Cormorant Garamond',serif;background:var(--blanco);color:var(--negro);font-weight:300;line-height:1.6}
nav{position:fixed;top:0;left:0;right:0;z-index:100;background:rgba(255,255,255,.97);backdrop-filter:blur(10px);border-bottom:1px solid var(--borde)}
.nav-container{max-width:1200px;margin:0 auto;padding:0 20px;height:58px;display:flex;align-items:center;justify-content:space-between}
.logo-btn{border:none;background:none;cursor:pointer;padding:0}
.logo-btn img{height:42px;width:42px;border-radius:50%;object-fit:cover;border:2px solid var(--dorado)}
.nav-links{display:flex;gap:24px;align-items:center}
.nav-links button{background:none;border:none;cursor:pointer;font-family:'Cormorant Garamond',serif;font-size:.82rem;font-weight:400;letter-spacing:.2em;text-transform:uppercase;color:var(--gris);transition:color .25s}
.nav-links button:hover{color:var(--dorado)}
#cart-count{display:inline-flex;align-items:center;justify-content:center;background:var(--bordo);color:#fff;font-size:.58rem;width:16px;height:16px;border-radius:50%;margin-left:4px}
.page{display:none;padding-top:58px;min-height:100vh}.page.active{display:block}
.carrusel{position:relative;width:100%;height:110px;overflow:hidden;background:var(--negro)}
@media(min-width:700px){.carrusel{height:210px}}
.slide{position:absolute;inset:0;opacity:0;transition:opacity 1.2s}.slide.active{opacity:1}
@keyframes kenBurnsUp{0%{transform:scale(1.1) translateY(5%)}100%{transform:scale(1) translateY(0)}}
@keyframes kenBurnsDiag{0%{transform:scale(1.1) translate(-3%,5%)}100%{transform:scale(1) translate(0,0)}}
.simg{width:100%;height:100%;object-fit:cover}
.slide.active .simg{animation:kenBurnsUp 5s ease-out forwards}
.slide:nth-child(even).active .simg{animation:kenBurnsDiag 5s ease-out forwards}
.arr{position:absolute;top:50%;transform:translateY(-50%);background:rgba(255,255,255,.6);border:none;width:28px;height:28px;font-size:1.2rem;cursor:pointer;z-index:5;color:var(--negro);display:flex;align-items:center;justify-content:center}
.arr-izq{left:8px}.arr-der{right:8px}
.dots-c{position:absolute;bottom:8px;left:50%;transform:translateX(-50%);display:flex;gap:7px;z-index:5}
.dot{width:6px;height:6px;transform:rotate(45deg);background:rgba(255,255,255,.3);border:none;cursor:pointer;display:inline-block;transition:background .2s}
.dot.activo{background:var(--dorado)}
.franja{width:100%;height:28px;overflow:hidden}.franja img{width:100%;height:28px;object-fit:cover;display:block}
.hero{text-align:center;padding:24px 24px 48px;background:var(--blanco)}
.logo-grande{display:flex;align-items:center;justify-content:center;margin:0 auto 20px;width:270px;height:270px;border-radius:50%;box-shadow:0 0 0 3px var(--dorado),0 0 0 7px var(--blanco),0 0 0 10px rgba(201,162,39,.25),0 12px 40px rgba(201,162,39,.12)}
.logo-grande img{width:260px;height:260px;border-radius:50%;object-fit:cover}
@media(min-width:700px){.logo-grande{width:320px;height:320px}.logo-grande img{width:310px;height:310px}}
@keyframes bob{0%,100%{transform:translateY(0)}50%{transform:translateY(-6px)}}
.logo-grande{animation:bob 6s ease-in-out infinite}
.frase{font-size:clamp(.95rem,2.5vw,1.1rem);font-style:italic;color:var(--gris);max-width:480px;margin:0 auto 32px;line-height:2;font-weight:300}
.botones{display:flex;flex-wrap:wrap;gap:12px;justify-content:center}
.btn{font-family:'Cormorant Garamond',serif;font-size:.8rem;font-weight:400;letter-spacing:.22em;text-transform:uppercase;padding:12px 32px;cursor:pointer;border:none;transition:all .3s;display:inline-flex;align-items:center;gap:7px}
.btn-oscuro{background:var(--negro);color:#fff}.btn-oscuro:hover{background:var(--dorado);color:var(--negro)}
.btn-claro{background:transparent;border:1px solid var(--negro);color:var(--negro)}.btn-claro:hover{border-color:var(--dorado);color:var(--dorado)}
.sep{width:100%;max-width:500px;margin:0 auto;padding:10px 0}.sep svg{width:100%;display:block}
.colecciones{background:var(--crema);padding:60px 24px}.colecciones-inner{max-width:960px;margin:0 auto}
.sec-titulo{font-size:.72rem;letter-spacing:.3em;text-transform:uppercase;color:var(--dorado);text-align:center;margin-bottom:36px}
.grid-colecciones{display:grid;grid-template-columns:repeat(2,1fr);gap:2px}
@media(min-width:680px){.grid-colecciones{grid-template-columns:repeat(4,1fr)}}
.col-item{background:var(--blanco);padding:24px 18px;border:1px solid var(--borde);transition:border-color .3s}.col-item:hover{border-color:var(--dorado)}
.col-rombo{width:10px;height:10px;transform:rotate(45deg);margin-bottom:14px}
.col-item:nth-child(1) .col-rombo{background:var(--bordo)}.col-item:nth-child(2) .col-rombo{background:var(--dorado)}
.col-item:nth-child(3) .col-rombo{background:var(--teal)}.col-item:nth-child(4) .col-rombo{background:var(--bordo)}
.col-nombre{font-size:1.3rem;font-weight:400;margin-bottom:7px}.col-desc{font-size:.83rem;color:var(--gris);line-height:1.75;font-weight:300}
.tipos{max-width:960px;margin:0 auto;padding:60px 24px}
.tipo-item{position:relative;padding-left:16px;margin-bottom:20px}
.tipo-item::before{content:'◆';position:absolute;left:0;top:3px;color:var(--dorado);font-size:.5rem}
.tipo-titulo{font-size:1.15rem;font-weight:500;margin-bottom:6px}.tipo-desc{font-size:.82rem;color:var(--gris);line-height:1.8;font-weight:300}
.catalogo-header{background:var(--crema);border-bottom:1px solid var(--borde);padding:48px 24px 32px}
.catalogo-header-inner{max-width:1200px;margin:0 auto}
.catalogo-header h1{font-size:clamp(2rem,7vw,3.5rem);font-weight:300;margin-bottom:6px}
.catalogo-header p{font-style:italic;color:var(--gris);font-size:.95rem}
.filtros{background:var(--blanco);border-bottom:1px solid var(--borde);padding:16px 24px}
.filtros-inner{max-width:1200px;margin:0 auto;display:flex;flex-direction:column;gap:12px}
.filtro-label{display:block;font-size:.6rem;letter-spacing:.2em;text-transform:uppercase;color:var(--dorado);margin-bottom:7px}
.pills{display:flex;flex-wrap:wrap;gap:5px}
.pill{font-size:.72rem;padding:5px 13px;border:1px solid var(--borde);background:transparent;cursor:pointer;color:var(--gris);transition:all .25s;font-family:'Cormorant Garamond',serif}
.pill:hover,.pill.on{border-color:var(--dorado);background:var(--dorado);color:var(--negro)}
.productos-section{max-width:1200px;margin:0 auto;padding:32px 24px}
.productos-count{font-size:.7rem;color:var(--gris);margin-bottom:22px}
.galeria{display:grid;grid-template-columns:repeat(auto-fill,minmax(230px,1fr));gap:2px}
.producto-card{background:var(--blanco);border:1px solid var(--borde);padding:22px;cursor:pointer;transition:border-color .3s,box-shadow .3s}
.producto-card:hover{border-color:var(--dorado);box-shadow:0 4px 18px rgba(201,162,39,.1)}
.prod-img{background:var(--crema);aspect-ratio:1;display:flex;align-items:center;justify-content:center;margin-bottom:14px;font-size:1.9rem;font-weight:300;color:var(--borde)}
.prod-sku{font-size:.58rem;letter-spacing:.2em;text-transform:uppercase;color:var(--dorado);margin-bottom:3px}
.prod-nombre{font-size:1.05rem;font-weight:400;margin-bottom:10px}
.prod-div{height:1px;background:var(--borde);margin-bottom:10px}
.prod-bottom{display:flex;align-items:flex-end;justify-content:space-between}
.prod-precio{font-size:1.35rem;font-weight:500}.prod-consultar{font-size:.72rem;color:var(--gris);font-weight:300}
.agregar-btn{width:30px;height:30px;background:var(--negro);border:none;color:#fff;cursor:pointer;font-size:1rem;display:flex;align-items:center;justify-content:center;transition:background .25s}
.agregar-btn:hover{background:var(--dorado);color:var(--negro)}
.carrito-container{max-width:760px;margin:0 auto;padding:48px 24px}
.carrito-container h1{font-size:clamp(1.9rem,7vw,3.3rem);font-weight:300;margin-bottom:8px}
.carrito-subtitulo{font-style:italic;color:var(--gris);margin-bottom:28px}
.carrito-item{background:var(--blanco);border:1px solid var(--borde);padding:18px;margin-bottom:8px}
.item-nombre{font-size:1.05rem;margin-bottom:8px}
.item-controles{display:flex;align-items:center;justify-content:space-between;gap:10px}
.cant-control{display:flex;align-items:center;border:1px solid var(--borde)}
.cant-btn{width:30px;height:30px;background:none;border:none;cursor:pointer;font-size:.95rem;display:flex;align-items:center;justify-content:center}
.cant-input{width:36px;height:30px;border:none;border-left:1px solid var(--borde);border-right:1px solid var(--borde);text-align:center;font-family:'Cormorant Garamond',serif;font-size:.88rem;background:transparent;outline:none}
.item-precio{text-align:right}.item-subtotal{font-size:1.15rem;font-weight:500}
.carrito-total{border-top:1px solid var(--negro);margin-top:28px;padding-top:18px;display:flex;justify-content:space-between;align-items:baseline;margin-bottom:18px}
.total-label{font-size:1.05rem;font-style:italic}.total-valor{font-size:2.1rem;font-weight:500;color:var(--bordo)}
.carrito-acciones{display:flex;flex-direction:column;gap:7px}
.carrito-vacio{text-align:center;padding:64px 0;font-style:italic;color:var(--gris)}
.checkout-container{max-width:540px;margin:0 auto;padding:48px 24px}
.checkout-container h1{font-size:clamp(1.8rem,6vw,2.8rem);font-weight:300;margin-bottom:6px}
.checkout-sub{font-style:italic;color:var(--gris);margin-bottom:28px}
.campo{margin-bottom:16px}
.campo label{display:block;font-size:.62rem;letter-spacing:.15em;text-transform:uppercase;color:var(--gris);margin-bottom:5px}
.campo input,.campo select,.campo textarea{width:100%;padding:10px 13px;border:1px solid var(--borde);background:var(--crema);font-family:'Cormorant Garamond',serif;font-size:.95rem;color:var(--negro);outline:none;transition:border-color .25s;border-radius:0;-webkit-appearance:none}
.campo input:focus,.campo select:focus,.campo textarea:focus{border-color:var(--dorado)}
.campo textarea{resize:vertical;min-height:85px}
.resumen-pedido{background:var(--crema);border:1px solid var(--borde);padding:18px;margin-bottom:24px}
.resumen-pedido h3{font-size:.62rem;letter-spacing:.2em;text-transform:uppercase;color:var(--dorado);margin-bottom:12px}
.resumen-item{display:flex;justify-content:space-between;font-size:.85rem;padding:4px 0;border-bottom:1px solid var(--borde)}
.resumen-total{display:flex;justify-content:space-between;margin-top:9px;font-size:1.1rem;font-weight:500}
.aviso{font-style:italic;color:var(--gris);font-size:.85rem;text-align:center;margin-top:16px}
.contacto-container{max-width:540px;margin:0 auto;padding:80px 24px;text-align:center}
.contacto-container h1{font-size:2.5rem;font-weight:300;margin-bottom:32px}
.contacto-container p{font-size:1.05rem;color:var(--gris);margin-bottom:12px}
.exito-container{max-width:520px;margin:0 auto;padding:90px 24px;text-align:center}
.exito-container h1{font-size:2.6rem;font-weight:300;margin-bottom:12px}
.exito-container p{font-style:italic;color:var(--gris);font-size:1rem;margin-bottom:32px;line-height:1.9}
footer{background:var(--negro);padding:40px 24px;text-align:center}
footer p{font-size:.75rem;color:rgba(255,255,255,.35);letter-spacing:.08em}
.toast{position:fixed;bottom:18px;right:18px;z-index:999;background:var(--negro);color:#fff;padding:11px 18px;font-family:'Cormorant Garamond',serif;font-size:.8rem;opacity:0;transition:opacity .3s;pointer-events:none;border-left:3px solid var(--dorado)}
.toast.on{opacity:1}
.back-btn{background:none;border:none;cursor:pointer;font-family:'Cormorant Garamond',serif;font-size:.7rem;letter-spacing:.15em;text-transform:uppercase;color:var(--gris);transition:color .2s;padding:0;display:block;margin:18px 24px 0}
.back-btn:hover{color:var(--dorado)}
.newsletter{background:var(--negro);padding:48px 24px;text-align:center}
.newsletter h3{font-family:'Cormorant Garamond',serif;font-size:1.8rem;font-weight:300;color:#fff;margin-bottom:10px;letter-spacing:.04em}
.newsletter p{font-size:.88rem;color:rgba(255,255,255,.55);font-style:italic;margin-bottom:28px}
.newsletter-form{display:flex;gap:8px;max-width:420px;margin:0 auto;flex-wrap:wrap;justify-content:center}
.newsletter-form input{flex:1;min-width:200px;padding:11px 16px;border:1px solid rgba(255,255,255,.2);background:rgba(255,255,255,.07);color:#fff;font-family:'Cormorant Garamond',serif;font-size:.95rem;outline:none;transition:border-color .25s;border-radius:0}
.newsletter-form input:focus{border-color:var(--dorado)}
.newsletter-form input::placeholder{color:rgba(255,255,255,.35)}
.newsletter-form button{padding:11px 24px;background:var(--dorado);color:var(--negro);border:none;cursor:pointer;font-family:'Cormorant Garamond',serif;font-size:.78rem;letter-spacing:.18em;text-transform:uppercase;transition:background .25s;white-space:nowrap}
.newsletter-form button:hover{background:#e0b42a}
.newsletter-ok{display:none;color:var(--dorado);font-style:italic;font-size:1rem;margin-top:12px}
.metodos-pago{display:flex;flex-direction:column;gap:8px;margin-top:8px}
.metodo-item{display:flex;align-items:center;gap:14px;padding:14px;border:1px solid var(--borde);cursor:pointer;transition:border-color .2s,background .2s;background:var(--blanco)}
.metodo-item:hover{border-color:var(--dorado)}
.metodo-item.seleccionado{border-color:var(--dorado);background:rgba(201,162,39,.06)}
.metodo-icono{font-size:1.4rem;flex-shrink:0}
.metodo-info{flex:1}
.metodo-nombre{font-size:.95rem;font-weight:400;margin-bottom:2px}
.metodo-desc{font-size:.72rem;color:var(--gris);font-weight:300}
.metodo-check{font-size:1.1rem;color:var(--dorado);flex-shrink:0}
</style>
</head>
<body>
<nav>
  <div class="nav-container">
    <button class="logo-btn" onclick="mostrarSeccion('home')"><img src="data:image/jpeg;base64,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
