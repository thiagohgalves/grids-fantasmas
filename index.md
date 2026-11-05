---
layout: base
title: Início
---
<p class="sobretitulo">Acervo de pranchas de montagem</p>
<h1 class="titulo-principal">{{ site.title }}</h1>

<div class="texto-longo">
  <p>Pranchas de montagem produzidas na pesquisa de doutorado em Comunicação de Thiago Henrique Gonçalves Alves (PPGCOM/UFC).</p>
  <p>As pranchas experimentam o método de montagem a partir de Aby Warburg e Georges Didi-Huberman, reunindo recortes de quadrinhos factuais para pensar relações entre imagem, memória e história.</p>
</div>

<div class="aviso-tese">
  <strong>Tese em andamento.</strong> As pranchas são registros de tentativas e práticas do método e podem ser revistas ao longo da pesquisa.
</div>

<h2 style="margin-top: 88px">Pranchas</h2>

{% assign pranchas = site.pranchas | sort: 'numero' %}
<div class="grade-pranchas">
  {% for p in pranchas %}
  <a class="cartao" href="{{ p.url | relative_url }}">
    <img src="{{ p.miniatura | relative_url }}" alt="" loading="lazy">
    <span class="sobretitulo" style="margin: 0">Prancha {{ p.numero }} · {{ p.ano }}</span>
    <span class="cartao-titulo">{{ p.title }}</span>
    <span class="cartao-meta">{{ p.obras }}</span>
  </a>
  {% endfor %}
</div>
