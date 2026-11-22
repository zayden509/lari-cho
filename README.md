# Lari Cho

Yon jwèt monn ouvè 3D nan yon vil ayisyen, ki mache nan navigatè sou telefòn ak òdinatè.

## Kijan pou jwe

Louvri `index.html` nan yon navigatè, oswa ale sou paj GitHub Pages pwojè a.

- **Telefòn:** pous goch pou mache oswa kondui, glise pous dwat pou gade, bouton MONTE/DESANN pou machin yo.
- **Òdinatè:** WASD pou mache, sourit pou gade, F pou monte/desann, Shift pou kouri, Espas pou sote, H pou klakson.

## Sa ki nan jwèt la

- Vil ak kay koulè, galri, tank dlo, poto kouran, pye kokoye, ak mòn dèyè vil la.
- Komisarya ak blende PNH, blende gri ak pickup lapolis.
- Taptap, sedan ak SUV ou ka kondui.
- Machann, timoun, moun nan lari a, ak yon geto ak gang.
- Misyon livrezon ak lapolis ki kouri dèyè w.

## Mòd anliy

Mòd anliy lan (jwe ak lòt moun, chat, mikwo) mache sèlman lè jwèt la louvri sou claude.ai. Sou GitHub Pages, jwèt la mache pou yon sèl jwè.

## Modèl 3D

Gade [modeles/README.md](modeles/README.md) pou kote pou mete modèl 3D reyalis yo.

## Kijan jwèt la mache (achitekti)

Tout kòd la nan `index.html`, separe an modil ak kòmantè `/* ===== ... ===== */`:

| Modil | Sa l fè |
|---|---|
| **Locomotion** (`playerUpdate`, `LOCO`) | Vitès ak momantòm: akselerasyon, frennen, vire ak inèsi, kouri ak estamina, bese (C), sote ak "coyote time" ak "jump buffer", glise sou mi |
| **Vitals** (`vitals`, `hurt`, `wasted`) | Sante, domaj (machin, gang), rejenerasyon, reaparisyon |
| **Camera** (`placeCam`, `CAM`, `sdamp`) | Kamera twazyèm moun ak resò amòti, kolizyon reyon-bwat, FOV dinamik, souke kamera |
| **HUD** (`hud`, `drawMap`) | Minimap ki vire ak zoom, ba sante/estamina, "prompt" kontekstyèl, vinyèt domaj |
| **Houses & Interiors** (`house`, `katye`) | 4 kay ou ka antre (salon, chanm, kizin), pòt ak charnyè, mi ak kolizyon |
| **Interaction** (`INTER`, `findFocus`) | Yon sèl bouton **E** pou tout bagay: pòt, televizyon, radyo, limyè, frijidè, kabann, machin |
| **Residents** (`residentUpdate`) | Moun ki rete nan kay yo: mache nan chanm yo, louvri pòt, soti, fèmen pòt dèyè yo |

Pou ajoute yon nouvo objè: `INTER.push({house:H, x, z, r:1.2, label:()=>'...', act:()=>{...}})`.

## Kredi

- Modèl 3D blende nwa a: [[Free] Armored Police Vehicle](https://sketchfab.com/3d-models/free-armored-police-vehicle-9aea4465dc974c728b6167eac5ffd22e) pa Roam_Man sou Sketchfab, lisans [CC BY 4.0](http://creativecommons.org/licenses/by/4.0/). Nou redwi tekstil yo pou jwèt la ka mache sou telefòn.
