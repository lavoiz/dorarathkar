!DOCTYPE html
html lang=ar dir=rtl
head
meta charset=UTF-8
meta name=viewport content=width=device-width, initial-scale=1.0
titleوردي اليوميtitle
link href=httpsfonts.googleapis.comcss2family=Amiriital,wght@0,400;0,700;1,400&family=Tajawalwght@300;400;700&display=swap rel=stylesheet
style
  root {
    --gold #c9a84c;
    --gold-light #e8d5a0;
    --gold-dark #8a6d20;
    --bg #0d1117;
    --bg2 #141b24;
    --bg3 #1a2332;
    --text #f0e8d5;
    --text-muted #8a7d6a;
    --green #2d6a4f;
    --green-light #52b788;
    --red #7b2d2d;
    --shadow 0 8px 32px rgba(0,0,0,0.5);
  }

   { box-sizing border-box; margin 0; padding 0; }

  body {
    background var(--bg);
    color var(--text);
    font-family 'Tajawal', sans-serif;
    min-height 100vh;
    overflow-x hidden;
  }

   Background pattern 
  bodybefore {
    content '';
    position fixed;
    inset 0;
    background-image
      radial-gradient(ellipse at 20% 20%, rgba(201,168,76,0.06) 0%, transparent 50%),
      radial-gradient(ellipse at 80% 80%, rgba(201,168,76,0.04) 0%, transparent 50%);
    pointer-events none;
    z-index 0;
  }

  .container {
    max-width 800px;
    margin 0 auto;
    padding 20px;
    position relative;
    z-index 1;
  }

   Header 
  header {
    text-align center;
    padding 40px 20px 30px;
    position relative;
  }

  .header-ornament {
    font-family 'Amiri', serif;
    color var(--gold);
    font-size 1.4rem;
    opacity 0.6;
    letter-spacing 8px;
    margin-bottom 8px;
  }

  h1 {
    font-family 'Amiri', serif;
    font-size 3rem;
    color var(--gold);
    text-shadow 0 0 40px rgba(201,168,76,0.3);
    font-weight 700;
    line-height 1.2;
  }

  .header-subtitle {
    color var(--text-muted);
    font-size 0.9rem;
    margin-top 8px;
    font-weight 300;
  }

  .divider {
    display flex;
    align-items center;
    gap 12px;
    margin 20px 0;
    color var(--gold);
    opacity 0.4;
  }
  .dividerbefore, .dividerafter {
    content '';
    flex 1;
    height 1px;
    background linear-gradient(to left, transparent, var(--gold), transparent);
  }

   Clock 
  .clock-widget {
    background var(--bg2);
    border 1px solid rgba(201,168,76,0.2);
    border-radius 16px;
    padding 20px;
    text-align center;
    margin-bottom 24px;
    position relative;
    overflow hidden;
  }
  .clock-widgetbefore {
    content '';
    position absolute;
    top 0; left 0; right 0;
    height 2px;
    background linear-gradient(90deg, transparent, var(--gold), transparent);
  }

  #clock-time {
    font-family 'Amiri', serif;
    font-size 3.5rem;
    color var(--gold);
    text-shadow 0 0 20px rgba(201,168,76,0.4);
    font-variant-numeric tabular-nums;
    letter-spacing 4px;
  }
  #clock-date {
    color var(--text-muted);
    font-size 0.95rem;
    margin-top 4px;
  }
  #prayer-status {
    margin-top 12px;
    padding 8px 16px;
    background rgba(201,168,76,0.1);
    border-radius 20px;
    display inline-block;
    font-size 0.9rem;
    color var(--gold-light);
  }

   Tabs 
  .tabs {
    display flex;
    gap 8px;
    margin-bottom 20px;
    background var(--bg2);
    padding 6px;
    border-radius 12px;
    border 1px solid rgba(201,168,76,0.15);
  }
  .tab-btn {
    flex 1;
    padding 10px;
    border none;
    background transparent;
    color var(--text-muted);
    font-family 'Tajawal', sans-serif;
    font-size 0.95rem;
    cursor pointer;
    border-radius 8px;
    transition all 0.3s;
  }
  .tab-btn.active {
    background var(--gold);
    color #0d1117;
    font-weight 700;
    box-shadow 0 2px 12px rgba(201,168,76,0.3);
  }

   Tab content 
  .tab-content { display none; }
  .tab-content.active { display block; }

   Azkar section 
  .azkar-section {
    margin-bottom 28px;
  }
  .section-title {
    font-family 'Amiri', serif;
    font-size 1.5rem;
    color var(--gold);
    margin-bottom 16px;
    padding-right 12px;
    border-right 3px solid var(--gold);
  }

  .zikr-card {
    background var(--bg2);
    border 1px solid rgba(201,168,76,0.15);
    border-radius 12px;
    padding 20px;
    margin-bottom 12px;
    position relative;
    transition all 0.3s;
    cursor pointer;
  }
  .zikr-cardhover {
    border-color rgba(201,168,76,0.4);
    transform translateY(-1px);
    box-shadow 0 4px 20px rgba(0,0,0,0.3);
  }
  .zikr-card.done {
    opacity 0.5;
    border-color rgba(82,183,136,0.3);
    background rgba(82,183,136,0.05);
  }
  .zikr-card.doneafter {
    content '✓';
    position absolute;
    left 16px;
    top 50%;
    transform translateY(-50%);
    color var(--green-light);
    font-size 1.4rem;
  }

  .zikr-text {
    font-family 'Amiri', serif;
    font-size 1.2rem;
    line-height 2;
    color var(--text);
    margin-bottom 12px;
  }

  .zikr-meta {
    display flex;
    align-items center;
    justify-content space-between;
  }

  .zikr-count-badge {
    background rgba(201,168,76,0.15);
    color var(--gold);
    padding 4px 12px;
    border-radius 20px;
    font-size 0.85rem;
    border 1px solid rgba(201,168,76,0.3);
  }

  .counter-controls {
    display flex;
    align-items center;
    gap 10px;
  }
  .counter-btn {
    width 34px;
    height 34px;
    border-radius 50%;
    border 1px solid rgba(201,168,76,0.3);
    background transparent;
    color var(--gold);
    font-size 1.2rem;
    cursor pointer;
    transition all 0.2s;
    display flex; align-items center; justify-content center;
  }
  .counter-btnhover {
    background rgba(201,168,76,0.2);
  }
  .counter-display {
    font-family 'Amiri', serif;
    font-size 1.2rem;
    color var(--text);
    min-width 40px;
    text-align center;
  }

   Progress bar 
  .progress-bar {
    height 3px;
    background rgba(255,255,255,0.1);
    border-radius 2px;
    margin-top 10px;
    overflow hidden;
  }
  .progress-fill {
    height 100%;
    background linear-gradient(90deg, var(--gold-dark), var(--gold));
    border-radius 2px;
    transition width 0.3s ease;
  }

   Alarms tab 
  .alarm-form {
    background var(--bg2);
    border 1px solid rgba(201,168,76,0.2);
    border-radius 16px;
    padding 24px;
    margin-bottom 24px;
  }
  .alarm-form h3 {
    font-family 'Amiri', serif;
    color var(--gold);
    font-size 1.3rem;
    margin-bottom 20px;
  }

  .form-row {
    display grid;
    grid-template-columns 1fr 1fr;
    gap 16px;
    margin-bottom 16px;
  }
  @media (max-width 500px) {
    .form-row { grid-template-columns 1fr; }
    h1 { font-size 2.2rem; }
    #clock-time { font-size 2.5rem; }
  }

  .form-group {
    display flex;
    flex-direction column;
    gap 6px;
  }
  .form-group label {
    color var(--text-muted);
    font-size 0.9rem;
  }
  .form-group select, .form-group input {
    background var(--bg3);
    border 1px solid rgba(201,168,76,0.2);
    color var(--text);
    padding 10px 14px;
    border-radius 8px;
    font-family 'Tajawal', sans-serif;
    font-size 1rem;
    outline none;
    transition border-color 0.2s;
  }
  .form-group selectfocus, .form-group inputfocus {
    border-color var(--gold);
  }

  .days-select {
    display flex;
    flex-wrap wrap;
    gap 8px;
    margin-bottom 16px;
  }
  .day-pill {
    padding 6px 14px;
    border-radius 20px;
    border 1px solid rgba(201,168,76,0.25);
    background transparent;
    color var(--text-muted);
    cursor pointer;
    font-family 'Tajawal', sans-serif;
    font-size 0.85rem;
    transition all 0.2s;
  }
  .day-pill.selected {
    background rgba(201,168,76,0.2);
    color var(--gold);
    border-color var(--gold);
  }

  .btn-primary {
    width 100%;
    padding 12px;
    background linear-gradient(135deg, var(--gold-dark), var(--gold));
    border none;
    border-radius 10px;
    color #0d1117;
    font-family 'Tajawal', sans-serif;
    font-size 1rem;
    font-weight 700;
    cursor pointer;
    transition all 0.3s;
    box-shadow 0 4px 15px rgba(201,168,76,0.25);
  }
  .btn-primaryhover {
    transform translateY(-1px);
    box-shadow 0 6px 20px rgba(201,168,76,0.4);
  }

   Alarm list 
  .alarm-list h3 {
    font-family 'Amiri', serif;
    color var(--gold);
    font-size 1.3rem;
    margin-bottom 16px;
  }
  .alarm-item {
    background var(--bg2);
    border 1px solid rgba(201,168,76,0.15);
    border-radius 12px;
    padding 16px 20px;
    margin-bottom 10px;
    display flex;
    align-items center;
    gap 16px;
    transition all 0.3s;
  }
  .alarm-item.inactive {
    opacity 0.5;
  }
  .alarm-time-display {
    font-family 'Amiri', serif;
    font-size 1.8rem;
    color var(--gold);
    min-width 90px;
  }
  .alarm-info {
    flex 1;
  }
  .alarm-label-text {
    font-size 1rem;
    color var(--text);
    margin-bottom 4px;
  }
  .alarm-days-display {
    font-size 0.8rem;
    color var(--text-muted);
  }
  .alarm-toggle {
    width 44px;
    height 24px;
    background var(--bg3);
    border-radius 12px;
    position relative;
    cursor pointer;
    border 1px solid rgba(255,255,255,0.1);
    transition background 0.3s;
    flex-shrink 0;
  }
  .alarm-toggle.on { background var(--gold); }
  .alarm-toggleafter {
    content '';
    position absolute;
    width 18px;
    height 18px;
    background white;
    border-radius 50%;
    top 2px;
    left 2px;
    transition transform 0.3s;
    box-shadow 0 1px 4px rgba(0,0,0,0.3);
  }
  .alarm-toggle.onafter { transform translateX(20px); }
  .alarm-delete {
    background none;
    border none;
    color var(--red);
    cursor pointer;
    font-size 1.1rem;
    padding 4px 8px;
    border-radius 6px;
    transition all 0.2s;
  }
  .alarm-deletehover { background rgba(123,45,45,0.2); }

   Notification 
  .notification {
    position fixed;
    top 20px;
    left 50%;
    transform translateX(-50%) translateY(-100px);
    background var(--bg2);
    border 1px solid var(--gold);
    border-radius 14px;
    padding 16px 24px;
    z-index 9999;
    text-align center;
    max-width 360px;
    width 90%;
    transition transform 0.4s cubic-bezier(0.34,1.56,0.64,1);
    box-shadow 0 8px 32px rgba(0,0,0,0.5), 0 0 0 1px rgba(201,168,76,0.2);
  }
  .notification.show { transform translateX(-50%) translateY(0); }
  .notif-icon { font-size 2rem; margin-bottom 8px; }
  .notif-title { font-family 'Amiri', serif; color var(--gold); font-size 1.3rem; margin-bottom 6px; }
  .notif-body { color var(--text-muted); font-size 0.9rem; }
  .notif-close {
    margin-top 12px;
    padding 6px 20px;
    background var(--gold);
    color #0d1117;
    border none;
    border-radius 6px;
    cursor pointer;
    font-family 'Tajawal', sans-serif;
    font-weight 700;
    font-size 0.9rem;
  }

   Tasbih counter 
  .tasbih-widget {
    background var(--bg2);
    border 1px solid rgba(201,168,76,0.2);
    border-radius 20px;
    padding 28px;
    text-align center;
    margin-bottom 20px;
  }
  .tasbih-count {
    font-family 'Amiri', serif;
    font-size 5rem;
    color var(--gold);
    text-shadow 0 0 30px rgba(201,168,76,0.3);
    line-height 1;
    margin 16px 0;
  }
  .tasbih-btn {
    width 100px;
    height 100px;
    border-radius 50%;
    background linear-gradient(135deg, var(--gold-dark), var(--gold));
    border none;
    color #0d1117;
    font-size 2.5rem;
    cursor pointer;
    transition all 0.15s;
    box-shadow 0 6px 20px rgba(201,168,76,0.3), inset 0 1px 0 rgba(255,255,255,0.2);
  }
  .tasbih-btnactive {
    transform scale(0.92);
    box-shadow 0 2px 8px rgba(201,168,76,0.2);
  }
  .tasbih-label {
    color var(--text-muted);
    font-size 0.9rem;
    margin-top 12px;
  }
  .tasbih-reset {
    background none;
    border 1px solid rgba(255,255,255,0.1);
    color var(--text-muted);
    padding 8px 20px;
    border-radius 8px;
    cursor pointer;
    font-family 'Tajawal', sans-serif;
    margin-top 12px;
    transition all 0.2s;
  }
  .tasbih-resethover { border-color rgba(255,255,255,0.3); color var(--text); }

  .empty-state {
    text-align center;
    padding 40px;
    color var(--text-muted);
    font-size 0.95rem;
  }
  .empty-state span { font-size 2.5rem; display block; margin-bottom 12px; opacity 0.5; }

  .progress-summary {
    background var(--bg2);
    border 1px solid rgba(201,168,76,0.15);
    border-radius 12px;
    padding 16px 20px;
    margin-bottom 24px;
    display flex;
    align-items center;
    gap 16px;
  }
  .progress-circle {
    width 60px;
    height 60px;
    flex-shrink 0;
  }
  .progress-circle svg { transform rotate(-90deg); }
  .progress-info { flex 1; }
  .progress-info h4 { color var(--text); font-size 0.95rem; margin-bottom 4px; }
  .progress-info p { color var(--text-muted); font-size 0.85rem; }
style
head
body

div id=notification class=notification
  div class=notif-icon🕌div
  div class=notif-title id=notif-titleتذكير بالأذكارdiv
  div class=notif-body id=notif-bodyحان وقت أذكارك اليوميةdiv
  button class=notif-close onclick=closeNotif()حسناًbutton
div

div class=container
  header
    div class=header-ornament﷽div
    h1وردي اليوميh1
    div class=header-subtitleأذكار الصباح والمساء من الجامع الصحيحdiv
  header

  div class=clock-widget
    div id=clock-time000000div
    div id=clock-datediv
    div id=prayer-status⏰ جارٍ تحميل الوقت...div
  div

  div class=tabs
    button class=tab-btn active onclick=switchTab('azkar')📖 الأذكارbutton
    button class=tab-btn onclick=switchTab('tasbih')📿 المسبحةbutton
    button class=tab-btn onclick=switchTab('alarms')🔔 المنبهbutton
  div

  !-- Tab Azkar --
  div id=tab-azkar class=tab-content active
    div class=progress-summary id=progress-summary
      svg class=progress-circle viewBox=0 0 60 60
        circle cx=30 cy=30 r=24 fill=none stroke=rgba(255,255,255,0.1) stroke-width=4
        circle id=progress-arc cx=30 cy=30 r=24 fill=none stroke=#c9a84c stroke-width=4
          stroke-dasharray=150.8 stroke-dashoffset=150.8 stroke-linecap=round
      svg
      div class=progress-info
        h4تقدمك اليومh4
        p id=progress-text0 من 0 ذكر مكتملp
      div
    div

    div class=azkar-section
      div class=section-titleأذكار الصباح والمساءdiv
      div id=azkar-listdiv
    div
  div

  !-- Tab Tasbih --
  div id=tab-tasbih class=tab-content
    div class=tasbih-widget
      div style=colorvar(--text-muted);font-size0.9remسبحان الله وبحمدهdiv
      div class=tasbih-count id=tasbih-num0div
      button class=tasbih-btn onclick=tapTasbih()☝️button
      div class=tasbih-label id=tasbih-labelاضغط للتسبيحdiv
      br
      button class=tasbih-reset onclick=resetTasbih()إعادة ضبطbutton
    div

    div class=azkar-section
      div class=section-titleالأذكار للعدّdiv
      div id=count-azkar-listdiv
    div
  div

  !-- Tab Alarms --
  div id=tab-alarms class=tab-content
    div class=alarm-form
      h3🔔 إضافة منبه جديدh3
      div class=form-row
        div class=form-group
          labelالوقتlabel
          input type=time id=alarm-time value=0500
        div
        div class=form-group
          labelنوع الذكرlabel
          select id=alarm-type
            option value=صباحأذكار الصباحoption
            option value=مساءأذكار المساءoption
            option value=عامتذكير عام بالأذكارoption
          select
        div
      div
      div class=form-group style=margin-bottom16px
        labelالأيامlabel
        div class=days-select id=days-select
          button class=day-pill selected data-day=0الأحدbutton
          button class=day-pill selected data-day=1الاثنينbutton
          button class=day-pill selected data-day=2الثلاثاءbutton
          button class=day-pill selected data-day=3الأربعاءbutton
          button class=day-pill selected data-day=4الخميسbutton
          button class=day-pill selected data-day=5الجمعةbutton
          button class=day-pill selected data-day=6السبتbutton
        div
      div
      button class=btn-primary onclick=addAlarm()إضافة المنبهbutton
    div

    div class=alarm-list
      h3المنبهات المضافةh3
      div id=alarm-list-containerdiv
    div
  div
div

script
 ===== DATA =====
const azkar = [
  {
    id 1,
    text لا إِلَهَ إِلَّا اللهُ وحدَهُ لا شَريكَ لَهُ، لَهُ الملكُ ولَهُ الحَمدُ وهو على كُلِّ شَيءٍ قديرٌ,
    total 1,
    note مرة واحدة
  },
  {
    id 2,
    text أَصبَحتُ أُثْني عليكَ حَمَدًا، وأَشهَدُ أَنْ لا إِلَهَ إِلَّا اللهُ,
    total 3,
    note ثلاث مرات
  },
  {
    id 3,
    text سُبحانَ اللَّهِ وبِحَمده,
    total 100,
    note مئة مرة
  },
  {
    id 4,
    text سُبحانَ اللَّهِ وبِحَمده، سُبحانَ اللَّهِ العَظيم,
    total 100,
    note مئة مرة
  },
  {
    id 5,
    text يا حَيُّ يا قَيُّومُ، بِرَحمَتِكَ أَستَغيثُ، أَصلِحْ لي شَأني كُلَّه، ولا تَكِلْني إلى نَفسي طَرفَةَ عَينٍ,
    total 1,
    note مرة واحدة
  },
  {
    id 6,
    text اللهُمَّ إِنِّي أَسأَلُكَ العافيةَ، في الدُّنيا والآخِرة، اللهُمَّ إِنِّي أَسأَلُكَ العَفوَ والعافيةَ، في ديني ودُنيايَ، وأهلي ومالي، اللهُمَّ استُرْ عَوراتي، وآمِنْ رَوعاتي,
    total 1,
    note مرة واحدة
  },
  {
    id 7,
    text اللهُمَّ فاطِرَ السَّماوات والأرض، عالِمَ الغَيب والشَّهادة، رَبَّ كُلِّ شَيءٍ ومَليكَه، أَشهَدُ أَنْ لا إِلَهَ إِلَّا أنتَ، أَعوذُ بكَ من شَرِّ نَفسي، وشَرِّ الشَّيطانِ وشِركَه,
    total 1,
    note مرة واحدة
  },
  {
    id 8,
    text أَعوذُ بِكَلِماتِ اللَّهِ التَّامَّات من شَرِّ ما خَلَقَ,
    total 3,
    note ثلاث مرات (يُقال في المساء)
  },
  {
    id 9,
    text سيِّدُ الاستِغفار اللهُمَّ أَنتَ رَبِّي لا إِلَهَ إِلَّا أنتَ، خَلَقتَني وأنا عَبدُكَ، وأنا على عَهدِكَ ووَعدِكَ ما استَطَعتُ، أَعوذُ بكَ من شَرِّ ما صَنَعتُ، أَبوءُ لكَ بنِعمَتِكَ علَيَّ، وأَبوءُ لكَ بذَنبي فاغفِرْ لي,
    total 1,
    note مرة واحدة
  },
  {
    id 10,
    text سُبحانَ اللَّهِ وبِحَمده، عَدَدَ خَلقِه، ورِضا نَفسِه، وزِنَةَ عَرشِه، ومِدادَ كَلِماتِه,
    total 3,
    note ثلاث مرات (يُقال في الصباح)
  },
  {
    id 11,
    text بِاسمِ اللَّهِ الذي لا يَضُرُّ مَعَ اسمِه شَيءٌ في الأرضِ ولا في السَّماءِ وهو السَّميعُ العَليمُ,
    total 3,
    note ثلاث مرات
  },
  {
    id 12,
    text اللهُمَّ بكَ أصبَحنا، وبكَ أمسَينا، وبكَ نَحيا، وبكَ نَموتُ، وإليكَ النُّشورُ,
    total 1,
    note مرة واحدة (في الصباح)
  },
  {
    id 13,
    text أَصبَحنا على فِطرةِ الإسلام وكَلمةِ الإخلاصِ ودينِ نَبيِّنا مُحمَّد ﷺ ومِلَّةِ أبينا إبراهيمَ حَنيفًا مُسلِمًا وما أنا مِنَ المُشركين,
    total 1,
    note مرة واحدة
  }
];

 State
let counts = {};
let alarms = JSON.parse(localStorage.getItem('azkar_alarms')  '[]');
let tasbihCount = parseInt(localStorage.getItem('tasbih_count')  '0');
let alarmInterval;

 Init counts from localStorage
const savedCounts = JSON.parse(localStorage.getItem('azkar_counts')  '{}');
const savedDate = localStorage.getItem('azkar_date');
const today = new Date().toDateString();
if (savedDate === today) {
  counts = savedCounts;
} else {
  azkar.forEach(z = counts[z.id] = 0);
  localStorage.setItem('azkar_date', today);
}
azkar.forEach(z = { if (counts[z.id] === undefined) counts[z.id] = 0; });

 ===== CLOCK =====
function updateClock() {
  co
