<!doctype html>
<html lang="ar">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>عرض توضيحي - تطبيق PUBG (Firebase)</title>
  <style>
    /* (نفس ستايل العرض الكبير الملائم لويندوز) */
    *{box-sizing:border-box;margin:0;padding:0;font-family:"Segoe UI", Tahoma, Arial, "Noto Naskh Arabic", sans-serif}
    html,body{height:100%}
    body{
      background: linear-gradient(135deg,#071226 0%, #081426 60%, #021024 100%);
      color:#e6eef8;
      display:flex;
      align-items:center;
      justify-content:center;
      padding:30px;
    }
    .ciner{
      width:150%;
      max-width:1400px;
      min-height:640px;
      background: linear-gradient(180deg, rgba(255,255,255,0.02), rgba(255,255,255,0.01));
      border-radius:18px;
      box-shadow: 0 18px 50px rgba(2,6,23,0.75);
      overflow:hidden;
      display:flex;
      gap:0;
    }
    .left{
      flex:1.6;
      padding:48px;
      background:
        radial-gradient(900px 450px at 10% 10%, rgba(255,255,255,0.02), transparent 12%),
        linear-gradient(90deg, rgba(255,0,110,0.04), rgba(0,140,255,0.03));
      display:flex;
      flex-direction:column;
      justify-content:center;
      gap:18px;
    }
    .brand{display:flex;gap:14px;align-items:center}
    .logo{width:86px;height:86px;border-radius:14px;
      background: linear-gradient(135deg,#ff2d95,#3aa0ff);
      display:flex;align-items:center;justify-content:center;
      font-weight:900;color:#041428;font-size:28px;
      box-shadow: 0 10px 34px rgba(58,160,255,0.12);
    }
    h1{font-size:34px;line-height:1.02}
    p.lead{color:rgba(230,238,248,0.92);font-size:16px;max-width:900px}
    .badges{display:flex;gap:10px;flex-wrap:wrap;margin-top:8px}
    .badge{
      background:rgba(255,255,255,0.03);
      padding:10px 14px;border-radius:999px;font-size:14px;border:1px solid rgba(255,255,255,0.03)
    }
    .cta{margin-top:22px;display:flex;gap:14px;align-items:center }
    .btn{
      padding:14px 20px;border-radius:12px;border:0;cursor:pointer;
      font-weight:800;background:linear-gradient(90deg,#ff2d95,#3aa0ff);
      color:#041428;box-shadow:0 10px 34px rgba(58,160,255,0.12);
      transition:transform .16s ease;
      font-size:15px;
    }
    .btn:active{transform:translateY(2px)}
    .muted{
      background:transparent;border:1px solid rgba(255,255,255,0.06);
      color:rgba(230,238,248,0.9);padding:12px 14px;border-radius:12px;font-weight:700;
    }
    .right{
      width:520px;
      background:linear-gradient(180deg, rgba(255,255,255,0.01), rgba(255,255,255,0.006));
      padding:28px;border-left:1px solid rgba(255,255,255,0.02);
      display:flex;flex-direction:column;gap:12px;
    }
    .panel{
      background:linear-gradient(180deg, rgba(255,255,255,0.008), rgba(255,255,255,0.004));
      border-radius:12px;padding:18px;border:1px solid rgba(255,255,255,0.02);
      box-shadow: inset 0 1px 0 rgba(255,255,255,0.008);
    }
    .tt{font-weight:900;font-size:20px}
    .small{font-size:13px;color:rgba(230,238,248,0.8)}
    form{display:flex;flex-direction:column;gap:10px;margin-top:10px}
    label{font-size:13px;color:rgba(230,238,248,0.85)}
    input[type="text"],input[type="number"]{
      padding:12px 14px;border-radius:10px;border:1px solid rgba(255,255,255,0.06);
      background:rgba(2,6,23,0.6);color:#e9f2ff;font-size:15px;
    }
    .note{font-size:12px;color:rgba(230,238,248,0.6);margin-top:-6px}
    .error{color:#ffb3b3;font-weight:700;font-size:13px}
    .success{color:#c8ffd1;font-weight:700;font-size:13px}
    .admin-list{margin-top:12px;display:flex;flex-direction:column;gap:8px;max-height:360px;overflow:auto;padding-right:6px}
    .account{
      background:linear-gradient(90deg, rgba(255,255,255,0.01), rgba(255,255,255,0.005));
      padding:12px;border-radius:10px;border:1px solid rgba(255,255,255,0.02);
      display:flex;justify-content:space-between;align-items:center;
    }
    .kbd{font-family:monospace;background:rgba(0,0,0,0.12);padding:6px 8px;border-radius:6px;font-size:13px}
    .disclaimer{
      min-width: 1200px;
      margin-top:12px;padding:12px;border-radius:10px;background:rgba(255,255,255,0.02);
      border:1px solid rgba(255,255,255,0.02);font-size:13px;color:#ffd9b3
