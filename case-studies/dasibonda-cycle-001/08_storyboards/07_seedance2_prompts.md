# Seedance 2.0 Prompt Pack - 1438년의 별

Source storyboard: `runs/cycle-001/06_pd2-5_storyboard.json`

Use these prompts in Runway / Seedance 2.0 as generation clips, not as one long prompt. For clips longer than 15 seconds, generate the listed segments separately and join them in edit. Keep every output 16:9.

## Global Style Bible

Korean historical science documentary, restrained EBS-style realism, natural light, stable camera, grounded historical props, calm but precise pacing. Joseon scenes use muted indigo dawn, candle amber, aged bronze, hanji paper, black ink, and soft atmospheric haze. Modern observatory scenes use clean cool light, dark sky, metal surfaces, and quiet scientific elegance. No fantasy, no exaggerated drama, no heroic facial close-ups.

## Global Negative Prompt

Avoid fake readable text, invented constellations, random star maps, modern objects in Joseon scenes, modern clothing, fantasy palaces, excessive lens flare, shaky camera, warped hands, malformed instruments, extra faces, random subtitles, logo hallucinations, over-saturated colors, sci-fi UI, anime style, cartoon style, floating unreadable glyphs.

## Post-Production Rule

Do not ask Seedance to generate accurate Korean/Chinese text, JPL data, star coordinates, eclipse timing, SN 1604 coordinates, tide data, labels, subtitles, source citations, or final credits. Generate clean visual plates only. Add all scientific overlays, Korean text, Chinese text, star fields, and data labels later in AfterEffects / Blender / Skyfield.

## Reference Asset Plan

- `@Image1`: Joseon observatory / Gyeongbokgung reconstruction style reference.
- `@Image2`: bronze ganui and armillary instrument material reference.
- `@Image3`: hanji, brush, and historical document texture reference.
- `@Image4`: Bohyeonsan modern observatory reference.
- `@Video1`: preferred slow documentary camera movement reference, if available.
- `@Audio1`: restrained documentary ambience or minimal strings, if using audio reference.

When using references, write: "Reference @Image1 for architecture only", "Reference @Image2 for bronze material only", or "Reference @Video1 for camera rhythm only." Do not let references override the scene content.

---

## Act 0 - Intro

### CLIP 001A - Cut 1 / S00_01 / 12s
Mode: Text-to-Video or use Seoul/Gwanghwamun reference image.

Prompt:
```text
〖Style〗Korean historical science documentary, realistic night cinematography, calm and precise.
〖Duration〗12 seconds
[00:00-00:12] A wide aerial view of Seoul Gwanghwamun Gate at night, with Gyeongbokgung Palace visible behind it. Urban lights glow softly, car light trails move in the distance, and dark building silhouettes sit beyond the palace. Camera makes one slow smooth push-in toward the palace rear garden area, as if searching for the former royal observatory site. Natural city ambience, restrained mood. Avoid shaky camera, fake text, distorted architecture, and tourist crowds.
```

Post notes: Add no historical labels in Seedance.

### CLIP 001B - Cut 1 / S00_01 / 10s
Mode: Extend from 001A if possible.

Prompt:
```text
Continue from @Video1. The same Gwanghwamun and Gyeongbokgung view slowly dissolves backward in time. City lights fade away, roads and modern buildings disappear, and the image becomes 1438 Hanyang at night, quiet and unlit. Camera remains stable and continues the same gentle push-in rhythm. The sky should become dark and open, but leave the star field sparse and generic for later compositing. Maintain solemn documentary realism. Avoid fantasy transformation effects, modern objects, and invented constellations. Duration: 10 seconds.
```

Post notes: Composite verified 1438 star layer afterward.

### CLIP 001C - Cut 1 / S00_01 / 8s
Mode: Text-to-Video.

Prompt:
```text
〖Style〗Quiet scientific documentary plate, minimal motion.
〖Duration〗8 seconds
[00:00-00:08] A dark 1438 Hanyang night-sky plate above the palace garden, almost still, with only a faint natural atmosphere and subtle night air. Camera holds steady in a wide composition with enough clean negative space in the upper left for later data overlay. Do not generate readable text. Do not generate an accurate star map; leave the sky simple for compositing. Avoid random subtitles, glowing symbols, and fantasy Milky Way effects.
```

Post notes: Add JPL Horizons line and exact Vega/Altair/Deneb/Big Dipper layer in post.

### CLIP 002 - Cut 2 / S00_02 / 15s
Prompt:
```text
〖Style〗Macro historical documentary, candlelit hanji texture, restrained.
〖Duration〗15 seconds
[00:00-00:15] A clean scientific computer output screen softly dissolves into hanji paper under candlelight. A Joseon-era astronomy record is being prepared with brush and ink; the brush touches the paper and dark ink slowly spreads into the fibers. Camera makes one slow push-in over the paper surface. Leave the written characters abstract and non-readable for later replacement. Warm candlelight, shallow depth, quiet mood. Avoid fake readable text, warped brush, modern stationery, and random glyphs.
```

Post notes: Overlay actual JPL line, hanja coordinate notation, and "0.05 degree" in AE.

### CLIP 003 - Cut 3 / S00_03 / 13s
Prompt:
```text
〖Style〗Minimal scientific space visualization, black background, elegant restraint.
〖Duration〗13 seconds
[00:00-00:13] A single bright star glows on a pure black background. The point of light breathes very subtly, with a natural atmospheric twinkle, then settles into a steady white point. Camera is locked off. The frame must remain clean with empty space below for later captioning. No additional stars, no nebula, no galaxy, no sci-fi effects. Avoid text generation and excessive lens flare.
```

### CLIP 004 - Cut 4 / S00_04 / 9s
Prompt:
```text
〖Style〗Minimal documentary title plate, black background, restrained Korean broadcast design.
〖Duration〗9 seconds
[00:00-00:09] A clean black title-card background with a very subtle paper-grain texture and a faint cool vignette. No generated text. Camera locked off, no motion except a barely visible fade-in of the background tone. Leave the center empty for later Korean and Chinese title typography. Avoid fake logos, random letters, bright gradients, and decorative particles.
```

Post notes: Add final title in editor.

---

## Act 1 - 1438 Hanyang

### CLIP 005A - Cut 5 / S01_01 / 11s
Prompt:
```text
〖Style〗15th-century Joseon royal observatory reconstruction, realistic documentary, predawn blue light.
〖Duration〗11 seconds
[00:00-00:11] Aerial reveal of the rear garden of Gyeongbokgung Palace before dawn. A royal observatory courtyard appears through low blue mist, surrounded by restrained Joseon architecture. Several bronze astronomical instruments stand in organized positions across the courtyard. Camera makes one slow aerial descent. Keep people absent or tiny silhouettes only. Avoid fantasy architecture, modern lights, invented labels, and excessive palace decoration.
```

### CLIP 005B - Cut 5 / S01_01 / 10s
Prompt:
```text
Continue from @Video1. The camera completes the slow descent into the observatory courtyard, revealing seven distinct bronze astronomical instruments as quiet silhouettes and detailed forms. Predawn wind moves faint mist along the ground. Maintain the same Joseon architecture, blue dawn palette, and documentary realism. Do not generate readable labels; leave space around instruments for later callouts. Avoid warped instruments, modern tripods, glass lenses, and crowds. Duration: 10 seconds.
```

Post notes: Add instrument labels after generation.

### CLIP 006A - Cut 6 / S01_02 / 12s
Prompt:
```text
〖Style〗Documentary infographic background plate, dark scientific design with Korean traditional material accents.
〖Duration〗12 seconds
[00:00-00:12] Seven bronze astronomical instruments appear as clean object silhouettes on a dark textured background, arranged like a data network. Thin golden connector lines slowly draw between them. Camera locked off with a subtle slow push-in. Do not generate readable Korean or Chinese labels; keep all boxes and lines clean for later graphics. Avoid clutter, random text, sci-fi holograms, and neon effects.
```

### CLIP 006B - Cut 6 / S01_02 / 12s
Prompt:
```text
〖Style〗Minimal scientific data-flow animation, dark background, restrained gold accents.
〖Duration〗12 seconds
[00:00-00:12] The instrument silhouettes remain still while simple golden arrows pulse gently from one instrument to the next, suggesting observation data moving through a system. Camera fixed. Leave generous empty space beside each instrument for labels added in post. The motion should be slow and readable, not flashy. Avoid generated text, glowing UI panels, and fantasy symbols.
```

### CLIP 007A - Cut 7 / S01_03 / 9s
Prompt:
```text
〖Style〗Museum-quality macro documentary, bronze material realism, high detail.
〖Duration〗9 seconds
[00:00-00:09] Extreme macro close-up of a 15th-century bronze astronomical ring. Fine engraved degree marks catch warm side light, with slight patina and tiny scratches on the metal. Camera makes a very slow lateral slide across the surface. No readable numbers; leave the marks as physical engravings for later labels. Avoid warped circles, fantasy ornament, and modern machining.
```

### CLIP 007B - Cut 7 / S01_03 / 9s
Prompt:
```text
Continue from @Video1. The camera moves closer to the bronze graduation marks until the engraved divisions fill the frame. The metal surface shows aged Korean craft, hand-polished edges, dust in grooves, and precise circular geometry. Stable macro focus, warm museum light. Do not generate text or numbers. Avoid unstable focus, melted metal, and decorative fantasy symbols. Duration: 9 seconds.
```

### CLIP 008 - Cut 8 / S01_04 / 12s
Prompt:
```text
〖Style〗Clean documentary data-visualization background, dark neutral palette.
〖Duration〗12 seconds
[00:00-00:12] A blank historical-science timeline plate forms on a dark background: a thin horizontal line, three empty marker points, and subtle gold highlight animation. Camera makes a slow push-in. Keep all text areas blank for later labels about Yi Cheon, Tycho Brahe, and Galileo. Avoid generated text, random dates, flashy motion graphics, and sci-fi styling.
```

Post notes: Build precision comparison entirely in AE.

### CLIP 009A - Cut 9 / S01_05 / 10s
Prompt:
```text
〖Style〗Modern scientific computer interface plate, realistic desktop capture look.
〖Duration〗10 seconds
[00:00-00:10] A clean scientific web-tool interface appears on a dark monitor. A cursor moves calmly between blank input fields, suggesting a JPL Horizons query. Camera locked off, slight monitor glow, realistic office darkness. Do not generate readable interface text or exact data. Leave fields clean for later screen replacement. Avoid sci-fi UI, random numbers, and distorted browser elements.
```

### CLIP 009B - Cut 9 / S01_05 / 10s
Prompt:
```text
Continue from @Video1. The same scientific interface shows blank output rows appearing one by one, as if coordinates are being returned. The cursor pauses, then the screen glow reflects faintly on the desk. Maintain fixed camera and realistic monitor look. All text must remain unreadable or blank for later compositing. Avoid fake NASA branding, random equations, and animated holograms. Duration: 10 seconds.
```

### CLIP 009C - Cut 9 / S01_05 / 9s
Prompt:
```text
Continue from @Video1. The monitor output area expands visually, with clean empty rows and a quiet blinking cursor. Camera holds steady. The scene should feel like a real scientific validation workflow, not science fiction. Leave all data to post-production. Avoid generated readable text, invented coordinates, logos, and busy desktop clutter. Duration: 9 seconds.
```

### CLIP 010A - Cut 10 / S01_06 / 13s
Prompt:
```text
〖Style〗Scientific celestial-map visualization plate, dark matte background, precise but text-free.
〖Duration〗13 seconds
[00:00-00:13] A clean stereographic celestial map surface slowly rotates in darkness. Thin coordinate grid lines curve across the sphere with a subtle white glow. A few placeholder points are present but not scientifically specific. Camera fixed on the rotating map. No labels and no readable data. Avoid random constellation drawings, fantasy galaxies, and dense star fields.
```

### CLIP 010B - Cut 10 / S01_06 / 13s
Prompt:
```text
Continue from @Video1. The celestial grid continues its slow rotation, with the dark background breathing softly. Placeholder star points shimmer gently, leaving room for accurate Vega, Altair, and Deneb compositing. The motion must be smooth and scientific. Avoid generated labels, mythological constellation art, and inaccurate crowded sky. Duration: 13 seconds.
```

### CLIP 010C - Cut 10 / S01_06 / 12s
Prompt:
```text
Continue from @Video1. The rotating celestial map eases to a near stop, holding a clean area where the accurate star layer will be added. Subtle atmospheric scintillation only. Keep the design minimal and data-ready. No text, no decorative particles, no invented coordinates. Duration: 12 seconds.
```

### CLIP 011 - Cut 11 / S01_07 / 15s
Prompt:
```text
〖Style〗First-person historical documentary, 1438 Hanyang royal observatory at night.
〖Duration〗15 seconds
[00:00-00:15] First-person point of view from a Joseon astronomer standing on the royal observatory platform at night. The courtyard below is dim, bronze instruments are barely visible, and the camera slowly tilts upward toward an empty dark sky plate. Leave the sky simple for later accurate star compositing. Natural night wind, quiet tension. Avoid visible modern buildings, fake constellations, and exaggerated fantasy moonlight.
```

### CLIP 012A - Cut 12 / S01_08_human / 9s
Prompt:
```text
〖Style〗Intimate historical human drama, candlelit Joseon interior, no face reveal.
〖Duration〗9 seconds
[00:00-00:09] Over-the-shoulder view from behind an elderly Korean Joseon scholar seated beside a water clock in Heumgyeonggak. He wears a white robe and black official hat. His hand holds a measurement paper near a low candle. Camera locked off, respectful distance, face never visible. Avoid readable text, modern furniture, and frontal portrait.
```

### CLIP 012B - Cut 12 / S01_08_human / 9s
Prompt:
```text
Continue from @Video1. The elderly scholar remains seen only from behind. A water droplet falls inside the clock, the candle flickers, and the paper shifts slightly in his hand. The mood is restrained, procedural, and human. Maintain same costume, lighting, and no-face framing. Avoid melodrama, random people, fake readable characters, and modern props. Duration: 9 seconds.
```

### CLIP 013 - Cut 13 / S01_09_human / 15s
Prompt:
```text
〖Style〗Macro historical documentary, tactile realism, candlelit hanji.
〖Duration〗15 seconds
[00:00-00:15] Extreme close-up of an elderly Korean scholar's weathered hand resting on hanji paper. The finger slowly points between two lines of brush-written coordinate records, but the characters remain abstract and non-readable for later replacement. Skin texture, age spots, black ink, and paper fibers are detailed. Camera is fixed macro. Avoid deformed fingers, fake readable text, and modern paper.
```

### CLIP 014A - Cut 14 / S01_10_human / 11s
Prompt:
```text
〖Style〗Macro brush-writing shot, Joseon candlelight, quiet procedural drama.
〖Duration〗11 seconds
[00:00-00:11] A brush tip touches fresh hanji paper and writes a slow black line. Ink spreads naturally into the fibers. The elderly scholar's hand is steady but aged. Camera fixed on the brush tip, shallow depth. Do not generate readable Chinese characters; create only abstract strokes for later replacement. Avoid warped hand anatomy, modern pens, and random text.
```

### CLIP 014B - Cut 14 / S01_10_human / 10s
Prompt:
```text
Continue from @Video1. The brush adds one final line beneath two earlier abstract lines, then pauses above the page. Candlelight flickers softly and the paper texture remains clear. Maintain macro framing and historical realism. No readable text; leave right side clean for later reenactment caption. Avoid excessive ink splashes, distorted fingers, and decorative calligraphy hallucinations. Duration: 10 seconds.
```

### CLIP 015 - Cut 15 / S01_11 / 12s
Prompt:
```text
〖Style〗Predawn Joseon courtyard, restrained silhouette, human presence without face.
〖Duration〗12 seconds
[00:00-00:12] Outside Heumgyeonggak before dawn, a long scholar's shadow stretches across the stone courtyard. Only the shadow and the lower edge of a robe are visible. Mist drifts low, blue predawn light enters from one side. Camera locked in a long shot. Avoid showing the face, modern lighting, fantasy fog, and extra people.
```

### CLIP 016 - Cut 16 / S01_12 / 15s
Prompt:
```text
〖Style〗Historical document scan plate, scholarly documentary, neutral light.
〖Duration〗15 seconds
[00:00-00:15] A close view of an old Joseon historical document texture on a desk, lit evenly like an archive. The page is authentic hanji with faint ink blocks, but no readable generated text. Camera makes a slow push-in toward an empty highlighted area. Leave room for real Sejong Sillok citation and translation in post. Avoid fake readable Chinese, random seals, and modern paper.
```

### CLIP 017A - Cut 17 / S01_13 / 9s
Prompt:
```text
〖Style〗Traditional Korean bookbinding timelapse, candlelit archive realism.
〖Duration〗9 seconds
[00:00-00:09] Hanji sheets stack one by one on a low wooden desk, forming a traditional Joseon book block. Hands align the paper carefully. Camera fixed overhead, warm candlelight, quiet scholarly atmosphere. Leave cover text blank for later title compositing. Avoid readable text, modern binding tools, and unrealistic fast motion.
```

### CLIP 017B - Cut 17 / S01_13 / 9s
Prompt:
```text
Continue from @Video1. The stacked hanji pages are tied into a traditional thread-bound book, then gently placed on a shelf. The blank cover faces camera with clean space for later "Chiljeongsan Naepyeon" text. Maintain warm candlelight and slow timelapse rhythm. Avoid fake characters, modern books, and fantasy glow. Duration: 9 seconds.
```

### CLIP 018 - Cut 18 / S01_14 / 12s
Prompt:
```text
〖Style〗Quiet historical timelapse, traditional archive shelf.
〖Duration〗12 seconds
[00:00-00:12] A thread-bound Joseon astronomy book rests on a wooden shelf as years pass. Dust slowly gathers, light changes from season to season, and the room remains still. Camera locked off. Leave a small clean corner for a later "+12 years" overlay. Avoid readable cover text, insects, decay, and dramatic fantasy effects.
```

### CLIP 019 - Cut 19 / S01_15 / 10s
Prompt:
```text
〖Style〗Scientific night-sky transition plate, calm documentary.
〖Duration〗10 seconds
[00:00-00:10] A dark Joseon night sky slowly pulls back and dissolves toward the surface of a closed traditional astronomy book. The sky contains only simple placeholder stars for later accurate compositing. Camera performs one smooth pull-out. The transition is quiet and elegant. Avoid fake constellations, readable text, galaxy effects, and flashy transitions.
```

### CLIP 020 - Cut 20 / S01_16 / 12s
Prompt:
```text
〖Style〗Macro human insert, candlelit Joseon archive, no face.
〖Duration〗12 seconds
[00:00-00:12] An elderly hand slowly closes a thread-bound classical book. A scholar's shadow briefly crosses the blank cover, then disappears as the candle flickers. Camera fixed macro. The cover must remain clean for later title if needed. Avoid readable text, distorted fingers, modern desk items, and frontal character reveal.
```

### CLIP 021 - Cut 21 / S01_17 / 4s
Prompt:
```text
〖Style〗Minimal black documentary transition plate.
〖Duration〗4 seconds
[00:00-00:04] Pure black background with a very subtle film-grain texture, no generated text. Camera locked off. Leave center clear for later date card. Avoid logos, random letters, and visual noise.
```

### CLIP 022 - Cut 22 / S01_18 / 9s
Prompt:
```text
〖Style〗1456 Hanyang predawn cityscape, realistic Joseon street documentary.
〖Duration〗9 seconds
[00:00-00:09] Aerial view of Hanyang streets under morning mist. Small groups of Joseon citizens step outside and look upward in anticipation before a solar eclipse. Camera makes a slow aerial drift over tiled roofs and narrow streets. Keep faces distant and indistinct. Avoid modern buildings, fantasy crowd behavior, and visible text.
```

---

## Act 2 - 1456 Eclipse

### CLIP 023A - Cut 23 / S02_01 / 9s
Prompt:
```text
〖Style〗Archive document plate, scholarly Korean history documentary.
〖Duration〗9 seconds
[00:00-00:09] A Joseon historical record page lies under neutral archive lighting. Camera slowly pushes in toward a blank highlighted passage area. The paper texture and ink blocks feel authentic, but the text is not readable. Leave space for real Sejo Sillok quote and translation. Avoid random Chinese characters, seals, and modern paper.
```

### CLIP 023B - Cut 23 / S02_01 / 9s
Prompt:
```text
Continue from @Video1. The highlighted area glows subtly while the old page remains still. Camera continues the slow push-in. Maintain scholarly restraint and realistic archive texture. No readable generated text. Avoid fake citations, decorative borders, and excessive motion. Duration: 9 seconds.
```

### CLIP 024A - Cut 24 / S02_02 / 11s
Prompt:
```text
〖Style〗Modern scientific validation interface plate, realistic and text-free.
〖Duration〗11 seconds
[00:00-00:11] A dark monitor shows a clean blank scientific calculation interface. Cursor movement suggests an eclipse query being entered. Camera locked off. Reflections on the desk are subtle. Do not generate readable numbers or NASA text; all data will be composited later. Avoid sci-fi UI, random timestamps, and fake logos.
```

### CLIP 024B - Cut 24 / S02_02 / 11s
Prompt:
```text
Continue from @Video1. The screen changes to a clean split comparison layout with two empty data panels side by side. A small highlight bar moves gently between them. Camera remains fixed and realistic. Leave panels blank for later "JPL" and "Chiljeongsan" timing overlays. Avoid generated text, random data, and animated holograms. Duration: 11 seconds.
```

### CLIP 024C - Cut 24 / S02_02 / 11s
Prompt:
```text
Continue from @Video1. The two blank data panels hold steady while a subtle red highlight space appears between them for later discrepancy annotation. The scene stays quiet, analytical, and realistic. No readable text. Avoid fake clocks, wrong numbers, and flashy UI. Duration: 11 seconds.
```

### CLIP 025A - Cut 25 / S02_03 / 13s
Prompt:
```text
〖Style〗Scientific solar-eclipse simulation plate, realistic sun disk, minimal.
〖Duration〗13 seconds
[00:00-00:13] A clean view of the sun in a muted sky begins a partial eclipse simulation. The moon's dark disk slowly enters from one side. Camera fixed with a very slight push-in. Leave lower corner empty for accurate time stamps added later. Avoid fake text, excessive corona, fantasy sky, and impossible eclipse shapes.
```

### CLIP 025B - Cut 25 / S02_03 / 13s
Prompt:
```text
Continue from @Video1. The partial eclipse deepens gradually, with the moon covering more of the sun. The motion is slow, physically plausible, and documentary. Camera remains stable. Leave clean space for post-production time labels. Avoid dramatic apocalyptic lighting, random clouds blocking the event, and generated numbers. Duration: 13 seconds.
```

### CLIP 025C - Cut 25 / S02_03 / 12s
Prompt:
```text
Continue from @Video1. The partial eclipse reaches the intended visual peak and holds briefly. The sun remains realistic and not fantasy-bright. Camera gently pushes in, then steadies. No text or labels. Avoid total-eclipse corona, lens artifacts, and inaccurate multiple moons. Duration: 12 seconds.
```

### CLIP 026 - Cut 26 / S02_04 / 12s
Prompt:
```text
〖Style〗Backlit Joseon observatory drama, silhouettes only, documentary restraint.
〖Duration〗12 seconds
[00:00-00:12] Joseon court astronomers stand as silhouettes on an observatory floor during the eclipse. They are seen from behind, gathered quietly, looking upward. Strong backlight creates long shadows. Camera locked in a long shot. Faces are never visible. Avoid crowds, modern glasses, fantasy robes, readable text, and exaggerated panic.
```

### CLIP 027A - Cut 27 / S02_05 / 10s
Prompt:
```text
〖Style〗Minimal analytical infographic background, dark documentary palette.
〖Duration〗10 seconds
[00:00-00:10] Two clean abstract process blocks appear on a dark background, connected by a thin line: one for raw observation and one for calendar compilation. Camera fixed with a slow push-in. All text areas remain blank for later Korean labels. Avoid generated text, random charts, neon UI, and clutter.
```

### CLIP 027B - Cut 27 / S02_05 / 10s
Prompt:
```text
Continue from @Video1. The two process blocks separate slightly, emphasizing that measurement and calendar compilation are different stages. A subtle highlight moves from the first block to the second. Keep the motion slow and analytical. No readable text. Avoid sci-fi graphics, fake numbers, and flashy transitions. Duration: 10 seconds.
```

### CLIP 028 - Cut 28 / S02_06 / 15s
Prompt:
```text
〖Style〗Macro Joseon archive revision scene, candlelit, procedural.
〖Duration〗15 seconds
[00:00-00:15] Hands of Joseon astronomers open a thread-bound calendar book, turn pages, and mark careful brush corrections on hanji. Camera fixed macro over the desk. Candlelight flickers, pages move naturally. Text remains abstract and non-readable for later replacement. Avoid modern pens, deformed hands, random readable characters, and dramatic acting.
```

### CLIP 029A - Cut 29 / S02_07 / 11s
Prompt:
```text
〖Style〗Long historical timelapse, archive table, restrained.
〖Duration〗11 seconds
[00:00-00:11] A Joseon calendar book on a wooden table grows thicker as new hanji pages are added in timelapse. Light shifts across years. Camera locked overhead. Leave one side clear for a later year counter. Avoid readable text, modern books, and chaotic paper motion.
```

### CLIP 029B - Cut 29 / S02_07 / 10s
Prompt:
```text
Continue from @Video1. More pages accumulate, the book becomes noticeably thicker, and dust and wear appear subtly on the cover. Brush and page sounds are implied by the action. Maintain the same overhead camera and archive lighting. No generated dates or labels. Avoid fantasy aging effects and random objects. Duration: 10 seconds.
```

### CLIP 030 - Cut 30 / S02_08 / 13s
Prompt:
```text
〖Style〗Clean scientific graph animation plate, restrained documentary.
〖Duration〗13 seconds
[00:00-00:13] A blank line graph appears on a dark neutral background. A single curve gradually descends over time, suggesting decreasing error, but all axis labels and numbers are left blank for later compositing. Camera fixed with subtle push-in. Avoid generated text, fake dates, bright neon colors, and complex clutter.
```

### CLIP 031 - Cut 31 / S02_09 / 7s
Prompt:
```text
〖Style〗Traditional Joseon book transition, candlelit, minimal.
〖Duration〗7 seconds
[00:00-00:07] A thread-bound calendar book closes slowly on a wooden desk. A small blank title plate area remains on the cover for later "Wanli" text overlay. Camera fixed close-up. Candlelight fades slightly. Avoid readable generated characters, modern props, and dramatic smoke.
```

### CLIP 032 - Cut 32 / S02_10 / 4s
Prompt:
```text
〖Style〗Minimal black documentary transition plate.
〖Duration〗4 seconds
[00:00-00:04] Pure black frame with subtle grain, no generated text. Leave center clean for later date card. Avoid logos and random letters.
```

---

## Act 3 - Myeongnyang

### CLIP 033A - Cut 33 / S03_01 / 11s
Prompt:
```text
〖Style〗Korean coastal documentary, predawn blue, realistic tidal force.
〖Duration〗11 seconds
[00:00-00:11] Aerial view of Myeongnyang Strait before sunrise. Dense mist hangs above the narrow waterway, and fast tidal currents twist through the channel. Camera drifts slowly above the water. No people, no ships yet, only landscape and forceful water. Avoid modern boats, bridges, fantasy waves, and over-dramatic storm lighting.
```

### CLIP 033B - Cut 33 / S03_01 / 10s
Prompt:
```text
Continue from @Video1. The aerial camera glides lower over the strait, revealing the current racing between dark island silhouettes. Predawn blue light grows slightly brighter. Maintain realistic Korean coast and natural water physics. Avoid modern structures, visible soldiers, and exaggerated waves. Duration: 10 seconds.
```

### CLIP 034A - Cut 34 / S03_02 / 9s
Prompt:
```text
〖Style〗Historical diary archive plate, scholarly documentary.
〖Duration〗9 seconds
[00:00-00:09] A digital archival view of an old Korean war diary page on dark background, with hanji texture and faint ink blocks. Camera slowly pushes in toward a blank highlighted passage. Text must be non-readable for later real Nanjung Ilgi overlay. Avoid fake Chinese text, modern fonts, and decorative seals.
```

### CLIP 034B - Cut 34 / S03_02 / 9s
Prompt:
```text
Continue from @Video1. The highlight area gently brightens as if marking lines about stars, moon, and tide. Camera remains steady and scholarly. Leave all readable text to post-production. Avoid random calligraphy, fake citations, and excessive glow. Duration: 9 seconds.
```

### CLIP 035A - Cut 35 / S03_03 / 13s
Prompt:
```text
〖Style〗Modern scientific validation interface with map panel, realistic desktop.
〖Duration〗13 seconds
[00:00-00:13] A clean blank scientific interface shows a dark map panel beside empty data fields, suggesting a query for historical moon phase and sunrise. Cursor movement is calm. Camera locked off. All text and numbers are blank for later compositing. Avoid sci-fi holograms, fake NASA text, random coordinates, and cluttered desktop.
```

### CLIP 035B - Cut 35 / S03_03 / 12s
Prompt:
```text
Continue from @Video1. The blank result panel expands and a simple moon-phase placeholder icon appears without labels. The map panel stays clean. Maintain realistic monitor glow and fixed camera. Data will be added later. Avoid generated readable text, wrong moon details, and flashy animations. Duration: 12 seconds.
```

### CLIP 035C - Cut 35 / S03_03 / 12s
Prompt:
```text
Continue from @Video1. The interface holds on a clean split-screen layout: empty data panel, empty map panel, and a quiet cursor pause. The mood is analytical and precise. No readable text or numbers. Avoid logos, sci-fi UI, and random charts. Duration: 12 seconds.
```

### CLIP 036A - Cut 36 / S03_04 / 12s
Prompt:
```text
〖Style〗Data comparison infographic plate, dark background, white and red highlight colors.
〖Duration〗12 seconds
[00:00-00:12] Two blank data columns appear side by side on a dark background, one representing a historical diary and one representing modern calculation. White highlight lines sweep across matching rows. Camera fixed. Leave all text blank for later overlay. Avoid generated numbers, random text, and flashy UI.
```

### CLIP 036B - Cut 36 / S03_04 / 11s
Prompt:
```text
Continue from @Video1. The matching-row highlights settle, and a blank percentage area appears at the bottom for later accuracy annotation. The movement is slow, readable, and restrained. No text generation. Avoid neon colors, fake charts, and complicated icons. Duration: 11 seconds.
```

### CLIP 037A - Cut 37 / S03_05 / 9s
Prompt:
```text
〖Style〗Macro Joseon almanac and tide-table plate, candlelit, realistic.
〖Duration〗9 seconds
[00:00-00:09] Close-up of a Joseon-era almanac page on hanji beside a simple tide-table booklet. Hands gently open the page. Camera fixed macro, warm candlelight, paper fibers clear. Text remains abstract and unreadable for later overlay. Avoid modern maps, printed fonts, and distorted hands.
```

### CLIP 037B - Cut 37 / S03_05 / 9s
Prompt:
```text
Continue from @Video1. The page turns to another blank historical table area, with a brush and small wooden ruler beside it. The scene feels practical, used for navigation and timing. Maintain macro framing and warm light. No readable text. Avoid fantasy props and modern tools. Duration: 9 seconds.
```

### CLIP 038A - Cut 38 / S03_06 / 12s
Prompt:
```text
〖Style〗Scientific tidal-current simulation plate, aerial map-like view.
〖Duration〗12 seconds
[00:00-00:12] A simplified aerial visualization of Myeongnyang Strait shows realistic water movement from above. Subtle arrow placeholders begin to form over the current paths, but no labels appear. Camera locked overhead. The water physics should feel strong and natural. Avoid modern map text, satellite labels, fantasy whirlpools, and unrealistic waves.
```

### CLIP 038B - Cut 38 / S03_06 / 11s
Prompt:
```text
Continue from @Video1. The tidal arrows slowly change direction, showing a time-compressed current reversal. Camera remains overhead and stable. Leave all time labels and KHOA data to post-production. Avoid generated text, wrong map labels, and flashy colors. Duration: 11 seconds.
```

### CLIP 039 - Cut 39 / S03_07_human / 15s
Prompt:
```text
〖Style〗Memory insert, 1438 candlelit macro, soft faded contrast.
〖Duration〗15 seconds
[00:00-00:15] Flashback to the elderly Joseon scholar's hand writing an average measurement on hanji. Only hand, brush, ink, and paper are visible. The black ink spreads slowly. Camera fixed macro, candlelight softened like memory. Text must remain non-readable for later replacement. Avoid face reveal, warped fingers, modern objects, and random characters.
```

### CLIP 040 - Cut 40 / S03_08_human / 15s
Prompt:
```text
〖Style〗Myeongnyang dawn silhouette, restrained war documentary without battle.
〖Duration〗15 seconds
[00:00-00:15] Cut back to 1597 Myeongnyang at dawn. A single dark ship silhouette appears on the turbulent current, distant and quiet. No figures are visible. Camera holds a long shot from shore level while mist moves across the water. Avoid battle action, modern ships, flags with readable symbols, and heroic close-ups.
```

### CLIP 041 - Cut 41 / S03_09 / 15s
Prompt:
```text
〖Style〗Conceptual typography background plate, Korean documentary graphic design.
〖Duration〗15 seconds
[00:00-00:15] A single abstract ink-brush form inspired by the Chinese character for time slowly transforms on a dark hanji-textured background. The movement suggests measurement becoming action. Do not generate readable text; leave the final typography to post. Camera locked off. Avoid random characters, neon effects, and decorative fantasy particles.
```

### CLIP 042 - Cut 42 / S03_10 / 13s
Prompt:
```text
〖Style〗Scientific globe transition, restrained documentary, dark space background.
〖Duration〗13 seconds
[00:00-00:13] A realistic globe rotates smoothly from the Korean peninsula toward central Europe. The earth is softly lit, with no readable map labels. Camera performs one slow orbit with the globe. The motion is calm and educational. Avoid country text, glowing borders, satellite clutter, and sci-fi interface effects.
```

### CLIP 043 - Cut 43 / S03_11 / 4s
Prompt:
```text
〖Style〗Minimal black documentary transition plate.
〖Duration〗4 seconds
[00:00-00:04] Pure black frame with subtle grain, no generated text. Leave center clean for later "1604" date card. Avoid logos and random letters.
```

### CLIP 044 - Cut 44 / S03_12 / 6s
Prompt:
```text
〖Style〗Minimal space silence before discovery.
〖Duration〗6 seconds
[00:00-00:06] A single dim star sits in a pure black frame, almost motionless. The darkness feels still, as if just before a sudden astronomical event. Camera locked off. No other stars, no nebula, no text, no flare. Avoid fantasy explosion effects in this clip.
```

### CLIP 045 - Cut 45 / S03_13 / 4s
Prompt:
```text
〖Style〗Minimal black transition counter plate.
〖Duration〗4 seconds
[00:00-00:04] Dark background with subtle grain and a faint horizontal guide line, no generated text. Leave center clean for a later year counter overlay. Avoid random letters, logos, and decorative motion.
```

### CLIP 046 - Cut 46 / S03_14 / 9s
Prompt:
```text
〖Style〗Geographic pull-out transition, Korean coast to globe, documentary.
〖Duration〗9 seconds
[00:00-00:09] The camera pulls out from Myeongnyang Strait at dawn until the waterway becomes a small point on the Korean peninsula. The movement is smooth and restrained. No labels or text. Avoid modern satellite UI, clouds covering the location, and fantasy zoom effects.
```

---

## Act 4 - 1604 Supernova

### CLIP 047A - Cut 47 / S04_01 / 12s
Prompt:
```text
〖Style〗Scientific supernova visualization, dark sky, restrained realism.
〖Duration〗12 seconds
[00:00-00:12] A sparse dark star field holds still. One small star-like point gradually brightens with a sudden but elegant increase in intensity, suggesting SN 1604 appearing in Ophiuchus. Camera locked off. Keep the surrounding sky simple for accurate overlay later. Avoid fantasy nebula, colorful explosions, and random constellation lines.
```

### CLIP 047B - Cut 47 / S04_01 / 11s
Prompt:
```text
Continue from @Video1. The bright point expands into a subtle scientific glow, then stabilizes as a new star in the dark field. The effect is restrained and astronomical, not cinematic destruction. Camera remains fixed. No labels or text. Avoid fireball effects, shockwave planets, and inaccurate dense sky. Duration: 11 seconds.
```

### CLIP 048A - Cut 48 / S04_02 / 9s
Prompt:
```text
〖Style〗Early modern European astronomical engraving archive plate.
〖Duration〗9 seconds
[00:00-00:09] A classical 17th-century astronomical diagram page lies under archive lighting. Engraved circles and star-chart textures are visible, but no readable generated text. Camera slowly pushes in toward a blank diagram area for later Kepler source compositing. Avoid fake Latin text, modern fonts, and ornate fantasy borders.
```

### CLIP 048B - Cut 48 / S04_02 / 9s
Prompt:
```text
Continue from @Video1. The camera pushes closer to the diagram texture and aged paper fibers. A faint highlight circle appears where the supernova location will be added in post. Maintain archive realism. No readable text or invented labels. Avoid random symbols and modern scan artifacts. Duration: 9 seconds.
```

### CLIP 049A - Cut 49 / S04_03 / 9s
Prompt:
```text
〖Style〗Joseon historical record archive plate, neutral scholarly lighting.
〖Duration〗9 seconds
[00:00-00:09] A Joseon annals page rests flat under archive lighting. The page has aged hanji texture and dark ink blocks, but no readable generated Chinese text. Camera slowly pushes in toward a blank highlighted passage. Leave room for the real Seonjo Sillok guest-star record. Avoid fake citations, random seals, and modern paper.
```

### CLIP 049B - Cut 49 / S04_03 / 9s
Prompt:
```text
Continue from @Video1. The highlighted passage area gently brightens while the page remains still. The mood is scholarly and restrained. No generated text. Avoid decorative glow, random characters, and modern document UI. Duration: 9 seconds.
```

### CLIP 050A - Cut 50 / S04_04 / 11s
Prompt:
```text
〖Style〗Celestial coordinate overlay background, scientific and clean.
〖Duration〗11 seconds
[00:00-00:11] A dark stereographic celestial coordinate grid appears, with two empty point markers slowly fading in. Camera makes a subtle push-in. The grid is clean and text-free for later Kepler and Joseon coordinate labels. Avoid random star names, constellation drawings, and sci-fi hologram styling.
```

### CLIP 050B - Cut 50 / S04_04 / 11s
Prompt:
```text
Continue from @Video1. The two empty point markers move slightly closer together on the coordinate grid, implying agreement between records. Camera continues a restrained push-in. No labels or numbers. Avoid generated text, colorful fantasy stars, and complex clutter. Duration: 11 seconds.
```

### CLIP 050C - Cut 50 / S04_04 / 11s
Prompt:
```text
Continue from @Video1. The two markers settle nearly together and hold, leaving clean space for a later numerical agreement annotation. The grid remains dark and precise. No text generation. Avoid inaccurate dense star fields and flashy transitions. Duration: 11 seconds.
```

### CLIP 051A - Cut 51 / S04_05 / 13s
Prompt:
```text
〖Style〗Modern astrophysics data comparison interface, realistic monitor plate.
〖Duration〗13 seconds
[00:00-00:13] A clean dark monitor interface shows three blank comparison panels: modern astrophysics data, Kepler record, and Joseon record. Camera locked off. Empty rows and subtle divider lines appear. Leave all coordinates and text to post-production. Avoid fake readable numbers, sci-fi UI, and random equations.
```

### CLIP 051B - Cut 51 / S04_05 / 12s
Prompt:
```text
Continue from @Video1. A blank coordinate chart expands beside the three panels, with one clean highlighted point. The mood is precise and modern. Camera remains fixed. No generated text or numbers. Avoid logos, fake NASA data, and neon effects. Duration: 12 seconds.
```

### CLIP 052 - Cut 52 / S04_06 / 15s
Prompt:
```text
〖Style〗Prague 1604 scholar study, candlelit early modern realism, silhouette only.
〖Duration〗15 seconds
[00:00-00:15] A 1604 Prague study room at night. A scholar's silhouette stands near a desk with star charts, a quadrant instrument, papers, and candles. There is no telescope. Camera locked in a long shot from the doorway. The figure remains anonymous. Avoid readable text, modern telescope, fantasy alchemy props, and frontal face close-up.
```

### CLIP 053 - Cut 53 / S04_07 / 15s
Prompt:
```text
〖Style〗Hanyang 1604 royal astronomy office, candlelit Joseon realism, silhouettes.
〖Duration〗15 seconds
[00:00-00:15] Joseon astronomers in a Hanyang observatory use a bronze quadrant-like measuring instrument while looking toward the night sky. They are silhouettes only, seen from behind. Camera holds a long shot with warm candlelight and dark blue night beyond. No telescope. Avoid modern optics, readable labels, fantasy robes, and visible faces.
```

### CLIP 054A - Cut 54 / S04_08 / 9s
Prompt:
```text
〖Style〗Parallel-history split-screen plate, restrained documentary.
〖Duration〗9 seconds
[00:00-00:09] Split screen: left side a candlelit Prague scholar study, right side a candlelit Hanyang observatory. Both are quiet, both show silhouettes and astronomical instruments, both have a dark window area for the same star overlay. Camera is locked. No generated text. Avoid mismatched styles, modern objects, and readable labels.
```

### CLIP 054B - Cut 54 / S04_08 / 9s
Prompt:
```text
Continue from @Video1. The split screen holds while both silhouettes look upward at the same moment. The lighting and pacing remain parallel, calm, and scientific. Leave center empty for later "same star" text. Avoid face reveals, random characters, and extra motion. Duration: 9 seconds.
```

### CLIP 055 - Cut 55 / S04_09 / 13s
Prompt:
```text
〖Style〗Minimal historical timeline graphic background, dark paper texture.
〖Duration〗13 seconds
[00:00-00:13] A clean timeline line forms from left to right on a dark textured background, with two blank milestone points and a restrained gold highlight. Camera locked off with subtle push-in. Leave all dates and text blank for post. Avoid generated numbers, neon, and complex icons.
```

### CLIP 056 - Cut 56 / S04_10 / 10s
Prompt:
```text
〖Style〗Scientific star-fade visualization, minimal black sky.
〖Duration〗10 seconds
[00:00-00:10] A bright star-like point in a sparse black sky slowly dims until it becomes barely visible. Camera locked off. The fade is quiet and realistic, suggesting SN 1604 disappearing over time. No labels, no constellation lines, no nebula. Avoid dramatic explosion, colorful particles, and generated text.
```

### CLIP 057 - Cut 57 / S04_11 / 6s
Prompt:
```text
〖Style〗Minimal black transition plate, restrained documentary.
〖Duration〗6 seconds
[00:00-00:06] Pure black frame with subtle film grain and a faint center glow that slowly fades. No generated text. Leave center clear for later "1604 to 2026" counter. Avoid logos, random letters, and decorative particles.
```

---

## Act 5 - 2026 Verification

### CLIP 058 - Cut 58 / S05_01 / 15s
Prompt:
```text
〖Style〗Modern Korean observatory documentary, realistic night operation.
〖Duration〗15 seconds
[00:00-00:15] A modern 1.8-meter class telescope inside a large observatory dome operates at night. The dome slit is open to a dark sky, and the telescope rotates slowly with quiet motor movement. Camera holds a long shot from inside the dome. Cool scientific lighting, metal surfaces, calm precision. Avoid fake logos, sci-fi design, people posing, and over-bright stars.
```

### CLIP 059 - Cut 59 / S05_02 / 15s
Prompt:
```text
〖Style〗Parallel scientific history split-screen, documentary realism.
〖Duration〗15 seconds
[00:00-00:15] Split screen: left shows a 1438 Joseon observatory courtyard with bronze instruments at night; right shows a 2026 modern Korean telescope dome. Both sides are calm, stable, and visually parallel, emphasizing the same function across time. Camera locked. Leave lower third blank for later bilingual labels. Avoid generated text, modern objects on Joseon side, and fantasy lighting.
```

### CLIP 060A - Cut 60 / S05_03 / 14s
Prompt:
```text
〖Style〗Modern scientific multi-query interface plate, realistic desktop.
〖Duration〗14 seconds
[00:00-00:14] A dark monitor shows a clean blank multi-query interface divided into four empty rows. A cursor moves calmly down the rows, suggesting four historical events being entered. Camera locked off, realistic monitor glow. All text and data must be blank for later compositing. Avoid fake NASA data, random numbers, and sci-fi UI.
```

### CLIP 060B - Cut 60 / S05_03 / 14s
Prompt:
```text
Continue from @Video1. Four blank output panels appear beside the query rows. Each panel receives a subtle highlight, one after another, like validated results arriving. Camera remains fixed. Leave all event names and coordinates to post-production. Avoid generated text, fake logos, and neon interface effects. Duration: 14 seconds.
```

### CLIP 060C - Cut 60 / S05_03 / 14s
Prompt:
```text
Continue from @Video1. The four blank output panels hold together in a final verification layout. A subtle white outline connects them, suggesting one complete validation sequence. Camera locked, analytical mood. No readable text or numbers. Avoid random charts, sci-fi holograms, and clutter. Duration: 14 seconds.
```

### CLIP 061A - Cut 61 / S05_04 / 11s
Prompt:
```text
〖Style〗Scientific celestial map plate, dark clean background, restrained color points.
〖Duration〗11 seconds
[00:00-00:11] A stereographic celestial map slowly rotates on a dark background. Four blank colored point placeholders appear: white, yellow, blue, and red. No labels or coordinate text. Camera fixed on the rotating map. The design is clean for later accurate overlay. Avoid random star names, constellation art, and dense fantasy sky.
```

### CLIP 061B - Cut 61 / S05_04 / 11s
Prompt:
```text
Continue from @Video1. The four colored points remain in place as the celestial map rotates slowly, implying four historical coordinates on one sky. Motion is smooth and scientific. Leave all labels to post-production. Avoid generated text, inaccurate star clusters, and flashy effects. Duration: 11 seconds.
```

### CLIP 061C - Cut 61 / S05_04 / 11s
Prompt:
```text
Continue from @Video1. The rotating celestial map eases to a stable final position with four colored points visible. The background stays dark and minimal. No labels, no numbers, no constellation drawings. Avoid jitter and fantasy glow. Duration: 11 seconds.
```

### CLIP 062 - Cut 62 / S05_05 / 12s
Prompt:
```text
〖Style〗Final memory insert, candlelit 1438 macro, soft fade.
〖Duration〗12 seconds
[00:00-00:12] The elderly Joseon scholar's hand writes two abstract lines on hanji paper, then fades gently toward darkness. Only the hand, brush, ink, and paper are visible. Camera fixed macro, warm candlelight, quiet human presence. No readable text. Avoid face reveal, warped fingers, modern objects, and melodrama.
```

### CLIP 063 - Cut 63 / S05_06 / 9s
Prompt:
```text
〖Style〗Modern telescope mirror close-up, scientific elegance.
〖Duration〗9 seconds
[00:00-00:09] Close-up of a modern telescope mirror catching a faint point of starlight. The mirror surface reflects cool blue highlights as the telescope moves almost imperceptibly. Camera fixed macro, clean and precise. Avoid sci-fi glow, fingerprints, random text, and exaggerated lens flare.
```

### CLIP 064 - Cut 64 / S05_07 / 7s
Prompt:
```text
〖Style〗Brief Myeongnyang memory insert, dawn silhouette.
〖Duration〗7 seconds
[00:00-00:07] A single ship silhouette briefly appears on the turbulent Myeongnyang current at dawn, then fades back into mist. No people are visible. Camera holds a distant long shot. Avoid battle action, modern ships, readable flags, and heroic close-up.
```

### CLIP 065A - Cut 65 / S05_08 / 10s
Prompt:
```text
〖Style〗Celestial convergence visualization, scientific and minimal.
〖Duration〗10 seconds
[00:00-00:10] Four colored points on a dark celestial sphere begin moving very slowly toward the center. The sphere grid is subtle and clean. Camera performs one slow push-in. No labels or text. Avoid random star maps, neon trails, and flashy particles.
```

### CLIP 065B - Cut 65 / S05_08 / 9s
Prompt:
```text
Continue from @Video1. The four points continue converging toward one central point, leaving faint restrained trails. The motion is smooth and precise, like a scientific diagram becoming a conclusion. Camera continues the slow push-in. No text. Avoid jitter, fantasy effects, and clutter. Duration: 9 seconds.
```

### CLIP 065C - Cut 65 / S05_08 / 9s
Prompt:
```text
Continue from @Video1. The four points meet at one clean white point and hold in the center of the frame. Leave space beside it for the later Korean phrase "600 years of procedure." Camera steadies. No generated text. Avoid explosion, lens flare, and random symbols. Duration: 9 seconds.
```

### CLIP 066 - Cut 66 / S05_09 / 12s
Prompt:
```text
〖Style〗Joseon water-clock bell macro, final quiet resonance.
〖Duration〗12 seconds
[00:00-00:12] Close-up of a small bronze bell from a Joseon water clock. The bell is struck once, vibrating subtly as candlelight flickers across aged metal. Camera fixed macro. The motion is minimal and tactile, ending in quiet stillness. Avoid fantasy ornament, modern bell stand, readable labels, and exaggerated sparks.
```

### CLIP 067 - Cut 67 / S05_10 / 4s
Prompt:
```text
〖Style〗Minimal black final transition plate.
〖Duration〗4 seconds
[00:00-00:04] Pure black frame with subtle grain, no generated text. Leave center clean for final date range typography. Avoid logos and random letters.
```

### CLIP 068A - Cut 68 / S05_11 / 10s
Prompt:
```text
〖Style〗Clean documentary credits background plate, black, restrained.
〖Duration〗10 seconds
[00:00-00:10] A pure black credits background with subtle film grain and a faint vertical scroll guide feeling, but no generated text. Camera locked off. Leave the whole frame clean for actual source credits in post. Avoid random letters, logos, and decorative effects.
```

### CLIP 068B - Cut 68 / S05_11 / 9s
Prompt:
```text
Continue from @Video1. The black credits background remains stable and clean, with only subtle grain and a faint fade toward silence. No text generation. Leave all credits to post-production. Avoid logos, random letters, and noise. Duration: 9 seconds.
```

### CLIP 069 - Cut 69 / S05_12 / 4s
Prompt:
```text
〖Style〗Clean broadcaster end-card background plate.
〖Duration〗4 seconds
[00:00-00:04] A simple dark end-card background, no generated logo or text. Very subtle fade-out. Leave center clean for the real EBS logo added in post. Avoid fake logos, random letters, and decorative particles.
```

### CLIP 070 - Cut 70 / S05_13 / 4s
Prompt:
```text
〖Style〗Final silence, black screen.
〖Duration〗4 seconds
[00:00-00:04] Pure black frame, no generated text, no logo, no motion except barely visible grain fading to complete black. This is the final silence after the bell resonance. Avoid visual noise, letters, and flicker.
```

---

## Production Notes

1. Generate Seedance clips as clean plates first, then add verified science layers in post.
2. For any extension prompt, upload the previous accepted output as `@Video1` and begin with `Continue from @Video1`.
3. Keep Joseon faces hidden unless a separate character reference and face-consistency workflow is prepared.
4. For scientific sky shots, Seedance should create mood and camera only. Exact stars come from Blender/Skyfield.
5. For archive/document shots, Seedance should create paper, light, hand, and camera only. Real source text comes from scans or AE typography.
