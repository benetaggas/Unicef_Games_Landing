# Road Safety Project — Landing Page

Static hub page that links to the three Unity WebGL game builds.

## Expected deployment layout

Host this folder's contents at the web root, with each game built into its own
subfolder next to `index.html`:

```
/ (web root)
├── index.html          ← this landing page
├── assets/             ← thumbnails used by the landing page
│   ├── game1.png
│   ├── game2.png
│   ├── game3.png
│   └── game4.png
├── game1/              ← Unity WebGL build of "Ready to Road"
│   └── index.html
├── game2/              ← Unity WebGL build of "Looking at the Road"
│   └── index.html
└── game3/              ← Unity WebGL build of "Sort that Sign!"
    └── index.html
```

## Building each game

Each game is a set of scenes inside the single Unity project. Build them one at a
time, swapping the **Scenes In Build** list (File ▸ Build Settings) before each
WebGL build:

| Folder  | Game                | Scenes (first = start scene)                                   |
|---------|---------------------|---------------------------------------------------------------|
| `game1` | Ready to Road       | `Game1Menu`, `CharacterSelect`, `HowToPlay`, `Game`, `Score`  |
| `game2` | Looking at the Road | `Game2`                                                       |
| `game3` | Sort that Sign!     | `Game3`                                                       |

The 4th card ("Drive Safe!", Classes 11-12) is shown disabled as *Coming soon*
until that game exists.

## Notes
- The card links are relative, so the hub works from any base URL.
- Game thumbnails live in `assets/` (copied from `Assets/LandingPageUI/`); replace
  those files to update the artwork without touching `index.html`.
