<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <meta name="color-scheme" content="dark light" />
  <title>Seattle Weather Widget</title>
  <style>
    :root{
      /* Defaults (override with URL params) */
      --bg: #0b1320;
      --card: rgba(255,255,255,.08);
      --text: rgba(255,255,255,.92);
      --muted: rgba(255,255,255,.70);
      --accent: #60a5fa;
      --radius: 18px;
      --shadow: 0 10px 30px rgba(0,0,0,.28);
      --font: ui-sans-serif, system-ui, -apple-system, Segoe UI, Roboto, Helvetica, Arial, "Apple Color Emoji", "Segoe UI Emoji";
      --border: rgba(255,255,255,.10);
    }
    [data-theme="light"]{
      --bg: #f6f7fb;
      --card: rgba(0,0,0,.04);
      --text: rgba(0,0,0,.88);
      --muted: rgba(0,0,0,.62);
      --accent: #2563eb;
      --shadow: 0 10px 26px rgba(15, 23, 42, .12);
      --border: rgba(0,0,0,.10);
    }

    html, body { height: 100%; }
    body{
      margin:0;
      font-family: var(--font);
      color: var(--text);
      background: radial-gradient(1200px 600px at 20% 0%, color-mix(in srgb, var(--accent) 22%, transparent), transparent 60%),
                  radial-gradient(900px 500px at 90% 10%, rgba(255,255,255,.08), transparent 55%),
                  var(--bg);
      display:flex;
      align-items:stretch;
      justify-content:center;
    }

    .wrap{
      width: min(720px, 100%);
      padding: 14px;
      box-sizing:border-box;
    }

    .card{
      background: linear-gradient(180deg, color-mix(in srgb, var(--card) 85%, transparent), var(--card));
      border: 1px solid var(--border);
      border-radius: var(--radius);
      box-shadow: var(--shadow);
      overflow:hidden;
    }

    .top{
      display:flex; gap:12px; align-items:center; justify-content:space-between;
      padding: 14px 16px 10px 16px;
    }

    .title{
      display:flex; flex-direction:column; gap:2px; min-width:0;
    }
    .title h1{
      font-size: 16px; margin:0; font-weight: 700; letter-spacing: .2px;
      white-space:nowrap; overflow:hidden; text-overflow:ellipsis;
    }
    .title .sub{
      font-size: 12px; color: var(--muted);
      white-space:nowrap; overflow:hidden; text-overflow:ellipsis;
    }

    .pillRow{ display:flex; gap:8px; align-items:center; }
    .pill{
      font-size:12px; color: var(--muted);
      border: 1px solid var(--border);
      padding: 6px 10px;
      border-radius: 999px;
      background: color-mix(in srgb, var(--card) 70%, transparent);
      user-select:none;
    }
    .pill strong{ color: var(--text); font-weight:700; }

    .main{
      display:grid;
      grid-template-columns: 1.1fr .9fr;
      gap: 10px;
      padding: 0 16px 12px;
    }
    @media (max-width: 520px){
      .main { grid-template-columns: 1fr; }
    }

    .big{
      display:flex; gap:12px; align-items:center;
      padding: 12px 14px;
      border: 1px solid var(--border);
      border-radius: calc(var(--radius) - 6px);
      background: color-mix(in srgb, var(--card) 76%, transparent);
    }
    .emoji{
      font-size: 34px;
      width: 46px; height: 46px;
      display:grid; place-items:center;
      border-radius: 14px;
      background: color-mix(in srgb, var(--accent) 18%, transparent);
      border: 1px solid color-mix(in srgb, var(--accent) 30%, var(--border));
      flex: 0 0 auto;
    }
    .big .temp{
      font-size: 34px;
      font-weight: 800;
      letter-spacing: -0.5px;
      line-height: 1.0;
      margin:0;
    }
    .big .cond{
      font-size: 13px;
      color: var(--muted);
      margin-top: 2px;
      white-space:nowrap; overflow:hidden; text-overflow:ellipsis;
      max-width: 40ch;
    }

    .grid{
      display:grid;
      grid-template-columns: repeat(2, minmax(0,1fr));
      gap: 10px;
    }
    .stat{
      padding: 10px 12px;
      border: 1px solid var(--border);
      border-radius: calc(var(--radius) - 8px);
      background: color-mix(in srgb, var(--card) 68%, transparent);
    }
    .stat .k{
      font-size: 11px; color: var(--muted);
      letter-spacing: .25px;
      text-transform: uppercase;
    }
    .stat .v{
      margin-top: 4px;
      font-size: 14px;
      font-weight: 700;
      color: var(--text);
    }

    .forecast{
      padding: 0 16px 16px;
    }
    .forecastHeader{
      display:flex; align-items:center; justify-content:space-between;
      padding: 6px 0 10px;
      color: var(--muted);
      font-size: 12px;
    }
    .days{
      display:grid;
      grid-template-columns: repeat(4, minmax(0,1fr));
      gap: 10px;
    }
    @media (max-width: 520px){
      .days{ grid-template-columns: repeat(2, minmax(0,1fr)); }
    }
    .day{
      border: 1px solid var(--border);
      border-radius: calc(var(--radius) - 8px);
      background: color-mix(in srgb, var(--card) 68%, transparent);
      padding: 10px 10px 11px;
      display:flex; flex-direction:column; gap: 6px;
      min-height: 78px;
    }
    .dow{
      font-size: 12px; color: var(--muted);
      display:flex; justify-content:space-between; gap: 8px;
    }
    .lohi{
      display:flex; justify-content:space-between; align-items:baseline;
      font-size: 14px; font-weight: 800;
      letter-spacing: -.2px;
    }
    .lohi span{ color: var(--muted); font-weight: 700; }
    .mini{
      display:flex; align-items:center; justify-content:space-between;
      gap: 8px;
      font-size: 12px;
      color: var(--muted);
    }
    .mini .ico{ font-size: 18px; }

    .footer{
      padding: 10px 16px 14px;
      border-top: 1px solid var(--border);
      display:flex; justify-content:space-between; align-items:center;
      gap: 10px;
      color: var(--muted);
      font-size: 11px;
    }
    .link{
      color: color-mix(in srgb, var(--accent) 85%, var(--text));
      text-decoration:none;
      border-bottom: 1px dashed color-mix(in srgb, var(--accent) 55%, transparent);
    }
    .error{
      padding: 14px 16px 16px;
      color: var(--muted);
      font-size: 13px;
    }
    .spinner{
      display:inline-block;
      width: 12px; height: 12px;
      border: 2px solid color-mix(in srgb, var(--muted) 40%, transparent);
      border-top-color: var(--accent);
      border-radius: 999px;
      animation: spin 1s linear infinite;
      vertical-align: -2px;
      margin-right: 6px;
    }
    @keyframes spin { to { transform: rotate(360deg); } }
  </style>
</head>
<body>
  <div class="wrap">
    <div class="card" id="card">
      <div class="top">
        <div class="title">
          <h1 id="place">Seattle, WA</h1>
          <div class="sub" id="updated"><span class="spinner"></span>Loading…</div>
        </div>
        <div class="pillRow">
          <div class="pill" id="unitPill">Units: <strong>°F</strong></div>
        </div>
      </div>

      <div class="main">
        <div class="big">
          <div class="emoji" id="emoji">⛅</div>
          <div style="min-width:0">
            <p class="temp" id="temp">--°</p>
            <div class="cond" id="cond">--</div>
          </div>
        </div>

        <div class="grid">
          <div class="stat">
            <div class="k">Feels like</div>
            <div class="v" id="feels">--</div>
          </div>
          <div class="stat">
            <div class="k">Wind</div>
            <div class="v" id="wind">--</div>
          </div>
          <div class="stat">
            <div class="k">Humidity</div>
            <div class="v" id="hum">--</div>
          </div>
          <div class="stat">
            <div class="k">Precip</div>
            <div class="v" id="precip">--</div>
          </div>
        </div>
      </div>

      <div class="forecast" id="forecast">
        <div class="forecastHeader">
          <span>Next 4 days</span>
          <span id="hiLoToday">Today: -- / --</span>
        </div>
        <div class="days" id="days"></div>
      </div>

      <div class="footer">
        <span id="sourceLine">Data: Open-Meteo</span>
        <a class="link" href="https://open-meteo.com/" target="_blank" rel="noreferrer">open-meteo.com</a>
      </div>

      <div class="error" id="error" style="display:none;"></div>
    </div>
  </div>

<script>
(() => {
  // ---- Defaults: Seattle ----
  const defaults = {
    lat: 47.6062,
    lon: -122.3321,
    tz: "America/Los_Angeles",
    units: "f",         // f | c
    wind: "mph",        // mph | kmh | ms | kn
    precip: "inch",     // inch | mm
    days: 4,            // show 4 days
    compact: 0,         // 1 hides forecast
    theme: null,        // dark | light | auto (null -> auto)
    accent: null, bg: null, text: null, card: null,
    radius: null, shadow: null, font: null,
    refreshMin: 20      // minutes
  };

  const q = new URLSearchParams(location.search);
  const opt = {
    ...defaults,
    lat: num(q.get("lat")) ?? defaults.lat,
    lon: num(q.get("lon")) ?? defaults.lon,
    tz: q.get("tz") ?? defaults.tz,
    units: (q.get("units") || defaults.units).toLowerCase(),
    wind: (q.get("wind") || defaults.wind).toLowerCase(),
    precip: (q.get("precip") || defaults.precip).toLowerCase(),
    days: clampInt(q.get("days"), 1, 16) ?? defaults.days,
    compact: clampInt(q.get("compact"), 0, 1) ?? defaults.compact,
    theme: (q.get("theme") || defaults.theme)?.toLowerCase() ?? null,
    accent: q.get("accent"),
    bg: q.get("bg"),
    text: q.get("text"),
    card: q.get("card"),
    radius: q.get("radius"),
    shadow: q.get("shadow"),
    font: q.get("font"),
    refreshMin: clampInt(q.get("refresh"), 5, 180) ?? defaults.refreshMin,
  };

  // ---- Apply theme & style overrides ----
  const root = document.documentElement;
  const preferLight = window.matchMedia && window.matchMedia('(prefers-color-scheme: light)').matches;
  const theme = (opt.theme === "light" || opt.theme === "dark")
    ? opt.theme
    : (preferLight ? "light" : "dark");
  root.dataset.theme = theme;

  setVar("--accent", opt.accent);
  setVar("--bg", opt.bg);
  setVar("--text", opt.text);
  setVar("--card", opt.card);
  if (opt.radius) setVar("--radius", px(opt.radius));
  if (opt.shadow) setVar("--shadow", decodeURIComponent(opt.shadow));
  if (opt.font) setVar("--font", decodeURIComponent(opt.font));

  document.getElementById("unitPill").innerHTML = `Units: <strong>${opt.units === "c" ? "°C" : "°F"}</strong>`;
  if (opt.compact) document.getElementById("forecast").style.display = "none";

  // ---- Open-Meteo request ----
  // Docs: /v1/forecast supports `current=` variables and `daily=` requires timezone. :contentReference[oaicite:1]{index=1}
  const tempUnit = opt.units === "c" ? "celsius" : "fahrenheit";
  const api = new URL("https://api.open-meteo.com/v1/forecast");
  api.searchParams.set("latitude", opt.lat);
  api.searchParams.set("longitude", opt.lon);
  api.searchParams.set("timezone", opt.tz);
  api.searchParams.set("temperature_unit", tempUnit);
  api.searchParams.set("wind_speed_unit", opt.wind);
  api.searchParams.set("precipitation_unit", opt.precip);
  api.searchParams.set("forecast_days", String(Math.max(opt.days, 4)));
  api.searchParams.set("current", [
    "temperature_2m",
    "apparent_temperature",
    "relative_humidity_2m",
    "precipitation",
    "weather_code",
    "wind_speed_10m",
    "wind_direction_10m",
    "is_day",
  ].join(","));
  api.searchParams.set("daily", [
    "temperature_2m_max",
    "temperature_2m_min",
    "precipitation_probability_max",
    "weather_code"
  ].join(","));

  // ---- Cache ----
  const cacheKey = `wx-cache:${opt.lat},${opt.lon}:${opt.units}:${opt.wind}:${opt.precip}:${opt.tz}`;
  const now = Date.now();
  const cached = safeJSON(localStorage.getItem(cacheKey));
  const cachedFresh = cached && (now - cached.at) < (opt.refreshMin * 60 * 1000);

  if (cachedFresh) render(cached.data, true);
  fetchLatest().catch(err => {
    if (cached?.data) {
      render(cached.data, true);
      showError(`Using cached data (offline or rate-limited).`);
    } else {
      showError(`Couldn’t load weather right now. (${err?.message || "unknown error"})`);
    }
  });

  async function fetchLatest(){
    const ctrl = new AbortController();
    const t = setTimeout(() => ctrl.abort(), 9000);
    const res = await fetch(api.toString(), { signal: ctrl.signal, cache: "no-store" });
    clearTimeout(t);
    if (!res.ok) throw new Error(`HTTP ${res.status}`);
    const data = await res.json();
    localStorage.setItem(cacheKey, JSON.stringify({ at: Date.now(), data }));
    render(data, false);
  }

  function render(data, wasCached){
    hideError();

    const uCur = data.current_units || {};
    const cur = data.current || {};
    const daily = data.daily || {};
    const dUnits = data.daily_units || {};

    const t = cur.temperature_2m;
    const feels = cur.apparent_temperature;
    const hum = cur.relative_humidity_2m;
    const wind = cur.wind_speed_10m;
    const wdir = cur.wind_direction_10m;
    const precip = cur.precipitation;
    const code = cur.weather_code;
    const isDay = cur.is_day === 1;

    const { label, emoji } = codeToWeather(code, isDay);

    byId("emoji").textContent = emoji;
    byId("temp").textContent = fmt0(t) + uCur.temperature_2m;
    byId("cond").textContent = label;
    byId("feels").textContent = fmt0(feels) + uCur.apparent_temperature;
    byId("hum").textContent = fmt0(hum) + uCur.relative_humidity_2m;
    byId("wind").textContent = fmt0(wind) + uCur.wind_speed_10m + " • " + compass(wdir);
    byId("precip").textContent = fmt1(precip) + " " + uCur.precipitation;

    const updated = data.current?.time ? new Date(data.current.time) : new Date();
    byId("updated").textContent =
      `${wasCached ? "Cached" : "Updated"} • ${updated.toLocaleString(undefined, { weekday:"short", hour:"numeric", minute:"2-digit" })}`;

    // Today hi/lo
    const tmax = daily.temperature_2m_max?.[0];
    const tmin = daily.temperature_2m_min?.[0];
    if (tmax != null && tmin != null) {
      byId("hiLoToday").textContent = `Today: ${fmt0(tmax)}${dUnits.temperature_2m_max} / ${fmt0(tmin)}${dUnits.temperature_2m_min}`;
    }

    // Forecast cards (next 4 days)
    const daysEl = byId("days");
    daysEl.innerHTML = "";
    const count = Math.min(4, (daily.time || []).length);
    for (let i = 0; i < count; i++){
      const dt = daily.time[i] ? new Date(daily.time[i] + "T00:00:00") : null;
      const dow = dt ? dt.toLocaleDateString(undefined, { weekday: "short" }) : `Day ${i+1}`;
      const codeD = daily.weather_code?.[i] ?? code;
      const wx = codeToWeather(codeD, true);

      const hi = daily.temperature_2m_max?.[i];
      const lo = daily.temperature_2m_min?.[i];
      const pop = daily.precipitation_probability_max?.[i];

      const card = document.createElement("div");
      card.className = "day";
      card.innerHTML = `
        <div class="dow">
          <span>${escapeHtml(dow)}</span>
          <span class="ico">${wx.emoji}</span>
        </div>
        <div class="lohi">
          <div>${fmt0(hi)}${dUnits.temperature_2m_max || ""}</div>
          <span>${fmt0(lo)}${dUnits.temperature_2m_min || ""}</span>
        </div>
        <div class="mini">
          <span>${escapeHtml(wx.label)}</span>
          <span>${pop != null ? `${fmt0(pop)}${dUnits.precipitation_probability_max || "%"}` : ""}</span>
        </div>
      `;
      daysEl.appendChild(card);
    }
  }

  // ---- Weather code mapping (Open-Meteo uses WMO codes) ----
  // Code list examples in docs. :contentReference[oaicite:2]{index=2}
  function codeToWeather(code, isDay){
    const c = Number(code);
    if (c === 0) return { label: "Clear", emoji: isDay ? "☀️" : "🌙" };
    if ([1,2].includes(c)) return { label: "Mostly clear", emoji: isDay ? "🌤️" : "🌙☁️" };
    if (c === 3) return { label: "Cloudy", emoji: "☁️" };
    if ([45,48].includes(c)) return { label: "Fog", emoji: "🌫️" };
    if ([51,53,55].includes(c)) return { label: "Drizzle", emoji: "🌦️" };
    if ([56,57].includes(c)) return { label: "Freezing drizzle", emoji: "🧊🌧️" };
    if ([61,63,65].includes(c)) return { label: "Rain", emoji: "🌧️" };
    if ([66,67].includes(c)) return { label: "Freezing rain", emoji: "🧊🌧️" };
    if ([71,73,75].includes(c)) return { label: "Snow", emoji: "🌨️" };
    if (c === 77) return { label: "Snow grains", emoji: "🌨️" };
    if ([80,81,82].includes(c)) return { label: "Showers", emoji: "🌧️" };
    if ([85,86].includes(c)) return { label: "Snow showers", emoji: "🌨️" };
    if (c === 95) return { label: "Thunderstorm", emoji: "⛈️" };
    if ([96,99].includes(c)) return { label: "Thunderstorm w/ hail", emoji: "⛈️🧊" };
    return { label: `Weather (${c})`, emoji: "🌡️" };
  }

  // ---- Helpers ----
  function byId(id){ return document.getElementById(id); }
  function fmt0(x){ return (x == null || Number.isNaN(Number(x))) ? "--" : Math.round(Number(x)).toString(); }
  function fmt1(x){ return (x == null || Number.isNaN(Number(x))) ? "--" : (Math.round(Number(x)*10)/10).toString(); }
  function num(x){ if (x == null) return null; const n = Number(x); return Number.isFinite(n) ? n : null; }
  function clampInt(x, a, b){ if (x == null) return null; const n = parseInt(x,10); if (!Number.isFinite(n)) return null; return Math.max(a, Math.min(b, n)); }
  function setVar(name, val){
    if (!val) return;
    try { document.documentElement.style.setProperty(name, decodeURIComponent(val)); }
    catch { document.documentElement.style.setProperty(name, val); }
  }
  function px(v){
    const n = num(v);
    if (n != null) return `${n}px`;
    return decodeURIComponent(v);
  }
  function safeJSON(s){ try { return JSON.parse(s); } catch { return null; } }
  function compass(deg){
    if (deg == null || Number.isNaN(Number(deg))) return "--";
    const dirs = ["N","NE","E","SE","S","SW","W","NW"];
    const i = Math.round(((Number(deg) % 360) / 45)) % 8;
    return `${dirs[i]}`;
  }
  function escapeHtml(str){
    return String(str).replaceAll("&","&amp;").replaceAll("<","&lt;").replaceAll(">","&gt;").replaceAll('"',"&quot;").replaceAll("'","&#039;");
  }
  function showError(msg){
    const el = byId("error");
    el.style.display = "block";
    el.textContent = msg;
  }
  function hideError(){
    const el = byId("error");
    el.style.display = "none";
    el.textContent = "";
  }
})();
</script>
</body>
</html>
