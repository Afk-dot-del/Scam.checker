# Scam.checker
The app that anyone can check the link or otp that is scam or real
<!DOCTYPE html>
<html lang="hi">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1, viewport-fit=cover">
<title>ScamGuard — स्कैम गार्ड</title>
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
<p class="sub">शक वाला मैसेज, लिंक या कॉल की बात यहां चिपकाओ। हम बताएंगे कि स्कैम है या नहीं।</p>
<textarea id="inp" placeholder="जैसे: 'आपका KYC अपडेट नहीं है, खाता बंद हो जाएगा, इस लिंक पर OTP डालें…'"></textarea>
<div class="row"><button class="b" onclick="check()">जांचो</button><button class="g" onclick="$('#inp').value='';$('#res').innerHTML=''">साफ़ करो</button></div>
<button class="lk" onclick="$('#inp').value=SM">उदाहरण भरकर देखो</button>
<div id="res" aria-live="polite"></div>
<h3>अब तक की जांच</h3>
<div class="st"><div><b id="n1">0</b>जांचे गए</div><div><b id="n2">0</b>खतरे वाले</div></div>
</section>

<section class="tab" id="t-hist" hidden>
<h1>इतिहास</h1>
<p class="sub">तुम्हारी पिछली जांच, सिर्फ़ इसी फोन में सेव है।</p>
<div id="hl"></div>
<button class="g" onclick="clr()">इतिहास मिटाओ</button>
</section>

<section class="tab" id="t-learn" hidden>
<h1>सीखो</h1>
<p class="sub">आम स्कैम और उनसे बचने का तरीका।</p>
<details><summary>डिजिटल अरेस्ट</summary><p>कोई खुद को पुलिस, CBI या कस्टम बताकर कहता है कि तुम्हारे नाम पर ड्रग्स या केस है, और वीडियो कॉल पर "अरेस्ट" रखता है।</p><p><b>सच:</b> कोई एजेंसी वीडियो कॉल पर अरेस्ट नहीं करती और पैसे नहीं मांगती। कॉल काटो।</p></details>
<details><summary>KYC और OTP ठगी</summary><p>"खाता बंद हो जाएगा" का डर दिखाकर लिंक पर OTP या कार्ड डिटेल मांगते हैं।</p><p><b>बचाव:</b> बैंक कभी OTP, पिन या CVV नहीं मांगता। बैंक के ऑफ़िशियल ऐप से ही चेक करो।</p></details>
<details><summary>डीपफेक और नकली आवाज़</summary><p>AI से घर वाले या दोस्त की आवाज़ बनाकर "अभी पैसे भेजो" कहा जाता है।</p><p><b>बचाव:</b> कॉल काटकर उसी के पुराने नंबर पर खुद फोन करो। घर में एक सीक्रेट कोड-वर्ड रखो।</p></details>
<details><summary>नौकरी और टास्क स्कैम</summary><p>"घर बैठे रोज़ कमाओ", वीडियो लाइक करो या टास्क पूरे करो। पहले छोटा पैसा देते हैं, फिर "डिपॉज़िट" मांगते हैं।</p><p><b>बचाव:</b> असली नौकरी में पहले फीस नहीं लगती।</p></details>
<details><summary>UPI और QR स्कैम</summary><p>"रिफंड पाने के लिए पिन डालो" या "QR स्कैन करो"।</p><p><b>सच:</b> पैसे पाने के लिए पिन डालना या QR स्कैन करना नहीं पड़ता। पिन सिर्फ़ पैसे भेजने के लिए होता है।</p></details>
<details><summary>नकली लोन और इन्वेस्टमेंट ऐप</summary><p>"पक्का मुनाफा" या "दोगुने पैसे" का वादा, या ऐसा लोन ऐप जो कॉन्टैक्ट और फोटो की इजाज़त मांगता है।</p><p><b>बचाव:</b> पक्के मुनाफे का वादा हमेशा झूठ होता है। APK फ़ाइल से कोई ऐप इंस्टॉल मत करो।</p></details>
<h3>छोटी क्विज़</h3>
<div class="card" id="q"></div>
</section>

<section class="tab" id="t-help" hidden>
<h1>मदद</h1>
<p class="sub">अगर ठगी हो चुकी है, तो पहले एक घंटा सबसे ज़रूरी है।</p>
<a class="call" href="tel:1930">📞 1930 पर कॉल करो (साइबर क्राइम हेल्पलाइन, भारत)</a>
<p>ऑनलाइन शिकायत: <a class="l" href="https://cybercrime.gov.in" target="_blank" rel="noopener">cybercrime.gov.in</a></p>
<h3>पैसे कट गए? ये करो</h3>
<div id="ck"></div>
<p class="n">दूसरे देश में हो? अपने बैंक और वहां की साइबर पुलिस से तुरंत संपर्क करो।</p>
</section>

<section class="tab" id="t-plus" hidden>
<style>[hidden]{display:none!important}.pl{border:2px solid var(--brand)}.pr{font-size:28px;font-weight:800;margin:4px 0}.nm{width:100%;padding:12px;font:inherit;font-size:16px;color:var(--ink);background:var(--bg);border:2px solid var(--line);border-radius:12px}.ab{position:fixed;top:calc(env(safe-area-inset-top,0px) + 8px);right:12px;z-index:9;padding:3px 12px;border-radius:999px;font-size:12px;font-weight:800;color:#3a2700;background:linear-gradient(135deg,#ffe08a,#e0a100 55%,#f7d25a);box-shadow:0 1px 6px rgba(160,110,0,.5);border:0;cursor:pointer}.pay{display:block;flex:1;text-align:center;text-decoration:none}.qr{text-align:center;margin:14px 0}#qrb{display:inline-block;background:#fff;padding:12px;border-radius:14px;border:1px solid var(--line)}</style>
<h1>⭐ ScamGuard Plus</h1>
<p class="sub">ज़्यादा सुरक्षा के लिए पेड प्लान।</p>
<div class="card pl"><div class="pr" id="pr"></div><ul><li>नंबर की जांच: कोड से देश और नंबर का प्रकार</li><li>30 दिन के लिए। UTR डालते ही तुरंत चालू</li></ul><div class="row" id="pw"><a class="b pay" id="pa" href="#" onclick="$('#bm').textContent='UPI ऐप नहीं खुला? यह बटन उस फोन पर दबाओ जिसमें UPI ऐप हो।'">UPI से ₹99 दो</a></div>
<div id="pu"><div class="qr"><div id="qrb"></div><p class="n">या किसी भी UPI ऐप से यह QR स्कैन करो।</p></div><p class="n">पेमेंट के बाद UPI ऐप से 12 अंकों का UTR नंबर देखकर यहां डालो।</p><input class="nm" id="ut" inputmode="numeric" maxlength="12" placeholder="UTR नंबर (12 अंक)"><div class="row"><button class="g" onclick="cf()">Plus चालू करो</button></div><p class="n">Plus न खुले, या फोन बदलने पर चला जाए, तो वही UTR नंबर दोबारा डालो। Plus फिर चालू हो जाएगा।</p></div>
<p class="n" id="bm"></p></div>
<div id="nf"></div>
<h3>एडमिन लॉगिन</h3>
<div id="ad"></div>
</section>

<section class="tab" id="t-adm" hidden>
<h1>👑 एडमिन पैनल</h1>
<p class="sub">यह सिर्फ़ इस फोन का डेटा है। ऐप दूसरों के मैसेज जमा नहीं करता।</p>
<div id="am"></div>
</section>
</main>

<button id="ab" class="ab" hidden onclick="go('adm')" aria-label="एडमिन पैनल खोलो">👑 ADMIN</button>
<nav aria-label="मेन मेन्यू">
<button data-t="chk" onclick="go('chk')"><span>🔍</span>जांचो</button>
<button data-t="hist" onclick="go('hist')"><span>🕘</span>इतिहास</button>
<button data-t="learn" onclick="go('learn')"><span>📚</span>सीखो</button>
<button data-t="help" onclick="go('help')"><span>🆘</span>मदद</button>
<button data-t="plus" onclick="go('plus')"><span>⭐</span>Plus</button>
</nav>

<script src="https://cdnjs.cloudflare.com/ajax/libs/qrcodejs/1.0.0/qrcode.min.js"></script>
<script>
const $=s=>document.querySelector(s);
const MEM={};
const ld=(k,d)=>{try{const v=JSON.parse(localStorage.getItem(k));if(v!==null)return v}catch(e){}return k in MEM?MEM[k]:d};
const sv=(k,v)=>{MEM[k]=v;try{localStorage.setItem(k,JSON.stringify(v))}catch(e){}};
const esc=s=>String(s).replace(/[&<>"]/g,c=>({"&":"&amp;","<":"&lt;",">":"&gt;",'"':"&quot;"}[c]));
const SM="SBI: आपका KYC अपडेट नहीं है, खाता आज ही बंद हो जाएगा। तुरंत लिंक खोलकर OTP डालें: http://sbi-kyc-update.xyz/login";
const R=[
[/otp|ओटीपी|cvv|\bpin\b|पिन|password|पासवर्ड/i,30,"OTP, पिन या पासवर्ड की बात है। असली बैंक या कंपनी ये कभी नहीं मांगती"],
[/kyc|केवाईसी|खाता.{0,20}(बंद|ब्लॉक)|account.{0,25}(block|suspend|clos|deactivat)|pan.{0,15}(update|link)|aadhaa?r.{0,15}(link|update)/i,25,"KYC या अकाउंट बंद होने का डर दिखाया गया है"],
[/urgent|immediately|asap|last chance|expire|तुरंत|आज ही|जल्दी|24 ?(hours|घंटे)|within \d+ ?(hours|hrs|min)/i,15,"जल्दबाज़ी कराई जा रही है"],
[/lottery|jackpot|you(?:'ve| have)? won|winner|prize|lucky draw|लॉटरी|इनाम|जीत(ा|े|ी)|kbc|gift ?card/i,30,"इनाम या लॉटरी का लालच है"],
[/registration fee|processing fee|advance|security deposit|send money|पैसे भेज|फीस|जमा करो|डिपॉज़िट|शुल्क/i,22,"पैसे भेजने या फीस जमा करने को कहा गया है"],
[/work from home|part[- ]?time|daily (income|earning)|per day|youtube|like and|घर बैठे|रोज़ कमाओ|पार्ट टाइम/i,22,"आसान कमाई या घर बैठे काम का ऑफ़र है"],
[/cbi|police|customs|narcotic|\bed\b|arrest|warrant|trai|सीबीआई|पुलिस|कस्टम|गिरफ़्?तार|वारंट|नारकोटिक्स/i,30,"पुलिस, CBI या कस्टम के नाम पर डराया जा रहा है (डिजिटल अरेस्ट जैसा स्कैम)"],
[/anydesk|teamviewer|quick ?support|rustdesk|screen share|स्क्रीन शेयर/i,35,"फोन की स्क्रीन या रिमोट एक्सेस मांगा गया है"],
[/enter.{0,12}pin|collect request|scan.{0,20}qr|क्यूआर|रिफंड|refund/i,25,"UPI पिन, QR या रिफंड के नाम पर पैसे कटवाने की कोशिश हो सकती है"],
[/don'?t tell|do not (tell|share)|keep .{0,15}secret|किसी को (मत|न) बता|गोपनीय|राज़ रखो/i,20,"किसी को न बताने को कहा गया है। ठग यही करते हैं"],
[/guaranteed|double your|100% (profit|return)|crypto|trading group|stock tip|दोगुना|पक्का मुनाफा|गारंटी/i,25,"पक्के मुनाफे या दोगुने पैसे का वादा है"],
[/new number|नया नंबर|accident|hospital|bail|एक्सीडेंट|अस्पताल|जमानत/i,15,"घर वाले या जान-पहचान के नाम पर इमरजेंसी बताई गई है"]];
const U=/(?:https?:\/\/|www\.)[^\s]+|[a-z0-9-]+(?:\.[a-z0-9-]+)+\.[a-z]{2,}(?:\/[^\s]*)?/gi;
const SH=/^(bit\.ly|tinyurl\.com|t\.co|cutt\.ly|rb\.gy|is\.gd|goo\.gl|shorturl\.at|tiny\.cc|ow\.ly)$/;
const TLD=/\.(xyz|top|click|icu|live|work|shop|vip|site|buzz|cfd|sbs|rest|gq|tk|ml|cf|ga|monster|cyou)$/;
const BR=["sbi","hdfc","icici","paytm","phonepe","amazon","flipkart","irctc","uidai","incometax","whatsapp","google","instagram","netflix"];
const AD={
bad:["इस मैसेज या कॉल का जवाब मत दो और कोई लिंक मत खोलो","OTP, पिन, पासवर्ड या पैसे बिल्कुल मत भेजो","नंबर ब्लॉक करो और 1930 पर या cybercrime.gov.in पर रिपोर्ट करो","पैसे कट गए हों तो तुरंत 'मदद' टैब देखो"],
warn:["जल्दबाज़ी मत करो। पहले बैंक या कंपनी के ऑफ़िशियल नंबर या ऐप से खुद पता करो","क्लिक करने से पहले घर के किसी समझदार इंसान को दिखाओ","पक्का होने तक कोई जानकारी या पैसा मत भेजो"],
ok:["कोई साफ़ खतरा नहीं दिखा, फिर भी OTP, पिन या पैसे कभी किसी को मत दो","शक हो तो ऑफ़िशियल ऐप या वेबसाइट से खुद जांचो"]};
let last="";
function analyze(t){
 const hit=new Map(),add=(w,r)=>{if(!hit.has(r))hit.set(r,w)};
 R.forEach(([re,w,r])=>{if(re.test(t))add(w,r)});
 (t.match(U)||[]).forEach(u=>{
  u=u.replace(/[.,;:!?)]+$/,"");let h;
  try{h=new URL(/^https?:\/\//i.test(u)?u:"http://"+u)}catch(e){return}
  const host=h.hostname.toLowerCase(),f=u.toLowerCase();
  if(SH.test(host))add(20,"छोटा (शॉर्ट) लिंक है, असली पता छुपा होता है: "+host);
  if(/^\d{1,3}(\.\d{1,3}){3}$/.test(host))add(30,"लिंक में वेबसाइट का नाम नहीं, सिर्फ़ नंबर (IP) है");
  if(host.includes("xn--"))add(25,"लिंक में नकली दिखने वाले अक्षर (punycode) हैं");
  if(TLD.test(host))add(20,"लिंक का अंत संदिग्ध है: "+host);
  BR.forEach(b=>{if(host.includes(b)&&!new RegExp("(^|\\.)"+b+"\\.(com|in|co\\.in|gov\\.in|net|org)$").test(host))add(30,"लिंक में "+b.toUpperCase()+" का नाम है पर वेबसाइट असली नहीं लगती: "+host)});
  if(/\.apk(\?|$)/.test(f))add(35,"APK फ़ाइल डाउनलोड कराई जा रही है। इससे फोन हैक हो सकता है");
  if((host.match(/-/g)||[]).length>=2||host.split(".").length>4)add(10,"लिंक का नाम अजीब और लंबा है");
  if(/^http:\/\//i.test(f))add(8,"लिंक सुरक्षित (https) नहीं है");
 });
 return{score:Math.min(100,[...hit.values()].reduce((a,b)=>a+b,0)),why:[...hit.keys()]};
}
function check(){
 const t=$("#inp").value.trim();
 if(!t){$("#res").innerHTML='<p class="n">ऊपर कुछ चिपकाओ, फिर "जांचो" दबाओ।</p>';return}
 last=t;const{score,why}=analyze(t),L=score>=50?"bad":score>=20?"warn":"ok";
 const T={bad:["🚨 खतरा","स्कैम होने की बहुत संभावना है"],warn:["⚠️ शक की बात","सावधान रहो, पहले पक्का करो"],ok:["✅ साफ़ खतरा नहीं दिखा","फिर भी सावधान रहो"]}[L];
 $("#res").innerHTML=`<div class="card ${L}"><div class="meter"><i style="width:0"></i></div><h2>${T[0]}</h2><p class="m">${T[1]}। स्कोर ${score}/100</p>${why.length?`<h3>क्यों शक है</h3><ul>${why.map(x=>`<li>${esc(x)}</li>`).join("")}</ul>`:""}<h3>अब क्या करो</h3><ul>${AD[L].map(x=>`<li>${x}</li>`).join("")}</ul>${L!=="ok"?'<div class="row"><button class="b" onclick="share()">परिवार को अलर्ट भेजो</button></div>':""}<p class="n">यह जांच सिर्फ़ अंदाज़ा देती है, पक्की गारंटी नहीं।</p></div>`;
 requestAnimationFrame(()=>requestAnimationFrame(()=>{$("#res .meter i").style.width=Math.max(score,4)+"%"}));
 const h=ld("sg_h",[]);h.unshift({t:Date.now(),s:score,l:L,x:t.slice(0,300)});sv("sg_h",h.slice(0,40));st();
}
function share(){
 const t="⚠️ स्कैम अलर्ट! मुझे ऐसा मैसेज या कॉल आया: \""+last.slice(0,120)+"…\" यह स्कैम हो सकता है। OTP, पिन या पैसे किसी को मत देना। ScamGuard से जांचो।";
 if(navigator.share){navigator.share({text:t}).catch(()=>{})}else window.open("https://wa.me/?text="+encodeURIComponent(t),"_blank");
}
function st(){const h=ld("sg_h",[]);$("#n1").textContent=h.length;$("#n2").textContent=h.filter(x=>x.l==="bad").length}
function rh(){const h=ld("sg_h",[]);$("#hl").innerHTML=h.length?h.map((x,i)=>`<button class="it" onclick="again(${i})"><span class="d ${x.l}"></span><span><b>${x.s}/100</b><span class="c">${esc(x.x)}</span><small>${new Date(x.t).toLocaleDateString("hi-IN")}</small></span></button>`).join(""):'<p class="n">अभी कुछ नहीं जांचा। पहली जांच करके देखो।</p>'}
function again(i){$("#inp").value=ld("sg_h",[])[i].x;go("chk");check()}
function clr(){sv("sg_h",[]);rh();st()}
const CK=["बैंक या UPI ऐप की हेल्पलाइन पर कॉल करके कार्ड और अकाउंट तुरंत ब्लॉक कराओ","1930 पर कॉल करो या cybercrime.gov.in पर शिकायत दर्ज करो","स्क्रीनशॉट, मैसेज, नंबर और ट्रांज़ैक्शन ID सुरक्षित रखो","बैंक, ईमेल और UPI के पासवर्ड और पिन बदलो","फोन में AnyDesk जैसा कोई अनजान ऐप हो तो हटाओ","शिकायत की कॉपी और नंबर संभालकर रखो, थाने जाना पड़े तो काम आएगा"];
function rc(){const c=ld("sg_c",{});$("#ck").innerHTML=CK.map((x,i)=>`<label class="ci"><input type="checkbox" ${c[i]?"checked":""} onchange="tc(${i},this.checked)"><span>${x}</span></label>`).join("")}
function tc(i,v){const c=ld("sg_c",{});c[i]=v;sv("sg_c",c)}
const Q=[["कॉल: 'मैं CBI से हूं, तुम्हारे पार्सल में ड्रग्स मिले हैं, वीडियो कॉल पर आओ।'",1,"असली एजेंसी कभी वीडियो कॉल पर अरेस्ट नहीं करती।"],["तुमने खुद बैंक ऐप में पेमेंट किया और उसी का OTP तुम्हारे फोन पर आया।",0,"अपने काम का OTP सही है, बस किसी और को मत बताओ।"],["'पैसे पाने के लिए अपना UPI पिन डालो।'",1,"पैसे पाने के लिए पिन कभी नहीं डालना पड़ता।"],["'पापा, नया नंबर है, अभी 20,000 भेजो।' आवाज़ बिल्कुल बेटे जैसी है।",1,"पहले बेटे के पुराने नंबर पर फोन करके पक्का करो। आवाज़ AI से नकली हो सकती है।"]];
let qi=0,sc=0;
function rq(){const b=$("#q");if(qi>=Q.length){b.innerHTML=`<p><b>स्कोर: ${sc}/${Q.length}</b></p><button class="g" onclick="qi=0;sc=0;rq()">फिर से खेलो</button>`;return}
 b.innerHTML=`<p>${qi+1}/${Q.length}. ${Q[qi][0]}</p><div class="row"><button class="g" onclick="ans(1)">🚨 स्कैम</button><button class="g" onclick="ans(0)">✅ सही</button></div>`}
function ans(a){const r=a===Q[qi][1];if(r)sc++;$("#q").innerHTML=`<p>${r?"✅ सही जवाब!":"❌ गलत।"} ${Q[qi][2]}</p><button class="g" onclick="qi++;rq()">आगे</button>`}
function go(n){document.querySelectorAll(".tab").forEach(t=>t.hidden=t.id!=="t-"+n);document.querySelectorAll("nav button").forEach(b=>b.setAttribute("aria-current",String(b.dataset.t===n)));if(n==="hist")rh();if(n==="adm")ra();window.scrollTo(0,0)}
const PRICE="₹99 / महीना",_u="bXlsb3ZlLnlvdTA5QG9rYXhpcw==",_k=6213405645263041;
const h53=(s,z=0)=>{let a=0xdeadbeef^z,b=0x41c6ce57^z;for(let i=0,c;i<s.length;i++){c=s.charCodeAt(i);a=Math.imul(a^c,2654435761);b=Math.imul(b^c,1597334677)}a=Math.imul(a^(a>>>16),2246822507)^Math.imul(b^(b>>>13),3266489909);b=Math.imul(b^(b>>>16),2246822507)^Math.imul(a^(a>>>13),3266489909);return 4294967296*(2097151&b)+(a>>>0)};
const nm=e=>{e=e.trim().toLowerCase();let[l,d]=e.split("@");if(d==="googlemail.com")d="gmail.com";if(d==="gmail.com")l=l.split("+")[0].replace(/\./g,"");return l+"@"+d};
const CC={"1":"अमेरिका/कनाडा","7":"रूस/कज़ाख़स्तान","44":"ब्रिटेन","60":"मलेशिया","61":"ऑस्ट्रेलिया","62":"इंडोनेशिया","63":"फिलीपींस","66":"थाईलैंड","84":"वियतनाम","86":"चीन","91":"भारत","92":"पाकिस्तान","95":"म्यांमार","234":"नाइजीरिया","254":"केन्या","855":"कंबोडिया","856":"लाओस","880":"बांग्लादेश","971":"UAE","977":"नेपाल"};
function rp(){const pr=ld("sg_p",null),adm=ld("sg_a",false),on=!!(pr&&Date.now()-pr.t<2592000000),p=on||adm;
 $("#pr").textContent=PRICE;$("#pw").hidden=$("#pu").hidden=on;$("#ab").hidden=!adm;
 $("#pa").href="upi://pay?pa="+encodeURIComponent(atob(_u))+"&pn=ScamGuard&am=99&cu=INR&tn="+encodeURIComponent("ScamGuard Plus");
 $("#bm").textContent=on?"✅ Plus चालू है, "+new Date(pr.t+2592000000).toLocaleDateString("hi-IN")+" तक (UTR ..."+String(pr.u).slice(-4)+")":"";
 $("#ad").innerHTML=adm?'<button class="g" onclick="lo()">एडमिन लॉगआउट</button>':'<input class="nm" id="em" type="email" placeholder="ईमेल" autocomplete="email"><div class="row"><button class="g" onclick="li()">लॉगिन</button></div><p class="n" id="lm"></p>';
 $("#nf").innerHTML=p?'<div class="card"><h3>नंबर की जांच</h3><p class="n">कॉल या मैसेज भेजने वाले का नंबर डालो।</p><input class="nm" id="nm" type="tel" inputmode="tel" placeholder="+92 300 1234567"><div class="row"><button class="b" onclick="nc()">जांचो</button></div><div id="nr"></div></div>':'<p class="n">नंबर की जांच Plus में मिलती है।</p>'}
function mq(){const b=$("#qrb");if(b.firstChild)return;try{new QRCode(b,{text:"upi://pay?pa="+atob(_u)+"&pn=ScamGuard&am=99&cu=INR&tn=ScamGuard%20Plus",width:190,height:190,correctLevel:QRCode.CorrectLevel.M})}catch(e){$(".qr").hidden=true}}
function cf(){const u=$("#ut").value.trim();if(!/^\d{12}$/.test(u)){$("#bm").textContent="UTR नंबर 12 अंकों का होता है। UPI ऐप में ट्रांज़ैक्शन की डिटेल में देखो।";return}sv("sg_p",{u:u,t:Date.now()});rp()}
function li(){const e=nm($("#em").value);if(e.includes("@")&&h53("sg:"+e)===_k){sv("sg_a",true);rp();return}$("#lm").textContent="यह ईमेल एडमिन नहीं है।"}
function lo(){sv("sg_a",false);rp()}
function nc(){
 const raw=$("#nm").value.trim(),d=raw.replace(/\D/g,""),L=[];
 if(d.length<7){$("#nr").innerHTML='<p class="n">पूरा नंबर डालो।</p>';return}
 const x=d.replace(/^00/,"");let cc="",n="";
 if(/^(\+|00)/.test(raw)){for(const l of [3,2,1]){if(CC[x.slice(0,l)]){cc=x.slice(0,l);break}}
  if(cc){L.push("देश कोड +"+cc+": "+CC[cc]);if(cc==="91")n=x.slice(2);else L.push("यह भारत से बाहर का नंबर है। अनजान विदेशी नंबर से पैसे, नौकरी या इनाम की बात स्कैम का आम तरीका है")}
  else L.push("इस देश का कोड पहचान में नहीं आया। अनजान नंबर पर भरोसा मत करो")}
 else n=x.replace(/^0/,"").replace(/^91(?=\d{10}$)/,"");
 if(n){if(n.length!==10)L.push("भारतीय नंबर 10 अंकों का होता है, इसकी लंबाई अलग है");
  else if(/^140/.test(n))L.push("140 सीरीज़ टेलीमार्केटिंग की होती है। बैंक या पुलिस इससे कॉल नहीं करती");
  else if(/^[6-9]/.test(n))L.push("भारतीय मोबाइल नंबर जैसा दिखता है, पर इससे भेजने वाला भरोसेमंद नहीं हो जाता");
  else L.push("यह भारतीय मोबाइल नंबर जैसा नहीं दिखता")}
 $("#nr").innerHTML="<ul>"+L.map(i=>"<li>"+esc(i)+"</li>").join("")+'</ul><p class="n">यह सिर्फ़ नंबर के कोड से मिली जानकारी है। भेजने वाला असल में कहां है, यह कोई ऐप नहीं बता सकता, क्योंकि ठग नकली नंबर और इंटरनेट कॉल इस्तेमाल करते हैं। 1930 पर रिपोर्ट करो, पुलिस टेलीकॉम कंपनी से असली जानकारी निकलवा सकती है।</p>'}
function ra(){
 if(!ld("sg_a",false)){go("chk");return}
 const h=ld("sg_h",[]),c=l=>h.filter(x=>x.l===l).length,pr=ld("sg_p",null),on=!!(pr&&Date.now()-pr.t<2592000000);
 $("#am").innerHTML=`<div class="st"><div><b>${h.length}</b>जांचे गए</div><div><b>${c("bad")}</b>खतरा</div></div><div class="st" style="margin-top:10px"><div><b>${c("warn")}</b>शक</div><div><b>${c("ok")}</b>सुरक्षित</div></div><div class="card"><b>Plus:</b> ${on?"चालू, "+new Date(pr.t+2592000000).toLocaleDateString("hi-IN")+" तक":"बंद"}</div><h3>हाल की जांच</h3>${h.slice(0,10).map(x=>`<div class="it"><span class="d ${x.l}"></span><span><b>${x.s}/100</b><span class="c">${esc(x.x)}</span><small>${new Date(x.t).toLocaleString("hi-IN")}</small></span></div>`).join("")||'<p class="n">अभी कोई जांच नहीं।</p>'}`}
go("chk");st();rc();rq();rp();mq();
</script>
</body>
</html>
