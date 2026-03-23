# Staxwise — How to add resources

## Folder structure

```
staxwise/
├── index.html                  ← Landing page (all subjects)
├── ocr-gcse-cs.html            ← OCR GCSE Computer Science
├── aqa-gcse-business.html      ← AQA GCSE Business Studies
├── btec-enterprise.html        ← BTEC Enterprise
├── btec-dit.html               ← BTEC Digital Information Technology
├── ks3-computing.html          ← KS3 Computing
└── resources/
    └── ocr-gcse-cs/            ← Put your OCR CS HTML files here
        ├── 1-1-cpu-fde.html
        ├── 1-1-von-neumann.html
        └── ...
```

## How to add a resource (OCR CS example)

1. Drop your HTML file into `resources/ocr-gcse-cs/`
   e.g. `resources/ocr-gcse-cs/1-1-cpu-fde.html`

2. Open `ocr-gcse-cs.html` in a text editor

3. Find the section you want (search for e.g. `ADD YOUR 1.1 RESOURCES`)

4. Add a line like this — remove the `coming` class to make it live:

   COMING SOON (placeholder):
   ```html
   <a href="resources/ocr-gcse-cs/1-1-cpu-fde.html" class="resource-item coming">
     <span class="resource-name">CPU & the Fetch-Decode-Execute Cycle</span>
     <span class="resource-open">COMING SOON</span>
   </a>
   ```

   LIVE (remove `coming` class and change button text):
   ```html
   <a href="resources/ocr-gcse-cs/1-1-cpu-fde.html" class="resource-item">
     <span class="resource-name">CPU & the Fetch-Decode-Execute Cycle</span>
     <span class="resource-open">OPEN →</span>
   </a>
   ```

## How to add a predicted topic

Find the `ADD YOUR PREDICTED TOPICS HERE` comment and add:

```html
<a href="resources/ocr-gcse-cs/1-1-cpu-fde.html" class="flat-item pred">
  <div class="flat-info">
    <p class="flat-title">CPU & the Fetch-Decode-Execute Cycle</p>
    <p class="flat-sub">1.1 Systems Architecture</p>
  </div>
  <span class="flat-arrow">OPEN →</span>
</a>
```

## How to add an exam technique resource

Find the `ADD YOUR EXAM TECHNIQUE RESOURCES HERE` comment and add:

```html
<a href="resources/ocr-gcse-cs/wtm-paper1.html" class="flat-item exam">
  <div class="flat-info">
    <p class="flat-title">Walking Talking Mock — Paper 1</p>
    <p class="flat-sub">Full paper walkthrough</p>
  </div>
  <span class="flat-arrow">OPEN →</span>
</a>
```

## Deploying to Netlify

1. Go to netlify.com and log in
2. Drag the entire `staxwise` folder onto the deploy area
3. Done — your site updates immediately

To connect your custom domain:
- In Netlify: Site settings → Domain management → Add custom domain
- In your domain registrar: Add a CNAME record pointing to your Netlify URL
