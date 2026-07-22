# Digital Product Constraints

Use this reference for small electronics, IP-style accessories, packaging, SKU sets, white-background images, main images, scene composites, and product-structure QA.

## Table Of Contents

- Product Truth
- Product DNA Template
- Source Priority
- Hard Structure Locks
- Engineering Logic
- Materials And Surface Artwork
- Lens, Lighting, And Scale
- Category Rules
- Packaging Rules
- IP Surface Artwork And Brand Text
- Image-Type Rules
- Prompt Blocks
- Failure Checklist

## Product Truth

Treat the subject as an existing engineered product, not a concept design. Preserve shape, proportions, thickness, roundness, ports, buttons, holes, screen, indicator lights, line paths, joints, hinges, stand structure, package shape, and print-area placement.

Allow visual changes only when they do not alter the product:

- Background, scene, props, and color atmosphere.
- Lighting direction and shadow softness.
- Camera angle within plausible product-photography limits.
- Overall scale and position in the canvas.
- Rendering polish, material clarity, and depth of field.

Forbid product changes:

- Redesigning the body, changing thickness, reshaping corners, or changing curve relationships.
- Moving, copying, deleting, or swapping ports, buttons, holes, screens, lights, lines, hinges, stands, nozzles, handles, vents, or package faces.
- Adding extra screens, buttons, ports, LEDs, screws, logos, accessories, labels, or fake functions.
- Removing real cables, straps, plugs, rings, stands, hooks, fan guards, lamp shades, nozzles, or package/accessory items.
- Hiding structure errors with glow, blur, props, shadow, reflection, or cropping.

## Product DNA Template

Fill this before image generation or detail-page planning:

```text
Product name:
Category:
Brand/model:
Real colors/SKUs:
Output platform and size:
Overall silhouette:
Length-width-thickness / height-width-depth relationship:
Corner radius and edge curvature:
Front structure:
Back structure:
Top structure:
Bottom structure:
Left-side structure:
Right-side structure:
Ports: count, type, and position:
Buttons/switches: count and position:
Screen/indicator/lighting position:
Holes/vents/grilles:
Lines/cables/plugs/straps:
Hinges/joints/stands/claws/supports:
Logo/pattern/artwork placement:
Material zones:
Color zones:
Packaging type and visible faces:
Accessories:
Confirmed parameters and source:
Unknown parameters:
Most likely structure mistakes:
Prohibited claims or words:
```

If a field is unknown, write `unknown` or `以实际参数为准`. Do not infer exact structure or exact parameters.

## Source Priority

Use this order when sources conflict:

1. Latest explicit user correction.
2. Six-view, CAD, or engineering structure reference.
3. Product real photo.
4. Manual, specification sheet, or package structure source.
5. Package or artwork file for print placement only.
6. Style reference for mood only.
7. AI inference for scene and layout only.

Six-view structure beats perspective beauty. Product hardware beats decorative artwork. Real parameters beat selling copy. If uncertain, reduce creativity and follow the most literal reference.

## Hard Structure Locks

Lock these when present:

- Outer silhouette, main body proportions, thickness, corner radius, curvature, seams, shell edge thickness, and face orientation.
- Front, back, top, bottom, left, and right relationships.
- Screen, digital display, indicator light, light strip, touch area, logo, surface pattern, decorative area, material zones, and color zones.
- USB-C, USB-A, Lightning, Micro USB, AC plug, audio port, charging contact, or other port type and position.
- Power button, function key, volume key, gear switch, slider, latch, and toggle position.
- Speaker mesh, sound holes, microphone holes, vents, air inlets, air outlets, heat holes, fan guard, lamp shade, and grilles.
- Cable, cable groove, plug, storage slot, strap, metal buckle, fixed base, and connector path.
- Hinge, support arm, clamp, base, anti-slip pad, folding structure, rotation joint, and support contact.
- Fan blades, guard, center cap, handle, base, rotation shaft.
- Blow-dryer barrel, handle, nozzle, inlet, outlet, buttons, indicator, power cord.
- Package type, six-face layout, package ratio, official artwork area, and post-production text area.

## Engineering Logic

All parts must look physically attached and mechanically plausible:

- Ports sit inside real openings, not floating on the surface.
- Screens, displays, and touch areas are embedded or flush with the shell.
- Buttons have thickness, boundary, and travel; they are not flat printed icons.
- Cables have real diameter, natural bend radius, and fixed endpoints.
- Hinges carry rotation; stands, clamps, case lids, fan heads, and lamp bodies must not float.
- Support products show center of gravity, contact area, anti-slip pads, and load-bearing relation.
- Packaging stays a real paper box, blister, bag, or gift box rather than changing shape for beauty.

## Materials And Surface Artwork

Render real material behavior from the source: matte plastic, glossy plastic, silicone, metal, fabric, glass, transparent parts, painted shell, mesh, or rubber.

Surface patterns are printed artwork or official stickers unless the product physically has raised parts. Keep artwork on the specified surface. Do not let it cross screens, ports, grooves, hinges, package folds, or hardware seams.

Do not let AI redraw official small text, authorization marks, barcodes, anti-counterfeit labels, manufacturer details, certification marks, copyright lines, or trademarks. Reserve clean areas for later compositing with official files.

## IP Surface Artwork And Brand Text

For IP products, preserve supplied or visible artwork as part of the product surface. Lock its print area, scale, orientation, color, and boundary. Do not move artwork across seams, screens, ports, grooves, hinges, cable slots, package folds, or hardware structure.

Do not invent new characters, logos, slogans, authorization text, brand partnerships, copyright lines, barcodes, official labels, or manufacturer copy. Do not imitate official wordmarks or require commercial fonts. When typography is needed, use generic safe directions such as clean rounded sans-serif, simple bold sans-serif, or soft generic handwritten-style text.

## Lens, Lighting, And Scale

Use stable product-photography lens language:

- Main image: 50-70mm.
- White-background image: around 70mm.
- Detail page: 35-50mm.
- Scene image: 35-50mm.
- Macro detail: 70-100mm.

Avoid fisheye, ultra-wide distortion, extreme perspective, exaggerated near-far scale, excessive macro distortion, cropped critical edges, and covered ports.

Use one lighting system across a set:

- Left-front 45-degree soft light by default.
- Soft shadow, clean highlight, readable edges, low-to-medium contrast.
- Consistent light direction, shadow direction, highlight position, reflection strength, saturation, and sharpness.

Scale rules:

- White-background: product occupies 75%-85%.
- Main selling image: 60%-70%.
- Detail-page hero: 50%-65%.
- Function page: 45%-60%.
- Detail close-up: local product detail occupies 60%-80%.
- Scene image: product occupies 35%-50%.
- SKU image: product occupies 55%-65%.
- Collection image: same product scale across all variants.

## Category Rules

Use category buyer concerns to guide selling-point selection, but keep exact claims source-backed. Visible structure can support soft claims; exact performance numbers require a reliable source.

### Earphones And Headphones

Lock left-right mirrored parts, earbud/earstem/earhook/earclip/headband/earcup structure, charging-case ratio, opening direction, hinge, screen, lights, port, internal slots, and contact points. Do not turn open-ear earphones into in-ear silicone earbuds, semi-in-ear earbuds into silicone-tip earbuds, or generate two same-side earbuds.

Buyer-angle selling points may include shape/style, IP appearance, wearing comfort, sound quality impression, battery/endurance, charging-case storage, connection/use convenience, portability, and giftability. Treat exact sound performance, noise cancellation, Bluetooth version, battery hours, waterproof level, codec, latency, and driver size as unknown unless supplied.

For hero and SKU scenes, earphones can use a polished 3D/cartoon-rendered ecommerce scene rather than a heavy model scene. Use case + earbuds as the main subject, with the earbuds close to the case and arranged through height, scale, front/back depth, and staggered placement. If multiple colors appear together, keep matching earbuds near their own case and use product positions to guide the eye, not drawn guide lines. Use hand/model scenes later only when proving wearing, holding, or packing.

### Power Banks

Lock body ratio, screen, ports, buttons, built-in cable, cable slot, strap, plug, protective cap, magnetic ring, and packaging. Do not mix USB-A, USB-C, Lightning, Micro USB, or AC plug types. Do not delete built-in cables or merge multiple lines. Do not invent capacity, power, protocols, airline approval, temperature-control chip, or certification.

Buyer-angle selling points may include appearance/IP style, capacity/endurance when sourced, charging convenience, cable/port layout, screen or indicator clarity, pocket/bag portability, compatibility, travel use, giftability, and safety/protection when sourced.

For hero scenes, power banks normally use a product-led rendered ecommerce scene: desk charging, pouch/backpack, pedestal, package, or travel-prop setup. A model should not dominate unless proving hand scale, charging, or packing. Keep ports, cables, screens, and built-in lines visible.

### Bluetooth Speakers

Lock body shape, speaker mesh, passive radiator, buttons, port cover, handle, strap, light strip, and base. Soundwave effects must not cover structure. Do not invent power, waterproof level, battery life, speaker-unit count, or Bluetooth version.

Buyer-angle selling points may include appearance/IP style, sound impression, battery/endurance when sourced, room/desktop atmosphere, portability, controls, gifting, and scenario fit.

### Cables

Lock connector type, metal shell, plastic shell, strain relief, line diameter, braided texture, magnetic tip, telescopic structure, and storage form. Bent cables must keep a constant diameter. Do not invent length, charging power, transfer speed, chip certification, or bend-test count.

### Chargers And Adapters

Lock plug standard, foldable plug, port count, port layout, shell proportion, certification-label position, and desktop/portable form. Do not mix CN/US/EU/UK plug forms. Do not invent GaN, PD, QC, PPS, wattage, certification, or compatibility.

### Stands

Lock base, arm, hinge, clamp, tray, anti-slip pad, magnetic ring, folding relation, and real support contact. Angle adjustment must follow the real joint. Do not show impossible floating states. Do not invent load-bearing capacity, rotation angle, device compatibility size, or material strength.

For hero scenes, stands normally use a product-led rendered ecommerce scene with phone/tablet relation, desk surface, support angle, and stable contact proof. Avoid model-heavy scenes unless the hand is operating, folding, or placing the stand. Product support logic must be more important than decorative lifestyle styling.

### Desk Fans And Handheld Fans

Lock fan type, blade count, blade shape, guard grille, center cap, handle, base, button, charge port, hinge, and strap hole. Handheld fan and hand scale must be realistic; desk fans need stable base and support. Do not invent speed gears, battery capacity, runtime, noise value, cooling effect, or safety certification.

### Tap Lamps And Desk Lamps

Lock body form, shade, base, touch area, emitting area, charge port, and switch. Glow must reveal the lamp, not hide it. Do not invent color temperature, brightness, battery life, eye-protection certification, timer, or waterproof level.

### Blow Dryers

Lock barrel, handle, inlet, outlet, nozzle, buttons, indicator, fold joint, power cord, dock, and real accessories. Handheld use must preserve hand-to-handle scale. Do not change the folding direction, nozzle attachment logic, air inlet grille, button position, or handle/barrel proportion. Do not stretch the barrel or turn it into a toy shape. Do not invent negative-ion, temperature-control, wattage, RPM, noise, hair-care certification, or safety certification.

Buyer-angle selling points may include appearance/IP style, wind strength impression, drying efficiency, hair-care comfort, temperature control when sourced, foldable storage, travel portability, grip comfort, noise impression, nozzle/accessory use, and giftability. Do not invent wattage, negative ions, temperature numbers, noise decibels, safety certification, or motor speed without a source.

For screen 01, blow dryers are person-heavy products. Prefer a realistic lifestyle model scene with the model appearing, arm extended forward, hand holding the dryer toward the viewer, and the dryer closest to camera. The composition should have stronger impact and depth than a static product render, but structure remains mandatory: outlet/nozzle, barrel, handle, buttons, fold joint, inlet, IP artwork, and cord/accessory state must stay readable and mechanically plausible. Avoid fisheye distortion, deformed hand anatomy, hidden key structures, or product proportions changed for drama.

## Packaging Rules

Record package type:

```text
Packaging type: 天地盖 / 抽屉盒 / 吊卡盒 / 直立纸盒 / 吸塑盒 / 软包 / 套装礼盒
Package size:
Front face:
Back face:
Left/right side:
Top/bottom:
Official text areas:
Barcode/certification/manufacturer areas:
Accessories list:
```

Do not change package type or proportions. Do not swap front/back/side/top/bottom content. Do not AI-generate official small text, barcode, certification, manufacturer information, authorization marks, anti-counterfeit labels, or trademark details.

## Image-Type Rules

### Detail Pages

Default Chinese ecommerce page width is 790px. Use 11-13 screens for richer digital-product pages; use 8 screens only when requested or when the product information is light.

Screen 02 should usually be a 5-6 selling-point card overview. Each card has one selling point, short title, 15-20 character explanation, icon/product detail/scene thumbnail, unified radius, spacing, shadow, and typography.

### White-Background Images

Use 1400 x 1400 square, pure white `#FFFFFF`, natural light-gray contact shadow, no props, no large text, and product at 75%-85%. Generate one product-only image per real color/SKU, package-only image per real package version, product + package image per real color, and optional state/accessory images only when the state/accessory exists.

### Main Images

Use 1400 x 1400 square. Plan 5-6 images when requested: core selling point, real scene, function, detail, package/gift, and SKU or all-color collection. Keep product scale, angle logic, and lighting consistent.

### SKU Images

Use real colors and packages only. Default square scene layout: left side for SKU name and 5-9 short selling points, right side for the corresponding color product. Background and props support that SKU color but do not overpower the product. Include a collection SKU image only for real multi-color products.

## Prompt Blocks

Use this product-faithfulness base at the front of generation prompts:

```text
这是一款真实存在的数码产品，不是概念设计，不是重新设计。严格依据参考图和六视图建立唯一产品模型。产品外轮廓、长宽厚比例、圆角、厚度、曲率、接口、按键、屏幕、指示灯、LOGO、线材、转轴、开孔、材质分区、颜色分区、包装结构和配件形态必须完全保持一致。产品只能整体等比缩放、整体旋转和整体改变观察角度，不允许局部拉伸、压扁、扭曲、移动结构、删除结构、增加结构、镜像错误或重新设计。结构准确性优先于美观效果。
```

Use this negative block when writing image prompts:

```text
错误接口位置，错误按键位置，错误屏幕位置，错误线材路径，缺少真实结构，额外接口，额外按钮，额外屏幕，额外灯珠，额外支架，机身比例错误，机身过薄，机身拉伸，圆角错误，线材穿模，线材漂浮，转轴断裂，支架悬浮，结构融合，左右结构混乱，背面出现多余零件，图案变成立体装饰，产品重设计，概念设计，幻想结构，不真实机械结构，虚构参数，虚构认证，包装小字乱写，低清晰度，畸变，拉伸，压扁，变形。
```

## Failure Checklist

Reject or revise the image if any of these appear:

- Wrong product category or redesigned silhouette.
- Wrong thickness, corner radius, curvature, or body proportion.
- Port, button, screen, light, hole, cable, hinge, stand, nozzle, or vent is moved, copied, missing, swapped, or floating.
- Left/right or front/back structure is confused.
- Built-in line, strap, ring, stand, clamp, guard, shade, nozzle, accessory, or package item disappears.
- Product uses an unconfirmed color or package.
- Surface artwork crosses hardware boundaries or becomes a raised object without source.
- Unauthorized IP character, logo, slogan, brand text, commercial font name, or protected wordmark style appears.
- Package type, six-face layout, or official text areas are wrong.
- AI writes fake barcode, certification, manufacturer, authorization, or parameter text.
- Claims mention exact unconfirmed values, certification, safety, medical, warranty, discount, or absolute performance.
- Product visibility is sacrificed for style.
