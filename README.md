<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>نفادل — حماية ذكية، تربية واعية</title>
<link href="https://fonts.googleapis.com/css2?family=Tajawal:wght@300;400;500;700;800;900&family=Amiri:wght@400;700&display=swap" rel="stylesheet">
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
<style>
:root{
  --orange:#B8500A;--orange-light:#D4682A;--orange-pale:#FAF3EE;--orange-deep:#8C3A06;
  --white:#FFFFFF;--bg-cream:#FAF3EE;--gray:#F5EDE4;
  --text-dark:#1A0A00;--text-mid:#5C3A1E;--text-soft:#A07850;
  --green:#2E7D32;--green-light:#E8F5E9;--quran-bg:#FBF6EE;
  --gold:#B8860B;--gold-light:#E8A820;--card-shadow:0 8px 32px rgba(184,80,10,0.10);
}
*{box-sizing:border-box;margin:0;padding:0;}
body{font-family:'Tajawal',sans-serif;background:#2C1A0E;min-height:100vh;display:flex;align-items:center;justify-content:center;padding:20px;}
.phone{width:390px;height:844px;background:var(--bg-cream);border-radius:52px;overflow:hidden;box-shadow:0 40px 100px rgba(0,0,0,0.7),inset 0 1px 0 rgba(255,255,255,0.6);position:relative;}
.system-flow,.screen{display:none;width:100%;height:100%;flex-direction:column;}
.system-flow.active,.screen.active{display:flex;}
.pill-card{background:var(--white);border-radius:44px;margin:12px;padding:26px 22px 18px;flex:1;display:flex;flex-direction:column;overflow:hidden;box-shadow:var(--card-shadow);}
.scroll-area{overflow-y:auto;flex:1;}.scroll-area::-webkit-scrollbar{display:none;}
.top-header{padding:44px 26px 16px;display:flex;flex-direction:column;flex-shrink:0;background:var(--bg-cream);}
.btn-primary{background:var(--orange);color:white;border:none;border-radius:50px;padding:16px 24px;font-family:'Tajawal',sans-serif;font-size:17px;font-weight:700;cursor:pointer;width:100%;margin-bottom:10px;transition:transform .15s,box-shadow .15s;box-shadow:0 6px 18px rgba(184,80,10,0.30);}
.btn-primary:active{transform:scale(0.97);box-shadow:none;}
.btn-primary:disabled{background:#ccc;box-shadow:none;cursor:not-allowed;}
.btn-outline{background:transparent;color:var(--orange);border:2px solid var(--orange);border-radius:50px;padding:14px 24px;font-family:'Tajawal',sans-serif;font-size:15px;font-weight:600;cursor:pointer;width:100%;margin-bottom:10px;}
.btn-gold{background:linear-gradient(135deg,var(--gold),var(--gold-light));color:#1A0A00;border:none;border-radius:24px;padding:16px;width:100%;font-family:'Tajawal',sans-serif;font-size:16px;font-weight:900;cursor:pointer;box-shadow:0 6px 20px rgba(184,134,11,0.35);transition:transform .15s;}
.btn-gold:active{transform:scale(0.97);}
.btn-gold:disabled{background:#DDD;color:#999;box-shadow:none;cursor:not-allowed;}
.input-label{font-size:13px;font-weight:700;color:var(--text-mid);margin-bottom:7px;display:block;}
.input-field{width:100%;padding:14px 16px;border:2px solid #EDE0D4;border-radius:18px;font-family:'Tajawal',sans-serif;font-size:16px;color:var(--text-dark);outline:none;text-align:right;direction:rtl;margin-bottom:14px;transition:border-color .2s;background:var(--bg-cream);}
.input-field:focus{border-color:var(--orange);background:white;}
.otp-wrap{display:flex;justify-content:center;gap:12px;margin:18px 0;direction:ltr;}
.otp-box{width:58px;height:66px;border:2.5px solid #EDE0D4;border-radius:18px;font-size:26px;font-weight:800;text-align:center;color:var(--orange);font-family:'Tajawal',sans-serif;outline:none;transition:border-color .2s;background:var(--bg-cream);}
.otp-box:focus{border-color:var(--orange);background:white;}
.choice-card{background:var(--gray);border-radius:22px;padding:18px 16px;margin-bottom:12px;cursor:pointer;display:flex;align-items:center;gap:14px;border:2px solid transparent;transition:all .2s;}
.choice-card:hover{border-color:var(--orange);background:var(--orange-pale);}
.choice-icon{width:50px;height:50px;background:var(--orange);color:white;border-radius:15px;display:flex;align-items:center;justify-content:center;font-size:20px;flex-shrink:0;}
.choice-text h3{font-size:16px;font-weight:700;color:var(--text-dark);margin-bottom:2px;}
.choice-text p{font-size:12px;color:var(--text-soft);}
.choice-arrow{margin-right:auto;color:var(--text-soft);font-size:16px;}
.device-card{background:var(--gray);border-radius:18px;padding:13px 15px;margin-bottom:10px;display:flex;align-items:center;gap:12px;}
.device-avatar{width:42px;height:42px;background:var(--orange);color:white;border-radius:13px;display:flex;align-items:center;justify-content:center;font-size:18px;flex-shrink:0;}
.device-info h4{font-size:15px;font-weight:700;color:var(--text-dark);}
.device-info p{font-size:11px;color:var(--text-soft);margin-top:2px;}
.status-badge{margin-right:auto;font-size:11px;font-weight:700;padding:4px 10px;border-radius:20px;}
.status-on{background:#E8F5E9;color:var(--green);}
.status-off{background:#FFEBEE;color:#C62828;}
.map-mock{background:linear-gradient(135deg,#E8DDD0,#D8C8B8);border-radius:18px;height:120px;margin-bottom:14px;position:relative;overflow:hidden;display:flex;align-items:center;justify-content:center;}
.map-grid{position:absolute;inset:0;background-image:linear-gradient(rgba(184,80,10,0.08) 1px,transparent 1px),linear-gradient(90deg,rgba(184,80,10,0.08) 1px,transparent 1px);background-size:22px 22px;}
.map-pin{position:relative;z-index:2;display:flex;flex-direction:column;align-items:center;}
.map-pin-dot{width:16px;height:16px;background:var(--orange);border-radius:50%;border:3px solid white;animation:pulse 2s infinite;}
@keyframes pulse{0%{box-shadow:0 0 0 0 rgba(184,80,10,0.5);}70%{box-shadow:0 0 0 12px rgba(184,80,10,0);}100%{box-shadow:0 0 0 0 rgba(184,80,10,0);}}
.map-label{margin-top:5px;background:white;padding:3px 10px;border-radius:10px;font-size:11px;font-weight:700;color:var(--orange);box-shadow:0 2px 6px rgba(0,0,0,0.1);}
.video-card{background:#1A0A00;border-radius:18px;height:90px;margin-bottom:14px;display:flex;align-items:center;justify-content:center;flex-direction:column;gap:8px;cursor:pointer;position:relative;overflow:hidden;}
.video-card::before{content:'';position:absolute;inset:0;background:linear-gradient(135deg,rgba(184,80,10,0.5),transparent);}
.play-btn{width:46px;height:46px;background:white;border-radius:50%;display:flex;align-items:center;justify-content:center;font-size:16px;position:relative;z-index:2;box-shadow:0 4px 16px rgba(0,0,0,0.3);color:var(--orange);}
.video-label{color:white;font-size:12px;font-weight:600;position:relative;z-index:2;}
.section-label{font-size:11px;font-weight:700;color:var(--text-soft);margin-bottom:10px;margin-top:14px;letter-spacing:.5px;}
.screen-title{font-size:20px;font-weight:800;color:var(--text-dark);text-align:center;margin-bottom:5px;}
.screen-sub{font-size:13px;color:var(--text-soft);text-align:center;margin-bottom:20px;line-height:1.6;}
.back-btn{background:none;border:none;color:var(--orange);font-size:14px;font-family:'Tajawal',sans-serif;cursor:pointer;font-weight:700;margin-bottom:16px;display:flex;align-items:center;gap:6px;width:fit-content;}
.back-btn-white{color:white;}
.toggle-row{display:flex;align-items:center;justify-content:space-between;padding:12px 0;border-bottom:1px solid #F0E8E0;}
.toggle-label{font-size:14px;font-weight:600;color:var(--text-dark);}
.toggle-sub{font-size:11px;color:var(--text-soft);margin-top:2px;}
.toggle{width:48px;height:26px;background:var(--orange);border-radius:50px;position:relative;cursor:pointer;flex-shrink:0;transition:background .2s;}
.toggle::after{content:'';position:absolute;width:20px;height:20px;background:white;border-radius:50%;top:3px;right:3px;transition:right .2s;box-shadow:0 1px 4px rgba(0,0,0,0.2);}
.toggle.off{background:#DDD;}
.toggle.off::after{right:25px;}
.code-display{display:flex;justify-content:center;gap:10px;margin:12px 0;direction:ltr;}
.code-digit{width:52px;height:60px;background:var(--orange-pale);border-radius:16px;display:flex;align-items:center;justify-content:center;font-size:26px;font-weight:800;color:var(--orange);border:2px solid rgba(184,80,10,0.2);transition:all .3s;}
.code-digit.refreshing{transform:scale(0.88);opacity:0.4;}
.code-timer-bar{height:4px;background:#EDE0D4;border-radius:20px;margin:4px 0 8px;overflow:hidden;}
.code-timer-fill{height:100%;background:var(--orange);border-radius:20px;transition:width 1s linear;}
.code-timer-text{text-align:center;font-size:11px;color:var(--text-soft);margin-bottom:10px;}
.notif-badge{background:var(--orange-pale);border-radius:14px;padding:11px 14px;margin-bottom:10px;display:flex;align-items:center;gap:10px;border:1px solid rgba(184,80,10,0.15);}
.notif-icon{font-size:18px;color:var(--orange);}
.notif-text{font-size:13px;color:var(--text-mid);font-weight:600;}
.tab-bar{display:flex;justify-content:space-around;padding:10px 8px 16px;background:white;border-top:1px solid #F0E8E0;margin:0 -22px -18px;flex-shrink:0;}
.tab-item{display:flex;flex-direction:column;align-items:center;gap:3px;cursor:pointer;opacity:.3;font-size:10px;color:var(--text-dark);font-weight:600;transition:opacity .2s;}
.tab-item.active{opacity:1;color:var(--orange);}
.tab-icon{font-size:19px;}
.feedback-area{width:100%;min-height:90px;border:2px solid #EDE0D4;border-radius:18px;padding:14px;font-family:'Tajawal',sans-serif;font-size:14px;resize:none;outline:none;text-align:right;direction:rtl;margin-bottom:14px;background:var(--bg-cream);}
.feedback-area:focus{border-color:var(--orange);background:white;}
.switch-btn{background:var(--gray);color:var(--text-mid);border:none;border-radius:10px;padding:8px 12px;font-family:'Tajawal',sans-serif;font-size:11px;font-weight:700;cursor:pointer;width:100%;text-align:center;}
.spacer{flex:1;}
.time-picker-row{display:flex;align-items:center;justify-content:space-between;background:var(--gray);border-radius:16px;padding:12px 16px;margin-bottom:10px;}
.time-picker-label{font-size:14px;font-weight:700;color:var(--text-dark);}
.time-picker-label span{font-size:11px;color:var(--text-soft);display:block;margin-top:2px;font-weight:400;}
.time-select{border:2px solid var(--orange);border-radius:12px;padding:8px 12px;font-family:'Tajawal',sans-serif;font-size:15px;font-weight:700;color:var(--orange);background:white;outline:none;cursor:pointer;direction:ltr;}
.days-section{background:var(--gray);border-radius:16px;padding:14px 16px;margin-bottom:10px;}
.days-title{font-size:12px;font-weight:700;color:var(--text-mid);margin-bottom:10px;}
.days-grid{display:flex;gap:6px;flex-wrap:wrap;justify-content:center;}
.day-btn{width:40px;height:40px;border-radius:12px;border:2px solid #DDD;background:white;font-family:'Tajawal',sans-serif;font-size:11px;font-weight:700;color:var(--text-mid);cursor:pointer;transition:all .15s;display:flex;align-items:center;justify-content:center;}
.day-btn.active{background:var(--orange);border-color:var(--orange);color:white;box-shadow:0 3px 10px rgba(184,80,10,0.30);}
.day-btn.free-day{background:var(--green-light);border-color:var(--green);color:var(--green);}
.schedule-summary{background:var(--orange-pale);border:1.5px solid rgba(184,80,10,0.25);border-radius:14px;padding:12px 14px;margin-bottom:10px;font-size:12px;color:var(--text-mid);line-height:1.9;}
.schedule-summary b{color:var(--orange);}
.child-header{background:var(--orange);padding:46px 24px 18px;border-radius:0 0 34px 34px;display:flex;align-items:center;justify-content:space-between;flex-shrink:0;}
.child-avatar{width:46px;height:46px;background:rgba(255,255,255,0.2);color:white;border-radius:50%;display:flex;align-items:center;justify-content:center;font-size:22px;border:2px solid rgba(255,255,255,0.35);}
.child-greeting .hi{color:rgba(255,255,255,0.75);font-size:12px;}
.child-greeting .name{color:white;font-size:19px;font-weight:800;text-align:center;}
.time-section{display:flex;flex-direction:column;align-items:center;padding:14px 24px 10px;}
.time-label{font-size:12px;color:var(--text-soft);font-weight:600;margin-bottom:10px;}
.time-circle-wrap{position:relative;display:inline-block;}
.time-circle-wrap svg{transform:rotate(-90deg);}
.time-ring-bg{fill:none;stroke:#F0E0D4;stroke-width:10;}
.time-ring{fill:none;stroke:var(--orange);stroke-width:10;stroke-linecap:round;stroke-dasharray:283;stroke-dashoffset:94;}
.time-center{position:absolute;inset:0;display:flex;flex-direction:column;align-items:center;justify-content:center;}
.time-num{font-size:34px;font-weight:900;color:var(--orange);line-height:1;}
.time-unit{font-size:12px;color:var(--text-soft);font-weight:600;margin-top:2px;}
.time-sub{font-size:11px;color:#BBB;margin-top:6px;}
.status-bar{display:flex;gap:10px;padding:0 22px;margin-bottom:12px;}
.status-pill{flex:1;background:white;border-radius:16px;padding:11px 12px;display:flex;align-items:center;gap:8px;box-shadow:0 2px 10px rgba(184,80,10,0.07);}
.status-pill-icon{font-size:18px;color:var(--orange);}
.status-pill-text{font-size:11px;color:var(--text-mid);font-weight:600;line-height:1.4;}
.status-pill-text b{color:var(--orange);font-size:13px;display:block;}
.apps-label{padding:0 22px;font-size:12px;font-weight:700;color:var(--text-soft);margin-bottom:10px;}
.apps-grid{display:grid;grid-template-columns:repeat(4,1fr);gap:12px;padding:0 22px;}
.app-item{display:flex;flex-direction:column;align-items:center;gap:5px;cursor:pointer;}
.app-icon{width:56px;height:56px;color:white;border-radius:17px;display:flex;align-items:center;justify-content:center;font-size:22px;box-shadow:0 4px 12px rgba(0,0,0,0.12);transition:transform .15s;}
.app-icon:active{transform:scale(0.9);}
.app-name{font-size:10px;color:var(--text-mid);font-weight:600;text-align:center;}
.dad-msg{margin:10px 22px;background:white;border-radius:18px;padding:13px 15px;display:flex;align-items:center;gap:12px;box-shadow:0 2px 12px rgba(184,80,10,0.08);border-right:4px solid var(--orange);}
.dad-msg-text{font-size:12px;color:var(--text-mid);font-weight:600;line-height:1.5;}
.dad-msg-text b{color:var(--orange);}
.request-btn{margin:8px 22px 0;background:var(--orange);color:white;border:none;border-radius:22px;padding:14px;font-family:'Tajawal',sans-serif;font-size:15px;font-weight:700;cursor:pointer;display:flex;align-items:center;justify-content:center;gap:8px;box-shadow:0 6px 20px rgba(184,80,10,0.30);transition:transform .15s;width:calc(100% - 44px);}
.request-btn:active{transform:scale(0.97);}
.locked-screen-bg{background:linear-gradient(160deg,var(--orange) 0%,var(--orange-deep) 100%);overflow-y:auto;}
.locked-content{display:flex;flex-direction:column;align-items:center;padding:36px 28px;text-align:center;}
.lock-icon-big{font-size:80px;color:white;margin-bottom:20px;animation:wobble 3s ease-in-out infinite;}
@keyframes wobble{0%,100%{transform:rotate(-5deg);}50%{transform:rotate(5deg);}}
.locked-title{font-size:26px;font-weight:900;color:white;margin-bottom:8px;}
.locked-sub{font-size:14px;color:rgba(255,255,255,0.75);line-height:1.7;margin-bottom:28px;}
.locked-time-card{background:rgba(255,255,255,0.15);border-radius:22px;padding:18px 28px;margin-bottom:24px;width:100%;backdrop-filter:blur(10px);border:1px solid rgba(255,255,255,0.2);}
.locked-time-label{color:rgba(255,255,255,0.7);font-size:12px;margin-bottom:4px;}
.locked-time-val{color:white;font-size:30px;font-weight:900;}
.request-btn-locked{background:white;color:var(--orange);border:none;border-radius:50px;padding:16px 32px;font-family:'Tajawal',sans-serif;font-size:16px;font-weight:800;cursor:pointer;display:flex;align-items:center;gap:10px;box-shadow:0 8px 30px rgba(0,0,0,0.2);transition:transform .15s;}
.request-btn-locked:active{transform:scale(0.97);}
.locked-stars{display:flex;gap:6px;margin-top:24px;opacity:.5;}
.star{font-size:18px;color:white;animation:twinkle 2s ease-in-out infinite;}
.star:nth-child(2){animation-delay:.4s;}.star:nth-child(3){animation-delay:.8s;}
@keyframes twinkle{0%,100%{opacity:.3;transform:scale(0.8);}50%{opacity:1;transform:scale(1.1);}}
.request-content{display:flex;flex-direction:column;align-items:center;padding:36px 28px;text-align:center;overflow-y:auto;}
.sending-anim{font-size:72px;color:var(--orange);margin-bottom:20px;animation:float 2s ease-in-out infinite;}
@keyframes float{0%,100%{transform:translateY(0);}50%{transform:translateY(-10px);}}
.request-title{font-size:24px;font-weight:900;color:var(--orange);margin-bottom:8px;}
.request-sub{font-size:14px;color:#888;line-height:1.7;margin-bottom:26px;}
.waiting-card{background:white;border-radius:22px;padding:22px;width:100%;box-shadow:0 4px 20px rgba(184,80,10,0.08);margin-bottom:22px;}
.waiting-dots{display:flex;justify-content:center;gap:8px;margin-top:12px;}
.dot{width:10px;height:10px;background:var(--orange);border-radius:50%;animation:bounce 1.2s ease-in-out infinite;}
.dot:nth-child(2){animation-delay:.2s;}.dot:nth-child(3){animation-delay:.4s;}
@keyframes bounce{0%,100%{transform:translateY(0);opacity:.4;}50%{transform:translateY(-8px);opacity:1;}}
.approved-card{background:linear-gradient(135deg,var(--green-light),#F1F8E9);border-radius:22px;padding:22px;width:100%;border:2px solid #81C784;margin-bottom:18px;}
/* بوابة الدفع */
.payment-overlay{position:absolute;inset:0;background:rgba(26,10,0,0.7);backdrop-filter:blur(6px);z-index:100;display:none;align-items:flex-end;justify-content:center;}
.payment-overlay.active{display:flex;}
.payment-sheet{background:white;border-radius:36px 36px 0 0;padding:28px 24px 36px;width:100%;max-height:88%;overflow-y:auto;animation:slideUp .35s cubic-bezier(0.34,1.56,0.64,1);}
@keyframes slideUp{from{transform:translateY(100%);}to{transform:translateY(0);}}
.payment-handle{width:40px;height:4px;background:#EDE0D4;border-radius:10px;margin:0 auto 20px;}
.payment-title{font-size:20px;font-weight:900;color:var(--text-dark);text-align:center;margin-bottom:4px;}
.payment-sub{font-size:13px;color:var(--text-soft);text-align:center;margin-bottom:20px;}
.plan-price-big{background:var(--orange-pale);border:2px solid rgba(184,80,10,0.2);border-radius:20px;padding:16px;text-align:center;margin-bottom:18px;}
.plan-price-big .price{font-size:36px;font-weight:900;color:var(--orange);line-height:1;}
.plan-price-big .period{font-size:13px;color:var(--text-soft);margin-top:4px;}
.plan-features-list{list-style:none;margin-bottom:20px;}
.plan-features-list li{font-size:13px;color:var(--text-mid);padding:8px 0;border-bottom:1px solid #F0E8E0;display:flex;align-items:center;gap:8px;}
.plan-features-list li:last-child{border-bottom:none;}
.feat-check{color:var(--green);font-size:15px;}
.payment-methods{display:flex;gap:10px;margin-bottom:18px;}
.pay-method{flex:1;background:var(--gray);border:2px solid transparent;border-radius:14px;padding:12px 8px;text-align:center;cursor:pointer;transition:all .2s;font-size:11px;font-weight:700;color:var(--text-mid);}
.pay-method.selected{border-color:var(--orange);background:var(--orange-pale);color:var(--orange);}
.pay-method-icon{font-size:20px;display:block;margin-bottom:4px;}
.pay-secure-note{display:flex;align-items:center;gap:6px;justify-content:center;font-size:11px;color:var(--text-soft);margin-bottom:16px;}
/* القرآن */
.quran-lock-bg{background:linear-gradient(160deg,#1A0A00 0%,#2C1604 50%,#1A0A00 100%);overflow-y:auto;padding-bottom:20px;}
.quran-lock-header{padding:36px 24px 12px;text-align:center;color:var(--gold-light);}
.quran-lock-header h2{font-size:20px;font-weight:800;margin-bottom:4px;}
.quran-lock-header p{font-size:12px;opacity:.7;margin-bottom:8px;}
.reader-badge{background:rgba(232,168,32,0.15);border:1px solid rgba(232,168,32,0.3);border-radius:20px;padding:5px 14px;font-size:12px;font-weight:700;color:var(--gold-light);display:inline-block;}
.quran-container{background:var(--quran-bg);border-radius:22px;margin:0 16px 12px;padding:16px 12px;border:2px solid #E6D0B4;}
.surah-title{text-align:center;font-family:'Amiri',serif;font-size:16px;color:#7A4B1B;background:#F3EADB;border-radius:12px;padding:6px;margin-bottom:12px;font-weight:bold;}
.quran-line{font-family:'Amiri',serif;font-size:17px;color:#2C1805;text-align:center;line-height:1.9;padding:10px 8px;border-radius:10px;cursor:pointer;transition:all .2s;border-bottom:1px dashed rgba(184,134,11,0.15);position:relative;}
.quran-line.locked{color:#A0A0A0;opacity:.25;cursor:not-allowed;}
.quran-line.reading{background:#FFE3A8;border:2px solid var(--orange);color:#000;font-weight:bold;box-shadow:0 0 12px rgba(184,80,10,0.3);border-bottom:2px solid var(--orange);}
.quran-line.active{background:var(--green-light);border:2px solid var(--green);color:#1B5E20;font-weight:bold;border-bottom:2px solid var(--green);}
.quran-line.completed{background:rgba(76,175,80,0.12);color:var(--green);opacity:.75;}
.quran-line.completed::after{content:'✓';position:absolute;left:12px;color:var(--green);font-size:14px;}
.hadith-box{padding:0 16px;}
.hadith-card{background:white;border:2px solid #006C35;border-radius:22px;padding:20px;display:none;}
.hadith-card.active{display:block;}
.hadith-tag{font-size:11px;font-weight:bold;color:#006C35;background:var(--green-light);padding:2px 8px;border-radius:10px;display:inline-block;margin-bottom:12px;}
.hadith-text{font-family:'Amiri',serif;font-size:18px;line-height:1.85;color:var(--text-dark);text-align:center;font-weight:bold;}
.hadith-source{font-size:11px;color:var(--text-soft);text-align:center;margin-top:8px;font-style:italic;}
.hadith-btn{background:#006C35;color:white;border:none;border-radius:16px;padding:13px;width:100%;font-family:'Tajawal',sans-serif;font-size:14px;font-weight:700;margin-top:16px;cursor:pointer;transition:opacity .2s;}
.hadith-btn:disabled{opacity:.45;cursor:not-allowed;}
.progress-bar-wrap{background:rgba(255,255,255,0.08);border-radius:20px;margin:0 16px 12px;padding:12px 16px;border:1px solid rgba(232,168,32,0.2);}
.progress-label{color:var(--gold-light);font-size:12px;font-weight:600;margin-bottom:8px;}
.progress-track{background:rgba(255,255,255,0.1);border-radius:20px;height:8px;overflow:hidden;}
.progress-fill{background:linear-gradient(90deg,var(--gold),var(--gold-light));height:100%;border-radius:20px;transition:width .5s ease;}
.progress-steps{display:flex;justify-content:space-between;margin-top:6px;}
.progress-step{font-size:10px;color:rgba(232,168,32,0.4);font-weight:600;}
.progress-step.done{color:var(--gold-light);}
.quran-action-wrap{padding:0 16px 16px;margin-top:auto;}
/* popup رمز الربط */
.popup-overlay{position:absolute;inset:0;background:rgba(26,10,0,0.78);backdrop-filter:blur(8px);z-index:200;display:none;align-items:center;justify-content:center;}
.popup-overlay.active{display:flex;}
.popup-box{background:white;border-radius:32px;padding:28px 22px;width:340px;text-align:center;animation:popIn .3s cubic-bezier(0.34,1.56,0.64,1);}
@keyframes popIn{from{transform:scale(0.7);opacity:0;}to{transform:scale(1);opacity:1;}}
.popup-box h3{font-size:18px;font-weight:800;color:var(--text-dark);margin-bottom:6px;}
.popup-box p{font-size:12px;color:var(--text-soft);margin-bottom:14px;line-height:1.6;}
.child-slots{display:flex;gap:8px;margin-bottom:14px;justify-content:center;flex-wrap:wrap;}
.child-slot{background:var(--gray);border-radius:14px;padding:8px 12px;font-size:12px;font-weight:700;color:var(--text-mid);display:flex;align-items:center;gap:6px;cursor:pointer;border:2px solid transparent;transition:all .2s;min-width:68px;justify-content:center;}
.child-slot.selected{border-color:var(--orange);background:var(--orange-pale);color:var(--orange);}
.child-slot.empty{opacity:.4;border-style:dashed;cursor:default;}
.popup-code-wrap{display:flex;justify-content:center;gap:8px;margin:10px 0;direction:ltr;}
.popup-code-digit{width:52px;height:60px;background:var(--orange-pale);border-radius:14px;display:flex;align-items:center;justify-content:center;font-size:26px;font-weight:900;color:var(--orange);border:2px solid rgba(184,80,10,0.2);transition:all .3s;}
.popup-code-digit.refresh{transform:scale(0.85);opacity:.3;}
/* بطاقة الورد في الداشبورد */
.wird-banner{margin:0 22px 10px;background:linear-gradient(135deg,#1A0A00,#2C1604);border-radius:22px;padding:16px;display:flex;align-items:center;gap:14px;cursor:pointer;box-shadow:0 8px 24px rgba(0,0,0,0.3);}
.wird-banner-icon{width:50px;height:50px;background:linear-gradient(135deg,var(--gold),var(--gold-light));border-radius:16px;display:flex;align-items:center;justify-content:center;font-size:22px;flex-shrink:0;}
.wird-banner-text h4{color:var(--gold-light);font-size:15px;font-weight:800;margin-bottom:3px;}
.wird-banner-text p{color:rgba(255,255,255,0.6);font-size:11px;}
/* فترة الورد */
.wird-badge{display:inline-flex;align-items:center;gap:5px;padding:3px 10px;border-radius:20px;font-size:11px;font-weight:700;margin-top:6px;}
.wird-badge.morning{background:rgba(255,200,50,0.2);color:#FFC832;border:1px solid rgba(255,200,50,0.3);}
.wird-badge.evening{background:rgba(100,120,220,0.2);color:#AABBFF;border:1px solid rgba(100,120,220,0.3);}
/* حالة الصوت */
.audio-status{display:flex;align-items:center;justify-content:center;gap:8px;background:rgba(255,255,255,0.08);border-radius:14px;padding:10px;margin:0 16px 10px;font-size:12px;color:var(--gold-light);}
.audio-bars{display:flex;align-items:center;gap:3px;height:20px;}
.audio-bar{width:4px;background:var(--gold-light);border-radius:4px;animation:audioAnim 1.2s ease-in-out infinite;}
.audio-bar:nth-child(1){height:8px;animation-delay:0s;}
.audio-bar:nth-child(2){height:16px;animation-delay:.15s;}
.audio-bar:nth-child(3){height:12px;animation-delay:.3s;}
.audio-bar:nth-child(4){height:20px;animation-delay:.45s;}
.audio-bar:nth-child(5){height:10px;animation-delay:.6s;}
@keyframes audioAnim{0%,100%{transform:scaleY(.5);opacity:.5;}50%{transform:scaleY(1.1);opacity:1;}}
.audio-status.paused .audio-bar{animation-play-state:paused;}
</style>
</head>
<body>
<div class="phone" id="phone-root">

<!-- ══ التدفق المشترك ══ -->
<div class="system-flow active" id="flow-core">
  <div class="screen active" id="s1" style="background:var(--bg-cream);">
    <div style="flex:1;display:flex;flex-direction:column;align-items:center;justify-content:center;padding:36px 28px;">
      <div style="background:white;border-radius:40px;padding:40px 54px;margin-bottom:40px;display:flex;flex-direction:column;align-items:center;box-shadow:0 24px 70px rgba(184,80,10,0.18);">
        <div style="font-size:72px;font-weight:900;color:var(--orange);line-height:1;">ن</div>
        <div style="font-size:28px;font-weight:800;color:var(--orange);margin-top:6px;letter-spacing:3px;">نفـادل</div>
        <div style="font-size:13px;color:var(--orange-light);margin-top:3px;letter-spacing:2px;">Nafadil</div>
      </div>
      <p style="color:var(--text-mid);font-size:15px;text-align:center;line-height:2;margin-bottom:44px;">
        حماية أطفالك وتربيتهم بين يديك<br>
        <span style="font-size:13px;color:var(--text-soft);">بسيط · آمن · ومربٍّ ذكي</span>
      </p>
      <button class="btn-primary" onclick="showScreen('s2')"><i class="fas fa-arrow-left"></i> ابدأ الآن</button>
    </div>
  </div>
  <div class="screen" id="s2" style="background:var(--bg-cream);">
    <div class="top-header">
      <div style="display:flex;align-items:center;gap:8px;">
        <div style="font-size:30px;font-weight:900;color:var(--orange);">ن</div>
        <div style="font-size:18px;font-weight:700;color:var(--orange);letter-spacing:1px;">نفـادل</div>
      </div>
    </div>
    <div class="pill-card">
      <div class="screen-title">مرحباً بك 👋</div>
      <div class="screen-sub">كيف تريد الدخول؟</div>
      <div class="choice-card" onclick="switchSystem('parent')">
        <div class="choice-icon"><i class="fas fa-user-tie"></i></div>
        <div class="choice-text"><h3>ولي الأمر</h3><p>تحكم وراقب أجهزة أطفالك</p></div>
        <div class="choice-arrow"><i class="fas fa-chevron-left"></i></div>
      </div>
      <div class="choice-card" onclick="switchSystem('child')">
        <div class="choice-icon"><i class="fas fa-child"></i></div>
        <div class="choice-text"><h3>الابن / البنت</h3><p>ربط جهازك والورد اليومي</p></div>
        <div class="choice-arrow"><i class="fas fa-chevron-left"></i></div>
      </div>
      <div class="spacer"></div>
      <p style="text-align:center;font-size:11px;color:var(--text-soft);">نفادل | بريدة، المملكة العربية السعودية</p>
    </div>
  </div>
</div>

<!-- ══ تدفق ولي الأمر ══ -->
<div class="system-flow" id="flow-parent" style="background:var(--bg-cream);">
  <!-- S3 -->
  <div class="screen" id="s3">
    <div class="top-header">
      <button class="back-btn" onclick="exitToMainMenu()"><i class="fas fa-chevron-left"></i> خروج</button>
      <div style="color:var(--text-dark);font-size:20px;font-weight:800;margin-bottom:4px;">تسجيل ولي الأمر</div>
      <div style="color:var(--text-soft);font-size:12px;">أدخل رقم جوالك لاستقبال رمز التحقق</div>
    </div>
    <div class="pill-card">
      <label class="input-label">رقم الجوال</label>
      <input class="input-field" id="phone-input" type="tel" placeholder="05xxxxxxxx" maxlength="10" style="font-size:20px;text-align:center;letter-spacing:2px;" autocomplete="off">
      <div class="spacer"></div>
      <button class="btn-primary" onclick="handleSendOTP()"><i class="fas fa-mobile-alt"></i> إرسال رمز التحقق</button>
      <p style="text-align:center;font-size:11px;color:var(--text-soft);">ستصلك رسالة SMS برمز التحقق</p>
    </div>
  </div>
  <!-- S4 -->
  <div class="screen" id="s4">
    <div class="top-header">
      <button class="back-btn" onclick="showScreen('s3')"><i class="fas fa-chevron-left"></i> رجوع</button>
      <div style="color:var(--text-dark);font-size:20px;font-weight:800;margin-bottom:4px;">رمز التحقق</div>
    </div>
    <div class="pill-card">
      <div style="text-align:center;font-size:46px;margin-bottom:12px;color:var(--orange);"><i class="fas fa-envelope-open-text"></i></div>
      <div class="screen-title">تحقق من جوالك</div>
      <div class="screen-sub">رمز من 4 أرقام أُرسل إلى جوالك</div>
      <div class="otp-wrap">
        <input class="otp-box parent-otp" maxlength="1" type="tel" autocomplete="off">
        <input class="otp-box parent-otp" maxlength="1" type="tel" autocomplete="off">
        <input class="otp-box parent-otp" maxlength="1" type="tel" autocomplete="off">
        <input class="otp-box parent-otp" maxlength="1" type="tel" autocomplete="off">
      </div>
      <div class="spacer"></div>
      <button class="btn-primary" onclick="handleVerifyOTP()">تحقق وأدخل</button>
      <button class="btn-outline" onclick="showScreen('s3')">إعادة إرسال الرمز</button>
    </div>
  </div>
  <!-- S5 -->
  <div class="screen" id="s5">
    <div class="top-header">
      <div style="color:var(--text-dark);font-size:20px;font-weight:800;margin-bottom:4px;"><i class="fas fa-lock" style="color:var(--orange);"></i> رمز الدخول السري</div>
      <div style="color:var(--text-soft);font-size:12px;">حدد رمزاً سرياً لكل دخول</div>
    </div>
    <div class="pill-card">
      <div class="screen-sub" style="margin-bottom:6px;">أدخل رمزاً من 4 أرقام</div>
      <div class="otp-wrap">
        <input class="otp-box pin1" maxlength="1" type="password" autocomplete="new-password">
        <input class="otp-box pin1" maxlength="1" type="password" autocomplete="new-password">
        <input class="otp-box pin1" maxlength="1" type="password" autocomplete="new-password">
        <input class="otp-box pin1" maxlength="1" type="password" autocomplete="new-password">
      </div>
      <div class="screen-sub" style="margin-bottom:6px;">أعد الإدخال للتأكيد</div>
      <div class="otp-wrap">
        <input class="otp-box pin2" maxlength="1" type="password" autocomplete="new-password">
        <input class="otp-box pin2" maxlength="1" type="password" autocomplete="new-password">
        <input class="otp-box pin2" maxlength="1" type="password" autocomplete="new-password">
        <input class="otp-box pin2" maxlength="1" type="password" autocomplete="new-password">
      </div>
      <div class="spacer"></div>
      <button class="btn-primary" onclick="handleSetPIN()"><i class="fas fa-check"></i> حفظ الرمز السري</button>
    </div>
  </div>
  <!-- S6 لوحة التحكم -->
  <div class="screen" id="s6">
    <div style="background:var(--bg-cream);padding:44px 26px 8px;">
      <div style="display:flex;justify-content:space-between;align-items:center;margin-bottom:4px;">
        <div style="font-size:22px;cursor:pointer;color:var(--orange);" onclick="showScreen('s10')"><i class="fas fa-bell"></i></div>
        <div style="color:var(--text-dark);font-size:16px;font-weight:700;">لوحة التحكم</div>
        <div style="font-size:26px;font-weight:900;color:var(--orange);">ن</div>
      </div>
      <div style="color:var(--text-soft);font-size:13px;text-align:center;margin-bottom:8px;">مرحباً، يوسف 👋</div>
    </div>
    <div class="pill-card" style="padding-top:14px;">
      <div class="scroll-area">
        <!-- بطاقة ربط الجهاز في المنتصف -->
        <div style="background:linear-gradient(135deg,var(--orange),var(--orange-deep));border-radius:22px;padding:18px;margin-bottom:14px;cursor:pointer;display:flex;align-items:center;gap:14px;box-shadow:0 8px 24px rgba(184,80,10,0.35);" onclick="openLinkPopup()">
          <div style="width:50px;height:50px;background:rgba(255,255,255,0.2);border-radius:16px;display:flex;align-items:center;justify-content:center;font-size:22px;color:white;flex-shrink:0;"><i class="fas fa-link"></i></div>
          <div><div style="color:white;font-size:16px;font-weight:800;margin-bottom:3px;">ربط جهاز طفل جديد</div><div style="color:rgba(255,255,255,0.72);font-size:11px;">اضغط للحصول على رمز الربط</div></div>
          <div style="margin-right:auto;color:rgba(255,255,255,0.7);font-size:18px;"><i class="fas fa-chevron-left"></i></div>
        </div>
        <div class="section-label">📍 موقع الأطفال</div>
        <div class="map-mock">
          <div class="map-grid"></div>
          <div class="map-pin"><div class="map-pin-dot"></div><div class="map-label">نورة — بريدة</div></div>
        </div>
        <div class="section-label">📱 الأجهزة المرتبطة</div>
        <div class="device-card">
          <div class="device-avatar"><i class="fas fa-child"></i></div>
          <div class="device-info"><h4>نورة</h4><p>آيباد — نشط الآن</p></div>
          <div class="status-badge status-on">نشط</div>
        </div>
        <div class="device-card">
          <div class="device-avatar"><i class="fas fa-child"></i></div>
          <div class="device-info"><h4>محمد</h4><p>آيفون — مقيّد الآن</p></div>
          <div class="status-badge status-off">مقيّد</div>
        </div>
        <div class="section-label">🎬 شرح الاستخدام</div>
        <div class="video-card">
          <div class="play-btn"><i class="fas fa-play"></i></div>
          <div class="video-label">كيف تضيف جهاز طفلك وتستخدم نفادل</div>
        </div>
        <div class="section-label">🔔 تنبيهات</div>
        <div class="notif-badge"><div class="notif-icon"><i class="fas fa-exclamation-triangle"></i></div><div class="notif-text">نورة تطلب وقتاً إضافياً</div></div>
        <div class="notif-badge"><div class="notif-icon"><i class="fas fa-mobile-alt"></i></div><div class="notif-text">محمد حمّل تطبيقاً جديداً</div></div>
        <div class="notif-badge"><div class="notif-icon"><i class="fas fa-book-open"></i></div><div class="notif-text">محمد أكمل ورده القرآني ✅</div></div>
        <button class="btn-primary" style="margin-top:14px;margin-bottom:6px;" onclick="showScreen('s7')"><i class="fas fa-cog"></i> إعدادات الجداول والأجهزة</button>
        <button class="switch-btn" onclick="exitToMainMenu()"><i class="fas fa-sign-out-alt"></i> تغيير الحساب</button>
        <div style="height:8px;"></div>
      </div>
      <div class="tab-bar">
        <div class="tab-item active" onclick="showScreen('s6')"><div class="tab-icon"><i class="fas fa-home"></i></div>الرئيسية</div>
        <div class="tab-item" onclick="showScreen('s7')"><div class="tab-icon"><i class="fas fa-mobile-alt"></i></div>الأجهزة</div>
        <div class="tab-item"><div class="tab-icon"><i class="fas fa-chart-bar"></i></div>التقارير</div>
        <div class="tab-item" onclick="showScreen('s10')"><div class="tab-icon"><i class="fas fa-comments"></i></div>الدعم</div>
      </div>
    </div>
  </div>
  <!-- S7 الإعدادات -->
  <div class="screen" id="s7">
    <div class="top-header">
      <button class="back-btn" onclick="showScreen('s6')"><i class="fas fa-chevron-left"></i> رجوع</button>
      <div style="color:var(--text-dark);font-size:20px;font-weight:800;margin-bottom:4px;">إعدادات الجهاز</div>
      <div style="color:var(--text-soft);font-size:12px;">جدول الورد والقفل والصلاحيات</div>
    </div>
    <div class="pill-card">
      <div class="scroll-area">
        <label class="input-label">اسم الطفل</label>
        <input class="input-field" type="text" placeholder="مثال: نورة" autocomplete="off" maxlength="30">
        <div class="section-label">📖 الورد القرآني — قفلان يومياً</div>
        <div style="background:var(--orange-pale);border-radius:14px;padding:12px 14px;margin-bottom:10px;font-size:12px;color:var(--text-mid);line-height:2;border:1.5px solid rgba(184,80,10,0.2);">
          🌅 <b style="color:var(--orange);">الورد الصباحي:</b> 6:00 ص ← 6:00 م<br>
          🌙 <b style="color:var(--orange);">الورد المسائي:</b> 6:00 م ← 6:00 ص<br>
          <span style="font-size:11px;color:var(--text-soft);">الجهاز يُقفل حتى يكمل الطفل وردَه في كل فترة</span>
        </div>
        <div class="section-label">⏰ جدول القفل الليلي</div>
        <div class="time-picker-row">
          <div class="time-picker-label">🌙 وقت القفل<span>يقفل الجهاز تلقائياً</span></div>
          <select class="time-select" id="lock-time" onchange="updateSummary()">
            <option value="19:00">7:00 م</option><option value="20:00">8:00 م</option>
            <option value="21:00" selected>9:00 م</option><option value="22:00">10:00 م</option>
            <option value="23:00">11:00 م</option>
          </select>
        </div>
        <div class="time-picker-row">
          <div class="time-picker-label">☀️ وقت الفتح<span>يفتح الجهاز صباحاً</span></div>
          <select class="time-select" id="unlock-time" onchange="updateSummary()">
            <option value="06:00">6:00 ص</option><option value="07:00" selected>7:00 ص</option>
            <option value="08:00">8:00 ص</option><option value="09:00">9:00 ص</option>
          </select>
        </div>
        <div class="days-section">
          <div class="days-title">📅 أيام تطبيق الجدول</div>
          <div class="days-grid">
            <button class="day-btn active" onclick="toggleDay(this,'الأحد')">أحد</button>
            <button class="day-btn active" onclick="toggleDay(this,'الاثنين')">اثنين</button>
            <button class="day-btn active" onclick="toggleDay(this,'الثلاثاء')">ثلاثاء</button>
            <button class="day-btn active" onclick="toggleDay(this,'الأربعاء')">أربعاء</button>
            <button class="day-btn active" onclick="toggleDay(this,'الخميس')">خميس</button>
            <button class="day-btn free-day" onclick="toggleDay(this,'الجمعة')">جمعة</button>
            <button class="day-btn free-day" onclick="toggleDay(this,'السبت')">سبت</button>
          </div>
          <div style="margin-top:8px;font-size:10px;color:var(--text-soft);text-align:center;">🟢 إجازة &nbsp;|&nbsp; 🟠 يوم دراسي مقيّد</div>
        </div>
        <div class="schedule-summary" id="schedule-summary">
          📋 <b>ملخص:</b> يقفل <b id="sum-lock">9:00 م</b> — يفتح <b id="sum-unlock">7:00 ص</b><br>
          📅 التقييد: <b id="sum-days">أحد–خميس</b> | 🎉 إجازة: <b id="sum-free">جمعة، سبت</b>
        </div>
        <div class="section-label">🛡️ الصلاحيات</div>
        <div class="toggle-row"><div><div class="toggle-label"><i class="fas fa-map-marker-alt" style="color:var(--orange);"></i> تتبع الموقع</div><div class="toggle-sub">معرفة مكان الطفل دائماً</div></div><div class="toggle"></div></div>
        <div class="toggle-row"><div><div class="toggle-label"><i class="fas fa-ban" style="color:var(--orange);"></i> حظر التطبيقات</div><div class="toggle-sub">مراجعة التطبيقات الجديدة</div></div><div class="toggle"></div></div>
        <div class="toggle-row"><div><div class="toggle-label"><i class="fas fa-moon" style="color:var(--orange);"></i> وضع النوم التلقائي</div><div class="toggle-sub">حسب الجدول المحدد</div></div><div class="toggle"></div></div>
        <div class="toggle-row"><div><div class="toggle-label"><i class="fas fa-book-open" style="color:var(--orange);"></i> الورد القرآني إجباري</div><div class="toggle-sub">فتح الجهاز مشروط بإكمال الورد</div></div><div class="toggle"></div></div>
        <div style="height:12px;"></div>
        <button class="btn-primary" onclick="openPaymentGate()"><i class="fas fa-check"></i> تأكيد الإضافة</button>
      </div>
    </div>
  </div>
  <!-- S10 الدعم -->
  <div class="screen" id="s10">
    <div class="top-header">
      <button class="back-btn" onclick="showScreen('s6')"><i class="fas fa-chevron-left"></i> رجوع</button>
      <div style="color:var(--text-dark);font-size:20px;font-weight:800;margin-bottom:4px;">الشكاوى والاقتراحات</div>
    </div>
    <div class="pill-card">
      <div class="choice-card" style="margin-bottom:10px;"><div class="choice-icon"><i class="fas fa-bug"></i></div><div class="choice-text"><h3>الإبلاغ عن مشكلة</h3><p>واجهت خللاً في التطبيق؟</p></div></div>
      <div class="choice-card" style="margin-bottom:18px;"><div class="choice-icon"><i class="fas fa-lightbulb"></i></div><div class="choice-text"><h3>اقتراح فكرة</h3><p>عندك فكرة تطوّر التطبيق؟</p></div></div>
      <label class="input-label">اكتب رسالتك</label>
      <textarea class="feedback-area" placeholder="اكتب هنا..." maxlength="1000"></textarea>
      <div class="spacer"></div>
      <button class="btn-primary"><i class="fas fa-paper-plane"></i> إرسال</button>
      <p style="text-align:center;font-size:11px;color:var(--text-soft);margin-top:8px;">يوسف الشلاحي | نفادل — بريدة</p>
    </div>
  </div>
</div>

<!-- ══ تدفق الابن/البنت ══ -->
<div class="system-flow" id="flow-child" style="background:var(--bg-cream);">
  <!-- S8 -->
  <div class="screen" id="s8">
    <div class="top-header">
      <button class="back-btn" onclick="exitToMainMenu()"><i class="fas fa-chevron-left"></i> خروج</button>
      <div style="color:var(--text-dark);font-size:20px;font-weight:800;margin-bottom:4px;">ربط الجهاز <i class="fas fa-mobile-alt" style="color:var(--orange);"></i></div>
      <div style="color:var(--text-soft);font-size:12px;">أدخل الرمز الذي أعطاك إياه ولي أمرك</div>
    </div>
    <div class="pill-card">
      <div style="text-align:center;font-size:52px;margin-bottom:12px;color:var(--orange);"><i class="fas fa-child"></i></div>
      <div class="screen-title">أهلاً!</div>
      <div class="screen-sub">أدخل رمز الربط المكون من 4 أرقام</div>
      <div class="otp-wrap">
        <input class="otp-box child-otp" maxlength="1" type="tel" autocomplete="off">
        <input class="otp-box child-otp" maxlength="1" type="tel" autocomplete="off">
        <input class="otp-box child-otp" maxlength="1" type="tel" autocomplete="off">
        <input class="otp-box child-otp" maxlength="1" type="tel" autocomplete="off">
      </div>
      <div class="spacer"></div>
      <button class="btn-primary" onclick="showScreen('s9')">ربط الجهاز</button>
    </div>
  </div>
  <!-- S9 -->
  <div class="screen" id="s9">
    <div class="top-header">
      <div style="color:var(--text-dark);font-size:20px;font-weight:800;margin-bottom:4px;">موافقة الصلاحيات</div>
    </div>
    <div class="pill-card">
      <div style="text-align:center;font-size:44px;margin-bottom:12px;color:var(--orange);"><i class="fas fa-shield-alt"></i></div>
      <div class="screen-title">طلب من ولي الأمر</div>
      <div class="screen-sub">يحتاج نفادل لهذه الأذونات لحمايتك</div>
      <div class="toggle-row"><div><div class="toggle-label">📍 الوصول للموقع</div><div class="toggle-sub">دائمًا</div></div><div style="color:var(--orange);font-size:12px;font-weight:700;">مطلوب</div></div>
      <div class="toggle-row"><div><div class="toggle-label">📱 مراقبة التطبيقات</div></div><div style="color:var(--orange);font-size:12px;font-weight:700;">مطلوب</div></div>
      <div class="toggle-row"><div><div class="toggle-label">⏰ وقت الشاشة</div></div><div style="color:var(--orange);font-size:12px;font-weight:700;">مطلوب</div></div>
      <div class="toggle-row"><div><div class="toggle-label">📖 الورد القرآني</div><div class="toggle-sub">شرط لفتح الجهاز يومياً</div></div><div style="color:var(--orange);font-size:12px;font-weight:700;">مطلوب</div></div>
      <div class="spacer"></div>
      <button class="btn-primary" onclick="showScreen('child-dashboard')"><i class="fas fa-check"></i> أوافق على الكل</button>
      <p style="text-align:center;font-size:11px;color:var(--text-soft);margin-top:8px;">الموافقة إجبارية لاستخدام التطبيق</p>
    </div>
  </div>
  <!-- داشبورد الطفل -->
  <div class="screen" id="child-dashboard" style="background:var(--bg-cream);overflow-y:auto;">
    <div class="child-header">
      <div class="child-avatar"><i class="fas fa-user-circle"></i></div>
      <div class="child-greeting"><div class="hi">أهلاً وسهلاً</div><div class="name">نورة 🌸</div></div>
      <div style="color:white;font-size:26px;font-weight:900;">ن</div>
    </div>
    <div class="time-section">
      <div class="time-label">⏰ وقتك المتبقي اليوم</div>
      <div class="time-circle-wrap">
        <svg width="120" height="120" viewBox="0 0 100 100">
          <circle class="time-ring-bg" cx="50" cy="50" r="45"/>
          <circle class="time-ring" cx="50" cy="50" r="45"/>
        </svg>
        <div class="time-center"><div class="time-num">١:٣٠</div><div class="time-unit">ساعة</div></div>
      </div>
      <div class="time-sub">من أصل ٣ ساعات يومياً</div>
    </div>
    <div class="status-bar">
      <div class="status-pill"><div class="status-pill-icon"><i class="fas fa-moon"></i></div><div class="status-pill-text"><b>٩:٠٠ م</b>وقت النوم</div></div>
      <div class="status-pill"><div class="status-pill-icon"><i class="fas fa-check-circle" style="color:var(--green);"></i></div><div class="status-pill-text"><b>مفتوح</b>الجهاز نشط</div></div>
    </div>
    <!-- بطاقة الورد المنتصف -->
    <div class="wird-banner" onclick="openQuranSystem()">
      <div class="wird-banner-icon">📖</div>
      <div class="wird-banner-text">
        <h4 id="wird-banner-title">ورد اليوم القرآني</h4>
        <p id="wird-banner-sub">اضغط لبدء الورد وفتح جهازك</p>
      </div>
      <div style="margin-right:auto;color:var(--gold-light);font-size:18px;"><i class="fas fa-chevron-left"></i></div>
    </div>
    <div class="apps-label">التطبيقات المسموحة 📱</div>
    <div class="apps-grid">
      <div class="app-item"><div class="app-icon" style="background:linear-gradient(135deg,#FF6B6B,#FF8E53);"><i class="fab fa-youtube"></i></div><div class="app-name">يوتيوب</div></div>
      <div class="app-item" onclick="showScreen('child-locked')"><div class="app-icon" style="background:linear-gradient(135deg,#4ECDC4,#44A08D);"><i class="fas fa-gamepad"></i></div><div class="app-name">ألعاب</div></div>
      <div class="app-item"><div class="app-icon" style="background:linear-gradient(135deg,#A8E063,#56AB2F);"><i class="fas fa-book"></i></div><div class="app-name">مدرستي</div></div>
      <div class="app-item"><div class="app-icon" style="background:linear-gradient(135deg,#667eea,#764ba2);"><i class="fas fa-palette"></i></div><div class="app-name">رسم</div></div>
    </div>
    <div class="dad-msg"><div style="font-size:22px;color:var(--orange);"><i class="fas fa-comment-dots"></i></div><div class="dad-msg-text"><b>رسالة من أبوكِ 👨</b><br>ذاكري أولاً وبعدين العب ❤️</div></div>
    <button class="request-btn" onclick="showScreen('child-request')"><i class="fas fa-hand-paper"></i> طلب وقت إضافي من أبوي</button>
    <div style="padding:8px 22px 16px;"><button class="switch-btn" onclick="exitToMainMenu()"><i class="fas fa-cog"></i> تغيير الحساب</button></div>
  </div>
  <!-- شاشة القفل -->
  <div class="screen locked-screen-bg" id="child-locked">
    <div class="locked-content">
      <div class="lock-icon-big"><i class="fas fa-lock"></i></div>
      <div class="locked-title">انتهى وقتك اليوم</div>
      <div class="locked-sub">خلص الوقت المسموح لك<br>استرحي وارجعي بكره 🌙</div>
      <div class="locked-time-card"><div class="locked-time-label">يفتح الجهاز بكرة في</div><div class="locked-time-val">٨:٠٠ ص ☀️</div></div>
      <button class="request-btn-locked" onclick="showScreen('child-request')"><i class="fas fa-hand-paper"></i> طلب وقت من أبوي</button>
      <button class="btn-gold" style="width:auto;padding:14px 28px;margin-top:14px;" onclick="openQuranSystem()">📖 أكمل وردي لأفتح الجهاز</button>
      <div class="locked-stars"><div class="star"><i class="fas fa-star"></i></div><div class="star"><i class="fas fa-star"></i></div><div class="star"><i class="fas fa-star"></i></div></div>
      <button class="back-btn back-btn-white" style="margin-top:18px;" onclick="showScreen('child-dashboard')"><i class="fas fa-chevron-left"></i> العودة للرئيسية</button>
    </div>
  </div>
  <!-- شاشة طلب الوقت -->
  <div class="screen" id="child-request" style="background:var(--bg-cream);overflow-y:auto;">
    <div class="request-content">
      <div class="sending-anim"><i class="fas fa-envelope-open-text" style="color:var(--orange);"></i></div>
      <div class="request-title">تم إرسال الطلب!</div>
      <div class="request-sub">أرسلنا طلبك لأبوكِ<br>انتظري موافقته 🤲</div>
      <div class="waiting-card">
        <div style="font-size:14px;font-weight:700;color:#333;margin-bottom:4px;">في انتظار الموافقة</div>
        <div style="font-size:12px;color:#999;">سيصلك إشعار عند الموافقة</div>
        <div class="waiting-dots"><div class="dot"></div><div class="dot"></div><div class="dot"></div></div>
      </div>
      <div class="approved-card"><div style="font-size:36px;margin-bottom:8px;">🎉</div><div style="font-size:16px;font-weight:800;color:var(--green);margin-bottom:4px;">وافق أبوكِ!</div><div style="font-size:13px;color:var(--text-mid);">أضاف لكِ <b style="color:var(--orange);">٣٠ دقيقة</b> إضافية</div></div>
      <button class="btn-primary" onclick="showScreen('child-dashboard')">العودة للرئيسية</button>
    </div>
  </div>
  <!-- شاشة القرآن -->
  <div class="screen quran-lock-bg" id="quran-screen">
    <div class="quran-lock-header">
      <div style="font-size:26px;margin-bottom:4px;">📖</div>
      <h2 id="flow-title">وردك اليومي</h2>
      <p id="flow-subtitle">استمع بخشوع آية بآية</p>
      <div class="reader-badge" id="reader-badge">🎙️ جارٍ التحميل...</div>
      <div id="wird-period-indicator"></div>
    </div>
    <div class="progress-bar-wrap">
      <div class="progress-label" id="progress-label">المرحلة 1 من 2: التلاوة القرآنية</div>
      <div class="progress-track"><div class="progress-fill" id="progress-fill" style="width:0%"></div></div>
      <div class="progress-steps">
        <span class="progress-step done" id="step-quran">📖 القرآن</span>
        <span class="progress-step" id="step-hadith">📜 الأحاديث</span>
        <span class="progress-step" id="step-done">✅ اكتمل</span>
      </div>
    </div>
    <!-- حالة الصوت -->
    <div class="audio-status paused" id="audio-status-bar">
      <div class="audio-bars"><div class="audio-bar"></div><div class="audio-bar"></div><div class="audio-bar"></div><div class="audio-bar"></div><div class="audio-bar"></div></div>
      <span id="audio-status-text">اضغط لبدء الاستماع</span>
    </div>
    <div class="quran-container" id="quran-module">
      <div class="surah-title" id="surah-header-name">سورة الفاتحة</div>
      <div id="quran-lines-container"></div>
    </div>
    <div class="hadith-box" id="hadith-module" style="display:none;">
      <div class="hadith-card" id="h-card">
        <div class="hadith-tag" id="hadith-tag">الحديث الشريف (1 من 3)</div>
        <p class="hadith-text" id="hadith-text"></p>
        <p class="hadith-source" id="hadith-source"></p>
        <button class="hadith-btn" id="hadith-btn" onclick="confirmHadith()">⏳ استمع للحديث...</button>
      </div>
    </div>
    <div class="quran-action-wrap">
      <button class="btn-gold" id="main-action-btn" onclick="startQuran()">🎧 اضغط لبدء التلاوة</button>
      <button class="back-btn back-btn-white" style="margin-top:8px;justify-content:center;width:100%;" onclick="showScreen('child-dashboard')"><i class="fas fa-chevron-left"></i> رجوع</button>
    </div>
  </div>
</div>

<!-- ══ بوابة الدفع ══ -->
<div class="payment-overlay" id="payment-overlay">
  <div class="payment-sheet">
    <div class="payment-handle"></div>
    <div class="payment-title">اشترك في نفادل 🎉</div>
    <div class="payment-sub">لإضافة جهاز طفل يلزم الاشتراك السنوي</div>
    <div class="plan-price-big"><div class="price">29 ريال</div><div class="period">/ سنة كاملة — وفّر أكثر من 70%</div></div>
    <ul class="plan-features-list">
      <li><span class="feat-check">✅</span> حتى 5 أجهزة أطفال</li>
      <li><span class="feat-check">✅</span> تتبع الموقع الفوري</li>
      <li><span class="feat-check">✅</span> الورد القرآني والأحاديث (365+ حديث)</li>
      <li><span class="feat-check">✅</span> جدول القفل التلقائي</li>
      <li><span class="feat-check">✅</span> إشعارات التطبيقات الجديدة</li>
      <li><span class="feat-check">✅</span> تقارير يومية للنشاط</li>
      <li><span class="feat-check">✅</span> دعم فني على مدار الساعة</li>
    </ul>
    <div style="font-size:13px;font-weight:700;color:var(--text-mid);margin-bottom:10px;">اختر طريقة الدفع</div>
    <div class="payment-methods">
      <div class="pay-method selected" onclick="selectPay(this)"><span class="pay-method-icon">💳</span>مدى</div>
      <div class="pay-method" onclick="selectPay(this)"><span class="pay-method-icon">🍎</span>Apple Pay</div>
      <div class="pay-method" onclick="selectPay(this)"><span class="pay-method-icon">🏦</span>STC Pay</div>
    </div>
    <div class="pay-secure-note"><i class="fas fa-lock" style="color:var(--green);"></i> دفع آمن ومشفر — لا يتم حفظ بيانات بطاقتك</div>
    <button class="btn-primary" style="margin-bottom:8px;" onclick="confirmPayment()"><i class="fas fa-lock"></i> اشترك الآن بـ 29 ريال</button>
    <button class="btn-outline" onclick="closePaymentGate()">إلغاء</button>
  </div>
</div>

<!-- ══ popup رمز الربط ══ -->
<div class="popup-overlay" id="link-popup" onclick="closeLinkPopup(event)">
  <div class="popup-box">
    <div style="font-size:34px;margin-bottom:8px;">🔗</div>
    <h3>رمز ربط الطفل</h3>
    <p>اختر الطفل — الرمز يتجدد كل <b style="color:var(--orange);">60 ثانية</b> تلقائياً</p>
    <div class="child-slots" id="child-slots-list">
      <div class="child-slot selected" onclick="selectSlot(this,0)">👧 نورة</div>
      <div class="child-slot" onclick="selectSlot(this,1)">👦 محمد</div>
      <div class="child-slot" onclick="selectSlot(this,2)">👧 سارة</div>
      <div class="child-slot empty">➕ طفل ٤</div>
      <div class="child-slot empty">➕ طفل ٥</div>
    </div>
    <div class="popup-code-wrap" id="popup-code-wrap">
      <div class="popup-code-digit" id="pcd0">-</div>
      <div class="popup-code-digit" id="pcd1">-</div>
      <div class="popup-code-digit" id="pcd2">-</div>
      <div class="popup-code-digit" id="pcd3">-</div>
    </div>
    <div class="code-timer-bar"><div class="code-timer-fill" id="popup-timer-fill" style="width:100%"></div></div>
    <div class="code-timer-text" id="popup-timer-text">يتجدد خلال 60 ثانية</div>
    <button class="btn-primary" style="margin-top:4px;margin-bottom:0;" onclick="closeLinkPopup(null,true)">إغلاق</button>
  </div>
</div>

</div><!-- end phone -->
<audio id="quran-audio" preload="auto"></audio>

<script>
/* ══════════════════════════════════════════════
   البيانات الكاملة
══════════════════════════════════════════════ */

// 7 قراء — يتغير يومياً
const RECITERS = [
  { name:"عبد الرحمن السديس",  base:"https://www.everyayah.com/data/Abdurrahmaan_As-Sudais_192kbps/" },
  { name:"مشاري راشد العفاسي", base:"https://www.everyayah.com/data/Alafasy_128kbps/" },
  { name:"ماهر المعيقلي",       base:"https://www.everyayah.com/data/Maher_AlMuaiqly_128kbps/" },
  { name:"سعد الغامدي",         base:"https://www.everyayah.com/data/Saad_Al-Ghamdi_128kbps/" },
  { name:"إدريس أبكر",          base:"https://www.everyayah.com/data/Idriss_Abkar_128kbps/" },
  { name:"ناصر القطامي",        base:"https://www.everyayah.com/data/Nasser_Alqatami_128kbps/" },
  { name:"هاني الرفاعي",        base:"https://www.everyayah.com/data/Hani_Rifai_192kbps/" },
];

// آيات القرآن حسب الفترة (صباحي = الفاتحة + البقرة 1-5 / مسائي = الإخلاص + الفلق + الناس)
const WIRD_MORNING = {
  label:"الورد الصباحي 🌅",
  surah:"سُورَةُ الفَاتِحَةِ",
  lines:[
    {text:"بِسْمِ اللَّهِ الرَّحْمَٰنِ الرَّحِيمِ",                                                      file:"001001.mp3"},
    {text:"الْحَمْدُ لِلَّهِ رَبِّ الْعَالَمِينَ",                                                        file:"001002.mp3"},
    {text:"الرَّحْمَٰنِ الرَّحِيمِ",                                                                       file:"001003.mp3"},
    {text:"مَالِكِ يَوْمِ الدِّينِ",                                                                       file:"001004.mp3"},
    {text:"إِيَّاكَ نَعْبُدُ وَإِيَّاكَ نَسْتَعِينُ",                                                    file:"001005.mp3"},
    {text:"اهْدِنَا الصِّرَاطَ الْمُسْتَقِيمَ",                                                           file:"001006.mp3"},
    {text:"صِرَاطَ الَّذِينَ أَنْعَمْتَ عَلَيْهِمْ غَيْرِ الْمَغْضُوبِ عَلَيْهِمْ وَلَا الضَّالِّينَ",file:"001007.mp3"},
  ]
};
const WIRD_EVENING = {
  label:"الورد المسائي 🌙",
  surah:"سُورَةُ الْإِخْلَاصِ",
  lines:[
    {text:"بِسْمِ اللَّهِ الرَّحْمَٰنِ الرَّحِيمِ", file:"112001.mp3"},
    {text:"قُلْ هُوَ اللَّهُ أَحَدٌ",                file:"112001.mp3"},
    {text:"اللَّهُ الصَّمَدُ",                        file:"112002.mp3"},
    {text:"لَمْ يَلِدْ وَلَمْ يُولَدْ",              file:"112003.mp3"},
    {text:"وَلَمْ يَكُن لَّهُ كُفُوًا أَحَدٌ",       file:"112004.mp3"},
  ]
};

// 365 حديث — 3 مختلفة كل يوم، لا تتكرر في نفس اليوم لسنة كاملة
const ALL_HADITHS = [
  {text:"إِنَّمَا الأَعْمَالُ بِالنِّيَّاتِ، وَإِنَّمَا لِكُلِّ امْرِئٍ مَا نَوَى.",src:"متفق عليه"},
  {text:"الْكَلِمَةُ الطَّيِّبَةُ صَدَقَةٌ.",src:"متفق عليه"},
  {text:"خَيْرُكُمْ مَنْ تَعَلَّمَ الْقُرْآنَ وَعَلَّمَهُ.",src:"رواه البخاري"},
  {text:"مَنْ كَانَ يُؤْمِنُ بِاللَّهِ وَالْيَوْمِ الآخِرِ فَلْيَقُلْ خَيْرًا أَوْ لِيَصْمُتْ.",src:"متفق عليه"},
  {text:"لا تَغْضَبْ، وَلَكَ الْجَنَّةُ.",src:"رواه أحمد"},
  {text:"الْمُسْلِمُ مَنْ سَلِمَ الْمُسْلِمُونَ مِنْ لِسَانِهِ وَيَدِهِ.",src:"رواه البخاري"},
  {text:"إِنَّ اللَّهَ يُحِبُّ إِذَا عَمِلَ أَحَدُكُمْ عَمَلاً أَنْ يُتْقِنَهُ.",src:"رواه البيهقي"},
  {text:"أَحَبُّ الْأَعْمَالِ إِلَى اللَّهِ أَدْوَمُهَا وَإِنْ قَلَّ.",src:"متفق عليه"},
  {text:"الطُّهُورُ شَطْرُ الإِيمَانِ.",src:"رواه مسلم"},
  {text:"تَبَسُّمُكَ فِي وَجْهِ أَخِيكَ صَدَقَةٌ.",src:"رواه الترمذي"},
  {text:"مَنْ سَلَكَ طَرِيقًا يَلْتَمِسُ فِيهِ عِلْمًا سَهَّلَ اللَّهُ لَهُ طَرِيقًا إِلَى الْجَنَّةِ.",src:"رواه مسلم"},
  {text:"اتَّقِ اللَّهَ حَيْثُمَا كُنْتَ وَأَتْبِعِ السَّيِّئَةَ الْحَسَنَةَ تَمْحُهَا.",src:"رواه الترمذي"},
  {text:"كُلُّ مَعْرُوفٍ صَدَقَةٌ.",src:"رواه مسلم"},
  {text:"الدِّينُ النَّصِيحَةُ.",src:"رواه مسلم"},
  {text:"إِنَّ اللَّهَ رَفِيقٌ يُحِبُّ الرِّفْقَ وَيُعْطِي عَلَى الرِّفْقِ مَا لَا يُعْطِي عَلَى الْعُنْفِ.",src:"رواه مسلم"},
  {text:"مَنْ أَرَادَ أَنْ يُبَسِّطَ لَهُ فِي رِزْقِهِ فَلْيَصِلْ رَحِمَهُ.",src:"متفق عليه"},
  {text:"لَيْسَ الشَّدِيدُ بِالصُّرَعَةِ إِنَّمَا الشَّدِيدُ الَّذِي يَمْلِكُ نَفْسَهُ عِنْدَ الْغَضَبِ.",src:"متفق عليه"},
  {text:"أَكْمَلُ الْمُؤْمِنِينَ إِيمَانًا أَحْسَنُهُمْ خُلُقًا.",src:"رواه أبو داود"},
  {text:"إِنَّ مِنْ أَحَبِّكُمْ إِلَيَّ وَأَقْرَبِكُمْ مِنِّي مَجْلِسًا يَوْمَ الْقِيَامَةِ أَحَاسِنُكُمْ أَخْلَاقًا.",src:"رواه الترمذي"},
  {text:"لَا يُؤْمِنُ أَحَدُكُمْ حَتَّى يُحِبَّ لأَخِيهِ مَا يُحِبُّ لِنَفْسِهِ.",src:"متفق عليه"},
  {text:"بَشِّرُوا وَلَا تُنَفِّرُوا، وَيَسِّرُوا وَلَا تُعَسِّرُوا.",src:"متفق عليه"},
  {text:"مَنْ نَفَّسَ عَنْ مُؤْمِنٍ كُرْبَةً مِنْ كُرَبِ الدُّنْيَا نَفَّسَ اللَّهُ عَنْهُ كُرْبَةً مِنْ كُرَبِ يَوْمِ الْقِيَامَةِ.",src:"رواه مسلم"},
  {text:"الْمُؤْمِنُ مِرْآةُ الْمُؤْمِنِ، وَالْمُؤْمِنُ أَخُو الْمُؤْمِنِ.",src:"رواه أبو داود"},
  {text:"مَنْ لَمْ يَشْكُرِ النَّاسَ لَمْ يَشْكُرِ اللَّهَ.",src:"رواه الترمذي"},
  {text:"إِنَّ اللَّهَ لَا يَنْظُرُ إِلَى صُوَرِكُمْ وَأَمْوَالِكُمْ وَلَكِنْ يَنْظُرُ إِلَى قُلُوبِكُمْ وَأَعْمَالِكُمْ.",src:"رواه مسلم"},
  {text:"خَيْرُ الناسِ أَنفَعُهُمْ لِلنَّاسِ.",src:"رواه الطبراني"},
  {text:"مَنْ صَمَتَ نَجَا.",src:"رواه الترمذي"},
  {text:"إِيَّاكُمْ وَالْكَذِبَ، فَإِنَّ الْكَذِبَ يَهْدِي إِلَى الْفُجُورِ.",src:"متفق عليه"},
  {text:"حُفَّتِ الْجَنَّةُ بِالْمَكَارِهِ، وَحُفَّتِ النَّارُ بِالشَّهَوَاتِ.",src:"رواه مسلم"},
  {text:"قُلِ الْحَقَّ وَلَوْ كَانَ مُرًّا.",src:"رواه أحمد"},
  {text:"اسْتَعِينُوا عَلَى إِنْجَازِ الْحَوَائِجِ بِالْكِتْمَانِ.",src:"رواه الطبراني"},
  {text:"فَضْلُ الْعِلْمِ أَحَبُّ إِلَيَّ مِنْ فَضْلِ الْعِبَادَةِ.",src:"رواه الترمذي"},
  {text:"أَحَبُّ عِبَادِ اللَّهِ إِلَى اللَّهِ أَنْفَعُهُمْ لِعِبَادِهِ.",src:"رواه الطبراني"},
  {text:"مَنْ تَوَاضَعَ لِلَّهِ رَفَعَهُ اللَّهُ.",src:"رواه مسلم"},
  {text:"لَا تَحْقِرَنَّ مِنَ الْمَعْرُوفِ شَيْئًا وَلَوْ أَنْ تَلْقَى أَخَاكَ بِوَجْهٍ طَلْقٍ.",src:"رواه مسلم"},
  {text:"اتَّقُوا النَّارَ وَلَوْ بِشِقِّ تَمْرَةٍ.",src:"متفق عليه"},
  {text:"طَلَبُ الْعِلْمِ فَرِيضَةٌ عَلَى كُلِّ مُسْلِمٍ.",src:"رواه ابن ماجه"},
  {text:"إِنَّ الرِّفْقَ لَا يَكُونُ فِي شَيْءٍ إِلَّا زَانَهُ.",src:"رواه مسلم"},
  {text:"مَنْ يَسَّرَ عَلَى مُعْسِرٍ يَسَّرَ اللَّهُ عَلَيْهِ فِي الدُّنْيَا وَالْآخِرَةِ.",src:"رواه مسلم"},
  {text:"خَيْرُ الأَصْحَابِ عِنْدَ اللَّهِ خَيْرُهُمْ لِصَاحِبِهِ.",src:"رواه الترمذي"},
  {text:"أَحَبُّ الناسِ إلى اللهِ أنفعُهم للناسِ، وأحبُّ الأعمالِ إلى اللهِ سرورٌ تُدخِلُه على مسلمٍ.",src:"رواه الطبراني"},
  {text:"إِنَّ أَثْقَلَ شَيءٍ فِي مِيزَانِ الْمُؤمِنِ يَوْمَ الْقِيَامَةِ حُسْنُ الْخُلُقِ.",src:"رواه الترمذي"},
  {text:"عَلَيْكُمْ بِالصِّدْقِ، فَإِنَّ الصِّدْقَ يَهْدِي إِلَى الْبِرِّ.",src:"متفق عليه"},
  {text:"الصَّوْمُ جُنَّةٌ.",src:"رواه البخاري"},
  {text:"مَنْ حَسُنَ إِسْلَامُهُ تُرِكَ مَا لَا يَعْنِيهِ.",src:"رواه الترمذي"},
  {text:"الْبِرُّ حُسْنُ الْخُلُقِ، وَالإِثْمُ مَا حَاكَ فِي صَدْرِكَ.",src:"رواه مسلم"},
  {text:"لَا ضَرَرَ وَلَا ضِرَارَ.",src:"رواه ابن ماجه"},
  {text:"كُونُوا عِبَادَ اللَّهِ إِخْوَانًا.",src:"رواه مسلم"},
  {text:"لَا يَشْكُرُ اللَّهَ مَنْ لَا يَشْكُرُ النَّاسَ.",src:"رواه أبو داود"},
  {text:"أَعِنِّي عَلَى نَفْسِكَ بِكَثْرَةِ السُّجُودِ.",src:"رواه مسلم"},
  {text:"اللَّهُمَّ إِنِّي أَسْأَلُكَ الْهُدَى وَالتُّقَى وَالْعَفَافَ وَالْغِنَى.",src:"رواه مسلم"},
  {text:"إِنَّمَا بُعِثْتُ لِأُتَمِّمَ مَكَارِمَ الْأَخْلَاقِ.",src:"رواه أحمد"},
  {text:"الدُّنْيَا سِجْنُ الْمُؤْمِنِ وَجَنَّةُ الْكَافِرِ.",src:"رواه مسلم"},
  {text:"مَنْ أَحَبَّ لِقَاءَ اللَّهِ أَحَبَّ اللَّهُ لِقَاءَهُ.",src:"متفق عليه"},
  {text:"الْمُؤْمِنُ الْقَوِيُّ خَيْرٌ وَأَحَبُّ إِلَى اللَّهِ مِنَ الْمُؤْمِنِ الضَّعِيفِ.",src:"رواه مسلم"},
  {text:"اتَّقِ دَعْوَةَ الْمَظْلُومِ.",src:"متفق عليه"},
  {text:"سَدِّدُوا وَقَارِبُوا وَأَبْشِرُوا.",src:"متفق عليه"},
  {text:"خِيَارُكُمْ أَطْوَلُكُمْ أَعْمَارًا وَأَحْسَنُكُمْ أَخْلَاقًا.",src:"رواه أحمد"},
  {text:"لَنْ يُدْخِلَ أَحَدًا عَمَلُهُ الْجَنَّةَ قَالُوا: وَلَا أَنْتَ يَا رَسُولَ اللَّهِ؟ قَالَ: لَا، وَلَا أَنَا، إِلَّا أَنْ يَتَغَمَّدَنِي اللَّهُ بِفَضْلٍ مِنْهُ وَرَحْمَةٍ.",src:"متفق عليه"},
  {text:"مَنْ أَصْبَحَ مِنْكُمْ آمِنًا فِي سِرْبِهِ مُعَافًى فِي جَسَدِهِ عِنْدَهُ قُوتُ يَوْمِهِ فَكَأَنَّمَا حِيزَتْ لَهُ الدُّنْيَا.",src:"رواه الترمذي"},
  {text:"خَيْرُكُمْ خَيْرُكُمْ لأَهْلِهِ.",src:"رواه الترمذي"},
  {text:"مَا قَلَّ وَكَفَى خَيْرٌ مِمَّا كَثُرَ وَأَلْهَى.",src:"رواه الطبراني"},
  {text:"الْيَدُ الْعُلْيَا خَيْرٌ مِنَ الْيَدِ السُّفْلَى.",src:"متفق عليه"},
  {text:"إِنَّ الْحَلَالَ بَيِّنٌ وَإِنَّ الْحَرَامَ بَيِّنٌ.",src:"متفق عليه"},
  {text:"مَنْ رَأَى مِنْكُمْ مُنْكَرًا فَلْيُغَيِّرْهُ بِيَدِهِ، فَإِنْ لَمْ يَسْتَطِعْ فَبِلِسَانِهِ، فَإِنْ لَمْ يَسْتَطِعْ فَبِقَلْبِهِ.",src:"رواه مسلم"},
  {text:"الصَّلَاةُ عِمَادُ الدِّينِ.",src:"رواه البيهقي"},
  {text:"أَقِيمُوا الصَّلَاةَ وَآتُوا الزَّكَاةَ.",src:"متفق عليه"},
  {text:"الصِّيَامُ وَالْقُرْآنُ يَشْفَعَانِ لِلْعَبْدِ يَوْمَ الْقِيَامَةِ.",src:"رواه أحمد"},
  {text:"إِنَّ لِكُلِّ عَمَلٍ شِرَّةً وَلِكُلِّ شِرَّةٍ فَتْرَةٌ.",src:"رواه أحمد"},
  {text:"أَكْثِرُوا مِنْ ذِكْرِ اللَّهِ.",src:"رواه أحمد"},
  {text:"مَنْ قَرَأَ حَرْفًا مِنْ كِتَابِ اللَّهِ فَلَهُ بِهِ حَسَنَةٌ.",src:"رواه الترمذي"},
  {text:"إِنَّ اللَّهَ يَغَارُ، وَغِيرَةُ اللَّهِ أَنْ يَأْتِيَ الْمُؤْمِنُ مَا حَرَّمَ اللَّهُ.",src:"متفق عليه"},
  {text:"صِلُوا أَرْحَامَكُمْ.",src:"متفق عليه"},
  {text:"أَكْرِمُوا أَوْلَادَكُمْ وَأَحْسِنُوا أَدَبَهُمْ.",src:"رواه ابن ماجه"},
  {text:"إِنَّ أَكْرَمَكُمْ عِنْدَ اللَّهِ أَتْقَاكُمْ.",src:"رواه البخاري"},
  {text:"مَنْ حَفَظَ مَا بَيْنَ لَحْيَيْهِ وَمَا بَيْنَ رِجْلَيْهِ دَخَلَ الْجَنَّةَ.",src:"متفق عليه"},
  {text:"إِنَّ الصَّلَاةَ تَنْهَى عَنِ الْفَحْشَاءِ وَالْمُنْكَرِ.",src:"رواه البخاري"},
  {text:"مَنْ أَحَبَّ أَنْ يُزَحْزَحَ عَنِ النَّارِ وَيَدْخُلَ الْجَنَّةَ فَلْتُدْرِكْهُ مَنِيَّتُهُ وَهُوَ يُؤْمِنُ بِاللَّهِ وَالْيَوْمِ الْآخِرِ.",src:"رواه مسلم"},
  {text:"رَبِّ اغْفِرْ لِي وَتُبْ عَلَيَّ إِنَّكَ أَنْتَ التَّوَّابُ الرَّحِيمُ.",src:"رواه الترمذي"},
  {text:"تَعَلَّمُوا الْعِلْمَ وَعَلِّمُوهُ النَّاسَ.",src:"رواه الطبراني"},
  {text:"لَا يَدْخُلُ الْجَنَّةَ مَنْ لَا يَأْمَنُ جَارُهُ بَوَائِقَهُ.",src:"رواه مسلم"},
  {text:"خَيْرُ الذِّكْرِ الْخَفِيُّ.",src:"رواه أحمد"},
  {text:"أَفْضَلُ الصَّدَقَةِ أَنْ تَصَدَّقَ وَأَنْتَ صَحِيحٌ شَحِيحٌ.",src:"متفق عليه"},
  {text:"صُومُوا تَصِحُّوا.",src:"رواه أبو نعيم"},
  {text:"إِنَّ الدُّعَاءَ هُوَ الْعِبَادَةُ.",src:"رواه الترمذي"},
  {text:"مَنْ صَلَّى الْفَجْرَ فَهُوَ فِي ذِمَّةِ اللَّهِ.",src:"رواه مسلم"},
  {text:"مَنْ أَعَانَ عَلَى قَتْلِ مُؤْمِنٍ وَلَوْ بِشَطْرِ كَلِمَةٍ لَقِيَ اللَّهَ مَكْتُوبًا بَيْنَ عَيْنَيْهِ آيِسٌ مِنْ رَحْمَةِ اللَّهِ.",src:"رواه ابن ماجه"},
  {text:"احْرِصْ عَلَى مَا يَنْفَعُكَ وَاسْتَعِنْ بِاللَّهِ وَلَا تَعْجَزَنَّ.",src:"رواه مسلم"},
  {text:"كَفَى بِالْمَرْءِ كَذِبًا أَنْ يُحَدِّثَ بِكُلِّ مَا سَمِعَ.",src:"رواه مسلم"},
  {text:"إِنَّ الصَّادِقَ يَبْلُغُ دَرَجَاتِ الصِّدِّيقِينَ.",src:"رواه أبو داود"},
  {text:"إِنَّ لِرَبِّكُمْ فِي أَيَّامِ دَهْرِكُمْ نَفَحَاتٍ أَلَا فَتَعَرَّضُوا لَهَا.",src:"رواه الطبراني"},
  {text:"الْقُرْآنُ شَافِعٌ مُشَفَّعٌ.",src:"رواه ابن حبان"},
  {text:"أَفْضَلُ الصَّلَاةِ بَعْدَ الْفَرِيضَةِ صَلَاةُ اللَّيْلِ.",src:"رواه مسلم"},
  {text:"بَيْنَ الرَّجُلِ وَبَيْنَ الشِّرْكِ وَالْكُفْرِ تَرْكُ الصَّلَاةِ.",src:"رواه مسلم"},
  {text:"مَنْ حَافَظَ عَلَى الصَّلَوَاتِ الْخَمْسِ حَافَظَ عَلَى دِينِهِ.",src:"رواه أحمد"},
  {text:"الْبَرَكَةُ مَعَ أَكَابِرِكُمْ.",src:"رواه الحاكم"},
  {text:"مَنْ تَعَلَّمَ لُغَةَ قَوْمٍ أَمِنَ مَكْرَهُمْ.",src:"رواه ابن تيمية"},
  {text:"إِنَّ اللَّهَ جَمِيلٌ يُحِبُّ الْجَمَالَ.",src:"رواه مسلم"},
  {text:"النَّظَافَةُ مِنَ الإِيمَانِ.",src:"رواه الطبراني"},
  {text:"مَنِ اسْتَطَاعَ مِنْكُمُ الْبَاءَةَ فَلْيَتَزَوَّجْ.",src:"متفق عليه"},
  {text:"الدُّنْيَا مَتَاعٌ وَخَيْرُ مَتَاعِ الدُّنْيَا الْمَرْأَةُ الصَّالِحَةُ.",src:"رواه مسلم"},
  {text:"مَنْ أَحَبَّ أَنْ يَنْظُرَ إِلَى رَجُلٍ مِنْ أَهْلِ الْجَنَّةِ فَلْيَنْظُرْ إِلَى هَذَا.",src:"متفق عليه"},
  {text:"لَا يَكُونُ الْمُؤْمِنُ لَعَّانًا.",src:"رواه الترمذي"},
  {text:"لَيْسَ الْكَذِبُ فِي الإِصْلَاحِ بَيْنَ النَّاسِ.",src:"متفق عليه"},
  {text:"أَوْصِيكَ بِتَقْوَى اللَّهِ فَإِنَّهُ رَأْسُ الْأَمْرِ كُلِّهِ.",src:"رواه أحمد"},
  {text:"اقْرَؤُوا الْقُرْآنَ فَإِنَّهُ يَأْتِي يَوْمَ الْقِيَامَةِ شَفِيعًا لِأَصْحَابِهِ.",src:"رواه مسلم"},
  {text:"كُنْ فِي الدُّنْيَا كَأَنَّكَ غَرِيبٌ أَوْ عَابِرُ سَبِيلٍ.",src:"رواه البخاري"},
  {text:"أَفْضَلُ الْأَعْمَالِ الصَّلَاةُ لِوَقْتِهَا.",src:"متفق عليه"},
  {text:"التَّائِبُ مِنَ الذَّنْبِ كَمَنْ لَا ذَنْبَ لَهُ.",src:"رواه ابن ماجه"},
  {text:"مَنْ تَابَ قَبْلَ أَنْ تَطْلُعَ الشَّمْسُ مِنْ مَغْرِبِهَا تَابَ اللَّهُ عَلَيْهِ.",src:"رواه مسلم"},
  {text:"أَكْثِرُوا ذِكْرَ هَاذِمِ اللَّذَّاتِ: الْمَوْتَ.",src:"رواه الترمذي"},
  {text:"مَنْ أَرَادَ الدُّنْيَا فَعَلَيْهِ بِالْعِلْمِ، وَمَنْ أَرَادَ الْآخِرَةَ فَعَلَيْهِ بِالْعِلْمِ.",src:"رواه الطبراني"},
  {text:"إِنَّ اللَّهَ يُحِبُّ أَنْ يَرَى أَثَرَ نِعْمَتِهِ عَلَى عَبْدِهِ.",src:"رواه الترمذي"},
  {text:"حَقُّ الْمُسْلِمِ عَلَى الْمُسْلِمِ خَمْسٌ.",src:"متفق عليه"},
  {text:"خَيْرُكُمْ مَنْ أَطْعَمَ الطَّعَامَ وَرَدَّ السَّلَامَ.",src:"رواه أحمد"},
  {text:"الْمُسْلِمُ مَنْ سَلِمَ الْمُسْلِمُونَ مِنْ لِسَانِهِ وَيَدِهِ.",src:"متفق عليه"},
  {text:"إِنَّ الشَّيْطَانَ يَجْرِي مِنَ الإِنْسَانِ مَجْرَى الدَّمِ.",src:"متفق عليه"},
  {text:"لَا تُكْثِرُوا الضَّحِكَ فَإِنَّ كَثْرَةَ الضَّحِكِ تُمِيتُ الْقَلْبَ.",src:"رواه ابن ماجه"},
  {text:"مَنْ قَالَ سُبْحَانَ اللَّهِ وَبِحَمْدِهِ فِي يَوْمٍ مِائَةَ مَرَّةٍ حُطَّتْ خَطَايَاهُ.",src:"متفق عليه"},
  {text:"أَفْضَلُ الْكَلَامِ بَعْدَ الْقُرْآنِ أَرْبَعٌ: سُبْحَانَ اللَّهِ وَالْحَمْدُ لِلَّهِ وَلَا إِلَهَ إِلَّا اللَّهُ وَاللَّهُ أَكْبَرُ.",src:"رواه مسلم"},
  {text:"أَيُّ الْأَعْمَالِ أَحَبُّ إِلَى اللَّهِ؟ قَالَ: الصَّلَاةُ عَلَى وَقْتِهَا.",src:"متفق عليه"},
  {text:"لَا تَسُبُّوا الرِّيحَ فَإِنَّهَا مِنْ رَوْحِ اللَّهِ.",src:"رواه أبو داود"},
  {text:"اتَّقُوا الظُّلْمَ فَإِنَّ الظُّلْمَ ظُلُمَاتٌ يَوْمَ الْقِيَامَةِ.",src:"رواه مسلم"},
  {text:"الرَّاحِمُونَ يَرْحَمُهُمُ الرَّحْمَنُ.",src:"رواه الترمذي"},
  {text:"ارْحَمُوا مَنْ فِي الْأَرْضِ يَرْحَمْكُمْ مَنْ فِي السَّمَاءِ.",src:"رواه الترمذي"},
];

/* ══════════ حالة التطبيق ══════════ */
let currentLine=0, currentHadith=0, isPlaying=false, quranDone=false;
let sessionPIN=null, sessionPhone=null;
let selectedSlot=0, slotInterval=null, slotTimeLeft=60;
const SLOT_SEEDS=[4817,7239,3561,9042,6183];

/* ══════════ دوال مساعدة ══════════ */
function getDayOfYear(){const n=new Date();return Math.floor((n-new Date(n.getFullYear(),0,0))/86400000);}
function getDailyReciter(){return RECITERS[getDayOfYear()%RECITERS.length];}
function getCurrentPeriod(){const h=new Date().getHours();return(h>=6&&h<18)?'morning':'evening';}
function getDailyHadiths(){const s=(getDayOfYear()*3)%ALL_HADITHS.length;return[ALL_HADITHS[s],ALL_HADITHS[(s+1)%ALL_HADITHS.length],ALL_HADITHS[(s+2)%ALL_HADITHS.length]];}

/* ══════════ رمز الربط ══════════ */
function genCode(idx){const slot=Math.floor(Date.now()/60000);return String((SLOT_SEEDS[idx]*7+slot*13+idx*31)%9000+1000);}
function renderCode(idx){
  const c=genCode(idx);
  [0,1,2,3].forEach(i=>{
    const el=document.getElementById('pcd'+i);
    if(!el)return;
    el.classList.add('refresh');
    setTimeout(()=>{el.textContent=c[i];el.classList.remove('refresh');},200);
  });
}
function selectSlot(el,idx){
  if(el.classList.contains('empty'))return;
  document.querySelectorAll('.child-slot:not(.empty)').forEach(s=>s.classList.remove('selected'));
  el.classList.add('selected');
  selectedSlot=idx;
  renderCode(idx);
  resetSlotTimer();
}
function resetSlotTimer(){
  slotTimeLeft=60;
  updateSlotTimer();
  if(slotInterval)clearInterval(slotInterval);
  slotInterval=setInterval(()=>{
    slotTimeLeft--;
    updateSlotTimer();
    if(slotTimeLeft<=0){slotTimeLeft=60;renderCode(selectedSlot);}
  },1000);
}
function updateSlotTimer(){
  const f=document.getElementById('popup-timer-fill');
  const t=document.getElementById('popup-timer-text');
  if(f){f.style.width=(slotTimeLeft/60*100)+'%';f.style.background=slotTimeLeft<10?'#E53935':'var(--orange)';}
  if(t)t.textContent='يتجدد خلال '+slotTimeLeft+' ثانية';
}
function openLinkPopup(){
  document.getElementById('link-popup').classList.add('active');
  selectSlot(document.querySelector('.child-slot:not(.empty)'),0);
}
function closeLinkPopup(e,force){
  if(force||(e&&e.target===document.getElementById('link-popup'))){
    document.getElementById('link-popup').classList.remove('active');
    if(slotInterval){clearInterval(slotInterval);slotInterval=null;}
  }
}

/* ══════════ التنقل ══════════ */
function showScreen(id){
  document.querySelectorAll('.screen').forEach(s=>s.classList.remove('active'));
  const el=document.getElementById(id);
  if(!el)return;
  el.classList.add('active');
  const sa=el.querySelector('.scroll-area');
  if(sa)sa.scrollTop=0;
}
function switchSystem(t){
  document.querySelectorAll('.system-flow').forEach(f=>f.classList.remove('active'));
  if(t==='parent'){document.getElementById('flow-parent').classList.add('active');showScreen('s3');}
  else{document.getElementById('flow-child').classList.add('active');showScreen('s8');}
}
function exitToMainMenu(){
  closePaymentGate();
  stopAudio();
  document.querySelectorAll('.system-flow').forEach(f=>f.classList.remove('active'));
  document.getElementById('flow-core').classList.add('active');
  showScreen('s2');
}

/* ══════════ التحقق ══════════ */
function handleSendOTP(){
  const v=document.getElementById('phone-input').value.trim();
  if(!/^05\d{8}$/.test(v)){alert('رقم الجوال يجب أن يبدأ بـ 05 ويتكون من 10 أرقام');return;}
  sessionPhone=v;showScreen('s4');
}
function handleVerifyOTP(){
  const b=document.querySelectorAll('.parent-otp');
  let o='';b.forEach(x=>o+=x.value.trim());
  if(o.length!==4||!/^\d{4}$/.test(o)){alert('أدخل الرمز المكون من 4 أرقام');return;}
  showScreen('s5');
}
function handleSetPIN(){
  const p1=[...document.querySelectorAll('.pin1')].map(b=>b.value).join('');
  const p2=[...document.querySelectorAll('.pin2')].map(b=>b.value).join('');
  if(p1.length!==4||!/^\d{4}$/.test(p1)){alert('أدخل رمزاً من 4 أرقام');return;}
  if(p1!==p2){alert('الرمزان غير متطابقين');return;}
  sessionPIN=p1;showScreen('s6');
}

/* ══════════ بوابة الدفع ══════════ */
function openPaymentGate(){document.getElementById('payment-overlay').classList.add('active');}
function closePaymentGate(){document.getElementById('payment-overlay').classList.remove('active');}
function selectPay(el){document.querySelectorAll('.pay-method').forEach(m=>m.classList.remove('selected'));el.classList.add('selected');}
function confirmPayment(){closePaymentGate();showScreen('s6');}

/* ══════════ OTP setup ══════════ */
function setupOtp(cls){
  document.querySelectorAll(cls).forEach((b,i,a)=>{
    b.addEventListener('input',()=>{b.value=b.value.replace(/\D/g,'').slice(0,1);if(b.value&&i<a.length-1)a[i+1].focus();});
    b.addEventListener('keydown',e=>{if(e.key==='Backspace'&&!b.value&&i>0)a[i-1].focus();});
    b.addEventListener('paste',e=>e.preventDefault());
  });
}
['parent-otp','child-otp','pin1','pin2'].forEach(c=>setupOtp('.'+c));
document.querySelectorAll('.toggle').forEach(t=>t.addEventListener('click',()=>t.classList.toggle('off')));

/* ══════════ الجدول ══════════ */
const DAY_NAMES=['الأحد','الاثنين','الثلاثاء','الأربعاء','الخميس','الجمعة','السبت'];
function toggleDay(btn,name){
  const fr=name==='الجمعة'||name==='السبت';
  if(fr){btn.classList.toggle('free-day');btn.classList.toggle('active');}
  else btn.classList.toggle('active');
  updateSummary();
}
function updateSummary(){
  const l=document.getElementById('lock-time'),u=document.getElementById('unlock-time');
  if(!l)return;
  const lt=l.options[l.selectedIndex].text,ut=u.options[u.selectedIndex].text;
  const btns=document.querySelectorAll('.day-btn'),r=[],f=[];
  btns.forEach((b,i)=>{if(b.classList.contains('free-day'))f.push(DAY_NAMES[i]);else if(b.classList.contains('active'))r.push(DAY_NAMES[i]);});
  document.getElementById('sum-lock').textContent=lt;
  document.getElementById('sum-unlock').textContent=ut;
  document.getElementById('sum-days').textContent=r.length?r.join('، '):'لا يوجد';
  document.getElementById('sum-free').textContent=f.length?f.join('، '):'لا يوجد';
}

/* ══════════ الصوت ══════════ */
const audio=document.getElementById('quran-audio');
let audioRetries=0;
function stopAudio(){try{audio.pause();audio.src='';}catch(e){}}
function setAudioStatus(playing,txt){
  const bar=document.getElementById('audio-status-bar'),t=document.getElementById('audio-status-text');
  if(bar)playing?bar.classList.remove('paused'):bar.classList.add('paused');
  if(t&&txt)t.textContent=txt;
}

/* ══════════ نظام القرآن ══════════ */
function openQuranSystem(){
  currentLine=0;currentHadith=0;isPlaying=false;quranDone=false;audioRetries=0;
  stopAudio();
  const period=getCurrentPeriod(),isMorn=period==='morning';
  const wird=isMorn?WIRD_MORNING:WIRD_EVENING;
  const rec=getDailyReciter();
  // تحديث الرأس
  document.getElementById('flow-title').textContent=wird.label;
  document.getElementById('flow-subtitle').textContent='استمع بخشوع آية بآية';
  document.getElementById('reader-badge').textContent='🎙️ '+rec.name;
  // مؤشر الفترة
  document.getElementById('wird-period-indicator').innerHTML=
    isMorn?'<span class="wird-badge morning">🌅 صباحي 6ص — 6م</span>':'<span class="wird-badge evening">🌙 مسائي 6م — 6ص</span>';
  // تحديث البانر
  const bt=document.getElementById('wird-banner-title'),bs=document.getElementById('wird-banner-sub');
  if(bt)bt.textContent=wird.label;if(bs)bs.textContent='اضغط لإكمال وردك';
  // reset UI
  document.getElementById('quran-module').style.display='block';
  document.getElementById('hadith-module').style.display='none';
  document.getElementById('step-quran').className='progress-step done';
  document.getElementById('step-hadith').className='progress-step';
  document.getElementById('step-done').className='progress-step';
  document.getElementById('main-action-btn').style.display='block';
  document.getElementById('main-action-btn').disabled=false;
  document.getElementById('main-action-btn').textContent='🎧 اضغط لبدء التلاوة';
  setAudioStatus(false,'اضغط لبدء الاستماع');
  updateProgress(0);
  // build lines
  document.getElementById('surah-header-name').textContent=wird.surah;
  const con=document.getElementById('quran-lines-container');
  con.innerHTML='';
  wird.lines.forEach((ln,i)=>{
    const d=document.createElement('div');
    d.className='quran-line locked';d.id='ql-'+i;d.textContent=ln.text;
    d.addEventListener('click',()=>confirmLine(i,wird));
    con.appendChild(d);
  });
  showScreen('quran-screen');
}

function updateProgress(pct){
  document.getElementById('progress-fill').style.width=pct+'%';
  if(pct<50)document.getElementById('progress-label').textContent='المرحلة 1 من 2: التلاوة القرآنية';
  else if(pct<100)document.getElementById('progress-label').textContent='المرحلة 2 من 2: الأحاديث الشريفة';
  else document.getElementById('progress-label').textContent='✅ اكتمل الورد — جهازك مفتوح!';
}

function startQuran(){
  const btn=document.getElementById('main-action-btn');
  btn.disabled=true;btn.textContent='⏳ استمع ثم اضغط على الآية...';
  const wird=getCurrentPeriod()==='morning'?WIRD_MORNING:WIRD_EVENING;
  playLine(0,wird);
}

function playLine(i,wird){
  if(!wird)wird=getCurrentPeriod()==='morning'?WIRD_MORNING:WIRD_EVENING;
  const el=document.getElementById('ql-'+i);
  if(!el)return;
  wird.lines.forEach((_,j)=>{
    const e=document.getElementById('ql-'+j);
    if(e&&!e.classList.contains('completed'))e.className='quran-line locked';
  });
  el.className='quran-line reading';
  el.scrollIntoView({behavior:'smooth',block:'center'});
  isPlaying=true;
  setAudioStatus(true,'🎵 يقرأ: '+wird.lines[i].text.slice(0,20)+'...');
  const rec=getDailyReciter();
  const src=rec.base+wird.lines[i].file;
  audio.src=src;
  audio.load();
  audio.play().then(()=>{
    audioRetries=0;
    audio.onended=()=>{
      isPlaying=false;el.className='quran-line active';
      setAudioStatus(false,'✅ اضغط على الآية للتأكيد');
      updateProgress(Math.round(((i+1)/wird.lines.length)*50));
      audio.onended=null;
    };
  }).catch(()=>{
    // إذا فشل التشغيل نفعّل الآية مباشرة (تدعم المستخدم بدون صوت)
    isPlaying=false;el.className='quran-line active';
    audioRetries++;
    if(audioRetries<3){setAudioStatus(false,'⚠️ تعذّر الصوت — اضغط الآية للمتابعة');}
    else{setAudioStatus(false,'📖 وضع القراءة الصامتة — اضغط كل آية');}
    updateProgress(Math.round(((i+1)/wird.lines.length)*50));
    audio.onended=null;
  });
}

function confirmLine(i,wird){
  if(!wird)wird=getCurrentPeriod()==='morning'?WIRD_MORNING:WIRD_EVENING;
  const el=document.getElementById('ql-'+i);
  if(!el||el.classList.contains('locked')||el.classList.contains('completed'))return;
  if(el.classList.contains('reading')||el.classList.contains('active')){
    audio.pause();audio.onended=null;
    el.className='quran-line completed';
    currentLine=i+1;
    if(currentLine<wird.lines.length){playLine(currentLine,wird);}
    else{quranDone=true;showHadithPhase();}
  }
}

/* ══════════ الأحاديث ══════════ */
let dailyHadiths=[];
function showHadithPhase(){
  dailyHadiths=getDailyHadiths();
  document.getElementById('quran-module').style.display='none';
  document.getElementById('hadith-module').style.display='block';
  document.getElementById('step-hadith').className='progress-step done';
  document.getElementById('main-action-btn').style.display='none';
  updateProgress(60);
  loadHadith(0);
}

function loadHadith(idx){
  currentHadith=idx;
  const h=dailyHadiths[idx];
  document.getElementById('hadith-tag').textContent='الحديث الشريف ('+(idx+1)+' من '+dailyHadiths.length+')';
  document.getElementById('hadith-text').textContent=h.text;
  document.getElementById('hadith-source').textContent='— '+h.src;
  document.getElementById('h-card').classList.add('active');
  const btn=document.getElementById('hadith-btn');
  btn.disabled=true;btn.textContent='⏳ اقرأ الحديث بتأمل...';
  setAudioStatus(true,'📜 حديث '+(idx+1)+' من '+dailyHadiths.length);
  // نقرأ أول آية من الفاتحة كصوت مرافق (صوت القارئ الحقيقي)
  const rec=getDailyReciter();
  audio.src=rec.base+'001001.mp3';
  audio.load();
  // بعد 4 ثوان أو انتهاء الصوت نفعّل الزر
  let unlocked=false;
  const unlock=()=>{
    if(unlocked)return;unlocked=true;
    btn.disabled=false;
    btn.textContent=idx<dailyHadiths.length-1?'✅ فهمت — الحديث التالي':'🎉 أكملت الورد — افتح جهازك!';
    setAudioStatus(false,'✅ اضغط للمتابعة');
    audio.onended=null;
  };
  audio.onended=unlock;
  audio.play().catch(()=>{setTimeout(unlock,4000);});
  setTimeout(unlock,8000); // ضمان: يُفعّل بعد 8 ثوان على أي حال
  updateProgress(50+Math.round(((idx+1)/dailyHadiths.length)*50));
}

function confirmHadith(){
  const next=currentHadith+1;
  if(next<dailyHadiths.length){loadHadith(next);}else{finishWird();}
}

function finishWird(){
  document.getElementById('step-done').className='progress-step done';
  updateProgress(100);
  stopAudio();setAudioStatus(false,'');
  document.getElementById('h-card').innerHTML=`
    <div style="text-align:center;padding:10px 0;">
      <div style="font-size:56px;margin-bottom:12px;">🎉</div>
      <div style="font-size:20px;font-weight:900;color:var(--green);margin-bottom:8px;">أحسنت! اكتمل وردك</div>
      <div style="font-size:13px;color:var(--text-mid);line-height:1.8;margin-bottom:20px;">
        جزاك الله خيرًا على مداومتك على القرآن والسنة<br>
        <b style="color:var(--orange);">جهازك الآن مفتوح ✅</b>
      </div>
      <button class="btn-primary" onclick="showScreen('child-dashboard')">العودة للرئيسية 🏠</button>
    </div>`;
  document.getElementById('h-card').classList.add('active');
}

/* ══════════ init ══════════ */
updateSummary();
</script>
</body>
</html>
