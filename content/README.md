# Installer content

`installer-content.json` is read by the Magic Lantern Installer (1.0.8+) at every launch. Editing it here changes the app for everyone within about 5 minutes, with no new release. If the file is invalid, the app ignores it completely and keeps the last good copy, or the content built into the release.

Every top-level key is optional. Leave one out to use the release's built-in version.

| Key | What it controls |
|---|---|
| `version` | Always `4`. |
| `promo` | Time-boxed promo (Black Friday etc). Use `null` for none. Has `startsAt`/`endsAt` (ISO), the orange `announcements` bar (`**bold**`, optional `from`/`until` per item), `headline` + orange `headlineAccent`, `subline`, `utmCampaign`, and per-product `badges`/`price`/`compareAt` keyed by product handle. |
| `shop` | The whole shop section on the final screen: up to 6 sections, each with `heading`, `description`, `collectionPath`, `collectionLabel` and 1–12 `products` (`handle`, `title`, `image`, optional `hoverImage`, `price`, `compareAt`, `badges`, `wide`). |
| `builds` | The build picker, in display order. Built-in builds that aren't listed are hidden. An entry with a built-in id (`filmatura`, `amit`, `filmgate`, `danne-tweaks`, `crop-mood`) overrides only the fields it sets. A new id adds a build and needs `label`, `description` and `githubRepo` (`owner/repo`); it installs that repo's latest GitHub release. Optional fields: `tagLabel`, `recommended` (the default pick), `previewImage` (banner) and `moreInfoUrl`. |

Rules the app enforces:
- Images must be `https://cdn.shopify.com/...`.
- Store links are paths like `/products/x`.
- `moreInfoUrl` must be https on github.com, magiclantern.fm or filmatura.com.
- Badge `tone` is `sale` (orange) or `info` (black).
- Each build card shows a tag: "Recommended" for the recommended build, otherwise its `tagLabel`. A build with no `tagLabel` shows "Not actively maintained", so set one, e.g. "Actively maintained" or "Experimental".
