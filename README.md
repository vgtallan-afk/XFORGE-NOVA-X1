# XFORGE NOVA X2.11

Files:

- `index.html` — the XFORGE NOVA X2.11 visual editor.
- `api/ai-editor.js` — Vercel server route for Groq-powered safe AI editing and brand sheet analysis.

## Vercel setup

Add this environment variable in Vercel:

```bash
GROQ_API_KEY=your_groq_key_here
```

Optional:

```bash
GROQ_MODEL=llama-3.3-70b-versatile
GROQ_VISION_MODEL=meta-llama/llama-4-scout-17b-16e-instruct
```

## Important

Never put your Groq API key inside `index.html`. The browser calls `/api/ai-editor`; the server route calls Groq.

## AI workflow

1. Upload/open HTML.
2. Select an element or section.
3. Open the AI tab.
4. Write a command.
5. Click Generate Preview.
6. Apply or Cancel.

## Brand sheet workflow

1. Open AI tab.
2. Upload a brand sheet image.
3. Click Analyze Brand Sheet.
4. The Brand Kit is filled for this project.
5. Use Apply page, Apply selected, or AI apply brand.


## X2.3 changes

- Two-rail Canva-style sidebar.
- Main rail stays compact.
- Active panel opens beside it.
- Removed duplicated visible actions from the Selected panel.


## X2.4 changes

- Floating toolbar Color opens visual color picker instead of prompt.
- Brand colors appear inside Colors panel.
- Floating toolbar Edit opens relevant left-side controls.


## X2.5 API fix

This version normalizes `GROQ_API_KEY` on the server:
- removes spaces
- removes line breaks
- removes a pasted `Bearer ` prefix
- validates that the key starts with `gsk_`

In Vercel Environment Variables, the value should still be only the real Groq key.


## X2.6 changes

- Selected text now opens the Text editing panel, not Spacing.
- Floating toolbar Edit opens the correct sidebar controls.
- Secondary sidebar auto-collapses when no element is selected.
- Side panel now shows one relevant panel at a time.


## X2.7 changes

- Floating toolbar now clamps inside the visible canvas and wraps when needed.
- Background panel now has Canva-style gradient controls: direction/type, start color, end color, preview and presets.


## X2.8 changes

- Added site title/browser tab name setting.
- Added favicon upload for exported page.
- Background color and gradients now apply automatically without Apply buttons.


## X2.9 changes

- Added copyable ChatGPT prompt to convert brand sheet image into CSV.
- Added CSV upload for Brand Kit.
- CSV applies colors, font and design rules to the project Brand Kit.
- Added Reset / remove gradient button.


## X2.10 changes

- Final Preview now respects the current edit mode.
- Desktop Edit opens desktop preview.
- Mobile Edit opens mobile-width preview.


## X2.11 changes

- Mobile Final Preview no longer injects CSS into the page.
- Mobile preview opens the clean exported page inside a 390px iframe, matching Mobile Edit more closely.
- Desktop preview still opens the clean exported page directly.
