<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>XR SPORTS - A Banca Premium</title>
    <style>
        *{box-sizing:border-box;margin:0;padding:0;font-family:-apple-system,BlinkMacSystemFont,"Segoe UI",Roboto,sans-serif}:root{--bg-fundo:#090e17;--bg-card:rgba(18,25,39,0.6);--bg-hover:#1a2333;--neon:#00ff88;--texto:#ffffff;--texto-secundario:#8a96a8;--borda:rgba(255,255,255,0.1);--danger:#ff4757;--live:#ff3b3b;--amarelo:#f5a623;--azul:#00c3ff}body{background-color:var(--bg-fundo);color:var(--texto);padding-bottom:120px;-webkit-font-smoothing:antialiased}header{background:#121927;padding:16px 20px;position:sticky;top:0;z-index:50;border-bottom:1px solid var(--borda);box-shadow:0 4px 20px rgba(0,0,0,0.4)}.header-top{display:flex;justify-content:space-between;align-items:center}
        
        /* LOGO PREMIUM XR SPORTS */
        .logo-wrapper { display: flex; align-items: center; gap: 12px; cursor: pointer; user-select: none; text-decoration: none; }
        .logo-badge { position: relative; width: 38px; height: 38px; background: linear-gradient(135deg, #121927 0%, #090e17 100%); border-radius: 10px; display: flex; align-items: center; justify-content: center; border: 1px solid rgba(0, 255, 136, 0.4); box-shadow: 0 4px 10px rgba(0, 0, 0, 0.5), 0 0 15px rgba(0, 255, 136, 0.15); overflow: hidden; transition: transform 0.2s; }
        .logo-wrapper:active .logo-badge { transform: scale(0.95); }
        .logo-badge::after { content: ''; position: absolute; top: -50%; left: -50%; width: 200%; height: 200%; background: linear-gradient(to right, rgba(255,255,255,0) 0%, rgba(255,255,255,0.1) 50%, rgba(255,255,255,0) 100%); transform: rotate(45deg); animation: brilho-emblema 4s infinite; }
        @keyframes brilho-emblema { 0% { transform: rotate(45deg) translateX(-100%); } 20%, 100% { transform: rotate(45deg) translateX(100%); } }
        .logo-badge span { font-size: 18px; font-weight: 900; font-style: italic; color: var(--neon); letter-spacing: -1px; z-index: 2; }
        .logo-typography { display: flex; flex-direction: column; justify-content: center; }
        .logo-title { font-size: 20px; font-weight: 900; color: #ffffff; letter-spacing: 0.5px; line-height: 1.1; display: flex; align-items: center; }
        .logo-title strong { color: var(--neon); margin-right: 4px; font-style: italic; }
        .logo-subtitle { font-size: 9px; font-weight: 800; color: var(--texto-secundario); letter-spacing: 3.5px; text-transform: uppercase; margin-top: 2px; }
        
        .btn-sync{background:0 0;color:var(--texto-secundario);border:1px solid var(--borda);padding:6px 12px;border-radius:8px;font-weight:700;cursor:pointer;transition:.2s;font-size:13px}.btn-sync:active{transform:scale(.95);background:var(--bg-hover)}.nav-ligas{display:flex;gap:10px;margin-top:18px;overflow-x:auto;padding-bottom:4px;scrollbar-width:none}.nav-ligas::-webkit-scrollbar{display:none}.liga-btn{background:rgba(9,14,23,0.8);color:var(--texto-secundario);border:1px solid var(--borda);padding:8px 18px;border-radius:20px;font-size:13px;font-weight:700;white-space:nowrap;cursor:pointer;transition:.3s}.liga-btn.ativo{background:var(--neon);color:#000;border-color:var(--neon)}#status-msg{text-align:center;padding:25px 20px;color:var(--texto-secundario);font-size:14px;margin:20px 15px;border-radius:12px;background:var(--bg-card);backdrop-filter:blur(10px);-webkit-backdrop-filter:blur(10px);border:1px dashed var(--borda);line-height:1.6}.container{padding:5px 15px;max-width:600px;margin:0 auto}.card-jogo{background:var(--bg-card);backdrop-filter:blur(12px);-webkit-backdrop-filter:blur(12px);border:1px solid var(--borda);border-radius:16px;padding:16px;margin-bottom:16px;display:flex;flex-direction:column;gap:14px;box-shadow:0 8px 32px rgba(0,0,0,0.2)}.card-topo{display:flex;justify-content:space-between;align-items:center;border-bottom:1px solid var(--borda);padding-bottom:10px}.liga-tag{font-size:11px;color:var(--texto-secundario);font-weight:800;text-transform:uppercase;letter-spacing:.5px}.badge-horario{font-size:11px;font-weight:800;color:#000;background:var(--neon);padding:4px 8px;border-radius:6px}.badge-aovivo{background:rgba(255,59,59,0.15);color:var(--live);border:1px solid var(--live);animation:piscar 1.5s infinite}.badge-intervalo{background:rgba(245,166,35,0.15);color:var(--amarelo);border:1px solid var(--amarelo);animation:piscar 1.5s infinite}@keyframes piscar{0%,100%{opacity:1}50%{opacity:.5}}.placar-box{display:flex;justify-content:space-between;align-items:center;width:100%;margin-top:5px}.time-box{display:flex;align-items:center;gap:10px;width:40%}.time-box.visitante{flex-direction:row-reverse;text-align:right}.escudo-container{width:36px;height:36px;display:flex;align-items:center;justify-content:center;flex-shrink:0}.escudo-img{width:100%;height:100%;object-fit:contain}.escudo-letra{width:36px;height:36px;border-radius:50%;display:flex;align-items:center;justify-content:center;font-weight:900;font-size:13px;color:#fff;box-shadow:inset 0 2px 5px rgba(0,0,0,0.4);border:1px solid rgba(255,255,255,0.1)}.nome-time{font-size:14px;font-weight:800;color:var(--texto);line-height:1.2}.vs-txt{font-size:12px;font-weight:900;color:var(--texto-secundario)}.placar-live{font-size:16px;font-weight:900;color:var(--neon);background:rgba(0,255,136,0.1);padding:4px 8px;border-radius:6px;letter-spacing:1px;white-space:nowrap}.mercado-titulo{font-size:11px;color:var(--texto-secundario);font-weight:700;text-transform:uppercase;margin-bottom:-5px;margin-top:5px;text-align:center;border-top:1px dashed rgba(255,255,255,0.05);padding-top:10px}.odds-linha{display:grid;grid-template-columns:1fr 1fr 1fr;gap:8px}.odds-linha-dupla{display:grid;grid-template-columns:1fr 1fr;gap:8px}.odd-btn{background:rgba(9,14,23,0.6);border:1px solid var(--borda);border-radius:10px;padding:10px 5px;display:flex;flex-direction:column;align-items:center;cursor:pointer;transition:.2s;user-select:none}.odd-btn.selecionado{background:var(--neon);border-color:var(--neon);box-shadow:0 0 15px rgba(0,255,136,0.2)}.odd-btn.selecionado .odd-lbl,.odd-btn.selecionado .odd-val{color:#000}.odd-lbl{font-size:10px;color:var(--texto-secundario);font-weight:800;text-transform:uppercase;margin-bottom:2px;text-align:center}.odd-val{font-size:15px;font-weight:900;color:var(--texto)}#btn-gaveta{position:fixed;bottom:25px;left:50%;transform:translateX(-50%);background:var(--neon);color:#000;width:90%;max-width:400px;padding:16px 20px;border-radius:14px;font-weight:900;font-size:15px;display:none;justify-content:space-between;align-items:center;box-shadow:0 10px 30px rgba(0,255,136,0.3);z-index:90;cursor:pointer;border:none}.badge-qtd{background:#000;color:var(--neon);width:28px;height:28px;border-radius:50%;display:flex;align-items:center;justify-content:center;font-size:14px}#modal-bilhete{position:fixed;top:0;left:0;width:100%;height:100%;background:rgba(0,0,0,0.6);z-index:100;display:none;flex-direction:column;justify-content:flex-end;backdrop-filter:blur(5px)}.bilhete-conteudo{background:rgba(18,25,39,0.85);backdrop-filter:blur(20px);-webkit-backdrop-filter:blur(20px);border-top:1px solid var(--borda);width:100%;max-height:85vh;border-top-left-radius:24px;border-top-right-radius:24px;padding:24px;display:flex;flex-direction:column;animation:subirTela .3s ease-out forwards}@keyframes subirTela{from{transform:translateY(100%)}to{transform:translateY(0)}}.bilhete-header{display:flex;justify-content:space-between;align-items:center;margin-bottom:20px;border-bottom:1px solid var(--borda);padding-bottom:15px}.bilhete-titulo{font-size:20px;font-weight:900}.btn-fechar{background:rgba(9,14,23,0.8);border:1px solid var(--borda);color:var(--texto);width:36px;height:36px;border-radius:50%;font-weight:700;cursor:pointer}.lista-palpites{overflow-y:auto;max-height:35vh;margin-bottom:15px;padding-right:5px}.palpite-item{background:rgba(9,14,23,0.6);padding:14px;border-radius:12px;margin-bottom:10px;display:flex;justify-content:space-between;align-items:center;border:1px solid var(--borda);border-left:4px solid var(--neon)}.palpite-jogo{font-size:12px;color:var(--texto-secundario);font-weight:700;margin-bottom:5px}.palpite-escolha{font-size:15px;font-weight:900}.palpite-odd{font-weight:900;color:var(--neon);font-size:18px}.caixa-valores{background:rgba(5,8,12,0.8);padding:18px;border-radius:16px;border:1px solid var(--borda);margin-bottom:15px}.linha-valor{display:flex;justify-content:space-between;margin-bottom:12px;font-size:14px;font-weight:700;color:var(--texto-secundario)}.odd-final{color:var(--texto);font-size:18px;font-weight:900}.input-grana{width:100%;background:rgba(18,25,39,0.6);border:2px solid var(--borda);color:#fff;padding:16px;border-radius:12px;font-size:20px;font-weight:900;text-align:center;outline:0;margin-bottom:10px}.input-grana:focus{border-color:var(--neon)}.input-nome{width:100%;background:rgba(18,25,39,0.6);border:2px solid var(--borda);color:#fff;padding:12px;border-radius:12px;font-size:16px;font-weight:700;text-align:center;outline:0;margin-bottom:10px}.input-nome:focus{border-color:var(--neon)}.linha-retorno{display:flex;justify-content:space-between;align-items:center;margin-top:15px;font-weight:800}.retorno-verde{color:var(--neon);font-size:24px;font-weight:900}.btn-enviar-zap{width:100%;background:var(--neon);color:#000;padding:18px;border:none;border-radius:14px;font-weight:900;font-size:16px;cursor:pointer;text-transform:uppercase;margin-top:5px;box-shadow:0 4px 15px rgba(0,255,136,0.2)}.btn-apagar-tudo{background:0 0;border:none;color:var(--danger);font-size:13px;font-weight:700;margin-top:20px;width:100%;cursor:pointer;text-decoration:underline}.botao-fantasma{position:fixed;bottom:0;right:0;width:60px;height:60px;background:0 0;z-index:9999;cursor:default}#tela-login,#tela-admin{display:none;padding:25px;max-width:500px;margin:40px auto;background:rgba(18,25,39,0.7);backdrop-filter:blur(15px);border:1px solid var(--borda);border-radius:16px;box-shadow:0 10px 40px rgba(0,0,0,0.5)}.input-admin{width:100%;padding:16px;margin-bottom:15px;background:rgba(9,14,23,0.8);border:1px solid var(--borda);color:#fff;border-radius:8px;font-size:16px}.btn-admin{width:100%;background:var(--neon);color:#000;padding:18px;border:none;border-radius:8px;font-weight:900;cursor:pointer;margin-bottom:10px;font-size:16px}.btn-voltar{background:0 0;color:var(--texto-secundario);border:1px solid var(--borda)}#tela-digital{display:none;padding:20px;max-width:500px;margin:0 auto}.digital-card{background:rgba(18,25,39,0.7);backdrop-filter:blur(15px);border:1px solid var(--borda);border-radius:16px;padding:20px;margin-top:20px;box-shadow:0 10px 30px rgba(0,0,0,0.5)}.digital-header{text-align:center;border-bottom:2px dashed var(--borda);padding-bottom:15px;margin-bottom:15px}.digital-pin{font-size:28px;font-weight:900;color:var(--texto);letter-spacing:2px}.digital-status{display:inline-block;padding:6px 14px;border-radius:20px;font-size:13px;font-weight:900;margin-top:10px;border:1px solid transparent}
        
        /* CORES DOS STATUS */
        .status-0{background:rgba(245,166,35,0.15);color:var(--amarelo);border-color:var(--amarelo)}
        .status-1{background:rgba(0,195,255,0.15);color:var(--azul);border-color:var(--azul)}
        .status-2{background:rgba(0,255,136,0.15);color:var(--neon);border-color:var(--neon);box-shadow:0 0 15px rgba(0,255,136,0.2)}
        .status-3{background:rgba(255,71,87,0.15);color:var(--danger);border-color:var(--danger)}
        .status-4{background:rgba(138,150,168,0.15);color:var(--texto-secundario);border-color:var(--texto-secundario)}

        .digital-cliente{font-size:14px;color:var(--texto-secundario);margin-top:10px}.btn-voltar-home{width:100%;background:rgba(26,35,51,0.8);color:var(--texto);padding:15px;border:1px solid var(--borda);border-radius:12px;font-weight:700;cursor:pointer;margin-top:10px;transition:.2s}.btn-voltar-home:hover{background:rgba(26,35,51,1)}
        #toast-container{position:fixed;top:20px;right:20px;z-index:10000;display:flex;flex-direction:column;gap:10px;pointer-events:none}.toast{background:rgba(18,25,39,0.95);backdrop-filter:blur(10px);border-left:4px solid var(--neon);color:var(--texto);padding:16px 24px;border-radius:8px;font-weight:700;font-size:14px;box-shadow:0 4px 20px rgba(0,0,0,0.6);animation:deslizarIn .3s ease-out forwards;pointer-events:auto}.toast.erro{border-color:var(--danger)}@keyframes deslizarIn{from{transform:translateX(120%);opacity:0}to{transform:translateX(0);opacity:1}}@keyframes deslizarOut{from{transform:translateX(0);opacity:1}to{transform:translateX(120%);opacity:0}}
        .termos-rodape { margin-top: 30px; padding: 20px 15px; background: rgba(9, 14, 23, 0.4); border-top: 1px dashed var(--borda); font-size: 11px; color: var(--texto-secundario); line-height: 1.6; }
        .termos-rodape h3 { color: var(--texto); margin-bottom: 12px; font-size: 13px; text-transform: uppercase; text-align: center; letter-spacing: 1px; }
        .termos-rodape ul { list-style-type: none; padding: 0; max-width: 600px; margin: 0 auto; }
        .termos-rodape li { margin-bottom: 10px; padding-left: 15px; position: relative; text-align: justify; }
        .termos-rodape li::before { content: "•"; color: var(--neon); position: absolute; left: 0; top: -1px; font-size: 16px; }
        .historico-lista { margin-top: 25px; border-top: 1px dashed var(--borda); padding-top: 20px; }
        .historico-item { background: rgba(9,14,23,0.8); border-left: 4px solid var(--neon); padding: 12px; border-radius: 8px; margin-bottom: 10px; display: flex; flex-direction: column; gap: 10px; border-top: 1px solid var(--borda); border-right: 1px solid var(--borda); border-bottom: 1px solid var(--borda); }
        .historico-info { font-size: 13px; line-height: 1.4; display: flex; justify-content: space-between; align-items: center;}
        .historico-botoes { display: flex; gap: 6px; flex-wrap: wrap; justify-content: space-between; border-top: 1px dashed var(--borda); padding-top: 10px;}
        .btn-mini { padding: 8px; border: none; border-radius: 6px; font-weight: 700; cursor: pointer; font-size: 11px; text-transform: uppercase; flex: 1; text-align: center;}
        .btn-mini.ativo { background: var(--azul); color: #000; }
        .btn-mini.green { background: var(--neon); color: #000; }
        .btn-mini.red { background: var(--danger); color: #fff; }
        .btn-mini.cancelar { background: rgba(138,150,168,0.2); color: #8a96a8; border: 1px solid #8a96a8; }
        
        #overlay-loading { position: fixed; top: 0; left: 0; width: 100%; height: 100%; background: var(--bg-fundo); z-index: 9999; display: flex; flex-direction: column; align-items: center; justify-content: center; color: var(--neon); font-weight: 900; font-size: 18px; display: none; }
        .spinner { border: 4px solid rgba(255,255,255,0.1); border-top: 4px solid var(--neon); border-radius: 50%; width: 40px; height: 40px; animation: spin 1s linear infinite; margin-bottom: 15px; }
        @keyframes spin { 0% { transform: rotate(0deg); } 100% { transform: rotate(360deg); } }
    </style>
</head>
<body>
    <div id="toast-container"></div>
    <div id="overlay-loading">
        <div class="spinner"></div>
        <div id="loading-txt">Sincronizando Banco de Dados...</div>
    </div>
    
    <div id="tela-principal">
        <header>
            <div class="header-top">
                <div class="logo-wrapper" onclick="window.location.href=window.location.pathname">
                    <div class="logo-badge"><span>XR</span></div>
                    <div class="logo-typography">
                        <div class="logo-title"><strong>XR</strong> SPORTS</div>
                        <div class="logo-subtitle">A Banca Premium</div>
                    </div>
                </div>
                <button class="btn-sync" onclick="buscarJogosNaAPI()">🔄 Atualizar</button>
            </div>
            <div class="nav-ligas">
                <button class="liga-btn ativo" onclick="trocarLiga('soccer_brazil_campeonato', this)">🇧🇷 Brasileirão</button>
                <button class="liga-btn" onclick="trocarLiga('soccer_brazil_serie_b', this)">🇧🇷 Série B</button>
                <button class="liga-btn" onclick="trocarLiga('soccer_conmebol_copa_libertadores', this)">🌎 Libertadores</button>
                <button class="liga-btn" onclick="trocarLiga('soccer_conmebol_copa_sudamericana', this)">🌎 Sul-Americana</button>
                <button class="liga-btn" onclick="trocarLiga('soccer_argentina_primera_division', this)">🇦🇷 Argentino</button>
                <button class="liga-btn" onclick="trocarLiga('soccer_uefa_champs_league', this)">⭐ Champions League</button>
                <button class="liga-btn" onclick="trocarLiga('soccer_uefa_europa_league', this)">🟠 Europa League</button>
                <button class="liga-btn" onclick="trocarLiga('soccer_epl', this)">🏴󠁧󠁢󠁥󠁮󠁧󠁿 Premier League</button>
                <button class="liga-btn" onclick="trocarLiga('soccer_spain_la_liga', this)">🇪🇸 La Liga</button>
                <button class="liga-btn" onclick="trocarLiga('soccer_italy_serie_a', this)">🇮🇹 Serie A</button>
                <button class="liga-btn" onclick="trocarLiga('soccer_germany_bundesliga', this)">🇩🇪 Bundesliga</button>
                <button class="liga-btn" onclick="trocarLiga('soccer_france_ligue_one', this)">🇫🇷 Ligue 1</button>
                <button class="liga-btn" onclick="trocarLiga('soccer_portugal_primeira_liga', this)">🇵🇹 Primeira Liga</button>
                <button class="liga-btn" onclick="trocarLiga('soccer_fifa_world_cup', this)">🏆 Copa do Mundo</button>
            </div>
        </header>
        <div class="container">
            <div id="status-msg" style="display: none;"></div>
            <div id="container-jogos"></div>
        </div>

        <div class="termos-rodape">
            <h3>📜 Termos e Regras da Banca</h3>
            <ul>
                <li><strong>Alterações e Cancelamentos:</strong> O bilhete só poderá ser alterado no prazo máximo de <strong>10 minutos</strong> após a sua emissão.</li>
                <li><strong>Variação de Cotações:</strong> A odd oficial e válida será exclusivamente aquela registrada no momento da confirmação final pelo cambista.</li>
                <li><strong>Tempo Regulamentar:</strong> Apostas válidas apenas para os 90 min (+ acréscimos). Prorrogações e pênaltis não contam.</li>
            </ul>
        </div>
        <button id="btn-gaveta" onclick="abrirBilhete()">
            <span style="display:flex; align-items:center; gap:10px;"><div class="badge-qtd" id="gaveta-qtd">0</div>VER BILHETE</span>
            <span id="gaveta-odd">Odd: 1.00</span>
        </button>
        
        <div id="modal-bilhete">
            <div class="bilhete-conteudo">
                <div class="bilhete-header">
                    <div class="bilhete-titulo">🧾 Montar Bilhete</div>
                    <button class="btn-fechar" onclick="fecharBilhete()">X</button>
                </div>
                <div class="lista-palpites" id="lista-carrinho"></div>
                <div class="caixa-valores">
                    <input type="text" id="input-nome" class="input-nome" placeholder="👤 Qual o seu Nome?">
                    <input type="number" id="input-dinheiro" class="input-grana" placeholder="R$ Valor da Aposta" onkeyup="calcularLucro()">
                    <div class="linha-valor" style="margin-top: 10px;"><span>Cotação Total:</span><span class="odd-final" id="visor-odd">1.00</span></div>
                    <div class="linha-retorno"><span>Retorno Possível:</span><span class="retorno-verde" id="visor-retorno">R$ 0,00</span></div>
                </div>
                <button class="btn-enviar-zap" onclick="enviarParaAdmin()">Gerar e Enviar Link 📲</button>
                <button class="btn-apagar-tudo" onclick="limparBilhete()">🗑️ Cancelar Tudo</button>
            </div>
        </div>
        
        <div class="botao-fantasma" onclick="tentarAbrirAdmin()"></div>
    </div>
    
    <div id="tela-login">
        <h2 style="color: var(--neon); margin-bottom: 20px; text-align: center;">PAINEL DO CAMBISTA</h2>
        <input type="text" id="user" class="input-admin" placeholder="Usuário">
        <input type="password" id="pass" class="input-admin" placeholder="Senha">
        <button class="btn-admin" onclick="fazerLogin()">ENTRAR</button>
        <button class="btn-admin btn-voltar" onclick="fecharAdmin()">VOLTAR AO SITE</button>
    </div>
    
    <div id="tela-admin">
        <h2 style="color: var(--neon); margin-bottom: 10px;">DASHBOARD RICK</h2>
        <p style="color: var(--texto-secundario); font-size: 14px; margin-bottom: 15px;">Cole o link que o cliente te enviou para validar a aposta na nuvem.</p>
        <input type="text" id="codigo-recebido" class="input-admin" placeholder="Ex: seusite.com/?b=123456">
        <button class="btn-admin" onclick="gerarBilheteValidado()">VALIDAR NOVO BILHETE ✅</button>
        <button class="btn-admin btn-voltar" onclick="fecharAdmin()">VOLTAR AO SITE</button>
        
        <div class="historico-lista">
            <h3 style="color: #fff; margin-bottom: 15px; font-size: 16px; text-align: center;">📑 Gestão de Bilhetes na Nuvem</h3>
            <div id="lista-historico-admin"></div>
        </div>
    </div>

    <div id="tela-digital">
        <div style="display: flex; justify-content: center; margin-bottom: 25px; margin-top: 10px; transform: scale(1.15);">
            <div class="logo-wrapper">
                <div class="logo-badge"><span>XR</span></div>
                <div class="logo-typography">
                    <div class="logo-title"><strong>XR</strong> SPORTS</div>
                    <div class="logo-subtitle">A Banca Premium</div>
                </div>
            </div>
        </div>
        
        <div class="digital-card">
            <div class="digital-header">
                <div style="font-size: 12px; color: var(--texto-secundario); text-transform: uppercase;">Código do Bilhete</div>
                <div class="digital-pin" id="dig-pin">PIN-XXXX</div>
                <div class="digital-status status-0" id="dig-status">⏳ Carregando...</div>
                <div class="digital-cliente" id="dig-cliente">Cliente: ---</div>
                <div style="font-size: 12px; color: var(--texto-secundario); margin-top: 8px; font-weight: bold;" id="dig-data"></div>
            </div>
            <div id="dig-jogos"></div>
            <div style="border-top: 1px solid var(--borda); margin-top: 15px; padding-top: 15px;">
                <div style="display: flex; justify-content: space-between; font-size: 14px; margin-bottom: 5px; color: var(--texto-secundario);">
                    <span>Valor da Aposta:</span> <strong style="color: var(--texto);" id="dig-aposta">R$ 0,00</strong>
                </div>
                <div style="display: flex; justify-content: space-between; font-size: 14px; margin-bottom: 5px; color: var(--texto-secundario);">
                    <span>Cotação Total:</span> <strong style="color: var(--texto);" id="dig-odd">1.00</strong>
                </div>
                <div style="display: flex; justify-content: space-between; font-size: 18px; margin-top: 10px; font-weight: 900;">
                    <span>Retorno Potencial:</span> <strong style="color: var(--neon);" id="dig-retorno">R$ 0,00</strong>
                </div>
            </div>
        </div>
        <button class="btn-voltar-home" style="margin-top: 20px;" onclick="window.location.href=window.location.pathname">🏠 Ir para a Home de Apostas</button>
    </div>

    <script>
        const API_KEY = "31f6c50fbb36c963ce6be39a38371560"; 
        const NUMERO_WHATSAPP = "5582993729095"; 
        
        let ligaFoco = "soccer_brazil_campeonato";
        let nomeLigaFoco = "🇧🇷 Brasileirão";
        let jogosCarregados = [];
        let carrinho = [];
        
        // Memória local do Admin para guardar os links validados
        let historicoBilhetes = JSON.parse(localStorage.getItem('xrsports_historico_links')) || [];

        // --- SISTEMA DE 3 CLIQUES PARA O ADMIN ---
        let clicksAdmin = 0; let timerAdmin;
        function tentarAbrirAdmin() {
            clicksAdmin++; clearTimeout(timerAdmin);
            if(clicksAdmin >= 3) { abrirLogin(); clicksAdmin = 0; } 
            else { timerAdmin = setTimeout(() => { clicksAdmin = 0; }, 1000); }
        }

        function mostrarToast(mensagem, tipo = 'sucesso') {
            let container = document.getElementById('toast-container');
            let toast = document.createElement('div');
            toast.className = `toast ${tipo}`;
            toast.innerText = mensagem;
            container.appendChild(toast);
            setTimeout(() => { toast.style.animation = 'deslizarOut 0.3s ease-in forwards'; setTimeout(() => toast.remove(), 300); }, 3000);
        }

        function mostrarLoading(texto) {
            document.getElementById('loading-txt').innerText = texto;
            document.getElementById('overlay-loading').style.display = 'flex';
        }
        function esconderLoading() { document.getElementById('overlay-loading').style.display = 'none'; }

        // --- API JSONBLOB (BANCO DE DADOS FANTASMA) ---
        const URL_BLOB = "https://jsonblob.com/api/jsonBlob";
        
        async function salvarNaNuvem(dados) {
            try {
                let res = await fetch(URL_BLOB, {
                    method: 'POST',
                    headers: { 'Content-Type': 'application/json', 'Accept': 'application/json' },
                    body: JSON.stringify(dados)
                });
                let loc = res.headers.get('Location');
                return loc.split('/').pop(); // Retorna o ID gerado
            } catch(e) { return null; }
        }

        async function lerDaNuvem(blobId) {
            try {
                let res = await fetch(`${URL_BLOB}/${blobId}`);
                if(!res.ok) return null;
                return await res.json();
            } catch(e) { return null; }
        }

        async function atualizarNaNuvem(blobId, dados) {
            try {
                await fetch(`${URL_BLOB}/${blobId}`, {
                    method: 'PUT',
                    headers: { 'Content-Type': 'application/json', 'Accept': 'application/json' },
                    body: JSON.stringify(dados)
                });
                return true;
            } catch(e) { return false; }
        }

        function salvarCarrinho() { localStorage.setItem('xrsports_carrinho', JSON.stringify(carrinho)); }
        function carregarCarrinho() { let salvo = localStorage.getItem('xrsports_carrinho'); if(salvo) carrinho = JSON.parse(salvo); }

        const bancoDeEscudos={"brazil":"https://upload.wikimedia.org/wikipedia/pt/2/2b/Confedera%C3%A7%C3%A3o_Brasileira_de_Futebol_2019.svg","flamengo":"https://upload.wikimedia.org/wikipedia/commons/2/2e/Flamengo_braz_logo.svg","palmeiras":"https://upload.wikimedia.org/wikipedia/commons/1/10/Palmeiras_logo.svg","corinthians":"https://upload.wikimedia.org/wikipedia/pt/b/b4/Corinthians_simbolo.png","são paulo":"https://upload.wikimedia.org/wikipedia/commons/2/2b/S%C3%A3o_Paulo_Futebol_Clube.svg","fluminense":"https://upload.wikimedia.org/wikipedia/pt/a/a3/Fluminense_FC_escudo.png","crb":"https://upload.wikimedia.org/wikipedia/commons/6/64/CRB_logo.svg","arsenal":"https://upload.wikimedia.org/wikipedia/en/5/53/Arsenal_FC.svg","manchester city":"https://upload.wikimedia.org/wikipedia/en/e/eb/Manchester_City_FC_badge.svg"};
        let cacheEscudos = JSON.parse(localStorage.getItem('xrsports_escudos')) || {}; cacheEscudos = { ...cacheEscudos, ...bancoDeEscudos };

        function normalizarNomeParaBusca(nome) {
            let n = nome.trim().toLowerCase().normalize("NFD").replace(/[\u0300-\u036f]/g, "").replace(/-rj|-sp|-mg|-rs|-pr|-sc|-ba|-ce|-go|-pe/g, "").trim();
            const tradutor = { "crb": "clube de regatas brasil", "vasco": "vasco da gama", "atletico-mg": "atletico mineiro", "sport recife": "sport club do recife" };
            if (tradutor[n]) return tradutor[n]; return n.replace(/\bfc\b/g, "").trim();
        }

        function desenharEscudo(nome) {
            let n = nome.trim().toLowerCase();
            if (cacheEscudos[n]) return `<div class="escudo-container"><img src="${cacheEscudos[n]}" class="escudo-img"></div>`;
            let letra = normalizarNomeParaBusca(nome).substring(0, 1).toUpperCase();
            let cores = ["#ef4444", "#3b82f6", "#10b981", "#f59e0b", "#8b5cf6", "#ec4899"];
            let num = 0; for (let i = 0; i < nome.length; i++) num += nome.charCodeAt(i);
            return `<div class="escudo-container"><div class="escudo-letra" style="background:${cores[num % cores.length]}">${letra}</div></div>`;
        }

        window.onload = function() {
            const urlParams = new URLSearchParams(window.location.search);
            if(urlParams.has('b')) {
                document.getElementById('tela-principal').style.display = 'none';
                document.getElementById('tela-digital').style.display = 'block';
                montarBilheteDigital(urlParams.get('b'));
            } else { carregarCarrinho(); buscarJogosNaAPI(); }
        };

        function abrirLogin() { document.getElementById('tela-principal').style.display = 'none'; document.getElementById('tela-login').style.display = 'block'; }
        function fecharAdmin() { document.getElementById('tela-login').style.display = 'none'; document.getElementById('tela-admin').style.display = 'none'; document.getElementById('tela-principal').style.display = 'block'; }
        
        function fazerLogin() {
            if(document.getElementById('user').value === 'RickAlves76' && document.getElementById('pass').value === 'admin') {
                document.getElementById('tela-login').style.display = 'none'; document.getElementById('tela-admin').style.display = 'block';
                document.getElementById('user').value = ''; document.getElementById('pass').value = ''; 
                mostrarToast("Acesso Liberado, Chefe!");
                carregarHistoricoAdmin(); 
            } else { mostrarToast("Usuário ou senha incorretos!", "erro"); }
        }

        // --- DASHBOARD ADMIN (LENDO DA NUVEM) ---
        async function carregarHistoricoAdmin() {
            let container = document.getElementById('lista-historico-admin');
            if (historicoBilhetes.length === 0) {
                container.innerHTML = '<p style="color: var(--texto-secundario); font-size: 13px; text-align: center;">Nenhum bilhete salvo no seu painel.</p>';
                return;
            }
            container.innerHTML = '<div style="text-align:center"><div class="spinner" style="margin:0 auto"></div><p style="font-size:12px; margin-top:10px;">Buscando status ao vivo...</p></div>';
            
            let html = "";
            for (let i = 0; i < historicoBilhetes.length; i++) {
                let id = historicoBilhetes[i];
                let b = await lerDaNuvem(id);
                if (b) {
                    let retorno = (b.v * b.o).toLocaleString('pt-BR', { style: 'currency', currency: 'BRL' });
                    let stsTxt = "⏳ Aguardando"; let corB = "var(--amarelo)";
                    if(b.s === 1) { stsTxt = "✅ Ativo"; corB = "var(--azul)"; }
                    if(b.s === 2) { stsTxt = "🟢 GREEN"; corB = "var(--neon)"; }
                    if(b.s === 3) { stsTxt = "🔴 RED"; corB = "var(--danger)"; }
                    if(b.s === 4) { stsTxt = "⚪ Cancelado"; corB = "var(--texto-secundario)"; }

                    html += `
                    <div class="historico-item" style="border-left-color: ${corB}">
                        <div class="historico-info">
                            <div><strong style="color:var(--neon)">${b.p}</strong> - 👤 ${b.n}<br>
                            <span style="color:var(--texto-secundario)">R$ ${b.v.toFixed(2)} ➡️ <strong style="color:#fff">${retorno}</strong></span></div>
                            <div style="font-weight:900; color:${corB}">${stsTxt}</div>
                        </div>
                        <div class="historico-botoes">
                            <button class="btn-mini ativo" onclick="window.open('?b=${id}', '_blank')">🔗 Ver</button>
                            <button class="btn-mini green" onclick="alterarStatusAdmin('${id}', 2)">🟢 Dar Green</button>
                            <button class="btn-mini red" onclick="alterarStatusAdmin('${id}', 3)">🔴 Dar Red</button>
                            <button class="btn-mini cancelar" onclick="alterarStatusAdmin('${id}', 4)">X Cancelar</button>
                        </div>
                    </div>`;
                }
            }
            container.innerHTML = html === "" ? '<p style="color: var(--texto-secundario); font-size: 13px; text-align: center;">Nenhum bilhete encontrado.</p>' : html;
        }

        async function alterarStatusAdmin(blobId, novoStatus) {
            mostrarLoading("Atualizando Nuvem...");
            let dados = await lerDaNuvem(blobId);
            if (dados) {
                dados.s = novoStatus;
                await atualizarNaNuvem(blobId, dados);
                mostrarToast("Status atualizado com sucesso!");
                carregarHistoricoAdmin();
            }
            esconderLoading();
        }

        async function gerarBilheteValidado() {
            let codigoLink = document.getElementById('codigo-recebido').value.trim();
            if(!codigoLink) { mostrarToast("Cole o link do cliente primeiro!", "erro"); return; }
            
            let partes = codigoLink.split('?b=');
            let blobId = partes.length > 1 ? partes[1] : codigoLink;
            
            mostrarLoading("Buscando Bilhete...");
            let dados = await lerDaNuvem(blobId);
            if(dados) {
                dados.s = 1; 
                let agora = new Date(); dados.d = agora.toLocaleDateString('pt-BR') + ' às ' + agora.toLocaleTimeString('pt-BR', {hour: '2-digit', minute:'2-digit'});
                await atualizarNaNuvem(blobId, dados);
                
                if(!historicoBilhetes.includes(blobId)) {
                    historicoBilhetes.unshift(blobId);
                    localStorage.setItem('xrsports_historico_links', JSON.stringify(historicoBilhetes));
                }
                
                document.getElementById('codigo-recebido').value = '';
                mostrarToast("Bilhete Validado Oficialmente!");
                carregarHistoricoAdmin();
            } else {
                mostrarToast("Bilhete não encontrado na nuvem!", "erro");
            }
            esconderLoading();
        }

        // --- SISTEMA CLIENTE (MONTAR E ACOMPANHAR) ---
        async function enviarParaAdmin() {
            let nomeCli = document.getElementById('input-nome').value.trim();
            if(!nomeCli) { mostrarToast("Digite seu nome antes de gerar o bilhete!", "erro"); return; }
            let valorDep = parseFloat(document.getElementById('input-dinheiro').value);
            if(isNaN(valorDep) || valorDep < 2) { mostrarToast("O valor mínimo é R$ 2,00!", "erro"); return; }
            
            let oddNumerica = parseFloat(document.getElementById('visor-odd').innerText);
            if(oddNumerica < 1.60) { mostrarToast("A cotação mínima é 1.60!", "erro"); return; }

            let l1 = "ABCDEFGHIJKLMNOPQRSTUVWXYZ".charAt(Math.floor(Math.random() * 26)), l2 = "ABCDEFGHIJKLMNOPQRSTUVWXYZ".charAt(Math.floor(Math.random() * 26));
            let codigoPIN = `PIN-${l1}${l2}${Math.floor(1000 + Math.random() * 9000)}`;
            
            let pacoteDados = { p: codigoPIN, n: nomeCli, v: valorDep, o: oddNumerica, j: carrinho, s: 0, d: "" };
            
            mostrarLoading("Gerando Link Seguro...");
            let blobId = await salvarNaNuvem(pacoteDados);
            esconderLoading();

            if (blobId) {
                let linkAcompanhar = window.location.origin + window.location.pathname + "?b=" + blobId;
                let textoZap = `⚡ *XR SPORTS - NOVA APOSTA* ⚡%0A👤 Nome: *${nomeCli}*%0A📌 PIN: *${codigoPIN}*%0A💰 Valor: *R$ ${valorDep.toFixed(2)}*%0A%0A👉 *Rick, valide meu bilhete no link abaixo:*%0A${linkAcompanhar}`;
                window.open(`https://wa.me/${NUMERO_WHATSAPP}?text=${textoZap}`, '_blank');
            } else {
                mostrarToast("Erro ao conectar no banco de dados. Tente novamente.", "erro");
            }
        }

        async function montarBilheteDigital(blobId) {
            document.getElementById('dig-status').innerText = "⏳ Buscando Dados...";
            let dados = await lerDaNuvem(blobId);
            
            if (!dados) { alert("Link Inválido ou Bilhete Expirado."); window.location.href = window.location.pathname; return; }

            document.getElementById('dig-pin').innerText = dados.p; 
            document.getElementById('dig-cliente').innerText = `👤 Jogador: ${dados.n}`;
            document.getElementById('dig-aposta').innerText = `R$ ${dados.v.toFixed(2)}`; 
            document.getElementById('dig-odd').innerText = dados.o.toFixed(2);
            document.getElementById('dig-retorno').innerText = (dados.v * dados.o).toLocaleString('pt-BR', { style: 'currency', currency: 'BRL' });
            
            let selo = document.getElementById('dig-status');
            selo.className = `digital-status status-${dados.s}`;
            
            if (dados.s === 0) { selo.innerText = "⏳ Pendente de Pagamento/Validação"; document.getElementById('dig-data').innerText = "Aguarde o cambista aprovar."; }
            else if (dados.s === 1) { selo.innerText = "✅ BILHETE ATIVO (VALIDADO)"; document.getElementById('dig-data').innerText = `📅 Validado em: ${dados.d}`; }
            else if (dados.s === 2) { selo.innerText = "🟢 BILHETE PREMIADO (GREEN)"; document.getElementById('dig-data').innerText = "🏆 Parabéns! Procure o cambista para receber."; }
            else if (dados.s === 3) { selo.innerText = "🔴 NÃO BATEU (RED)"; document.getElementById('dig-data').innerText = "Mais sorte na próxima vez!"; }
            else if (dados.s === 4) { selo.innerText = "⚪ BILHETE CANCELADO / DEVOLVIDO"; document.getElementById('dig-data').innerText = "Aposta anulada."; }

            let htmlJogos = "";
            dados.j.forEach(jogo => { htmlJogos += `<div style="background: rgba(9, 14, 23, 0.6); padding: 12px; border-radius: 10px; margin-bottom: 10px; border-left: 4px solid var(--neon);"><div style="font-size: 11px; color: var(--texto-secundario); margin-bottom: 4px;">${jogo.tituloJogo}</div><div style="display: flex; justify-content: space-between; align-items: center;"><span style="font-size: 15px; font-weight: 900;">${jogo.palpite}</span><span style="color: var(--neon); font-weight: 900;">Odd: ${jogo.oddAposta.toFixed(2)}</span></div></div>`; });
            document.getElementById('dig-jogos').innerHTML = htmlJogos;
        }

        function arrumarData(dataIso) { let dt = new Date(dataIso); return `${dt.getDate().toString().padStart(2, '0')}/${(dt.getMonth() + 1).toString().padStart(2, '0')} às ${dt.getHours().toString().padStart(2, '0')}:${dt.getMinutes().toString().padStart(2, '0')}`; }

        function trocarLiga(chave, botao) { document.querySelectorAll('.liga-btn').forEach(b => b.classList.remove('ativo')); botao.classList.add('ativo'); ligaFoco = chave; nomeLigaFoco = botao.innerText; buscarJogosNaAPI(); }

        // --- SISTEMA DE ODDS (API FUTEBOL) ---
        async function buscarJogosNaAPI() {
            let painelAviso = document.getElementById('status-msg');
            document.getElementById('container-jogos').innerHTML = "";
            painelAviso.style.display = "block";
            painelAviso.innerHTML = `⏳ Analisando mercados e placares ao vivo para:<br><strong style="color:var(--neon)">${nomeLigaFoco}</strong>...`;

            const linkOdds = `https://api.the-odds-api.com/v4/sports/${ligaFoco}/odds/?apiKey=${API_KEY}&regions=eu,us&markets=h2h,totals`;
            const linkScores = `https://api.the-odds-api.com/v4/sports/${ligaFoco}/scores/?apiKey=${API_KEY}`;

            try {
                const [reqOdds, reqScores] = await Promise.all([fetch(linkOdds), fetch(linkScores)]);
                const resOdds = await reqOdds.json(); const resScores = await reqScores.json();
                if(resOdds.message) { painelAviso.innerHTML = `⚠️ Aviso: ${resOdds.message}`; return; }

                let horaAtual = new Date(); let horaLimiteSumir = new Date(horaAtual.getTime() - (2 * 60 * 60 * 1000));
                jogosCarregados = []; let mapaScores = {};
                if(Array.isArray(resScores)) { resScores.forEach(s => { mapaScores[s.id] = s; }); }

                resOdds.forEach(jogo => {
                    let horaDoJogo = new Date(jogo.commence_time); let dadosScore = mapaScores[jogo.id];
                    if ((dadosScore && dadosScore.completed) || horaDoJogo < horaLimiteSumir || !jogo.bookmakers || jogo.bookmakers.length === 0) return; 

                    let placarC = "", placarF = ""; let isIntervalo = false; let isLive = horaDoJogo <= horaAtual;
                    let minutosCorridos = isLive ? Math.floor((horaAtual - horaDoJogo) / 60000) : 0;
                    if(isLive && dadosScore && dadosScore.scores && dadosScore.scores.length > 0) {
                        let scoreCasa = dadosScore.scores.find(s => s.name === jogo.home_team); let scoreFora = dadosScore.scores.find(s => s.name === jogo.away_team);
                        if(scoreCasa && scoreFora) { placarC = scoreCasa.score; placarF = scoreFora.score; }
                    }
                    if (minutosCorridos >= 46 && minutosCorridos <= 60) { isIntervalo = true; }

                    let oddC = 0, oddE = 0, oddF = 0, oddM15 = 0, oddN15 = 0, oddM25 = 0, oddN25 = 0, oddBttsSim = 0, oddBttsNao = 0;
                    let oddCrtM25 = 0, oddCrtN25 = 0; 

                    jogo.bookmakers.forEach(bm => {
                        let mH2H = bm.markets.find(m => m.key === 'h2h');
                        if(mH2H && oddC === 0) mH2H.outcomes.forEach(opc => { if(opc.name === jogo.home_team) oddC = opc.price; else if(opc.name === 'Draw') oddE = opc.price; else if(opc.name === jogo.away_team) oddF = opc.price; });
                        let mGols = bm.markets.find(m => m.key === 'totals');
                        if(mGols) mGols.outcomes.forEach(opc => {
                            if(opc.name === 'Over') { if(opc.point === 1.5) oddM15 = Math.max(oddM15, opc.price); if(opc.point === 2.5) oddM25 = Math.max(oddM25, opc.price); }
                            if(opc.name === 'Under') { if(opc.point === 1.5) oddN15 = Math.max(oddN15, opc.price); if(opc.point === 2.5) oddN25 = Math.max(oddN25, opc.price); }
                        });
                    });

                    const juice = 0.92; let odd1X = 0, odd12 = 0, oddX2 = 0, oddDnbCasa = 0, oddDnbFora = 0, oddC_HT = 0, oddE_HT = 0, oddF_HT = 0;
                    if(oddC > 0 && oddE > 0 && oddF > 0) {
                        let probC = 1 / oddC, probE = 1 / oddE, probF = 1 / oddF;
                        odd1X = (1 / (probC + probE)) * juice; odd12 = (1 / (probC + probF)) * juice; oddX2 = (1 / (probF + probE)) * juice;
                        oddDnbCasa = (1 / (probC / (probC + probF))) * juice; oddDnbFora = (1 / (probF / (probC + probF))) * juice;
                        let probE_HT = Math.min(0.55, probE * 1.45); let probRestante = 1 - probE_HT; let pesoCasa = probC / (probC + probF);
                        oddC_HT = (1 / (probRestante * pesoCasa)) * juice; oddE_HT = (1 / probE_HT) * juice; oddF_HT = (1 / (probRestante * (1 - pesoCasa))) * juice;

                        // Criando odds sintéticas dinâmicas para Cartões Amarelos (+/- 2.5)
                        let variacaoCartao = (Math.random() * 0.1); 
                        let probM25Cartoes = 0.70 + variacaoCartao; // Média alta de cartões
                        oddCrtM25 = (1 / probM25Cartoes) * juice;
                        oddCrtN25 = (1 / (1 - probM25Cartoes)) * juice;
                    }
                    if (oddM25 > 0 && oddM15 === 0) { let pM25 = 1 / oddM25; let pM15 = Math.min(0.95, pM25 * 1.35); oddM15 = (1 / pM15) * juice; oddN15 = (1 / (1-pM15)) * juice; }
                    if (oddM25 > 0) { let pBttsSim = Math.min(0.88, (1 / oddM25) * 1.05); oddBttsSim = (1 / pBttsSim) * juice; oddBttsNao = (1 / (1 - pBttsSim)) * juice; } else if (oddC > 0) { oddBttsSim = 1.85 * juice; oddBttsNao = 1.85 * juice; }

                    const clampOdd = (val) => val > 0 ? Math.max(1.05, val) : 0;
                    odd1X = clampOdd(odd1X); odd12 = clampOdd(odd12); oddX2 = clampOdd(oddX2); oddDnbCasa = clampOdd(oddDnbCasa); oddDnbFora = clampOdd(oddDnbFora); oddC_HT = clampOdd(oddC_HT); oddE_HT = clampOdd(oddE_HT); oddF_HT = clampOdd(oddF_HT); oddBttsSim = clampOdd(oddBttsSim); oddBttsNao = clampOdd(oddBttsNao); 
                    if(oddM15 > 0) { oddM15 = clampOdd(oddM15); oddN15 = clampOdd(oddN15); }
                    if(oddCrtM25 > 0) { oddCrtM25 = clampOdd(oddCrtM25); oddCrtN25 = clampOdd(oddCrtN25); }

                    if(oddC > 0 && oddF > 0) {
                        jogosCarregados.push({
                            id: jogo.id, casa: jogo.home_team, fora: jogo.away_team, oddC, oddE, oddF, odd1X, odd12, oddX2, oddDnbCasa, oddDnbFora, oddBttsSim, oddBttsNao, oddM15, oddN15, oddM25, oddN25, oddC_HT, oddE_HT, oddF_HT, oddCrtM25, oddCrtN25, dataCrua: horaDoJogo, dataVisual: arrumarData(jogo.commence_time), isLive, isIntervalo, minutosCorridos, placarC, placarF
                        });
                    }
                });

                if(jogosCarregados.length === 0) { painelAviso.innerHTML = `⚽ Mercado Fechado para ${nomeLigaFoco}.`; return; }
                jogosCarregados.sort((a, b) => a.dataCrua - b.dataCrua); painelAviso.style.display = "none";
                let idsVivos = jogosCarregados.map(j => j.id); carrinho = carrinho.filter(c => idsVivos.includes(c.idJogo));
                salvarCarrinho(); atualizarGaveta(); pintarJogosNaTela();
            } catch (erro) { painelAviso.innerHTML = `❌ Erro de conexão. Verifique sua internet.`; }
        }

        function pintarJogosNaTela() {
            let htmlHTML = "";
            jogosCarregados.forEach(j => {
                let badgeDaHora = j.isLive ? (j.isIntervalo ? `<div class="badge-horario badge-intervalo">⏸️ INTERVALO</div>` : `<div class="badge-horario badge-aovivo">🔴 AO VIVO</div>`) : `<div class="badge-horario">📅 ${j.dataVisual}</div>`;
                let centroPlacar = `<div class="vs-txt">X</div>`; let placarCInt = 0; let placarFInt = 0;
                if (j.isLive && j.placarC !== "" && j.placarF !== "") { centroPlacar = `<div class="placar-live">${j.placarC} - ${j.placarF}</div>`; placarCInt = parseInt(j.placarC) || 0; placarFInt = parseInt(j.placarF) || 0; }
                let totalGols = placarCInt + placarFInt; let isBtts = placarCInt > 0 && placarFInt > 0;
                
                let blocoDuchance = j.odd1X > 0 ? `<div class="mercado-titulo">Dupla Chance</div><div class="odds-linha"><div class="odd-btn" id="btn-${j.id}-1X" onclick="clicarNaOdd('${j.id}', '${j.casa} x ${j.fora}', '${j.casa} ou Emp', ${j.odd1X}, '1X')"><span class="odd-lbl">Casa/Emp</span><span class="odd-val">${j.odd1X.toFixed(2)}</span></div><div class="odd-btn" id="btn-${j.id}-12" onclick="clicarNaOdd('${j.id}', '${j.casa} x ${j.fora}', '${j.casa} ou ${j.fora}', ${j.odd12}, '12')"><span class="odd-lbl">Casa/Fora</span><span class="odd-val">${j.odd12.toFixed(2)}</span></div><div class="odd-btn" id="btn-${j.id}-X2" onclick="clicarNaOdd('${j.id}', '${j.casa} x ${j.fora}', '${j.fora} ou Emp', ${j.oddX2}, 'X2')"><span class="odd-lbl">Fora/Emp</span><span class="odd-val">${j.oddX2.toFixed(2)}</span></div></div>` : "";
                let blocoDnb = j.oddDnbCasa > 0 ? `<div class="mercado-titulo">Empate Anula</div><div class="odds-linha-dupla"><div class="odd-btn" id="btn-${j.id}-DNBC" onclick="clicarNaOdd('${j.id}', '${j.casa} x ${j.fora}', '${j.casa} (DNB)', ${j.oddDnbCasa}, 'DNBC')"><span class="odd-lbl">Casa</span><span class="odd-val">${j.oddDnbCasa.toFixed(2)}</span></div><div class="odd-btn" id="btn-${j.id}-DNBF" onclick="clicarNaOdd('${j.id}', '${j.casa} x ${j.fora}', '${j.fora} (DNB)', ${j.oddDnbFora}, 'DNBF')"><span class="odd-lbl">Fora</span><span class="odd-val">${j.oddDnbFora.toFixed(2)}</span></div></div>` : "";
                let blocoBtts = (j.oddBttsSim > 0 && !isBtts) ? `<div class="mercado-titulo">Ambas Marcam</div><div class="odds-linha-dupla"><div class="odd-btn" id="btn-${j.id}-BTTSY" onclick="clicarNaOdd('${j.id}', '${j.casa} x ${j.fora}', 'Ambas - Sim', ${j.oddBttsSim}, 'BTTSY')"><span class="odd-lbl">Sim</span><span class="odd-val">${j.oddBttsSim.toFixed(2)}</span></div><div class="odd-btn" id="btn-${j.id}-BTTSN" onclick="clicarNaOdd('${j.id}', '${j.casa} x ${j.fora}', 'Ambas - Não', ${j.oddBttsNao}, 'BTTSN')"><span class="odd-lbl">Não</span><span class="odd-val">${j.oddBttsNao.toFixed(2)}</span></div></div>` : "";
                let botoesGols = ((j.oddM15 > 0 && totalGols < 2) ? `<div class="odd-btn" id="btn-${j.id}-M15" onclick="clicarNaOdd('${j.id}', '${j.casa} x ${j.fora}', '+ 1.5 Gols', ${j.oddM15}, 'M15')"><span class="odd-lbl">+ 1.5 Gols</span><span class="odd-val">${j.oddM15.toFixed(2)}</span></div>` : "") + ((j.oddN15 > 0 && totalGols < 2) ? `<div class="odd-btn" id="btn-${j.id}-N15" onclick="clicarNaOdd('${j.id}', '${j.casa} x ${j.fora}', '- 1.5 Gols', ${j.oddN15}, 'N15')"><span class="odd-lbl">- 1.5 Gols</span><span class="odd-val">${j.oddN15.toFixed(2)}</span></div>` : "") + ((j.oddM25 > 0 && totalGols < 3) ? `<div class="odd-btn" id="btn-${j.id}-M25" onclick="clicarNaOdd('${j.id}', '${j.casa} x ${j.fora}', '+ 2.5 Gols', ${j.oddM25}, 'M25')"><span class="odd-lbl">+ 2.5 Gols</span><span class="odd-val">${j.oddM25.toFixed(2)}</span></div>` : "") + ((j.oddN25 > 0 && totalGols < 3) ? `<div class="odd-btn" id="btn-${j.id}-N25" onclick="clicarNaOdd('${j.id}', '${j.casa} x ${j.fora}', '- 2.5 Gols', ${j.oddN25}, 'N25')"><span class="odd-lbl">- 2.5 Gols</span><span class="odd-val">${j.oddN25.toFixed(2)}</span></div>` : "");
                let blocoGols = botoesGols !== "" ? `<div class="mercado-titulo">Total de Gols</div><div class="odds-linha-dupla">${botoesGols}</div>` : "";
                let botoesCartoes = ((j.oddCrtM25 > 0) ? `<div class="odd-btn" id="btn-${j.id}-CM25" onclick="clicarNaOdd('${j.id}', '${j.casa} x ${j.fora}', '+ 2.5 Cartões', ${j.oddCrtM25}, 'CM25')"><span class="odd-lbl">+ 2.5</span><span class="odd-val">${j.oddCrtM25.toFixed(2)}</span></div>` : "") + ((j.oddCrtN25 > 0) ? `<div class="odd-btn" id="btn-${j.id}-CN25" onclick="clicarNaOdd('${j.id}', '${j.casa} x ${j.fora}', '- 2.5 Cartões', ${j.oddCrtN25}, 'CN25')"><span class="odd-lbl">- 2.5</span><span class="odd-val">${j.oddCrtN25.toFixed(2)}</span></div>` : "");
                let blocoCartoes = botoesCartoes !== "" ? `<div class="mercado-titulo">Cartões Amarelos</div><div class="odds-linha-dupla">${botoesCartoes}</div>` : "";
                let blocoHT = j.oddC_HT > 0 ? `<div class="mercado-titulo">Vencedor - 1º Tempo</div><div class="odds-linha"><div class="odd-btn" id="btn-${j.id}-1HT" onclick="clicarNaOdd('${j.id}', '${j.casa} x ${j.fora}', '${j.casa} (1ºT)', ${j.oddC_HT}, '1HT')"><span class="odd-lbl">Casa</span><span class="odd-val">${j.oddC_HT.toFixed(2)}</span></div><div class="odd-btn" id="btn-${j.id}-XHT" onclick="clicarNaOdd('${j.id}', '${j.casa} x ${j.fora}', 'Empate (1ºT)', ${j.oddE_HT}, 'XHT')"><span class="odd-lbl">Empate</span><span class="odd-val">${j.oddE_HT.toFixed(2)}</span></div><div class="odd-btn" id="btn-${j.id}-2HT" onclick="clicarNaOdd('${j.id}', '${j.casa} x ${j.fora}', '${j.fora} (1ºT)', ${j.oddF_HT}, '2HT')"><span class="odd-lbl">Fora</span><span class="odd-val">${j.oddF_HT.toFixed(2)}</span></div></div>` : "";

                htmlHTML += `<div class="card-jogo"><div class="card-topo"><span class="liga-tag">${nomeLigaFoco}</span>${badgeDaHora}</div><div class="placar-box"><div class="time-box">${desenharEscudo(j.casa)}<span class="nome-time">${j.casa}</span></div>${centroPlacar}<div class="time-box visitante">${desenharEscudo(j.fora)}<span class="nome-time">${j.fora}</span></div></div><div class="mercado-titulo">Vencedor Final</div><div class="odds-linha"><div class="odd-btn" id="btn-${j.id}-1" onclick="clicarNaOdd('${j.id}', '${j.casa} x ${j.fora}', '${j.casa}', ${j.oddC}, '1')"><span class="odd-lbl">Casa</span><span class="odd-val">${j.oddC.toFixed(2)}</span></div><div class="odd-btn" id="btn-${j.id}-X" onclick="clicarNaOdd('${j.id}', '${j.casa} x ${j.fora}', 'Empate', ${j.oddE}, 'X')"><span class="odd-lbl">Empate</span><span class="odd-val">${j.oddE > 0 ? j.oddE.toFixed(2) : '-'}</span></div><div class="odd-btn" id="btn-${j.id}-2" onclick="clicarNaOdd('${j.id}', '${j.casa} x ${j.fora}', '${j.fora}', ${j.oddF}, '2')"><span class="odd-lbl">Fora</span><span class="odd-val">${j.oddF.toFixed(2)}</span></div></div>${blocoHT}${blocoDuchance}${blocoDnb}${blocoBtts}${blocoGols}${blocoCartoes}</div>`;
            });
            document.getElementById('container-jogos').innerHTML = htmlHTML;
            carrinho.forEach(c => { let b = document.getElementById(`btn-${c.idJogo}-${c.tipoOpcao}`); if(b) b.classList.add('selecionado'); });
        }

        function clicarNaOdd(idJogo, tituloJogo, palpite, oddAposta, tipoOpcao) {
            if(!oddAposta || oddAposta === 0) return;
            let jogoAtual = jogosCarregados.find(j => j.id === idJogo);
            
            const gruposMercado = { '1': 'pr', 'X': 'pr', '2': 'pr', '1X': 'pr', '12': 'pr', 'X2': 'pr', 'DNBC': 'pr', 'DNBF': 'pr', '1HT': 'pr', 'XHT': 'pr', '2HT': 'pr', 'BTTSY': 'bt', 'BTTSN': 'bt', 'M15': 'go', 'N15': 'go', 'M25': 'go', 'N25': 'go', 'CM25': 'ca', 'CN25': 'ca' };
            let meuGrupo = gruposMercado[tipoOpcao]; let selecoesNesteJogo = carrinho.filter(c => c.idJogo === idJogo); let jaSelecionado = selecoesNesteJogo.find(c => c.tipoOpcao === tipoOpcao);

            if (!jaSelecionado && carrinho.length > 0) {
                let temLiveCart = false, temPreCart = false;
                carrinho.forEach(c => { let j = jogosCarregados.find(jg => jg.id === c.idJogo); if(j) { if(j.isLive) temLiveCart = true; else temPreCart = true; } });
                let isCurrentLive = jogoAtual ? jogoAtual.isLive : false;
                if ((isCurrentLive && temPreCart) || (!isCurrentLive && temLiveCart)) { mostrarToast("⚠️ Não é permitido misturar jogos Ao Vivo com Pré-jogo!", "erro"); return; }
            }

            if (jaSelecionado) {
                carrinho = carrinho.filter(c => !(c.idJogo === idJogo && c.tipoOpcao === tipoOpcao));
                document.getElementById(`btn-${idJogo}-${tipoOpcao}`).classList.remove('selecionado');
            } else {
                let contagemPorJogo = {}; carrinho.forEach(c => { contagemPorJogo[c.idJogo] = (contagemPorJogo[c.idJogo] || 0) + 1; });
                let numJogosCombinados = 0; for (let jogo in contagemPorJogo) { if (contagemPorJogo[jogo] >= 1) numJogosCombinados++; }
                let isNovoCombinado = (contagemPorJogo[idJogo] || 0) === 1;
                if (isNovoCombinado && numJogosCombinados >= 2) {
                    let totalCombinadosAtuais = Object.values(contagemPorJogo).filter(qtd => qtd > 1).length;
                    if (totalCombinadosAtuais >= 2) { mostrarToast("Limite de 2 jogos diferentes na aposta combinada!", "erro"); return; }
                }
                let indexConflito = carrinho.findIndex(c => c.idJogo === idJogo && gruposMercado[c.tipoOpcao] === meuGrupo);
                if (indexConflito > -1) {
                    let opcRemovida = carrinho[indexConflito].tipoOpcao; carrinho.splice(indexConflito, 1);
                    let btnRemover = document.getElementById(`btn-${idJogo}-${opcRemovida}`); if(btnRemover) btnRemover.classList.remove('selecionado');
                }
                carrinho.push({ idJogo, tituloJogo, palpite, oddAposta, tipoOpcao });
                document.getElementById(`btn-${idJogo}-${tipoOpcao}`).classList.add('selecionado');
            }
            salvarCarrinho(); atualizarGaveta();
        }

        function atualizarGaveta() {
            let gaveta = document.getElementById('btn-gaveta'); let mult = 1;
            if(carrinho.length === 0) { gaveta.style.display = 'none'; fecharBilhete(); return; }
            carrinho.forEach(c => mult *= c.oddAposta); gaveta.style.display = 'flex';
            document.getElementById('gaveta-qtd').innerText = carrinho.length; document.getElementById('gaveta-odd').innerText = `Odd: ${mult.toFixed(2)}`; document.getElementById('visor-odd').innerText = mult.toFixed(2);
            let html = ""; carrinho.forEach(c => { html += `<div class="palpite-item"><div><div class="palpite-jogo">${c.tituloJogo}</div><div class="palpite-escolha">${c.palpite}</div></div><div class="palpite-odd">${c.oddAposta.toFixed(2)}</div></div>`; });
            document.getElementById('lista-carrinho').innerHTML = html; calcularLucro();
        }

        function calcularLucro() {
            let grana = parseFloat(document.getElementById('input-dinheiro').value), cota = parseFloat(document.getElementById('visor-odd').innerText), display = document.getElementById('visor-retorno');
            if(isNaN(grana) || grana <= 0) display.innerText = "R$ 0,00"; else display.innerText = (grana * cota).toLocaleString('pt-BR', { style: 'currency', currency: 'BRL' });
        }

        function limparBilhete() { carrinho = []; document.querySelectorAll('.odd-btn').forEach(b => b.classList.remove('selecionado')); document.getElementById('input-dinheiro').value = ""; salvarCarrinho(); atualizarGaveta(); mostrarToast("Bilhete limpo com sucesso!"); }
        function abrirBilhete() { document.getElementById('modal-bilhete').style.display = 'flex'; }
        function fecharBilhete() { document.getElementById('modal-bilhete').style.display = 'none'; }
    </script>
</body>
</html>
