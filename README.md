<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Postulación - Pixeled Community</title>
<link href="https://fonts.googleapis.com/css2?family=Rajdhani:wght@500;600;700&family=Nunito:wght@400;500;600&display=swap" rel="stylesheet">
<style>
  :root{--purple:#7F77DD;--purple-d:#534AB7;--purple-bg:#1E1B3A;--bg:#0D0D0D;--surface:#151515;--surface2:#1E1E1E;--border:#2A2A2A;--text:#F0F0F0;--text-muted:#888;--success:#3DB87A;--error:#E24B4A;}
  *{box-sizing:border-box;margin:0;padding:0;}
  body{background:var(--bg);color:var(--text);font-family:'Nunito',sans-serif;min-height:100vh;padding:2rem 1rem;}
  body::before{content:'';position:fixed;top:0;left:0;width:100%;height:100%;background:radial-gradient(ellipse at 20% 20%,rgba(127,119,221,.07) 0%,transparent 60%),radial-gradient(ellipse at 80% 80%,rgba(83,74,183,.05) 0%,transparent 60%);pointer-events:none;z-index:0;}
  .wrap{max-width:700px;margin:0 auto;position:relative;z-index:1;}
  .header{text-align:center;margin-bottom:2.5rem;}
  .logo-img{width:96px;height:96px;object-fit:contain;margin-bottom:1rem;image-rendering:pixelated;}
  .title{font-family:'Rajdhani',sans-serif;font-size:32px;font-weight:700;letter-spacing:3px;background:linear-gradient(135deg,#fff 0%,var(--purple) 100%);-webkit-background-clip:text;-webkit-text-fill-color:transparent;background-clip:text;}
  .subtitle{font-size:14px;color:var(--text-muted);margin-top:4px;}
  .progress-wrap{margin-bottom:2rem;}
  .progress-steps{display:flex;justify-content:space-between;margin-bottom:8px;}
  .step-label{font-size:11px;color:var(--text-muted);font-weight:600;letter-spacing:.5px;}
  .step-label.active{color:var(--purple);}
  .progress-bar{height:3px;background:var(--border);border-radius:2px;overflow:hidden;}
  .progress-fill{height:100%;background:var(--purple);border-radius:2px;transition:width .4s ease;width:20%;}
  .card{background:var(--surface);border:1px solid var(--border);border-radius:16px;padding:1.75rem;margin-bottom:1rem;display:none;}
  .card.active{display:block;animation:fadeIn .3s ease;}
  @keyframes fadeIn{from{opacity:0;transform:translateY(8px)}to{opacity:1;transform:translateY(0)}}
  .section-title{font-family:'Rajdhani',sans-serif;font-size:12px;font-weight:700;color:var(--purple);letter-spacing:2px;text-transform:uppercase;display:flex;align-items:center;gap:8px;margin-bottom:1.25rem;padding-bottom:.75rem;border-bottom:1px solid var(--border);}
  .section-title::before{content:'';display:block;width:3px;height:14px;background:var(--purple);border-radius:2px;}
  .section-num{background:var(--purple-bg);color:var(--purple);font-size:10px;font-weight:700;padding:2px 8px;border-radius:10px;margin-left:auto;}
  .grid-2{display:grid;grid-template-columns:1fr 1fr;gap:1rem;}
  .grid-1{display:grid;grid-template-columns:1fr;gap:1rem;}
  @media(max-width:520px){.grid-2{grid-template-columns:1fr;}}
  .field{display:flex;flex-direction:column;gap:6px;}
  .field label{font-size:12px;font-weight:600;color:var(--text-muted);text-transform:uppercase;letter-spacing:.5px;}
  .field label span{color:var(--purple);margin-left:2px;}
  .field input,.field select,.field textarea{background:var(--surface2);border:1px solid var(--border);border-radius:8px;color:var(--text);font-family:'Nunito',sans-serif;font-size:14px;padding:10px 14px;outline:none;transition:border-color .2s,box-shadow .2s;width:100%;}
  .field input:focus,.field select:focus,.field textarea:focus{border-color:var(--purple);box-shadow:0 0 0 3px rgba(127,119,221,.15);}
  .field select option{background:#1E1E1E;}
  .field textarea{resize:vertical;min-height:90px;line-height:1.6;}
  .field.error input,.field.error select,.field.error textarea{border-color:var(--error);}
  .err-msg{font-size:11px;color:var(--error);display:none;}
  .field.error .err-msg{display:block;}
  .char-count{font-size:11px;color:var(--text-muted);text-align:right;}
  .opts{display:flex;flex-wrap:wrap;gap:8px;}
  .opt-btn{padding:7px 16px;border:1px solid var(--border);border-radius:20px;background:var(--surface2);color:var(--text-muted);font-size:13px;font-family:'Nunito',sans-serif;font-weight:500;cursor:pointer;transition:all .15s;}
  .opt-btn:hover{border-color:var(--purple);color:var(--purple);}
  .opt-btn.active{background:var(--purple-bg);border-color:var(--purple);color:var(--purple);font-weight:600;}
  .chk-list{display:flex;flex-direction:column;gap:8px;}
  .chk-item{display:flex;align-items:center;gap:10px;background:var(--surface2);border:1px solid var(--border);border-radius:8px;padding:10px 14px;cursor:pointer;transition:border-color .15s;font-size:14px;}
  .chk-item:hover{border-color:var(--purple);}
  .chk-item input[type="checkbox"]{width:18px;height:18px;accent-color:var(--purple);cursor:pointer;flex-shrink:0;}
  .chk-item.checked{border-color:var(--purple);background:var(--purple-bg);}
  .quiz-item{background:var(--surface2);border:1px solid var(--border);border-radius:10px;padding:1rem;margin-bottom:1rem;}
  .quiz-item:last-child{margin-bottom:0;}
  .quiz-q{font-size:14px;font-weight:600;color:var(--text);margin-bottom:10px;line-height:1.5;}
  .quiz-q span{color:var(--purple);font-family:'Rajdhani',sans-serif;font-size:16px;margin-right:4px;}
  .quiz-opts{display:flex;flex-direction:column;gap:6px;}
  .quiz-opt{display:flex;align-items:center;gap:10px;padding:8px 12px;border:1px solid var(--border);border-radius:8px;cursor:pointer;transition:all .15s;font-size:13px;color:var(--text-muted);background:var(--surface);}
  .quiz-opt:hover{border-color:var(--purple);color:var(--text);}
  .quiz-opt input[type="radio"]{accent-color:var(--purple);flex-shrink:0;}
  .quiz-opt.selected{border-color:var(--purple);background:var(--purple-bg);color:var(--purple);}
  .quiz-feedback{font-size:12px;margin-top:6px;display:none;padding:6px 10px;border-radius:6px;}
  .quiz-feedback.correct{background:rgba(61,184,122,.1);color:var(--success);border:1px solid rgba(61,184,122,.3);display:block;}
  .quiz-feedback.wrong{background:rgba(226,75,74,.1);color:var(--error);border:1px solid rgba(226,75,74,.3);display:block;}
  .nav-btns{display:flex;gap:10px;margin-top:1.5rem;}
  .btn-back{flex:1;padding:12px;background:transparent;border:1px solid var(--border);border-radius:10px;color:var(--text-muted);font-family:'Rajdhani',sans-serif;font-size:15px;font-weight:600;letter-spacing:1px;cursor:pointer;transition:all .15s;}
  .btn-back:hover{border-color:var(--purple);color:var(--purple);}
  .btn-next{flex:2;padding:12px;background:var(--purple);border:none;border-radius:10px;color:#fff;font-family:'Rajdhani',sans-serif;font-size:16px;font-weight:700;letter-spacing:1px;cursor:pointer;transition:all .15s;box-shadow:0 4px 20px rgba(127,119,221,.25);}
  .btn-next:hover{background:var(--purple-d);}
  .btn-next:disabled{opacity:.5;cursor:not-allowed;}
  .btn-next.loading::after{content:'';display:inline-block;width:12px;height:12px;border:2px solid rgba(255,255,255,.4);border-top-color:#fff;border-radius:50%;animation:spin .7s linear infinite;margin-left:8px;vertical-align:middle;}
  @keyframes spin{to{transform:rotate(360deg)}}
  .notice{background:var(--purple-bg);border:1px solid var(--purple-d);border-radius:10px;padding:1rem 1.25rem;font-size:13px;color:#aaa;line-height:1.6;margin-bottom:1.25rem;}
  .notice strong{color:var(--purple);}
  .score-bar{background:var(--surface2);border:1px solid var(--border);border-radius:10px;padding:1rem;margin-bottom:1rem;display:flex;align-items:center;gap:12px;}
  .score-num{font-family:'Rajdhani',sans-serif;font-size:28px;font-weight:700;color:var(--purple);}
  .score-label{font-size:13px;color:var(--text-muted);}
  .score-label strong{color:var(--text);}
  .global-error{background:rgba(226,75,74,.1);border:1px solid var(--error);border-radius:10px;padding:1rem;color:var(--error);font-size:13px;margin-bottom:1rem;display:none;}
  .success-screen{display:none;text-align:center;padding:4rem 2rem;}
  .success-icon{width:80px;height:80px;background:rgba(61,184,122,.15);border:2px solid var(--success);border-radius:50%;display:inline-flex;align-items:center;justify-content:center;font-size:36px;margin-bottom:1.5rem;animation:pop .4s ease;}
  @keyframes pop{0%{transform:scale(.5);opacity:0}80%{transform:scale(1.1)}100%{transform:scale(1);opacity:1}}
  .success-screen h2{font-family:'Rajdhani',sans-serif;font-size:26px;font-weight:700;color:var(--success);margin-bottom:10px;}
  .success-screen p{font-size:15px;color:var(--text-muted);line-height:1.7;}
</style>
</head>
<body>
<div class="wrap">
  <div class="header">
    <img src="./myLogo.png" alt="Pixeled Community" class="logo-img"><br>
    <div class="title">PIXELED COMMUNITY</div>
    <div class="subtitle">Formulario de postulación al servidor</div>
  </div>
  <div class="progress-wrap">
    <div class="progress-steps">
      <span class="step-label active" id="sl1">Datos</span>
      <span class="step-label" id="sl2">Experiencia</span>
      <span class="step-label" id="sl3">Personaje</span>
      <span class="step-label" id="sl4">Test Normas</span>
      <span class="step-label" id="sl5">Enviar</span>
    </div>
    <div class="progress-bar"><div class="progress-fill" id="progress-fill"></div></div>
  </div>
  <div id="form-wrap">
    <!-- PASO 1 -->
    <div class="card active" id="step-1">
      <div class="section-title">Datos Personales <span class="section-num">1 / 5</span></div>
      <div class="grid-2">
        <div class="field" id="f-nick"><label>Nick de FiveM <span>*</span></label><input type="text" id="nick" placeholder="Tu nombre en el juego" maxlength="30"><span class="err-msg">Campo obligatorio</span></div>
        <div class="field" id="f-discord"><label>Discord <span>*</span></label><input type="text" id="discord" placeholder="@usuario o usuario#0000" maxlength="50"><span class="err-msg">Campo obligatorio</span></div>
        <div class="field" id="f-edad"><label>Edad real <span>*</span></label><input type="number" id="edad" placeholder="Tu edad" min="14" max="99"><span class="err-msg">Mínimo 14 años</span></div>
        <div class="field"><label>País</label><select id="pais"><option value="">Selecciona tu país</option><option>España</option><option>México</option><option>Argentina</option><option>Colombia</option><option>Chile</option><option>Venezuela</option><option>Perú</option><option>Otro</option></select></div>
      </div>
      <div class="nav-btns"><button class="btn-next" onclick="nextStep(1)">CONTINUAR →</button></div>
    </div>
    <!-- PASO 2 -->
    <div class="card" id="step-2">
      <div class="section-title">Experiencia en Roleplay <span class="section-num">2 / 5</span></div>
      <div class="grid-1">
        <div class="field" id="f-exp"><label>¿Cuánto tiempo llevas haciendo roleplay? <span>*</span></label><div class="opts" id="exp-opts"><button class="opt-btn" onclick="selectOpt('exp-opts','exp',this)">Soy nuevo</button><button class="opt-btn" onclick="selectOpt('exp-opts','exp',this)">Menos de 1 año</button><button class="opt-btn" onclick="selectOpt('exp-opts','exp',this)">1 - 3 años</button><button class="opt-btn" onclick="selectOpt('exp-opts','exp',this)">Más de 3 años</button></div><input type="hidden" id="exp"><span class="err-msg">Selecciona una opción</span></div>
        <div class="field"><label>Servidores anteriores</label><input type="text" id="servidores" placeholder="Ej: NoPixel, Eclipse, otros..." maxlength="100"></div>
        <div class="field" id="f-conoce"><label>¿Cómo conociste Pixeled Community? <span>*</span></label><select id="conoce"><option value="">Selecciona...</option><option>Discord</option><option>Amigo o conocido</option><option>Redes sociales</option><option>YouTube / Twitch</option><option>Otro</option></select><span class="err-msg">Campo obligatorio</span></div>
      </div>
      <div class="nav-btns"><button class="btn-back" onclick="prevStep(2)">← VOLVER</button><button class="btn-next" onclick="nextStep(2)">CONTINUAR →</button></div>
    </div>
    <!-- PASO 3 -->
    <div class="card" id="step-3">
      <div class="section-title">Tu Personaje <span class="section-num">3 / 5</span></div>
      <div class="grid-2" style="margin-bottom:1rem">
        <div class="field" id="f-nombre-per"><label>Nombre del personaje <span>*</span></label><input type="text" id="nombre-per" placeholder="Nombre Apellido" maxlength="50"><span class="err-msg">Campo obligatorio</span></div>
        <div class="field"><label>Rol deseado</label><select id="trabajo"><option value="">Selecciona un rol</option><option>Civil</option><option>Policía (LSPD)</option><option>Médico (EMS)</option><option>Mecánico</option><option>Empresario</option><option>Criminal</option><option>Sin decidir</option></select></div>
      </div>
      <div class="field" id="f-backstory"><label>Historia del personaje (backstory) <span>*</span></label><textarea id="backstory" placeholder="¿De dónde viene? ¿Por qué llegó a Los Santos? ¿Qué busca? (mín. 100 caracteres)" maxlength="1000" oninput="updateCount('backstory','bs-count',1000)"></textarea><div style="display:flex;justify-content:space-between"><span class="err-msg">Mínimo 100 caracteres</span><span class="char-count" id="bs-count">0 / 1000</span></div></div>
      <div class="nav-btns"><button class="btn-back" onclick="prevStep(3)">← VOLVER</button><button class="btn-next" onclick="nextStep(3)">CONTINUAR →</button></div>
    </div>
    <!-- PASO 4: TEST -->
    <div class="card" id="step-4">
      <div class="section-title">Test de Normas RP <span class="section-num">4 / 5</span></div>
      <p style="font-size:13px;color:var(--text-muted);margin-bottom:1.25rem;line-height:1.6;">Responde las 10 preguntas sobre las normas básicas del roleplay antes de continuar.</p>
      <div id="quiz-container"></div>
      <div class="score-bar" id="score-bar" style="display:none"><div class="score-num" id="score-num">0/10</div><div class="score-label"><strong id="score-msg"></strong><br><span id="score-sub"></span></div></div>
      <div class="nav-btns"><button class="btn-back" onclick="prevStep(4)">← VOLVER</button><button class="btn-next" id="btn-check-quiz" onclick="checkQuiz()">COMPROBAR RESPUESTAS</button></div>
    </div>
    <!-- PASO 5 -->
    <div class="card" id="step-5">
      <div class="section-title">Compromisos y Envío <span class="section-num">5 / 5</span></div>
      <div class="grid-1">
        <div class="field" id="f-ooc"><label>¿Qué entiendes por "romper el personaje" (OOC)? <span>*</span></label><textarea id="ooc" placeholder="Explica con tus propias palabras..." maxlength="400" oninput="updateCount('ooc','ooc-count',400)"></textarea><div style="display:flex;justify-content:space-between"><span class="err-msg">Campo obligatorio</span><span class="char-count" id="ooc-count">0 / 400</span></div></div>
        <div class="field" id="f-me-do"><label>¿Para qué se usan /me y /do? Da un ejemplo de cada uno <span>*</span></label><textarea id="me-do" placeholder="Ej: /me saca la cartera lentamente — /do La puerta está entreabierta..." maxlength="400" oninput="updateCount('me-do','medo-count',400)"></textarea><div style="display:flex;justify-content:space-between"><span class="err-msg">Campo obligatorio</span><span class="char-count" id="medo-count">0 / 400</span></div></div>
        <div class="field" id="f-checks"><label>Confirmo que <span>*</span></label>
          <div class="chk-list">
            <label class="chk-item" id="ci1"><input type="checkbox" id="chk1" onchange="toggleChk('ci1')"> He leído y acepto todas las normas del servidor</label>
            <label class="chk-item" id="ci2"><input type="checkbox" id="chk2" onchange="toggleChk('ci2')"> Tengo micrófono y me comprometo a usarlo siempre en RP</label>
            <label class="chk-item" id="ci3"><input type="checkbox" id="chk3" onchange="toggleChk('ci3')"> Entiendo y respetaré las normas de IC/OOC en todo momento</label>
            <label class="chk-item" id="ci4"><input type="checkbox" id="chk4" onchange="toggleChk('ci4')"> No practicaré metagaming, powergaming, RDM, VDM ni RK</label>
            <label class="chk-item" id="ci5"><input type="checkbox" id="chk5" onchange="toggleChk('ci5')"> Me comprometo a mantener un ambiente respetuoso con todos</label>
          </div>
          <span class="err-msg">Debes aceptar todos los compromisos</span>
        </div>
      </div>
      <div class="notice"><strong>⏱ Plazo de respuesta:</strong> Tu postulación será revisada en <strong>24-72 horas</strong>. Recibirás respuesta por Discord. Pixeled Community se reserva el derecho de aceptar o denegar cualquier postulación.</div>
      <div class="global-error" id="global-error-2">❌ Error al enviar. Comprueba tu conexión e inténtalo de nuevo.</div>
      <div class="nav-btns"><button class="btn-back" onclick="prevStep(5)">← VOLVER</button><button class="btn-next" id="btn-submit" onclick="submitForm()">ENVIAR POSTULACIÓN ✓</button></div>
    </div>
  </div>
  <div class="success-screen" id="success-screen">
    <div class="success-icon">✓</div>
    <h2>¡Postulación recibida!</h2>
    <p>Gracias por querer unirte a <strong>Pixeled Community</strong>.<br>Revisaremos tu solicitud y recibirás una respuesta<br>en las próximas <strong>24-72 horas</strong> por Discord.</p>
  </div>
</div>
<script>
// ⚠️ REEMPLAZA CON TU WEBHOOK DE DISCORD
const WEBHOOK_URL='AQUI_TU_WEBHOOK';

const questions=[
  {q:'¿Qué significa IC (In Character)?',opts:['Hablar por Discord durante el juego','Todo lo que hace y dice tu personaje dentro del roleplay','Un comando para hablar con el staff','Salir del juego temporalmente'],correct:1,exp:'IC es todo lo que ocurre dentro del roleplay: acciones, palabras y decisiones de tu personaje.'},
  {q:'¿Qué es el Metagaming (MG)?',opts:['Usar información de fuera del juego (Discord, streams...) dentro del RP','Jugar muchas horas seguidas','Usar mods externos','Hablar por voz con otros jugadores'],correct:0,exp:'El Metagaming es usar información real (OOC) para beneficiarse en el RP. Está estrictamente prohibido.'},
  {q:'¿Qué es el RDM (Random Death Match)?',opts:['Un modo de juego especial','Matar o agredir a alguien sin motivo de RP válido','Un comando para terminar combates','Morir por accidente'],correct:1,exp:'El RDM es atacar a otro jugador sin contexto de RP previo. Siempre debe existir una razón de rol.'},
  {q:'¿Para qué sirve el comando /me?',opts:['Enviar un mensaje privado','Describir una acción física de tu personaje','Reportar a un jugador','Ver tu perfil'],correct:1,exp:'/me describe una acción visible para los cercanos. Ej: /me saca lentamente la cartera del bolsillo.'},
  {q:'¿Para qué sirve el comando /do?',opts:['Hacer una acción de combate','Describir el entorno o detalles de la escena','Cambiar de personaje','Llamar a un taxi'],correct:1,exp:'/do describe detalles del entorno. Ej: /do La puerta está oxidada y apenas se puede abrir.'},
  {q:'¿Qué significa el Powergaming?',opts:['Jugar muchas horas para subir de nivel','Forzar acciones sobre otros sin darles oportunidad de reaccionar','Usar builds muy potentes','Tener mucho dinero en el juego'],correct:1,exp:'El Powergaming es forzar situaciones sobre otros sin permitir reacción. Ej: /me le roba sin esperar respuesta.'},
  {q:'¿Qué es el Fear RP?',opts:['Un servidor de terror','La obligación de que tu personaje sienta miedo ante peligro real','Un comando para rendirse','Una norma que prohíbe armas'],correct:1,exp:'El Fear RP obliga a reaccionar con miedo ante peligro real. Si alguien te apunta, tu personaje no puede ignorarlo.'},
  {q:'¿Qué es el VDM (Vehicle Death Match)?',opts:['Un modo de carreras','Usar un vehículo para atropellar jugadores sin motivo de RP','Un fallo técnico','Una misión de conducción'],correct:1,exp:'El VDM es atropellar intencionadamente a jugadores con un vehículo sin razón de RP válida.'},
  {q:'¿Qué es el Revenge Kill (RK)?',opts:['Matar a quien te mató antes sin haber olvidado ese evento','Un contrato de asesinato','Recuperar objetos al morir','Pedir ayuda al staff tras un PK'],correct:0,exp:'El RK es volver a por quien te mató. Al morir, tu personaje olvida lo ocurrido en ese evento.'},
  {q:'¿Cuándo está permitido romper el personaje (ir OOC)?',opts:['Siempre que quieras','Nunca bajo ningún concepto','Solo en situaciones técnicas urgentes usando los canales correctos','Cuando no sabes cómo continuar el RP'],correct:2,exp:'Solo se puede ir OOC en casos técnicos urgentes (bug, crash) usando /ooc o Discord. Nunca para evitar RP.'}
];

function renderQuiz(){
  document.getElementById('quiz-container').innerHTML=questions.map((q,i)=>`
    <div class="quiz-item" id="qi-${i}">
      <div class="quiz-q"><span>${i+1}.</span>${q.q}</div>
      <div class="quiz-opts">${q.opts.map((o,j)=>`<label class="quiz-opt" id="qo-${i}-${j}" onclick="selQ(${i},${j})"><input type="radio" name="q${i}" value="${j}"> ${o}</label>`).join('')}</div>
      <div class="quiz-feedback" id="qf-${i}"></div>
    </div>`).join('');
}

function selQ(qi,oi){
  document.querySelectorAll(`[id^="qo-${qi}-"]`).forEach(e=>e.classList.remove('selected'));
  document.getElementById(`qo-${qi}-${oi}`).classList.add('selected');
  document.querySelector(`input[name="q${qi}"][value="${oi}"]`).checked=true;
  const fb=document.getElementById(`qf-${qi}`);fb.className='quiz-feedback';fb.style.display='none';
}

let quizScore=0,quizChecked=false;

function checkQuiz(){
  let score=0,all=true;
  questions.forEach((q,i)=>{
    const sel=document.querySelector(`input[name="q${i}"]:checked`);
    if(!sel){all=false;return;}
    const v=parseInt(sel.value),fb=document.getElementById(`qf-${i}`);
    if(v===q.correct){score++;fb.textContent='✓ Correcto — '+q.exp;fb.className='quiz-feedback correct';}
    else{fb.textContent='✗ Incorrecto — '+q.exp;fb.className='quiz-feedback wrong';}
  });
  if(!all){alert('Responde todas las preguntas antes de comprobar.');return;}
  quizScore=score;quizChecked=true;
  const sb=document.getElementById('score-bar'),sn=document.getElementById('score-num'),sm=document.getElementById('score-msg'),ss=document.getElementById('score-sub'),btn=document.getElementById('btn-check-quiz');
  sb.style.display='flex';sn.textContent=score+'/10';
  // El jugador solo ve que puede continuar, sin saber si aprobó o suspendió
  sn.style.color='var(--purple)';
  sm.textContent='Test completado. Puedes continuar.';
  ss.textContent='El staff revisará tus respuestas junto con tu postulación.';
  btn.textContent='CONTINUAR →';
  btn.onclick=()=>nextStep(4);
}

function selectOpt(gid,fid,btn){
  document.querySelectorAll('#'+gid+' .opt-btn').forEach(b=>b.classList.remove('active'));
  btn.classList.add('active');document.getElementById(fid).value=btn.textContent;
  document.getElementById('f-'+fid).classList.remove('error');
}
function updateCount(id,cid,max){document.getElementById(cid).textContent=document.getElementById(id).value.length+' / '+max;}
function toggleChk(id){const cb=document.getElementById(id).querySelector('input[type="checkbox"]');document.getElementById(id).classList.toggle('checked',cb.checked);}

const stepW=['20%','40%','60%','80%','100%'];

function showStep(s){
  document.querySelectorAll('.card').forEach(c=>c.classList.remove('active'));
  document.getElementById('step-'+s).classList.add('active');
  document.getElementById('progress-fill').style.width=stepW[s-1];
  for(let i=1;i<=5;i++)document.getElementById('sl'+i).classList.toggle('active',i===s);
  window.scrollTo({top:0,behavior:'smooth'});
}

function validateStep(s){
  let ok=true;
  const req=(fid,cond)=>{const f=document.getElementById(fid);if(cond){f.classList.add('error');ok=false;}else f.classList.remove('error');};
  if(s===1){req('f-nick',!document.getElementById('nick').value.trim());req('f-discord',!document.getElementById('discord').value.trim());const e=parseInt(document.getElementById('edad').value);req('f-edad',!e||e<14);}
  if(s===2){req('f-exp',!document.getElementById('exp').value);req('f-conoce',!document.getElementById('conoce').value);}
  if(s===3){req('f-nombre-per',!document.getElementById('nombre-per').value.trim());req('f-backstory',document.getElementById('backstory').value.trim().length<100);}
  if(s===5){req('f-ooc',!document.getElementById('ooc').value.trim());req('f-me-do',!document.getElementById('me-do').value.trim());const all=['chk1','chk2','chk3','chk4','chk5'].every(id=>document.getElementById(id).checked);req('f-checks',!all);}
  return ok;
}

function nextStep(s){
  if(!validateStep(s))return;
  if(s===4&&!quizChecked){alert('Debes completar el test antes de continuar.');return;}
  showStep(s+1);
}
function prevStep(s){showStep(s-1);}

function buildEmbed(){
  // Solo el staff ve si aprobó o suspendió
  const aprobado=quizScore>=7;
  const estadoEmoji=aprobado?'✅':'❌';
  const estadoTexto=aprobado?'APROBADO':'SUSPENDIDO';
  const embedColor=aprobado?0x3DB87A:0xE24B4A;

  const ans=questions.map((q,i)=>{
    const sel=document.querySelector(`input[name="q${i}"]:checked`);
    const v=sel?parseInt(sel.value):-1;
    return`${v===q.correct?'✅':'❌'} **P${i+1}:** ${q.q.substring(0,55)}...\n→ ${v>=0?q.opts[v]:'Sin responder'}`;
  }).join('\n');

  return{
    username:'Pixeled Community',
    embeds:[{
      title:`📋 Nueva Postulación — ${document.getElementById('nick').value.trim()}`,
      color:embedColor,
      fields:[
        {name:`${estadoEmoji} Resultado del Test`,value:`**${estadoTexto}** — ${quizScore}/10 correctas\n${aprobado?'El candidato ha superado el test de normas.':'El candidato no ha superado el test de normas (mínimo 7/10).'}`,inline:false},
        {name:'👤 Datos Personales',value:`**Nick:** ${document.getElementById('nick').value.trim()}\n**Discord:** ${document.getElementById('discord').value.trim()}\n**Edad:** ${document.getElementById('edad').value} años\n**País:** ${document.getElementById('pais').value||'No especificado'}`,inline:false},
        {name:'🎮 Experiencia',value:`**Tiempo en RP:** ${document.getElementById('exp').value}\n**Servidores:** ${document.getElementById('servidores').value||'Ninguno'}\n**Cómo nos conoció:** ${document.getElementById('conoce').value}`,inline:false},
        {name:'🎭 Personaje',value:`**Nombre:** ${document.getElementById('nombre-per').value.trim()}\n**Rol deseado:** ${document.getElementById('trabajo').value||'Sin decidir'}`,inline:false},
        {name:'📖 Backstory',value:document.getElementById('backstory').value.trim().substring(0,1024),inline:false},
        {name:`🎯 Respuestas del Test (${quizScore}/10)`,value:ans.substring(0,1024),inline:false},
        {name:'❓ OOC / Romper el personaje',value:document.getElementById('ooc').value.trim().substring(0,500),inline:false},
        {name:'⌨️ /me y /do',value:document.getElementById('me-do').value.trim().substring(0,500),inline:false},
        {name:'✅ Compromisos aceptados',value:'✔ Normas del servidor\n✔ Uso de micrófono\n✔ IC/OOC\n✔ Sin MG/PG/RDM/VDM/RK\n✔ Respeto',inline:false},
      ],
      footer:{text:`Pixeled Community · ${new Date().toLocaleString('es-ES')}`},
      timestamp:new Date().toISOString()
    }]
  };
}

async function submitForm(){
  document.getElementById('global-error-2').style.display='none';
  if(!validateStep(5))return;
  const btn=document.getElementById('btn-submit');
  btn.disabled=true;btn.classList.add('loading');btn.textContent='ENVIANDO...';
  try{
    const res=await fetch(WEBHOOK_URL,{method:'POST',headers:{'Content-Type':'application/json'},body:JSON.stringify(buildEmbed())});
    if(res.ok||res.status===204){
      document.getElementById('form-wrap').style.display='none';
      document.getElementById('success-screen').style.display='block';
      window.scrollTo({top:0,behavior:'smooth'});
    }else throw new Error();
  }catch{
    document.getElementById('global-error-2').style.display='block';
    btn.disabled=false;btn.classList.remove('loading');btn.textContent='ENVIAR POSTULACIÓN ✓';
  }
}
renderQuiz();
</script>
</body>
</html>
