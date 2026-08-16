# Muhammad Asim — Portfolio (Blazor WebAssembly)

A single-page portfolio site built with Blazor WebAssembly (.NET 8).

## Design

- **Concept:** the hero is a mock code editor showing a C# class that
  describes you (`MuhammadAsim.cs`) — a signature grounded in your own
  craft rather than a generic photo/tagline hero.
- **Palette:** near-black navy background (`#0d0f16`), .NET-brand-adjacent
  violet accent (`#8a6bff`), teal for section labels/types (`#45d9c4`),
  amber for string/number highlights.
- **Type:** Space Grotesk (display), Inter (body), JetBrains Mono (code,
  labels, eyebrows).
- Fully responsive, keyboard-focus visible, respects
  `prefers-reduced-motion`.

## Run locally

Requires the [.NET 8 SDK](https://dotnet.microsoft.com/download).

```bash
cd PortfolioApp
dotnet restore
dotnet run
```

Then open the URL shown in the terminal (typically `https://localhost:5001`).

## Edit your content

All page copy — experience, projects, skills, contact info — lives in
`Pages/Home.razor`, in the `@code` block at the bottom (the `Jobs`,
`Projects`, and `SkillGroups` arrays) and inline in the markup above it.
Styling lives in `wwwroot/css/app.css`.

Your resume file is included at `wwwroot/files/Muhammad_Asim_Resume.docx`
and is wired to the "Download CV" button on the hero. Replace that file
any time you update your resume — the filename must stay the same, or
update the `href` in `Pages/Home.razor`.

## Deploy for free

**GitHub Pages**
```bash
dotnet publish -c Release
# then follow: https://learn.microsoft.com/aspnet/core/blazor/host-and-deploy/webassembly/github-pages
```

**Azure Static Web Apps** — connect your GitHub repo in the Azure portal;
it detects Blazor WASM automatically and builds/deploys on every push.

**Netlify** — set build command to `dotnet publish -c Release -o build`
and publish directory to `build/wwwroot`.
