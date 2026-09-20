# Muhammad Asim — Portfolio (Blazor WebAssembly)

A single-page portfolio site built with Blazor WebAssembly (.NET 8).

## Design

- **Concept:** editorial studio layout — serif headlines, brass accent, numbered sections, case-study work.
- **Palette:** near-black (`#0c0d10`), ivory type (`#f3efe6`), brass (`#c9a46a`).
- **Type:** Cormorant Garamond (display), Manrope (body), IBM Plex Mono (labels).
- Fully responsive, keyboard-focus visible, respects `prefers-reduced-motion`.

## Run locally

Requires the [.NET 8 SDK](https://dotnet.microsoft.com/download).

```bash
cd PortfolioApp
dotnet restore
dotnet run
```

Then open the URL shown in the terminal (typically `https://localhost:58433`).

## Edit your content

All page copy lives in `Pages/Home.razor` (`Jobs`, `Projects`, and `SkillGroups` plus the markup above). Styling lives in `wwwroot/css/app.css`.
