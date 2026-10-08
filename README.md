# Scam.checker
The app that anyone can check the link or otp that is scam or real
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1, viewport-fit=cover">
<title>ScamGuard</title>
<style>
:root{--bg:#eef2fa;--card:#fff;--ink:#14213d;--mute:#56627f;--line:#d8e0f0;--brand:#2347c5;--bi:#fff;--ok:#16825d;--warn:#a85f00;--bad:#c9302c;--okb:#e0f4ec;--wb:#fff0d6;--bb:#fde4e3;box-sizing:border-box;padding-top:env(safe-area-inset-top,0px);padding-bottom:env(safe-area-inset-bottom,0px)}
@media (prefers-color-scheme:dark){:root:not([data-theme="light"]){--bg:#0c1324;--card:#162038;--ink:#e8ecf6;--mute:#9aa6c4;--line:#2a3555;--brand:#7d99ff;--bi:#0c1324;--ok:#4fd1a0;--warn:#f0b24a;--bad:#ff7b76;--okb:#10332a;--wb:#3a2c10;--bb:#401a1a}}
:root[data-theme="dark"]{--bg:#0c1324;--card:#162038;--ink:#e8ecf6;--mute:#9aa6c4;--line:#2a3555;--brand:#7d99ff;--bi:#0c1324;--ok:#4fd1a0;--warn:#f0b24a;--bad:#ff7b76;--okb:#10332a;--wb:#3a2c10;--bb:#401a1a}
html{scroll-padding-top:env(safe-area-inset-top,0px)}
*{box-sizing:border-box}
body{margin:0;background:var(--bg);color:var(--ink);font:16px/1.55 system-ui,-apple-system,"Segoe UI","Noto Sans Devanagari","Mangal",sans-serif}
main{max-width:520px;margin:0 auto;padding:16px 16px 100px}
h1{font-size:26px;margin:4px 0 2px;letter-spacing:-.3px}h2{font-size:20px;margin:6px 0 2px}h3{font-size:15px;margin:14px 0 4px}
.sub,.m,.n,small{color:var(--mute)}.n{font-size:13px}
textarea{width:100%;min-height:150px;padding:14px;font:inherit;font-size:16px;color:var(--ink);background:var(--card);border:2px solid var(--line);border-radius:14px;resize:vertical}
textarea:focus{border-color:var(--brand);outline:none}
button{font:inherit;cursor:pointer}
.b,.g{padding:12px 18px;border-radius:12px;border:2px solid var(--brand);font-weight:700}
.b{background:var(--brand);color:var(--bi)}.g{background:transparent;color:var(--brand)}
.row{display:flex;gap:10px;flex-wrap:wrap;margin:12px 0}
.row .b{flex:1}
.lk{background:none;border:0;color:var(--brand);text-decoration:underline;padding:4px 0;font-size:14px}
.card{background:var(--card);border:1px solid var(--line);border-radius:16px;padding:16px;margin:14px 0}
.card.ok{border-left:6px solid var(--ok)}.card.warn{border-left:6px solid var(--warn)}.card.bad{border-left:6px solid var(--bad)}
.card.ok h2{color:var(--ok)}.card.warn h2{color:var(--warn)}.card.bad h2{color:var(--bad)}
.meter{height:12px;border-radius:8px;background:var(--line);overflow:hidden;margin-bottom:10px}
.meter i{display:block;height:100%;transition:width .9s cubic-bezier(.2,.8,.2,1)}
.ok .meter i{background:var(--ok)}.warn .meter i{background:var(--warn)}.bad .meter i{background:var(--bad)}
ul{padding-left:20px;margin:4px 0}li{margin:3px 0}
.st{display:flex;gap:10px}.st div{flex:1;background:var(--card);border:1px solid var(--line);border-radius:12px;padding:10px;text-align:center}
.st b{font-size:24px;display:block}
.it{display:flex;gap:10px;width:100%;text-align:left;background:var(--card);color:var(--ink);border:1px solid var(--line);border-radius:12px;padding:12px;margin:8px 0}
.it span:last-child{min-width:0}.it span b{margin-right:6px}
.it .c{display:-webkit-box;-webkit-line-clamp:2;-webkit-box-orient:vertical;overflow:hidden;word-break:break-word}
.d{flex:none;width:12px;height:12px;border-radius:50%;margin-top:7px}.d.ok{background:var(--ok)}.d.warn{background:var(--warn)}.d.bad{background:var(--bad)}
details{background:var(--card);border:1px solid var(--line);border-radius:12px;padding:12px 14px;margin:8px 0}
summary{font-weight:700;cursor:pointer}details p{margin:8px 0 2px}
.ci{display:flex;gap:10px;align-items:flex-start;padding:10px 0;border-bottom:1px solid var(--line)}
.ci input{width:22px;height:22px;flex:none;margin-top:2px;accent-color:var(--brand)}
.call{display:block;text-align:center;background:var(--bad);color:#fff;text-decoration:none;font-weight:700;padding:14px;border-radius:12px;margin:10px 0}
a.l{color:var(--brand)}
nav{position:fixed;left:0;right:0;bottom:0;display:flex;background:var(--card);border-top:1px solid var(--line);padding-bottom:env(safe-area-inset-bottom,0px)}
nav button{flex:1;background:none;border:0;color:var(--mute);padding:8px 2px 10px;font-size:12px}
nav button span{display:block;font-size:22px;line-height:1.2}
nav button[aria-current="true"]{color:var(--brand);font-weight:700;box-shadow:inset 0 3px 0 var(--brand)}
:focus-visible{outline:3px solid var(--brand);outline-offset:2px}
@media (prefers-reduced-motion:reduce){*{transition:none!important}}
</style>
</head>
<body>
<main>
<section class="tab" id="t-chk">
<h1>🛡️ ScamGuard</h1>
<p class="sub">Paste a suspicious message, link or call details here. We'll tell you whether it's a scam.</p>
<textarea id="inp" placeholder="e.g. 'Your KYC is not updated, your account will be blocked, enter your OTP at this link…'"></textarea>
<div class="row"><button class="b" onclick="check()">Check</button><button class="g" onclick="$('#inp').value='';$('#res').innerHTML=''">Clear</button></div>
<button class="lk" onclick="$('#inp').value=SM">Try an example</button>
<div id="res" aria-live="polite"></div>
<h3>Checks so far</h3>
<div class="st"><div><b id="n1">0</b>Checked</div><div><b id="n2">0</b>Dangerous</div></div>
</section>

<section class="tab" id="t-hist" hidden>
<h1>History</h1>
<p class="sub">Your past checks, saved only on this phone.</p>
<div id="hl"></div>
<button class="g" onclick="clr()">Clear history</button>
</section>

<section class="tab" id="t-learn" hidden>
<h1>Learn</h1>
<p class="sub">Common scams and how to avoid them.</p>
<details><summary>Digital arrest</summary><p>Someone claims to be police, CBI or customs, says drugs or a case are linked to your name, and keeps you on a video call as if you are "under arrest".</p><p><b>The truth:</b> No agency arrests people on a video call or asks for money. Hang up.</p></details>
<details><summary>KYC and OTP fraud</summary><p>They scare you with "your account will be blocked" and ask for an OTP or card details on a link.</p><p><b>Protection:</b> A bank never asks for your OTP, PIN or CVV. Check only in the bank's official app.</p></details>
<details><summary>Deepfakes and fake voices</summary><p>AI is used to copy a family member's or friend's voice and say "send money right now".</p><p><b>Protection:</b> Hang up and call them yourself on their old number. Keep a secret code word at home.</p></details>
<details><summary>Job and task scams</summary><p>"Earn daily from home", like videos or complete tasks. They pay a small amount first, then ask for a "deposit".</p><p><b>Protection:</b> A real job never asks for a fee first.</p></details>
<details><summary>UPI and QR scams</summary><p>"Enter your PIN to get a refund" or "scan this QR".</p><p><b>The truth:</b> You never need to enter a PIN or scan a QR to receive money. A PIN is only for sending money.</p></details>
<details><summary>Fake loan and investment apps</summary><p>Promises of "guaranteed profit" or "double your money", or a loan app that asks for access to your contacts and photos.</p><p><b>Protection:</b> A promise of guaranteed profit is always a lie. Never install an app from an APK file.</p></details>
<h3>Quick quiz</h3>
<div class="card" id="q"></div>
</section>

<section class="tab" id="t-help" hidden>
<h1>Help</h1>
<p class="sub">If you've already been cheated, the first hour matters most.</p>
<a class="call" href="tel:1930">📞 Call 1930 (Cyber Crime Helpline, India)</a>
<p>Online complaint: <a class="l" href="https://cybercrime.gov.in" target="_blank" rel="noopener">cybercrime.gov.in</a></p>
<h3>Lost money? Do this</h3>
<div id="ck"></div>
<p class="n">In another country? Contact your bank and the local cyber police right away.</p>
</section>

<section class="tab" id="t-plus" hidden>
<style>[hidden]{display:none!important}.pl{border:2px solid var(--brand)}.pr{font-size:28px;font-weight:800;margin:4px 0}.nm{width:100%;padding:12px;font:inherit;font-size:16px;color:var(--ink);background:var(--bg);border:2px solid var(--line);border-radius:12px}.ab{position:fixed;top:calc(env(safe-area-inset-top,0px) + 8px);right:12px;z-index:9;padding:3px 12px;border-radius:999px;font-size:12px;font-weight:800;color:#3a2700;background:linear-gradient(135deg,#ffe08a,#e0a100 55%,#f7d25a);box-shadow:0 1px 6px rgba(160,110,0,.5);border:0;cursor:pointer}.pay{display:block;flex:1;text-align:center;text-decoration:none}.qr{text-align:center;margin:14px 0}#qrb{display:inline-block;background:#fff;padding:12px;border-radius:14px;border:1px solid var(--line)}</style>
<h1>⭐ ScamGuard Plus</h1>
<p class="sub">A paid plan for extra protection.</p>
<div class="card pl"><div class="pr" id="pr"></div><ul><li>Number check: country and number type from the code</li><li>Valid for 30 days. Turns on instantly once you enter the UTR</li></ul><div class="row" id="pw"><a class="b pay" id="pa" href="#" onclick="$('#bm').textContent='UPI app did not open? Tap this button on a phone that has a UPI app.'">Pay ₹99 via UPI</a></div>
<div id="pu"><div class="qr"><div id="qrb"></div><p class="n">Or scan this QR with any UPI app.</p></div><p class="n">After paying, find the 12-digit UTR number in your UPI app and enter it here.</p><input class="nm" id="ut" inputmode="numeric" maxlength="12" placeholder="UTR number (12 digits)"><div class="row"><button class="g" onclick="cf()">Activate Plus</button></div><p class="n">If Plus does not open, or disappears after you change phones, enter the same UTR number again. Plus will turn on again.</p></div>
<p class="n" id="bm"></p></div>
<div id="nf"></div>
<h3>Admin login</h3>
<div id="ad"></div>
</section>

<section class="tab" id="t-adm" hidden>
<h1>👑 Admin panel</h1>
<p class="sub">This is data from this phone only. The app does not collect other people's messages.</p>
<div id="am"></div>
</section>
</main>

<button id="ab" class="ab" hidden onclick="go('adm')" aria-label="Open admin panel">👑 ADMIN</button>
<nav aria-label="Main menu">
<button data-t="chk" onclick="go('chk')"><span>🔍</span>Check</button>
<button data-t="hist" onclick="go('hist')"><span>🕘</span>History</button>
<button data-t="learn" onclick="go('learn')"><span>📚</span>Learn</button>
<button data-t="help" onclick="go('help')"><span>🆘</span>Help</button>
<button data-t="plus" onclick="go('plus')"><span>⭐</span>Plus</button>
</nav>

<script src="https://cdnjs.cloudflare.com/ajax/libs/qrcodejs/1.0.0/qrcode.min.js"></script>
<script>
const $=s=>document.querySelector(s);
const MEM={};
const ld=(k,d)=>{try{const v=JSON.parse(localStorage.getItem(k));if(v!==null)return v}catch(e){}return k in MEM?MEM[k]:d};
const sv=(k,v)=>{MEM[k]=v;try{localStorage.setItem(k,JSON.stringify(v))}catch(e){}};
const esc=s=>String(s).replace(/[&<>"]/g,c=>({"&":"&amp;","<":"&lt;",">":"&gt;",'"':"&quot;"}[c]));
const SM="SBI: Your KYC is not updated and your account will be blocked today. Open the link immediately and enter your OTP: http://sbi-kyc-update.xyz/login";
const R=[
[/otp|ओटीपी|cvv|\bpin\b|पिन|password|पासवर्ड/i,30,"It mentions an OTP, PIN or password. A real bank or company never asks for these"],
[/kyc|केवाईसी|खाता.{0,20}(बंद|ब्लॉक)|account.{0,25}(block|suspend|clos|deactivat)|pan.{0,15}(update|link)|aadhaa?r.{0,15}(link|update)/i,25,"It uses fear of KYC or account closure"],
[/urgent|immediately|asap|last chance|expire|तुरंत|आज ही|जल्दी|24 ?(hours|घंटे)|within \d+ ?(hours|hrs|min)/i,15,"It is rushing you"],
[/lottery|jackpot|you(?:'ve| have)? won|winner|prize|lucky draw|लॉटरी|इनाम|जीत(ा|े|ी)|kbc|gift ?card/i,30,"It dangles a prize or lottery"],
[/registration fee|processing fee|advance|security deposit|send money|पैसे भेज|फीस|जमा करो|डिपॉज़िट|शुल्क/i,22,"It asks you to send money or pay a fee"],
[/work from home|part[- ]?time|daily (income|earning)|per day|youtube|like and|घर बैठे|रोज़ कमाओ|पार्ट टाइम/i,22,"It offers easy earnings or work from home"],
[/cbi|police|customs|narcotic|\bed\b|arrest|warrant|trai|सीबीआई|पुलिस|कस्टम|गिरफ़्?तार|वारंट|नारकोटिक्स/i,30,"It scares you in the name of police, CBI or customs (a digital-arrest-style scam)"],
[/anydesk|teamviewer|quick ?support|rustdesk|screen share|स्क्रीन शेयर/i,35,"It asks for your phone screen or remote access"],
[/enter.{0,12}pin|collect request|scan.{0,20}qr|क्यूआर|रिफंड|refund/i,25,"It may be trying to get money deducted in the name of a UPI PIN, QR or refund"],
[/don'?t tell|do not (tell|share)|keep .{0,15}secret|किसी को (मत|न) बता|गोपनीय|राज़ रखो/i,20,"It tells you not to tell anyone. Scammers do exactly this"],
[/guaranteed|double your|100% (profit|return)|crypto|trading group|stock tip|दोगुना|पक्का मुनाफा|गारंटी/i,25,"It promises guaranteed profit or doubled money"],
[/new number|नया नंबर|accident|hospital|bail|एक्सीडेंट|अस्पताल|जमानत/i,15,"It claims an emergency involving family or someone you know"]];
const U=/(?:https?:\/\/|www\.)[^\s]+|[a-z0-9-]+(?:\.[a-z0-9-]+)+\.[a-z]{2,}(?:\/[^\s]*)?/gi;
const SH=/^(bit\.ly|tinyurl\.com|t\.co|cutt\.ly|rb\.gy|is\.gd|goo\.gl|shorturl\.at|tiny\.cc|ow\.ly)$/;
const TLD=/\.(xyz|top|click|icu|live|work|shop|vip|site|buzz|cfd|sbs|rest|gq|tk|ml|cf|ga|monster|cyou)$/;
const BR=["sbi","hdfc","icici","paytm","phonepe","amazon","flipkart","irctc","uidai","incometax","whatsapp","google","instagram","netflix"];
const AD={
bad:["Do not reply to this message or call, and do not open any link","Never send an OTP, PIN, password or money","Block the number and report it on 1930 or cybercrime.gov.in","If money has already been deducted, open the 'Help' tab right away"],
warn:["Do not rush. First verify yourself using the bank's or company's official number or app","Show it to a sensible person at home before you click anything","Do not send any information or money until you are sure"],
ok:["No clear danger found, but still never give anyone your OTP, PIN or money","If in doubt, verify yourself through the official app or website"]};
let last="";
function analyze(t){
 const hit=new Map(),add=(w,r)=>{if(!hit.has(r))hit.set(r,w)};
 R.forEach(([re,w,r])=>{if(re.test(t))add(w,r)});
 (t.match(U)||[]).forEach(u=>{
  u=u.replace(/[.,;:!?)]+$/,"");let h;
  try{h=new URL(/^https?:\/\//i.test(u)?u:"http://"+u)}catch(e){return}
  const host=h.hostname.toLowerCase(),f=u.toLowerCase();
  if(SH.test(host))add(20,"It is a short link, which hides the real address: "+host);
  if(/^\d{1,3}(\.\d{1,3}){3}$/.test(host))add(30,"The link has only a number (IP), not a website name");
  if(host.includes("xn--"))add(25,"The link has fake-looking characters (punycode)");
  if(TLD.test(host))add(20,"The link ending is suspicious: "+host);
  BR.forEach(b=>{if(host.includes(b)&&!new RegExp("(^|\\.)"+b+"\\.(com|in|co\\.in|gov\\.in|net|org)$").test(host))add(30,"The link contains the name "+b.toUpperCase()+" but the website does not look genuine: "+host)});
  if(/\.apk(\?|$)/.test(f))add(35,"An APK file is being downloaded. This can hack your phone");
  if((host.match(/-/g)||[]).length>=2||host.split(".").length>4)add(10,"The link name is strange and long");
  if(/^http:\/\//i.test(f))add(8,"The link is not secure (https)");
 });
 return{score:Math.min(100,[...hit.values()].reduce((a,b)=>a+b,0)),why:[...hit.keys()]};
}
function check(){
 const t=$("#inp").value.trim();
 if(!t){$("#res").innerHTML='<p class="n">Paste something above, then press "Check".</p>';return}
 last=t;const{score,why}=analyze(t),L=score>=50?"bad":score>=20?"warn":"ok";
 const T={bad:["🚨 Danger","Very likely a scam"],warn:["⚠️ Suspicious","Be careful, verify first"],ok:["✅ No clear danger found","Still stay careful"]}[L];
 $("#res").innerHTML=`<div class="card ${L}"><div class="meter"><i style="width:0"></i></div><h2>${T[0]}</h2><p class="m">${T[1]}. Score ${score}/100</p>${why.length?`<h3>Why it looks suspicious</h3><ul>${why.map(x=>`<li>${esc(x)}</li>`).join("")}</ul>`:""}<h3>What to do now</h3><ul>${AD[L].map(x=>`<li>${x}</li>`).join("")}</ul>${L!=="ok"?'<div class="row"><button class="b" onclick="share()">Alert your family</button></div>':""}<p class="n">This check is only an estimate, not a guarantee.</p></div>`;
 requestAnimationFrame(()=>requestAnimationFrame(()=>{$("#res .meter i").style.width=Math.max(score,4)+"%"}));
 const h=ld("sg_h",[]);h.unshift({t:Date.now(),s:score,l:L,x:t.slice(0,300)});sv("sg_h",h.slice(0,40));st();
}
function share(){
 const t="⚠️ Scam alert! I got this message or call: \""+last.slice(0,120)+"…\" It may be a scam. Do not give anyone your OTP, PIN or money. Check with ScamGuard.";
 if(navigator.share){navigator.share({text:t}).catch(()=>{})}else window.open("https://wa.me/?text="+encodeURIComponent(t),"_blank");
}
function st(){const h=ld("sg_h",[]);$("#n1").textContent=h.length;$("#n2").textContent=h.filter(x=>x.l==="bad").length}
function rh(){const h=ld("sg_h",[]);$("#hl").innerHTML=h.length?h.map((x,i)=>`<button class="it" onclick="again(${i})"><span class="d ${x.l}"></span><span><b>${x.s}/100</b><span class="c">${esc(x.x)}</span><small>${new Date(x.t).toLocaleDateString("en-IN")}</small></span></button>`).join(""):'<p class="n">Nothing checked yet. Try your first check.</p>'}
function again(i){$("#inp").value=ld("sg_h",[])[i].x;go("chk");check()}
function clr(){sv("sg_h",[]);rh();st()}
const CK=["Call your bank or UPI app helpline and block your cards and account immediately","Call 1930 or file a complaint at cybercrime.gov.in","Keep screenshots, messages, numbers and transaction IDs safe","Change your bank, email and UPI passwords and PINs","Remove any unknown app like AnyDesk from your phone","Keep a copy of the complaint and its number safe; it will help if you have to visit the police station"];
function rc(){const c=ld("sg_c",{});$("#ck").innerHTML=CK.map((x,i)=>`<label class="ci"><input type="checkbox" ${c[i]?"checked":""} onchange="tc(${i},this.checked)"><span>${x}</span></label>`).join("")}
function tc(i,v){const c=ld("sg_c",{});c[i]=v;sv("sg_c",c)}
const Q=[["Call: 'I am from CBI, drugs were found in your parcel, join a video call.'",1,"A real agency never arrests anyone on a video call."],["You made a payment in your bank app yourself and the OTP for it came on your phone.",0,"An OTP for your own action is fine; just do not tell it to anyone."],["'Enter your UPI PIN to receive money.'",1,"You never need to enter a PIN to receive money."],["'Papa, this is my new number, send 20,000 right now.' The voice sounds exactly like your son's.",1,"First call your son's old number to confirm. The voice could be faked by AI."]];
let qi=0,sc=0;
function rq(){const b=$("#q");if(qi>=Q.length){b.innerHTML=`<p><b>Score: ${sc}/${Q.length}</b></p><button class="g" onclick="qi=0;sc=0;rq()">Play again</button>`;return}
 b.innerHTML=`<p>${qi+1}/${Q.length}. ${Q[qi][0]}</p><div class="row"><button class="g" onclick="ans(1)">🚨 Scam</button><button class="g" onclick="ans(0)">✅ Genuine</button></div>`}
function ans(a){const r=a===Q[qi][1];if(r)sc++;$("#q").innerHTML=`<p>${r?"✅ Correct!":"❌ Wrong."} ${Q[qi][2]}</p><button class="g" onclick="qi++;rq()">Next</button>`}
function go(n){document.querySelectorAll(".tab").forEach(t=>t.hidden=t.id!=="t-"+n);document.querySelectorAll("nav button").forEach(b=>b.setAttribute("aria-current",String(b.dataset.t===n)));if(n==="hist")rh();if(n==="adm")ra();window.scrollTo(0,0)}
const PRICE="₹99 / month",_u="bXlsb3ZlLnlvdTA5QG9rYXhpcw==",_k=6213405645263041;
const h53=(s,z=0)=>{let a=0xdeadbeef^z,b=0x41c6ce57^z;for(let i=0,c;i<s.length;i++){c=s.charCodeAt(i);a=Math.imul(a^c,2654435761);b=Math.imul(b^c,1597334677)}a=Math.imul(a^(a>>>16),2246822507)^Math.imul(b^(b>>>13),3266489909);b=Math.imul(b^(b>>>16),2246822507)^Math.imul(a^(a>>>13),3266489909);return 4294967296*(2097151&b)+(a>>>0)};
const nm=e=>{e=e.trim().toLowerCase();let[l,d]=e.split("@");if(d==="googlemail.com")d="gmail.com";if(d==="gmail.com")l=l.split("+")[0].replace(/\./g,"");return l+"@"+d};
const CC={"1":"USA/Canada","7":"Russia/Kazakhstan","44":"United Kingdom","60":"Malaysia","61":"Australia","62":"Indonesia","63":"Philippines","66":"Thailand","84":"Vietnam","86":"China","91":"India","92":"Pakistan","95":"Myanmar","234":"Nigeria","254":"Kenya","855":"Cambodia","856":"Laos","880":"Bangladesh","971":"UAE","977":"Nepal"};
function rp(){const pr=ld("sg_p",null),adm=ld("sg_a",false),on=!!(pr&&Date.now()-pr.t<2592000000),p=on||adm;
 $("#pr").textContent=PRICE;$("#pw").hidden=$("#pu").hidden=on;$("#ab").hidden=!adm;
 $("#pa").href="upi://pay?pa="+encodeURIComponent(atob(_u))+"&pn=ScamGuard&am=99&cu=INR&tn="+encodeURIComponent("ScamGuard Plus");
 $("#bm").textContent=on?"✅ Plus is active until "+new Date(pr.t+2592000000).toLocaleDateString("en-IN")+" (UTR ..."+String(pr.u).slice(-4)+")":"";
 $("#ad").innerHTML=adm?'<button class="g" onclick="lo()">Admin logout</button>':'<input class="nm" id="em" type="email" placeholder="Email" autocomplete="email"><div class="row"><button class="g" onclick="li()">Log in</button></div><p class="n" id="lm"></p>';
 $("#nf").innerHTML=p?'<div class="card"><h3>Number check</h3><p class="n">Enter the number of the person who called or messaged you.</p><input class="nm" id="nm" type="tel" inputmode="tel" placeholder="+92 300 1234567"><div class="row"><button class="b" onclick="nc()">Check</button></div><div id="nr"></div></div>':'<p class="n">Number check comes with Plus.</p>'}
function mq(){const b=$("#qrb");if(b.firstChild)return;try{new QRCode(b,{text:"upi://pay?pa="+atob(_u)+"&pn=ScamGuard&am=99&cu=INR&tn=ScamGuard%20Plus",width:190,height:190,correctLevel:QRCode.CorrectLevel.M})}catch(e){$(".qr").hidden=true}}
function cf(){const u=$("#ut").value.trim();if(!/^\d{12}$/.test(u)){$("#bm").textContent="A UTR number has 12 digits. Check the transaction details in your UPI app.";return}sv("sg_p",{u:u,t:Date.now()});rp()}
function li(){const e=nm($("#em").value);if(e.includes("@")&&h53("sg:"+e)===_k){sv("sg_a",true);rp();return}$("#lm").textContent="This email is not an admin."}
function lo(){sv("sg_a",false);rp()}
function nc(){
 const raw=$("#nm").value.trim(),d=raw.replace(/\D/g,""),L=[];
 if(d.length<7){$("#nr").innerHTML='<p class="n">Enter the full number.</p>';return}
 const x=d.replace(/^00/,"");let cc="",n="";
 if(/^(\+|00)/.test(raw)){for(const l of [3,2,1]){if(CC[x.slice(0,l)]){cc=x.slice(0,l);break}}
  if(cc){L.push("Country code +"+cc+": "+CC[cc]);if(cc==="91")n=x.slice(2);else L.push("This is a number from outside India. Money, job or prize talk from an unknown foreign number is a common scam method")}
  else L.push("Country code not recognised. Do not trust unknown numbers")}
 else n=x.replace(/^0/,"").replace(/^91(?=\d{10}$)/,"");
 if(n){if(n.length!==10)L.push("An Indian number has 10 digits; this one has a different length");
  else if(/^140/.test(n))L.push("The 140 series is used for telemarketing. Banks and police do not call from it");
  else if(/^[6-9]/.test(n))L.push("Looks like an Indian mobile number, but that does not make the sender trustworthy");
  else L.push("Does not look like an Indian mobile number")}
 $("#nr").innerHTML="<ul>"+L.map(i=>"<li>"+esc(i)+"</li>").join("")+'</ul><p class="n">This is only what the number\'s code shows. No app can tell where the sender really is, because scammers use fake numbers and internet calls. Report it on 1930; the police can get the real details from the telecom company.</p>'}
function ra(){
 if(!ld("sg_a",false)){go("chk");return}
 const h=ld("sg_h",[]),c=l=>h.filter(x=>x.l===l).length,pr=ld("sg_p",null),on=!!(pr&&Date.now()-pr.t<2592000000);
 $("#am").innerHTML=`<div class="st"><div><b>${h.length}</b>Checked</div><div><b>${c("bad")}</b>Dangerous</div></div><div class="st" style="margin-top:10px"><div><b>${c("warn")}</b>Suspicious</div><div><b>${c("ok")}</b>Safe</div></div><div class="card"><b>Plus:</b> ${on?"Active until "+new Date(pr.t+2592000000).toLocaleDateString("en-IN"):"Off"}</div><h3>Recent checks</h3>${h.slice(0,10).map(x=>`<div class="it"><span class="d ${x.l}"></span><span><b>${x.s}/100</b><span class="c">${esc(x.x)}</span><small>${new Date(x.t).toLocaleString("en-IN")}</small></span></div>`).join("")||'<p class="n">No checks yet.</p>'}`}
go("chk");st();rc();rq();rp();mq();
</script>
</body>
</html>
