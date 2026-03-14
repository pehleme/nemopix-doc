
<style>
@import url('https://fonts.googleapis.com/css2?family=Outfit:wght@400;500;600;700;800&family=Plus+Jakarta+Sans:wght@400;500;600;700&display=swap');

*{box-sizing:border-box;margin:0;padding:0;}
:root{
  --primary:#0D9488;
  --primary-light:#CCFBF1;
  --primary-dim:rgba(13,148,136,0.12);
  --secondary:#F97316;
  --secondary-light:#FFF7ED;
  --bg:#FAFAF9;
  --surface:#FFFFFF;
  --border:#E7E5E4;
  --text:#1C1917;
  --muted:#78716C;
  --success:#059669;
  --success-dim:rgba(5,150,105,0.1);
  --blue:#2563EB;
  --blue-dim:rgba(37,99,235,0.1);
  --red:#E11D48;
  --red-dim:rgba(225,29,72,0.08);
  --font-d:'Outfit',sans-serif;
  --font-b:'Plus Jakarta Sans',sans-serif;
}

body{font-family:var(--font-b);background:var(--bg);color:var(--text);}
.wrap{background:var(--bg);border-radius:24px;overflow:hidden;border:1px solid var(--border);box-shadow:0 8px 40px rgba(13,148,136,0.08);}

/* Hero */
.hero-bar{
  background:linear-gradient(135deg,#0D9488 0%,#0891B2 100%);
  padding:28px 32px;
  display:flex;align-items:flex-end;justify-content:space-between;
  flex-wrap:wrap;gap:12px;
  position:relative;overflow:hidden;
}
.hero-bar::before{
  content:'';position:absolute;top:-40px;right:-40px;
  width:220px;height:220px;border-radius:50%;
  background:rgba(255,255,255,0.06);
}
.hero-bar::after{
  content:'';position:absolute;bottom:-60px;right:80px;
  width:140px;height:140px;border-radius:50%;
  background:rgba(249,115,22,0.15);
}
.hero-title{
  font-family:var(--font-d);font-size:38px;font-weight:800;
  letter-spacing:-0.02em;color:white;line-height:1;
  position:relative;z-index:1;
}
.hero-title em{color:#FED7AA;font-style:normal;}
.hero-tag{
  font-family:var(--font-b);font-size:12px;font-weight:500;
  color:rgba(255,255,255,0.65);margin-top:6px;letter-spacing:0;
  position:relative;z-index:1;
}

/* Phases */
.phases{display:grid;grid-template-columns:repeat(3,minmax(0,1fr));border-bottom:1px solid var(--border);}
.phase{padding:20px 24px;border-right:1px solid var(--border);}
.phase:last-child{border:none;}
.ph-tag{font-size:10px;font-weight:700;letter-spacing:0.08em;text-transform:uppercase;margin-bottom:5px;}
.ph-name{font-family:var(--font-d);font-size:22px;font-weight:700;letter-spacing:-0.01em;margin-bottom:4px;}
.ph-time{font-size:12px;color:var(--muted);}
.ph1 .ph-tag{color:var(--success);}
.ph2 .ph-tag{color:var(--blue);}
.ph3 .ph-tag{color:var(--secondary);}
.ph1 .ph-name{color:var(--success);}
.ph2 .ph-name{color:var(--blue);}
.ph3 .ph-name{color:var(--secondary);}

.body{padding:28px 32px;display:flex;flex-direction:column;gap:28px;}

/* Section head */
.section-head{
  display:flex;align-items:center;gap:14px;
  border-bottom:2px solid var(--border);padding-bottom:12px;margin-bottom:16px;
}
.sh-num{
  font-family:var(--font-d);font-size:13px;font-weight:700;
  background:var(--primary);color:white;
  width:28px;height:28px;border-radius:8px;
  display:flex;align-items:center;justify-content:center;
  letter-spacing:0;flex-shrink:0;
}
.sh-title{font-family:var(--font-d);font-size:22px;font-weight:700;letter-spacing:-0.01em;}
.sh-badge{font-size:10px;font-weight:700;letter-spacing:0.07em;text-transform:uppercase;padding:4px 12px;border-radius:20px;margin-left:auto;}
.mvp-badge{background:var(--success-dim);color:var(--success);}
.v2-badge{background:var(--blue-dim);color:var(--blue);}
.diff-badge{background:var(--primary-dim);color:var(--primary);}

/* Feature cards */
.feat-grid{display:grid;grid-template-columns:repeat(2,minmax(0,1fr));gap:10px;}
.feat-grid.three{grid-template-columns:repeat(3,minmax(0,1fr));}
.feat{
  background:var(--surface);border:1.5px solid var(--border);border-radius:16px;
  padding:16px 18px;position:relative;overflow:hidden;
  transition:box-shadow 0.2s,border-color 0.2s;
}
.feat:hover{box-shadow:0 4px 20px rgba(13,148,136,0.1);border-color:#A7F3D0;}
.feat-icon{
  width:8px;height:8px;border-radius:50%;background:var(--muted);
  display:inline-block;margin-right:8px;vertical-align:middle;flex-shrink:0;
}
.feat.mvp .feat-icon{background:var(--success);}
.feat.mvp{border-left:3px solid var(--success);}
.feat.v2 .feat-icon{background:var(--blue);}
.feat.v2{border-left:3px solid var(--blue);}
.feat.diff .feat-icon{background:var(--secondary);}
.feat.diff{border-left:3px solid var(--secondary);}
.feat-name{font-size:13px;font-weight:700;display:flex;align-items:center;margin-bottom:5px;color:var(--text);}
.feat-desc{font-size:12px;color:var(--muted);line-height:1.6;}

/* Diff section */
.diff-section{
  background:linear-gradient(135deg,#0D9488 0%,#0891B2 100%);
  border-radius:20px;padding:24px 26px;
  position:relative;overflow:hidden;
}
.diff-section::before{
  content:'';position:absolute;top:-50px;right:-50px;
  width:250px;height:250px;border-radius:50%;
  background:rgba(255,255,255,0.05);
}
.diff-title{
  font-family:var(--font-d);font-size:24px;font-weight:800;
  letter-spacing:-0.01em;color:white;margin-bottom:4px;position:relative;z-index:1;
}
.diff-sub{font-size:12px;color:rgba(255,255,255,0.6);margin-bottom:20px;position:relative;z-index:1;}
.diff-grid{display:grid;grid-template-columns:repeat(2,minmax(0,1fr));gap:10px;position:relative;z-index:1;}
.diff-card{
  background:rgba(255,255,255,0.1);
  border:1px solid rgba(255,255,255,0.15);
  border-radius:14px;padding:14px 16px;
  backdrop-filter:blur(4px);
}
.diff-card:hover{background:rgba(255,255,255,0.15);}
.diff-card-num{
  font-family:var(--font-d);font-size:11px;font-weight:700;
  color:rgba(254,215,170,0.7);line-height:1;margin-bottom:6px;
  letter-spacing:0.05em;
}
.diff-card-title{font-size:13px;font-weight:700;color:#FED7AA;margin-bottom:5px;}
.diff-card-desc{font-size:11px;color:rgba(255,255,255,0.6);line-height:1.6;}

/* VS Table */
.vs-table{border:1.5px solid var(--border);border-radius:16px;overflow:hidden;}
.vs-row{display:grid;grid-template-columns:1.4fr 1fr 1fr 1fr;border-bottom:1px solid var(--border);}
.vs-row:last-child{border:none;}
.vs-row.header{background:var(--text);}
.vs-cell{padding:11px 16px;font-size:12px;border-right:1px solid var(--border);}
.vs-cell:last-child{border:none;}
.vs-row.header .vs-cell{font-size:10px;font-weight:700;letter-spacing:0.08em;text-transform:uppercase;color:rgba(255,255,255,0.45);}
.vs-row.header .vs-cell:first-child{color:rgba(255,255,255,0.85);}
.vs-feature{font-weight:600;font-size:12px;color:var(--text);}
.has{color:var(--success);font-weight:700;}
.partial{color:#D97706;font-weight:600;}
.no{color:#A8A29E;}
.our{color:var(--success);font-weight:700;background:var(--success-dim);}
.our-hd{color:#6EE7B7 !important;font-size:10px;font-weight:700;letter-spacing:0.08em;text-transform:uppercase;}
.vs-row:hover:not(.header){background:#F9FAFB;}

/* Roadmap */
.roadmap{display:grid;grid-template-columns:repeat(3,minmax(0,1fr));gap:10px;}
.rm-col{border:1.5px solid var(--border);border-radius:16px;overflow:hidden;}
.rm-hd{padding:12px 16px;font-size:10px;font-weight:700;letter-spacing:0.08em;text-transform:uppercase;}
.rm-hd.m1{background:var(--success-dim);color:var(--success);}
.rm-hd.m2{background:var(--blue-dim);color:var(--blue);}
.rm-hd.m3{background:var(--red-dim);color:var(--red);}
.rm-item{padding:8px 16px;border-top:1px solid var(--border);font-size:12px;display:flex;align-items:center;gap:10px;color:var(--text);}
.rm-item:hover{background:var(--bg);}
.rm-dot{width:6px;height:6px;border-radius:50%;flex-shrink:0;}
.m1-dot{background:var(--success);}
.m2-dot{background:var(--blue);}
.m3-dot{background:var(--red);}

/* Stack */
.stack-row{display:flex;flex-wrap:wrap;gap:8px;}
.stack-chip{
  background:var(--surface);border:1.5px solid var(--border);
  border-radius:10px;padding:6px 14px;
  font-family:var(--font-b);font-size:12px;font-weight:600;color:var(--text);
  transition:border-color 0.2s,color 0.2s;
}
.stack-chip:hover{border-color:var(--primary);color:var(--primary);}
</style>

<div class="wrap">
  <div class="hero-bar">
    <div>
      <div class="hero-title">NEMO<em>PIX</em> — VISÃO DO SISTEMA</div>
      <div class="hero-tag">Plataforma de monetização para streamers · LivePix + PixGG + Patreon killer</div>
    </div>
  </div>

  <div class="phases">
    <div class="phase ph1">
      <div class="ph-tag">Fase 1</div>
      <div class="ph-name">MVP</div>
      <div class="ph-time">Mês 1 · 4 semanas</div>
    </div>
    <div class="phase ph2">
      <div class="ph-tag">Fase 2</div>
      <div class="ph-name">Competitivo</div>
      <div class="ph-time">Mês 2 · 4 semanas</div>
    </div>
    <div class="phase ph3">
      <div class="ph-tag">Fase 3</div>
      <div class="ph-name">Diferencial</div>
      <div class="ph-time">Mês 3 · 4 semanas</div>
    </div>
  </div>

  <div class="body">

    <div>
      <div class="section-head">
        <div class="sh-num">01</div>
        <div class="sh-title">Features do MVP</div>
        <div class="sh-badge mvp-badge">Fase 1</div>
      </div>
      <div class="feat-grid">
        <div class="feat mvp">
          <div class="feat-name"><span class="feat-icon"></span>Cadastro de streamer</div>
          <div class="feat-desc">Onboarding com verificação KYC, configuração de chave PIX e geração automática de link.</div>
        </div>
        <div class="feat mvp">
          <div class="feat-name"><span class="feat-icon"></span>Página pública de doação</div>
          <div class="feat-desc">URL personalizada (nemopix.com/usuario), banner, avatar, meta e ranking de apoiadores.</div>
        </div>
        <div class="feat mvp">
          <div class="feat-name"><span class="feat-icon"></span>Fluxo de doação PIX</div>
          <div class="feat-desc">Modal → nome + valor + mensagem → QR Code gerado → webhook de confirmação em tempo real.</div>
        </div>
        <div class="feat mvp">
          <div class="feat-name"><span class="feat-icon"></span>Widget OBS</div>
          <div class="feat-desc">Overlay via URL para OBS, StreamElements e Streamlabs. Alerta animado ao receber doação.</div>
        </div>
        <div class="feat mvp">
          <div class="feat-name"><span class="feat-icon"></span>Carteira + saque PIX</div>
          <div class="feat-desc">Saldo interno, histórico de transações, saque manual via PIX com taxa de 3,5%.</div>
        </div>
        <div class="feat mvp">
          <div class="feat-name"><span class="feat-icon"></span>Dashboard simples</div>
          <div class="feat-desc">Receita hoje/mês, feed de doações, meta da live, top apoiadores.</div>
        </div>
      </div>
    </div>

    <div>
      <div class="section-head">
        <div class="sh-num">02</div>
        <div class="sh-title">Features Fase 2</div>
        <div class="sh-badge v2-badge">Fase 2</div>
      </div>
      <div class="feat-grid">
        <div class="feat v2">
          <div class="feat-name"><span class="feat-icon"></span>Cartão de crédito</div>
          <div class="feat-desc">Gateway adicional para doadores sem PIX ou internacionais.</div>
        </div>
        <div class="feat v2">
          <div class="feat-name"><span class="feat-icon"></span>Alertas animados avançados</div>
          <div class="feat-desc">Temas, efeitos visuais, som customizado e gifs por faixa de valor.</div>
        </div>
        <div class="feat v2">
          <div class="feat-name"><span class="feat-icon"></span>Ranking + metas de live</div>
          <div class="feat-desc">Placar ao vivo no overlay, metas com barra de progresso visível na stream.</div>
        </div>
        <div class="feat v2">
          <div class="feat-name"><span class="feat-icon"></span>Áudio do doador</div>
          <div class="feat-desc">Doador grava ou envia áudio curto que é reproduzido ao vivo na live.</div>
        </div>
        <div class="feat v2">
          <div class="feat-name"><span class="feat-icon"></span>Editor de página visual</div>
          <div class="feat-desc">Componentes arrastáveis: banner, vídeo, links, produtos, meta e ranking.</div>
        </div>
        <div class="feat v2">
          <div class="feat-name"><span class="feat-icon"></span>Analytics completo</div>
          <div class="feat-desc">Gráfico diário/mensal, conversão de audiência, origem do tráfego, ranking histórico.</div>
        </div>
      </div>
    </div>

    <div>
      <div class="diff-section">
        <div class="diff-title">DIFERENCIAIS COMPETITIVOS</div>
        <div class="diff-sub">O que vai fazer a plataforma ganhar do LivePix e PixGG</div>
        <div class="diff-grid">
          <div class="diff-card">
            <div class="diff-card-num">01</div>
            <div class="diff-card-title">Voz IA de personagens</div>
            <div class="diff-card-desc">Mensagens lidas com vozes clonadas de personagens, celebridades ou do próprio streamer. Efeito viral na live — vira propaganda orgânica.</div>
          </div>
          <div class="diff-card">
            <div class="diff-card-num">02</div>
            <div class="diff-card-title">Gamificação de doações</div>
            <div class="diff-card-desc">Desafios por faixa de valor, efeito terremoto, explosão na tela, minigames ativados por doação. Engajamento muito além de um alerta simples.</div>
          </div>
          <div class="diff-card">
            <div class="diff-card-num">03</div>
            <div class="diff-card-title">Taxa 3,5% — menor do mercado</div>
            <div class="diff-card-desc">LivePix cobra mais. Estratégia de entrada: 0% por 3 meses para os primeiros 100 streamers de médio porte.</div>
          </div>
          <div class="diff-card">
            <div class="diff-card-num">04</div>
            <div class="diff-card-title">Assinaturas + comunidade</div>
            <div class="diff-card-desc">Planos mensais com cargos automáticos no Discord e bot Telegram. LivePix não tem. PixGG tem parcialmente.</div>
          </div>
          <div class="diff-card">
            <div class="diff-card-num">05</div>
            <div class="diff-card-title">Overlay marketplace</div>
            <div class="diff-card-desc">Criadores vendem e compram temas, alertas e animações. Receita adicional e efeito de rede na plataforma.</div>
          </div>
          <div class="diff-card">
            <div class="diff-card-num">06</div>
            <div class="diff-card-title">Multi-plataforma nativa</div>
            <div class="diff-card-desc">Integração nativa com Twitch, YouTube, Kick e TikTok Live — não só OBS. Abre mercado além do streaming tradicional.</div>
          </div>
        </div>
      </div>
    </div>

    <div>
      <div class="section-head">
        <div class="sh-num">03</div>
        <div class="sh-title">Comparativo com concorrentes</div>
      </div>
      <div class="vs-table">
        <div class="vs-row header">
          <div class="vs-cell">Feature</div>
          <div class="vs-cell our-hd">NemoPix</div>
          <div class="vs-cell">LivePix</div>
          <div class="vs-cell">PixGG</div>
        </div>
        <div class="vs-row">
          <div class="vs-cell vs-feature">Doação PIX</div>
          <div class="vs-cell our has">✓ Sim</div>
          <div class="vs-cell has">✓ Sim</div>
          <div class="vs-cell has">✓ Sim</div>
        </div>
        <div class="vs-row">
          <div class="vs-cell vs-feature">Taxa</div>
          <div class="vs-cell our has">3,5%</div>
          <div class="vs-cell partial">~5%</div>
          <div class="vs-cell partial">~4%</div>
        </div>
        <div class="vs-row">
          <div class="vs-cell vs-feature">Voz IA / personagens</div>
          <div class="vs-cell our has">✓ Sim</div>
          <div class="vs-cell no">✗ Não</div>
          <div class="vs-cell has">✓ Sim</div>
        </div>
        <div class="vs-row">
          <div class="vs-cell vs-feature">Gamificação</div>
          <div class="vs-cell our has">✓ Sim</div>
          <div class="vs-cell no">✗ Não</div>
          <div class="vs-cell partial">Parcial</div>
        </div>
        <div class="vs-row">
          <div class="vs-cell vs-feature">Assinaturas recorrentes</div>
          <div class="vs-cell our has">✓ Sim</div>
          <div class="vs-cell partial">Parcial</div>
          <div class="vs-cell no">✗ Não</div>
        </div>
        <div class="vs-row">
          <div class="vs-cell vs-feature">Discord / Telegram bot</div>
          <div class="vs-cell our has">✓ Sim</div>
          <div class="vs-cell no">✗ Não</div>
          <div class="vs-cell no">✗ Não</div>
        </div>
        <div class="vs-row">
          <div class="vs-cell vs-feature">Overlay marketplace</div>
          <div class="vs-cell our has">✓ Sim</div>
          <div class="vs-cell no">✗ Não</div>
          <div class="vs-cell no">✗ Não</div>
        </div>
        <div class="vs-row">
          <div class="vs-cell vs-feature">Twitch / YouTube / Kick</div>
          <div class="vs-cell our has">✓ Nativo</div>
          <div class="vs-cell partial">Parcial</div>
          <div class="vs-cell partial">Parcial</div>
        </div>
        <div class="vs-row">
          <div class="vs-cell vs-feature">Cripto</div>
          <div class="vs-cell our has">✓ Fase 2</div>
          <div class="vs-cell no">✗ Não</div>
          <div class="vs-cell no">✗ Não</div>
        </div>
        <div class="vs-row">
          <div class="vs-cell vs-feature">API pública</div>
          <div class="vs-cell our has">✓ Fase 3</div>
          <div class="vs-cell no">✗ Não</div>
          <div class="vs-cell no">✗ Não</div>
        </div>
      </div>
    </div>

    <div>
      <div class="section-head">
        <div class="sh-num">04</div>
        <div class="sh-title">Roadmap 90 dias</div>
      </div>
      <div class="roadmap">
        <div class="rm-col">
          <div class="rm-hd m1">Mês 1 — MVP</div>
          <div class="rm-item"><div class="rm-dot m1-dot"></div>Cadastro + KYC</div>
          <div class="rm-item"><div class="rm-dot m1-dot"></div>Página pública</div>
          <div class="rm-item"><div class="rm-dot m1-dot"></div>Fluxo PIX completo</div>
          <div class="rm-item"><div class="rm-dot m1-dot"></div>Widget OBS</div>
          <div class="rm-item"><div class="rm-dot m1-dot"></div>Alerta na live</div>
          <div class="rm-item"><div class="rm-dot m1-dot"></div>Carteira + saque</div>
          <div class="rm-item"><div class="rm-dot m1-dot"></div>Dashboard base</div>
        </div>
        <div class="rm-col">
          <div class="rm-hd m2">Mês 2 — Competitivo</div>
          <div class="rm-item"><div class="rm-dot m2-dot"></div>Cartão de crédito</div>
          <div class="rm-item"><div class="rm-dot m2-dot"></div>Alertas avançados</div>
          <div class="rm-item"><div class="rm-dot m2-dot"></div>Áudio do doador</div>
          <div class="rm-item"><div class="rm-dot m2-dot"></div>Ranking ao vivo</div>
          <div class="rm-item"><div class="rm-dot m2-dot"></div>Metas de live</div>
          <div class="rm-item"><div class="rm-dot m2-dot"></div>Analytics completo</div>
          <div class="rm-item"><div class="rm-dot m2-dot"></div>Editor de página</div>
        </div>
        <div class="rm-col">
          <div class="rm-hd m3">Mês 3 — Diferencial</div>
          <div class="rm-item"><div class="rm-dot m3-dot"></div>Voz IA</div>
          <div class="rm-item"><div class="rm-dot m3-dot"></div>Assinaturas</div>
          <div class="rm-item"><div class="rm-dot m3-dot"></div>Discord bot</div>
          <div class="rm-item"><div class="rm-dot m3-dot"></div>Telegram bot</div>
          <div class="rm-item"><div class="rm-dot m3-dot"></div>Gamificação</div>
          <div class="rm-item"><div class="rm-dot m3-dot"></div>Campanhas</div>
          <div class="rm-item"><div class="rm-dot m3-dot"></div>Overlay marketplace</div>
        </div>
      </div>
    </div>

    <div>
      <div class="section-head">
        <div class="sh-num">05</div>
        <div class="sh-title">Stack tecnológica</div>
      </div>
      <div style="display:flex;flex-direction:column;gap:14px;">
        <div>
          <div style="font-size:10px;font-weight:700;letter-spacing:0.08em;text-transform:uppercase;color:var(--muted);margin-bottom:8px;">Frontend</div>
          <div class="stack-row">
            <div class="stack-chip">Next.js</div>
            <div class="stack-chip">Tailwind</div>
            <div class="stack-chip">Socket.io</div>
            <div class="stack-chip">React</div>
          </div>
        </div>
        <div>
          <div style="font-size:10px;font-weight:700;letter-spacing:0.08em;text-transform:uppercase;color:var(--muted);margin-bottom:8px;">Backend</div>
          <div class="stack-row">
            <div class="stack-chip">.Net</div>
            <div class="stack-chip">PostgreSQL</div>
            <div class="stack-chip">Redis</div>
            <div class="stack-chip">WebSocket</div>
            <div class="stack-chip">S3</div>
          </div>
        </div>
        <div>
          <div style="font-size:10px;font-weight:700;letter-spacing:0.08em;text-transform:uppercase;color:var(--muted);margin-bottom:8px;">Infra</div>
          <div class="stack-row">
            <div class="stack-chip">AWS</div>
            <div class="stack-chip">Cloudflare</div>
            <div class="stack-chip">Docker</div>
          </div>
        </div>
      </div>
    </div>

  </div>
</div>
