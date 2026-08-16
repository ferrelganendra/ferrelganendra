# Hi, I'm Ferrel

I like the messy part of building: turning a rough note into a screen, then into something with real data, handled edge cases, and a reason to exist.

```aura width=860 height=290 align=center
<div style={{ width:'100%', height:'100%', background:'linear-gradient(160deg,#0A0A0C 0%,#111116 55%,#0A0A0C 100%)', display:'flex', position:'relative', overflow:'hidden', borderRadius:20, border:'1px solid rgba(255,59,48,0.25)' }}>
  <style>{`
    @keyframes floatOrb { 0%,100% { transform:translate(0,0); opacity:.5; } 50% { transform:translate(22px,-16px); opacity:.95; } }
    @keyframes floatOrb2 { 0%,100% { transform:translate(0,0); opacity:.35; } 50% { transform:translate(-18px,12px); opacity:.8; } }
    @keyframes ringP { 0% { transform:scale(.7); opacity:.6; } 100% { transform:scale(1.7); opacity:0; } }
    @keyframes bob { 0%,100% { transform:translateY(0); } 50% { transform:translateY(-6px); } }
    @keyframes ringPulse { 0% { transform:scale(.8); opacity:.7; } 100% { transform:scale(1.45); opacity:0; } }
    #ping1 { animation:ringPulse 2.6s ease-out infinite; transform-origin:center; transform-box:fill-box; }
    #ping2 { animation:ringPulse 2.6s ease-out infinite; animation-delay:1.3s; transform-origin:center; transform-box:fill-box; }
    #ph { animation:bob 5s ease-in-out infinite; }
    #org1 { animation:floatOrb 8s ease-in-out infinite; }
    #org2 { animation:floatOrb2 11s ease-in-out infinite; }
  `}</style>

  <svg width="860" height="290" style={{ position:'absolute', top:0, left:0 }}>
    <defs>
      <radialGradient id="gA" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(255,59,48,0.40)"/>
        <stop offset="100%" stopColor="rgba(255,59,48,0)"/>
      </radialGradient>
      <radialGradient id="gB" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(120,40,255,0.25)"/>
        <stop offset="100%" stopColor="rgba(120,40,255,0)"/>
      </radialGradient>
      <pattern id="gridBg" width="30" height="30" patternUnits="userSpaceOnUse">
        <path d="M30 0 L0 0 0 30" fill="none" stroke="rgba(255,255,255,0.04)" strokeWidth="1"/>
      </pattern>
    </defs>
    <rect width="860" height="290" fill="url(#gridBg)"/>
    <ellipse id="org1" cx="690" cy="70" rx="250" ry="200" fill="url(#gA)"/>
    <ellipse id="org2" cx="110" cy="250" rx="220" ry="170" fill="url(#gB)"/>
  </svg>

  <div style={{ display:'flex', alignItems:'center', padding:'34px 38px', gap:28, position:'relative', fontFamily:'Inter' }}>
    <div style={{ position:'relative', width:128, height:128, display:'flex', alignItems:'center', justifyContent:'center' }}>
      <svg width="128" height="128" viewBox="0 0 128 128">
        <circle id="ping1" cx="64" cy="64" r="62" fill="none" stroke="#FF3B30" strokeWidth="2"/>
        <circle id="ping2" cx="64" cy="64" r="62" fill="none" stroke="#FF3B30" strokeWidth="2"/>
      </svg>
      <div id="ph" style={{ position:'absolute', width:104, height:104, borderRadius:52, overflow:'hidden', border:'3px solid #FF3B30', background:'#1a1a20', display:'flex', alignItems:'center', justifyContent:'center' }}>
        <img src="https://github.com/ferrelganendra.png" width={104} height={104} style={{ borderRadius:52 }}/>
      </div>
      <div style={{ position:'absolute', right:0, bottom:4, width:20, height:20, borderRadius:10, background:'#2ea44f', border:'3px solid #0A0A0C' }}></div>
    </div>

    <div style={{ display:'flex', flexDirection:'column', gap:9 }}>
      <div style={{ fontSize:12, letterSpacing:5, color:'#FF3B30', fontWeight:700 }}>WEB · AI · SHIPPED</div>
      <div style={{ fontSize:46, fontWeight:800, color:'#ffffff', letterSpacing:'-1.5px', lineHeight:1.05 }}>FERREL GANENDRA</div>
      <div style={{ fontSize:14, color:'rgba(201,209,217,0.85)', fontWeight:400, maxWidth:430, lineHeight:1.45 }}>
        {github?.user?.bio || 'Turning rough notes into shipped apps - RAG, LLM tools, and web apps with real inputs.'}
      </div>
    </div>
  </div>

    <div style={{ display:'flex', gap:9, padding:'0 38px 26px', flexWrap:'wrap', position:'absolute', bottom:0, left:0, right:0, fontFamily:'Inter' }}>
    <div style={{ display:'flex', padding:'5px 13px', borderRadius:18, background:'rgba(255,59,48,0.14)', border:'1px solid rgba(255,59,48,0.4)', color:'#FF6B5F', fontSize:12, fontWeight:600 }}>
      {github?.user?.location || 'Yogyakarta, Indonesia'}
    </div>
    <div style={{ display:'flex', padding:'5px 13px', borderRadius:18, background:'rgba(201,209,217,0.06)', border:'1px solid rgba(201,209,217,0.18)', color:'#c9d1d9', fontSize:12, fontWeight:600 }}>AI Engineer</div>
    <div style={{ display:'flex', padding:'5px 13px', borderRadius:18, background:'rgba(201,209,217,0.06)', border:'1px solid rgba(201,209,217,0.18)', color:'#c9d1d9', fontSize:12, fontWeight:600 }}>{github?.stats?.totalRepos || 10} repos</div>
    <div style={{ display:'flex', padding:'5px 13px', borderRadius:18, background:'rgba(201,209,217,0.06)', border:'1px solid rgba(201,209,217,0.18)', color:'#c9d1d9', fontSize:12, fontWeight:600 }}>{github?.stats?.totalCommits || 533} commits</div>
  </div>
</div>
```

```aura width=860 height=230 align=center
<div style={{ width:'100%', height:'100%', background:'#0d0d10', display:'flex', flexDirection:'column', position:'relative', overflow:'hidden', borderRadius:20, border:'1px solid rgba(201,209,217,0.1)', padding:'26px 34px', gap:8, fontFamily:'Inter' }}>
  <style>{`
    @keyframes fillbar { 0% { width:0; } 100% { width:100%; } }
    .langbar { animation: fillbar 1.7s ease-out forwards; }
  `}</style>
  <div style={{ fontSize:12, letterSpacing:3, color:'#FF3B30', fontWeight:700 }}>THE STACK</div>
  <div style={{ display:'flex', flexDirection:'column', gap:10, marginTop:6 }}>
    {(github && github.languages && github.languages.length ? github.languages.slice(0,5) : []).map(function(l,i){
      return (
        <div key={i} style={{ display:'flex', flexDirection:'column', gap:3 }}>
          <div style={{ display:'flex', justifyContent:'space-between', fontSize:12, color:'#c9d1d9' }}>
            <span style={{ fontWeight:600 }}>{l.name}</span>
            <span style={{ color:'rgba(201,209,217,0.55)' }}>{Math.round(l.percentage)}%</span>
          </div>
          <div style={{ width:'100%', height:8, borderRadius:4, background:'rgba(201,209,217,0.08)', overflow:'hidden', display:'flex' }}>
            <div className="langbar" style={{ width:(l.percentage||10)+'%', height:'100%', borderRadius:4, background:l.color||'#FF3B30' }}></div>
          </div>
        </div>
      );
    })}
  </div>
</div>
```

## What I'm building

```aura width=860 height=230 align=center
<div style={{ width:'100%', height:'100%', background:'#0d0d10', display:'flex', fontFamily:'Inter', flexDirection:'column', position:'relative', overflow:'hidden', borderRadius:20, border:'1px solid rgba(201,209,217,0.1)', padding:'26px 34px', gap:12 }}>
  <style>{`
    @keyframes slideRow { 0%,100% { transform:translateX(0); } 50% { transform:translateX(4px); } }
    .row-hover { animation:slideRow 2.6s ease-in-out infinite; }
    @keyframes openGlow { 0%,100% { opacity:1; } 50% { opacity:.55; } }
    .opw { animation:openGlow 1.8s ease-in-out infinite; }
  `}</style>
  <div style={{ fontSize:12, letterSpacing:3, color:'#FF3B30', fontWeight:700 }}>NOW BUILDING</div>

  <div className="row-hover" style={{ display:'flex', justifyContent:'space-between', alignItems:'center', borderBottom:'1px solid rgba(201,209,217,0.08)', paddingBottom:10 }}>
    <div style={{ display:'flex', flexDirection:'column', gap:2 }}>
      <span style={{ fontSize:15, fontWeight:700, color:'#f5f5f7' }}>RAG QA engine</span>
      <span style={{ fontSize:12, color:'rgba(201,209,217,0.65)' }}>multi-model, streaming, citations, eval</span>
    </div>
    <span style={{ fontSize:11, color:'#FF6B5F', fontFamily:'Menlo,monospace' }}>rag-chatbot</span>
  </div>

  <div className="row-hover" style={{ display:'flex', justifyContent:'space-between', alignItems:'center', borderBottom:'1px solid rgba(201,209,217,0.08)', paddingBottom:10 }}>
    <div style={{ display:'flex', flexDirection:'column', gap:2 }}>
      <span style={{ fontSize:15, fontWeight:700, color:'#f5f5f7' }}>Job aggregator</span>
      <span style={{ fontSize:12, color:'rgba(201,209,217,0.65)' }}>spanning 14 industries</span>
    </div>
    <span style={{ fontSize:11, color:'#FF6B5F', fontFamily:'Menlo,monospace' }}>jobradar</span>
  </div>

  <div className="opw" style={{ display:'flex', alignSelf:'flex-start', padding:'5px 13px', borderRadius:16, background:'rgba(255,59,48,0.12)', border:'1px solid rgba(255,59,48,0.4)', color:'#FF6B5F', fontSize:12, fontWeight:700, marginTop:2 }}>
    OPEN TO WORK
  </div>
</div>
```

## Where I'm strong

- **AI tools with real inputs** - RAG, automation, and LLM flows that still behave after the demo stops being cute.
- **Web apps with a clear path** - one obvious main action, error states handled, not an afterthought.
- **Shipping** - small things that work, instead of demos that die in a README.

## Featured work

```aura width=860 height=190 align=center
<div style={{ width:'100%', height:'100%', background:'#0d0d10', display:'flex', fontFamily:'Inter', flexDirection:'column', position:'relative', overflow:'hidden', borderRadius:20, border:'1px solid rgba(201,209,217,0.1)', padding:'22px 30px', gap:12 }}>
  <style>{`
    @keyframes featuredReveal { 0% { opacity:0; transform:translateY(8px); } 100% { opacity:1; transform:translateY(0); } }
    @keyframes featuredNudge { 0%,100% { opacity:.45; transform:translateX(0); } 50% { opacity:1; transform:translateX(4px); } }
    @keyframes featuredPulse { 0%,100% { opacity:1; } 50% { opacity:.55; } }
    .featured-row { animation:featuredReveal .65s ease-out both; }
    .featured-row-1 { animation-delay:.05s; }
    .featured-row-2 { animation-delay:.18s; }
    .featured-row-3 { animation-delay:.31s; }
    .featured-arrow { animation:featuredNudge 2s ease-in-out infinite; }
    .featured-label { animation:featuredPulse 2.4s ease-in-out infinite; }
  `}</style>
  <div className="featured-label" style={{ fontSize:12, letterSpacing:3, color:'#FF3B30', fontWeight:700 }}>FEATURED WORK</div>
  <div style={{ display:'flex', flexDirection:'column', gap:11 }}>
    <div className="featured-row featured-row-1" style={{ display:'flex', justifyContent:'space-between', alignItems:'center' }}>
      <span style={{ fontSize:14, fontWeight:700, color:'#f5f5f7' }}>rag-chatbot</span>
      <span style={{ display:'flex', alignItems:'center', gap:8, fontSize:12, color:'rgba(201,209,217,0.6)' }}>Python · ★ 1 <span className="featured-arrow" style={{ color:'#FF3B30', fontSize:14 }}>→</span></span>
   </div>
    <div className="featured-row featured-row-2" style={{ display:'flex', justifyContent:'space-between', alignItems:'center' }}>
      <span style={{ fontSize:14, fontWeight:700, color:'#f5f5f7' }}>jobradar-live</span>
      <span style={{ display:'flex', alignItems:'center', gap:8, fontSize:12, color:'rgba(201,209,217,0.6)' }}>Python · ★ 0 <span className="featured-arrow" style={{ color:'#FF3B30', fontSize:14 }}>→</span></span>
   </div>
    <div className="featured-row featured-row-3" style={{ display:'flex', justifyContent:'space-between', alignItems:'center' }}>
      <span style={{ fontSize:14, fontWeight:700, color:'#f5f5f7' }}>Puthic-Sari</span>
      <span style={{ display:'flex', alignItems:'center', gap:8, fontSize:12, color:'rgba(201,209,217,0.6)' }}>JavaScript · ★ 0 <span className="featured-arrow" style={{ color:'#FF3B30', fontSize:14 }}>→</span></span>
   </div>
 </div>
</div>
```

<div align="center">

[rag-chatbot](https://github.com/ferrelganendra/rag-chatbot) · [JobRadar LIVE](https://jobradar-live.pages.dev) · [Puthic-Sari](https://github.com/ferrelganendra/Puthic-Sari)

</div>

## GitHub

<div align="center">

![3D contributions](./profile-3d-contrib/profile-custom-gitblock.svg)

![Snake](https://raw.githubusercontent.com/ferrelganendra/ferrelganendra/output/github-contribution-grid-snake-dark.svg)

</div>

## Connect

Let's build something - connect with me below.

<div align="center">

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/ferrelganendra/)
[![Portfolio](https://img.shields.io/badge/Portfolio-FF3B30?style=for-the-badge&logo=octocat&logoColor=white)](https://ferrelganendra.my.id)

</div>

```aura width=860 height=40 align=center
<div style={{ width:'100%', height:'100%', display:'flex', alignItems:'center', overflow:'hidden', fontFamily:'Menlo,monospace', background:'#0d0d10', borderRadius:10, border:'1px solid rgba(255,59,48,0.2)', position:'relative', padding:'0 14px' }}>
  <style>{`
    @keyframes scroll { 0% { transform:translateX(0); } 100% { transform:translateX(-50%); } }
    #ticker { animation:scroll 20s linear infinite; display:flex; }
  `}</style>
  <div style={{ position:'absolute', zIndex:2, left:0, top:0, bottom:0, width:20, background:'linear-gradient(90deg,#0d0d10,transparent)' }}></div>
  <div style={{ position:'absolute', zIndex:2, right:0, top:0, bottom:0, width:20, background:'linear-gradient(270deg,#0d0d10,transparent)' }}></div>
  <div style={{ position:'relative', zIndex:2, display:'flex' }}>
    <div id="ticker" style={{ fontSize:11, color:'rgba(201,209,217,0.65)', whiteSpace:'pre', letterSpacing:'2px' }}>  PYTHON &nbsp;·&nbsp; TYPESCRIPT &nbsp;·&nbsp; REACT &nbsp;·&nbsp; NEXT.JS &nbsp;·&nbsp; FASTAPI &nbsp;·&nbsp; SUPABASE &nbsp;·&nbsp; RAG &nbsp;·&nbsp; LLM &nbsp;·&nbsp;  PYTHON &nbsp;·&nbsp; TYPESCRIPT &nbsp;·&nbsp; REACT &nbsp;·&nbsp; NEXT.JS &nbsp;·&nbsp; FASTAPI &nbsp;·&nbsp; SUPABASE &nbsp;·&nbsp; RAG &nbsp;·&nbsp; LLM &nbsp;·&nbsp;</div>
  </div>
</div>
```

*If it starts as a messy note and ends as a working app, I'm probably interested.*
