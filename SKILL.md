---
name: detail-flow
description: Plan, generate, audit, revise, or deliver product detail pages and ecommerce long images from product photos, six-view references, packaging files, product concepts, screenshots, or style references. Use when the user says 生成新的详情页, asks for Chinese ecommerce详情页, 8-screen or 11-13-screen detail pages, product sales pages, digital-product long images, product-structure locking, visual master planning, staged image generation, stitched-preview QA, page-copy planning, SKU/white-background/main-image planning that belongs to a detail-page project, and detail-page workflow optimization.
---

# zhuchao的SKILL

## Overview

Use this skill to build a product-detail-page system before generating final images. Treat the page as one buying narrative and the product as a real engineered object. Optimize for product faithfulness, buyer clarity, page continuity, verified claims, staged review, and clean project isolation.

For digital products, small electronics, IP-style accessories, packaging, SKU images, white-background images, or product-structure QA, read [references/digital-product-constraints.md](references/digital-product-constraints.md). For Sanrio, Crayon Shin-chan, PINGU, Disney, tokidoki, Brunch Brothers, Coca-Cola, or other IP-style products, read [references/ip-style-guidance.md](references/ip-style-guidance.md). For screen order, copy patterns, and long-page structures, read [references/detail-page-patterns.md](references/detail-page-patterns.md).

When planning visual style, choose the scene-rendering route by product category before writing prompts. Low-model categories such as earphones, power banks, stands, chargers, cables, speakers, and compact desk accessories may use a polished 3D/cartoon-rendered ecommerce scene with pedestals, soft IP props, clean cards, and product-led composition. Person-heavy categories such as blow dryers, beauty appliances, and products whose first buying proof depends on body/hand use should use a more realistic lifestyle model scene. For blow dryers, screen 01 should normally show a model appearing in scene, hand extended forward holding the dryer toward the viewer, with stronger perspective tension and product impact while keeping the dryer structure accurate and dominant.

When the user asks to reference MarTUBE, martube.com, martubegift.com, or tw.martube.com for PINGU products, use the PINGU / MarTUBE store-reference rules in `ip-style-guidance.md`: extract palette, scene bank, buyer emphasis, product angle, scale, depth, and typography rhythm, but do not copy official assets, slogans, store copy, protected wordmarks, or unsupported parameters.

## Non-Negotiable Contract

When the trigger phrase is `生成新的详情页`, treat the request as a new product-detail-page project. Reset all previous product context unless the user explicitly says to continue the same product. Do not carry over the previous product's DNA, SKU colors, IP, logo, artwork, packaging, accessories, parameters, claims, scene style, layout decisions, file names, output count, or correction history. Use only the current message's attachments, current explicit instructions, and facts the user intentionally repeats.

If the user writes `生成新的详情页` but provides no current product source, ask for product images or product files before producing product DNA. Do not fill the new project with the last product's information.

Follow this order for image-led ecommerce detail-page work:

1. Analyze inputs.
2. Establish product DNA and claim-source categories.
3. Produce the pre-generation direction package and fully list three sections: `文案方向`, `风格方向`, and `画面方向`.
4. Stop for direction confirmation.
5. Produce the complete page blueprint from the confirmed direction.
6. Establish the text master, visual master, product-structure lock, IP style master when relevant, and optional 1:3 spatial master.
7. Generate screen 01 and screen 02 only as the first visual sample package.
8. Stitch screen 01 and screen 02 into a short preview when useful.
9. Audit the sample package.
10. Stop for style confirmation.
11. Generate the remaining slices only after the user confirms the style.
12. Stitch the full preview, audit, revise the smallest responsible layer, and deliver.

Do not produce the blueprint before the user confirms the fully listed `文案方向`, `风格方向`, and `画面方向`. Do not generate final page images before the blueprint is produced. Do not generate screen 03 or later before the user confirms the style from screen 01 and screen 02. A casual "continue" does not approve an unreviewed direction package or visual sample package.

Keep the standard workflow to these two normal approval gates. Gate 1 confirms the direction package: product DNA summary, claim-source handling, copy direction, IP/visual style, required visual content, and prohibited content. Gate 2 confirms the style: screen 01, screen 02, optional stitched preview, visual/IP master, and audit. Ask for additional confirmation only when a serious product-structure failure, missing source, blueprint conflict, or changed scope makes continuation unsafe.

Do not create websites, videos, scripts, workflow nodes, placeholder mockups, or unrelated artifacts unless the user asks for them. Use lightweight utilities only for deterministic tasks such as checking image size, stitching approved slices, or verifying files.

## Input Analysis

Separate the inputs by authority:

- **Product structure source**: six-view image, real photo, CAD render, product close-up, packaging dieline, or specification sheet.
- **Surface artwork source**: logo, IP graphic, pattern file, label, package front, sticker, or print area reference.
- **IP style source**: confirmed IP name, official product artwork, supplied authorized graphic, packaging system, or user-provided IP mood reference.
- **Style source**: mood image, page reference, photography style, color palette, prop language, model/hand language, or competitor page.
- **User correction**: latest explicit instruction, such as "do not show the silver part" or "keep this exact angle".

For a new detail-page project, first write a one-line `project_context_status`: `new project, previous product context cleared`. Then list only the product, IP, packaging, style, and claim sources available in the current request.

Use source priority:

1. Latest user correction.
2. Product six-view or CAD-like structural reference.
3. Product real photo.
4. Manual/specification/packaging structure file.
5. Official or user-supplied IP artwork for print placement and IP mood only.
6. Surface artwork or packaging art for print placement only.
7. Style reference for mood, lighting, palette, and composition only.
8. AI inference for background, scene, and layout only.

Never let a style reference override product structure.

Never use a previous chat product as a hidden source. Previous product information may be used only if the user explicitly says the new request continues that exact product or repeats the relevant files/facts in the current request.

Before writing the direction package, give the user one concise chance to provide confirmed selling points, parameters, prohibited claims, target platform, or output size when they are missing. Do not make this a long questionnaire. If the user does not add information, proceed with visible facts and cautious category-level inference, and label inferred claims for review.

## Product DNA

Before page planning, write a product DNA block. Do not continue to image prompting without it.

Include:

- Product name, category, brand/model when known.
- Product IP, authorized surface artwork, and target audience when known.
- Product style fit: IP identity, product category tone, use scenario, buyer group, and why the selected visual style matches all three.
- Real colors/SKUs and whether packaging/accessories exist.
- Overall silhouette, length-width-thickness or height-width-depth relationship, roundness, edge curvature, and thickness.
- Front, back, top, bottom, left, and right structures when visible.
- Ports, buttons, holes, screens, indicators, vents, hinges, joints, lines, straps, plugs, stands, handles, nozzles, or other fixed elements.
- Logo, pattern, artwork, surface-print area, material zones, and color zones.
- IP style DNA: target audience, palette, emotional tone, scene direction, prop level, optional PVC-style figure accent rule, and buyer preference fit.
- Packaging type, six-face ownership, text/label areas, and parts list when supplied.
- The easiest structure mistakes to make.
- Unknowns that must remain blank or be written as "以实际参数为准".

If any DNA field would require borrowing from a previous product, mark it as unknown instead. Do not infer prior SKU colors, prior IP artwork, prior packaging, prior product angle, prior title, or prior selling points.

Treat the product as one rigid model across the entire project. It may be scaled, rotated, lit, staged, or placed in a new scene, but it must not be locally stretched, flattened, re-proportioned, mirrored incorrectly, or redesigned.

## Claim Control

For every product category, think about selling points from the buyer's perspective before writing copy. Start with what the buyer wants to know, worry about, compare, or value in that category, then map each point back to confirmed facts, visible facts, or cautious category-level inference.

Do not start from engineering features alone. Translate features into buyer-facing reasons:

- Appearance and giftability: "好不好看 / 是否符合 IP 调性 / 适不适合送礼".
- Experience: "用起来是否舒服、方便、稳定、省心".
- Performance: "音质、风力、充电速度、支撑稳定性、照明效果等品类核心体验".
- Endurance and power: "电池、续航、是否够日常使用"; exact numbers require source.
- Portability: "是否轻便、可折叠、好收纳、能不能放进包里".
- Safety and reliability: "是否稳定、是否有保护、是否不容易误用"; exact protections require source.
- Compatibility: "能不能适配常见设备/场景"; exact lists require source.

For every product, produce a buyer-angle concern list before choosing claim seeds. For example, earphones should consider shape/style, IP appearance, wearing comfort, sound quality, battery, endurance, connection/use convenience, charging-case storage, portability, and giftability. Blow dryers should consider shape/IP appearance, wind experience, drying efficiency, hair-care comfort, folding/storage, travel portability, grip, nozzle use, and giftability. Power banks should consider appearance, capacity/endurance when sourced, charging convenience, port/cable layout, portability, compatibility, travel use, and safety when sourced. Do not invent exact performance parameters without a source.

Classify each claim:

- **Confirmed**: supplied by the user, a spec table, packaging, manual, or source text.
- **Visible fact**: directly observable from images, such as color, shape, port count, open/closed state, or included accessory.
- **Reasonable inference**: category-level buyer concern or soft use case, such as travel, desk use, giftability, storage, or daily convenience.
- **Unknown**: exact parameters, certifications, measured performance, official compatibility, regulated claims, warranty, award, discount, authorization, or safety promise without source.

Use confirmed and visible facts freely. Use reasonable inference only as soft copy. Do not write unknowns as facts. Use "以实际参数为准" or reserve a replacement area when exact information is missing.

Never invent battery capacity, power, fast-charge protocol, Bluetooth version, waterproof level, noise value, load-bearing number, rotation angle, material grade, certifications, authorization codes, manufacturer information, barcode content, warranty, medical effect, absolute safety, or IP partnership.

For IP products covered by this skill, assume the IP project is authorized. You may use the IP name, character world, packaging rhythm, title hierarchy, and supplied or visible official artwork as part of the visual direction. Preserve exact product/package artwork placement. Do not invent legal small print, authorization codes, barcodes, manufacturer text, unsupported slogans, unconfirmed bundle gifts, exact parameters, or brand-partnership details outside the current brief.

## Style Fit Rule

Before choosing scene style, color, props, typography, or layout rhythm, judge fit from three inputs in this order:

1. **IP identity**: the confirmed IP, supplied artwork, package mood, and safe IP-adjacent style.
2. **Product category tone**: what the product is used for, such as listening, charging, drying hair, desk support, travel storage, gift display, or daily carry.
3. **Target audience**: the likely buyer and user, such as young female buyer, student, commuter, gift buyer, parent-child buyer, collector, office user, or trend buyer.

The final style must satisfy all three. Do not make every IP product automatically pink, cute, or toy-like. Do not let the IP mood hide the product's practical use. Do not let a practical category become cold or generic when the product is clearly for giftable/IP-style buyers.

Examples:

- Sanrio / Hello Kitty electronics can use soft pink, cream, bedroom gift, vanity desk, and gentle girl-cute styling when aimed at young female or gift buyers.
- PINGU products should avoid ice, snow, glaciers, and winter-only worlds unless the user explicitly asks for them. Use sky blue, light blue, cream yellow, warm white, black-white product/IP contrast, and small red/orange accents for student, gift, or daily-use buyers.
- MarTUBE-style PINGU product pages should be treated as cool-cute daily electronics and giftable collectibles: blue page frame, cream/yellow warm base, small red/orange accents, tote/backpack portability, desk, room, gift, package, shelf, or summer daily-use scenes, clear core-grid proof, and product-first hero layout.
- Crayon Shin-chan products can use brighter playful life scenes, comic labels, and warm color accents, while staying readable and product-first.
- tokidoki products can use colorful pop, sticker density, acrylic display, and collector energy when the target buyer likes trend toys or IP collecting.
- Brunch Brothers products can use warm cream, food-inspired desk scenes, soft morning light, and relaxed cute layouts.
- Coca-Cola products can use red-white refreshment, retro-pop, summer/ice accents, and clean high-contrast cards without copying protected script or slogans.

If the IP, product tone, and audience point to different directions, present the conflict in the direction package and recommend the safest style. For example, a premium family product should use restrained gift/premium styling even if the IP is cute; a travel charging product should still show portability and charging clarity even if the IP mood is decorative.

## Direction Package

Before the full blueprint, present a complete direction package and stop for confirmation. Do not compress this into a short summary. Use these exact user-facing headings and fully list the content under each heading:

1. `文案方向`
2. `风格方向`
3. `画面方向`

The direction package must include:

- **Project context status**: state whether this is a new project, whether previous product context has been cleared, and which current sources are being used.
- **Buyer-angle selling points**: buyer type, category concerns, 2-4 selected claim seeds, and proof level for each claim.
- **Copy direction**: core selling proposition, 2-4 first-screen claim seeds, visible-copy tone, suggested headline style, short selling-point wording, and unsupported claims to avoid.
- **Style direction**: IP identity, product category tone, target audience, style-fit reason, palette, analogous color extension, small contrast-color accents, lighting, typography direction, text layout reference, card/icon language, prop density, PINGU one-extra-character-per-screen rule when relevant, layout diversity plan, and commercial-font/IP-text safety rule.
- **Visual content direction**: planned hero product treatment, scene-rendering route, required scenes, model-use scene, backpack portability scene, packaging/list treatment, props, product rendering style, product angles, product scale rhythm, foreground/background placement, background-color relationship, first-screen title placement, PINGU character count when relevant, and what must not be hidden.
- **Structure and claim guardrails**: product DNA summary, package lock, confirmed facts, visible facts, reasonable inferences, and unknowns that remain "以实际参数为准".

Map the bullets into the three headings instead of outputting them as scattered notes:

- Put copy proposition, buyer-angle selling points, first-screen claim seeds, headline/copy tone, and unsupported claims under `文案方向`.
- Put IP identity, product category tone, target audience, palette, typography, layout mood, scene-rendering route, prop density, color strategy, and font/IP safety under `风格方向`.
- Put hero composition, screen-01 product focus, model-use requirement, backpack portability requirement, screen-02 grid proof plan, product angles, scale/depth rhythm, background relationship, packaging/list treatment, PINGU character count, and hidden-structure risks under `画面方向`.

After the three sections are fully listed, end with a clear confirmation question such as `请确认这三个方向，确认后我再生成完整蓝图。` Do not write the screen-by-screen blueprint until the user confirms this direction package. If the user revises the direction, update the direction package first, then continue to the blueprint.

## Page Blueprint

Produce a structured blueprint after the direction package is confirmed and before image generation.

For Chinese ecommerce digital-product pages, default to 11-13 screens unless the user asks for 8 screens or a different platform format. For the original DetailFlow style, 8 screens remain acceptable when the user explicitly asks for 8 screens, a lighter sales page, SaaS/model pages, or a non-Chinese marketplace page.

Each screen must include:

- `slice_id`
- `buyer_question`
- `module_type`
- `module_label`
- `claim_seed`
- `screen_job`
- `evidence_type`
- `content_density`
- `layout_archetype`
- `layout_variation_reason`
- `color_strategy`
- `copy_module_type`
- `copy_structure_pattern`
- `primary_module`
- `secondary_modules`
- `text_exact`
- `text_layout_reference`
- `hierarchy_strategy`
- `composition_shift`
- `top_edge_anchor`
- `bottom_edge_anchor`
- `visual_composition`
- `product_render_style`
- `scene_rendering_route`
- `product_angle_reason`
- `product_scale_depth_reason`
- `product_background_relationship`
- `hero_title_layout_reason` for screen 01
- `product_dna_lock`
- `package_lock`
- `ip_style_direction`
- `target_audience_fit`
- `font_license_rule`
- `claim_source`
- `reference_style_notes`
- `reference_layout_borrow`
- `risk_unknowns`

Screen 01 must establish 2-4 claim seeds. Later screens must expand, prove, visualize, compare, or contextualize those seeds. Do not introduce unrelated later-screen selling points unless the user asks for a new chapter.

For every visual screen, explain why the chosen product angle proves the selling point. Use front or 3/4 front for appearance and IP identity; top or 45-degree overhead for opening, inner structure, mouth, lid, port layout, or storage relation; side or rear angle for thickness, fold direction, handle, hinge, cable, inlet/outlet, or backpack placement; macro crop for texture, interface, lock, nozzle, mesh, button, seam, or material proof; hand/model angle for grip, wearing, operating, packing, or scale proof; consistent same-angle lineup for SKU/color comparison.

For every visual screen, define product scale and depth relationship. Screen 01 uses the largest product scale and product-first depth. Screen 02 uses smaller product/detail proofs inside cards. Structure screens may crop product parts very large. Scenario screens use medium scale so the hand, bag, desk, or model can prove context. Parameter screens shrink the product and let the information card dominate. SKU screens keep all variants the same scale, angle, and light.

For every visual screen, decide whether the background makes the product stand out or blend into the scene. Hero and structure proof should make the product stand out through silhouette, brightness, shadow, card backing, or contrast accents. Scenario, hand-use, and backpack screens may let the product partially blend into the scene through shared light and palette, but the product edge, key structure, and official artwork must remain readable. Do not let the background color, props, or IP decoration swallow the product.

For screen 01, explain the title layout. The title should create emotion and the first memory point, not list parameters. For authorized IP products, prefer an IP-first title hierarchy when the reference supports it: large IP name or authorized title area first, then Chinese product/selling-point subtitle below or beside it. Place it where it leads the eye into the product: top center for a centered hero, top-left for a right-weighted or diagonal product, tilted/sticker-like only when the IP mood supports it. Keep it close enough to the product to feel connected, but never cover the product silhouette, logo, artwork, port, button, handle, fold line, nozzle, case opening, or other identity structure. Use official supplied title/logo assets or safe editable typography for final commercial output.

Choose claim seeds by buyer priority for the product category. A good first-screen seed is not just a feature label; it should answer a buyer question such as "why does it look appealing", "will it work well", "is it easy to carry", "is it comfortable", "does it last long enough", or "is it giftable". If exact performance data is missing, keep the seed soft and visual instead of numeric.

For digital ecommerce pages, screen 02 is fixed as the product core selling-point overview. Use a grid/card layout similar to the user's reference: preferably a 2x3 six-point grid, or 5 cards only when the product truly has fewer sourced or buyer-relevant points. Each card must include a visible number, short title, short explanation, and one supporting visual such as product crop, structure proof, icon, mini scene, phone/device relation, portability proof, or SKU/color proof. Do not turn screen 02 into a single hero poster, one large scene, or a repeated screen-01 visual. Use varied modules across the rest of the page: mechanism, structure proof, function experience, scenario, detail craft, compatibility, safety/trust, packaging/list, parameter table, comparison, and closing CTA.

Every ecommerce detail page blueprint must include these required visual modules unless the user explicitly removes them:

- **Hero product focus**: screen 01 must make the product immediately noticeable. The product should be the dominant visual subject, large, clear, well lit, and not crowded by props, models, packaging, or text.
- **Core selling-point grid**: screen 02 must summarize the product's main buyer-facing reasons in a 5-6 point grid, with short text and visual evidence in every card.
- **Model-use image**: at least one screen must show a model using or holding the product in a realistic way. The model/hand/body should support the use scenario; avoid distorted anatomy and avoid blocking key product structure.
- **Backpack portability image**: at least one screen must show the product being placed into, partly inside, or next to a backpack/travel bag to communicate portability. Keep scale believable and do not hide critical product structures.

Do not make every screen `headline + subtitle + centered product`. Vary copy forms: guide title, Q&A, label cluster, annotation map, three-point breakdown, mini steps, scene captions, trust checklist, comparison snippets, parameter table, or quiet closing.

When the user supplies detail-page references for text layout, borrow their typography arrangement and information rhythm: large playful headline blocks, IP-first title hierarchy, short subtitle lines, sticker labels, small badge text, arrow callouts, speech bubbles, bracket labels, rounded information cards, mini comparison boxes, parameter sheets, and tilted photo/card captions. Keep text short and readable. For authorized IP projects, the IP title/name can be part of the hierarchy; exact final wordmark should use supplied official artwork or safe editable type. Do not copy unrelated visible text, commercial font names, unsupported slogans, unrelated product claims, legal small print, or unprovided parameters.

Use diverse detail-page layouts. For 11-13 screen ecommerce pages, use at least 8 distinct layout archetypes. For 8-screen pages, use at least 5 distinct layout archetypes. Adjacent screens must not use the same visual grammar, text rhythm, product scale, and card structure at the same time. Borrow only layout language from user-supplied reference pages, such as large hero product, sticker callouts, multi-card overview, macro magnifier, diagonal product angle, hand operation, backpack portability, polaroid/photo frame, comic speech bubble, split color block, step sequence, package/list grid, parameter sheet, and SKU collection. Do not copy the reference page's exact text, fonts, official IP elements, character art, logo treatment, or unrelated product details.

Use a controlled color system for scene style and detail-page layout. Start from the product/IP base colors, then add neighboring analogous colors to enrich backgrounds, cards, props, and transitions. Use a small amount of contrast color only for visual emphasis such as stickers, arrows, badges, small icons, key separators, or tiny decorative accents. Contrast accents must stay secondary and should not overpower the product, change real SKU colors, reduce text readability, or make the page look like a different IP/product series.

Before approval 1, audit the blueprint:

- Each screen answers a different buyer question.
- Screen 01 strongly highlights the product as the first visual focus.
- Screen 01 title placement explains why it sits there and how it leads the eye to the product without covering identity structures.
- Screen 02 is a fixed core selling-point grid with 5-6 numbered cards, short readable copy, and visual proof per card.
- Each screen has a product angle reason, scale/depth reason, and background relationship reason tied to the selling point.
- The blueprint includes one model-use screen and one backpack portability screen.
- The blueprint uses enough distinct layout archetypes and no adjacent screens repeat the same visual grammar.
- Adjacent screens do not repeat the same copy rhythm.
- Later screens trace back to screen-01 claim seeds.
- Unsupported claims are marked as unknown or placeholders.
- Product DNA and package locks are present where the product or packaging appears.
- IP tone, scene choice, title hierarchy, and typography fit the target audience without adding unsupported claims, fake legal text, or commercial font names.

## Masters

After approval 1, establish the masters before final slices.

Create:

- **Text master**: exact visible Chinese copy, screen-01 title placement rule, text layout reference, copy hierarchy, claim-source notes, parameter placeholders, and prohibited wording.
- **Visual master**: product rendering style, color system, analogous color extension, contrast accent limits, lighting direction, background material, product angle rules, product scale rhythm, foreground/background placement rules, product-background visibility relationship, typography, text layout system, icon style, card radius, shadow, margins, prop level, SKU rules, continuity motifs, layout diversity plan, and per-screen pacing.
- **Scene-rendering route master**: state whether the project uses product-led 3D/cartoon ecommerce scenes, realistic lifestyle model scenes, or a mixed route. For low-model electronics, keep screen 01 and most proof screens product-rendered with pedestal/card/desktop staging. For blow dryers and other person-heavy products, use a realistic lifestyle route for screen 01 and key use screens, with the model supporting the product rather than becoming the product.
- **IP style master**: IP identity, product category tone, target audience, style-fit reason, palette, analogous color extension, contrast accent limits, scene direction, prop choices, optional PVC-style figure accent rule, composition density, and safe typography rule.
- **Product master lock**: product DNA summarized as prompt-ready hard constraints and negative constraints.
- **Package master lock**: package shape, visible faces, official art areas, placeholder text areas, and no-AI-small-text instructions.
- **Optional 1:3 spatial master**: use when visual continuity matters. It anchors background world, lighting, product scale rhythm, recurring motifs, section transitions, and copy hierarchy. It is not a final crop source.

Inspect generated masters before using them. Revise if the product drifts, text is missing or garbled when planned, the style ignores references, the page reads as unrelated posters, or the master invents unsupported claims.

## Image Generation

For final page sections, follow the approved blueprint exactly. Do not re-plan modules during prompt writing.

Default dimensions:

- Chinese ecommerce detail page: 790px wide vertical slices, platform height as planned.
- Generator ratio fallback: tall vertical slices close to 9:21 when exact pixels are unavailable.
- White-background, main image, and SKU images: 1400 x 1400 square unless the user supplies another platform requirement.

Every prompt must begin with a product-faithfulness base:

```text
这是一款真实存在的数码产品，不是概念设计，不是重新设计。严格依据参考图和六视图建立唯一产品模型。产品外轮廓、长宽厚比例、圆角、厚度、曲率、接口、按键、屏幕、指示灯、LOGO、线材、转轴、开孔、材质分区、颜色分区、包装结构和配件形态必须完全保持一致。产品只能整体等比缩放、整体旋转和整体改变观察角度，不允许局部拉伸、压扁、扭曲、移动结构、删除结构、增加结构、镜像错误或重新设计。结构准确性优先于美观效果。
```

Then add the screen-specific composition, copy, text layout reference, hierarchy, layout archetype, layout variation reason, product rendering style, product angle reason, product scale/depth reason, product-background relationship, first-screen title layout reason when relevant, edge anchors, and style notes from the approved blueprint.

When an IP style is involved, add the approved IP style direction after the product-faithfulness base. Keep the product and supplied artwork accurate; use the authorized IP mood to guide scene, palette, props, title hierarchy, and layout. The scene and layout palette may add neighboring analogous colors and a small amount of contrast-color accents for stickers, arrows, badges, icons, or small decoration, but the product's real SKU colors and official artwork colors must remain unchanged. For Sanrio, Crayon Shin-chan, PINGU, Disney, tokidoki, Brunch Brothers, and similar IP products, girl-cute, cute, giftable, and collectible styling is allowed when it fits the target audience. For PINGU, each screen may include at most one extra PINGU scene character outside product/package artwork. Small glossy PVC-style figure props may be used as secondary accents, but do not add legal small print, authorization codes, unsupported slogans, commercial-font names, or props that imply unconfirmed bundle contents.

Apply the approved scene-rendering route in every prompt:

- **Low-model product-led route**: for earphones, power banks, stands, chargers, cables, speakers, compact fans/lamps, and similar products where a model is not the main proof, use a polished 3D/cartoon-rendered ecommerce scene. Use clean pedestals, desk mats, rounded cards, soft shelf/room props, gentle depth, and IP-matched color. Build visual guidance through product placement, height, scale, overlap, and front/back depth, not through unnecessary drawn guide lines. Keep the product as the largest visual subject.
- **Realistic model lifestyle route**: for blow dryers, beauty tools, and other products whose value is strongly proven by a hand/model using it, use a more photoreal lifestyle scene. For blow-dryer screen 01, show a model in a room/vanity/lifestyle scene, arm extended forward, hand holding the dryer toward the viewer. Make the dryer large, close to camera, and instantly noticeable; use stronger perspective tension and body/hand depth, but avoid fisheye distortion, deformed hands, blocked buttons, hidden nozzle/outlet, or incorrect handle/barrel proportions.
- **Mixed route**: a detail page may combine routes. For example, a blow dryer can use a realistic model hero and use scenes, then product-rendered cards for structure, nozzle, folding, packaging, SKU, and parameters. Earphones or power banks can use product-rendered hero scenes but still include one later hand/model-use proof screen if required by the page contract.

Use staged generation:

1. Generate screen 01 first from the approved blueprint and masters.
2. Generate screen 02 second from the same product DNA and visual/IP style system. Screen 02 must be the fixed core selling-point grid: preferably 2x3 six cards, with number badge, buyer-facing title, short explanation, and visual proof in each card.
3. Stitch screen 01 and screen 02 vertically when useful.
4. Inspect product structure, text quality, visual continuity, style match, repeated poster grammar, and unsupported claims.
5. Present screen 01, screen 02, optional stitched preview, and audit for style confirmation.
6. Generate screen 03 and later only after the user confirms the style.

## Related Image Sets

When the detail-page project also asks for main images, white-background images, SKU images, or packaging/list images, plan them under the same product DNA and visual master. Do not let related image sets interrupt the required detail-page flow.

Use this strict order:

1. Finish the full detail page: generate, stitch, audit, and approve.
2. Generate the `1:1` main-image set from the approved detail-page slices.
3. Generate the `1:1` SKU image set after the main-image set is complete.

Do not generate SKU images before the detail page and main images are finished.

- **Main images after detail pages**: decide the main-image count from the final detail-page slice count. Convert each approved detail-page slice into one corresponding `1:1` square main image unless the user supplies another platform rule. Preserve the slice's selling point, product angle, style, and copy hierarchy, but recompose it for square format instead of cropping, stretching, or squeezing the long slice. Keep the product prominent and readable in every square image.
- **White-background images**: use pure `#FFFFFF`, natural light-gray contact shadow, no props, no large text, product at 75%-85% of the square canvas, one image per real color/SKU, and consistent angle/light/scale.
- **SKU images**: generate only after the detail page and main-image set are complete. SKU images are `1:1` square, default 1400 x 1400 unless the platform requires otherwise. Decide SKU image count from confirmed product colors. If there are three confirmed colors, create three SKU images; if there is one confirmed color, create one SKU image. Use real colors/SKUs only; default to scene-based square images with left-side SKU name/selling points and right-side product, unless the user supplies another layout.
- **Color collection images**: keep all products the same scale, angle, light, and structure; never invent unconfirmed colors.
- **Packaging/list images**: keep package shape, face ownership, and accessory count true; reserve official small text and barcodes for later compositing.
- **IP-style images**: adapt the scene, title hierarchy, and layout to the authorized product IP tone and target audience. Girl-cute/cute styling and small PVC-style figure accents are allowed for suitable IP products, while exact product/package artwork placement remains locked.

Do not expand the deliverable count beyond these rules or the user's request without approval. If color count or final slice count is unknown, ask once or mark the image count as pending until confirmed.

## Audit And Revision Routing

Fail a result if it contains product redesign, wrong proportions, wrong port/button/screen/line/hinge position, missing real structure, extra parts, wrong SKU color, wrong package shape, invented parameters, fake legal/authorization text, unsupported IP slogans or bundle claims, more than one extra PINGU scene character in a PINGU screen, PVC-style figures that dominate or imply unconfirmed accessories, commercial-font names, unreadable critical text, copied unrelated reference text, distorted or unreliable AI-rendered official wordmarks, contrast colors that overpower the product, palette shifts that change the product/IP identity, repeated standalone-poster layouts, repeated adjacent layout grammar, insufficient layout diversity, or broken page continuity.

Also fail a result when the product angle does not prove the claimed selling point, the product is too small for the screen job, the depth relationship hides the product, the background makes the product disappear, or the screen-01 title competes with or covers the product identity.

Route revisions to the smallest responsible layer:

- Copy or claim problem: revise `text_exact` or claim source and repair only affected text/slice.
- Product structure problem: strengthen product DNA and regenerate only affected slice or product area.
- Packaging problem: revise package lock or reserve official text areas.
- IP style problem: revise the IP style master, target-audience fit, prop level, or typography rule without changing product DNA.
- Single-screen hierarchy problem: revise that screen's modules, density, or hierarchy.
- Adjacent transition problem: revise the two edge anchors and regenerate the smallest neighboring range.
- Repeated layout problem: revise `composition_shift` for the repeated screens.
- Whole-page style problem: revise the visual master and only dependent slices.
- Narrative problem: return to the blueprint.

Full regeneration is appropriate only when the approved story, product DNA, or visual master changes substantially.

## Delivery

After final audit, save the complete approved set in a clear output folder. Include the approved master when used, every final slice with sequential filenames, the early 2-slice preview, the full stitched long image, the `1:1` main-image set derived from the approved detail slices when requested, and the `1:1` SKU image set based on confirmed colors when requested. Exclude rejected or superseded variants unless the user asks for all iterations.

Verify files exist before reporting completion. Report the output folder path and concise status.
