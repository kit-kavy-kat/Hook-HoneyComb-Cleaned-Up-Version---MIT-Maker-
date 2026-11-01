# Hook-HoneyComb-Cleaned-Up-Version---MIT-Maker-
Hello MIT this is my cleaned up version of Hook&HoneyComb. As a kid I used to alot of times delete my pre-coded packages and start from scratch alot. So for you all to see my full cleaned up version of Hook & Honeycomb I combined them all into a new account!

Basics: 

A browser-based crochet sketchbook for visual learners. Built around the idea of previewing simple patterns and experimenting with custom rows.

Included
Pattern parser: ch, sc, hdc, dc, tr; comma-separated groups; optional row labels.

Visual row builder, selectable stitch map, replacement/deletion, pattern undo/redo.

Three.js rotatable 3D preview, front/reset view, color palette, three visual yarn thickness presets.

Stitch-by-stitch playback, scrubber, row/stitch instruction label.

Named local projects, JSON import/export, PNG preview export.

Mobile layout, input validation, WebGL fallback message.

Parser tests and GitHub Pages build/deployment workflow.

Run
Use Node.js 22.12 or newer.

text
npm install
npm test
npm run dev
Open the address printed by Vite. For a production check:

text
npm run build
npm run preview
Commit package-lock.json after the first install. No API keys or backend required. Fonts load from Google Fonts with system fallbacks.

Publish on GitHub Pages
Upload the extracted contents so package.json and index.html are at the repository root. Include the hidden .github folder (it contains the workflow).

In repository Settings → Pages → Build and deployment, select GitHub Actions.

Push to main or run the workflow manually in Actions. The workflow installs dependencies, runs parser tests, builds, and deploys dist.

Check Actions for errors and the deployment URL. GitHub Pages must be available for your repository/account.

A Codespace can run npm install and npm run dev; open its forwarded Vite port. Otherwise run locally in a terminal.

Pattern syntax
text
Row 1: sc 12
Row 2: sc 4, dc 4, sc 4
Row 3: hdc 12
US terminology. Up to 30 rows, 40 stitches per row, and 600 total. Row labels do not reorder rows. Pattern history covers applied pattern edits, not color changes or project-file operations. Raw text edits are applied with Visualize; invalid text preserves the previous preview. Row builder first applies pending valid text.

Important limits
This is a flat, schematic stitch visualization, NOT a topology-correct crochet simulator or hook-motion tutorial. Stitches are separate decorative loop motifs; chains are illustrative. No connected yarn solving, increases, decreases, rounds, turning logic, repeats, physical density, tension, gauge, drape, or measured size. Playback uses left-to-right entered order in every row, not alternating crochet work direction. Rows are centered independently, and mixed-height rows use the tallest stitch for spacing. Display scale fits the preview; it is not a physical unit scale. Yarn presets alter tube radius, not real material properties.

Local saving is explicit, not automatic. Browser storage may be cleared or unavailable. Export JSON for durable backups. PNG exports the current visible 3D view, including partial playback, without page UI. No account sync, native mobile packaging, or App Store publication is included.

Verification
Parser tests are provided in tests/pattern.test.js. All five parser/validation test groups passed in the generation environment, and JavaScript syntax checks passed. Dependencies were not installed and no browser or production build was run, so do not treat this package as browser-tested or production-verified. Run npm test and npm run build, then check editing, playback, saving, importing, exporting and touch controls on your devices.

Story
I started learning crochet in eighth grade with help from my friend Emily. As a visual learner, I wanted a way to picture patterns before making them. Hook & HoneyComb grew from that idea. Emily's suggestion to explore different yarn densities inspired the visual yarn controls; real density and gauge modeling remain future work.
