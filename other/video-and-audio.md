---
description: >-
  Which player Kalium uses for video and audio, and how autoplay, repeat and
  YouTube behave.
---

# Video and Audio

Kalium replaces WordPress's plain media player with a themed one, so video and audio match the rest of your site rather than looking like a browser default.

The settings are at **Appearance -> Customize -> General -> Media**, and they apply to **every** video and audio on your site at once.

***

### Media Player

**Video.js** — Kalium's themed player. This is the default, and it's what makes video match your site's styling. It only loads when a video actually scrolls into view, so it costs nothing on pages without one.

**Browser Native** — the player built into the visitor's browser. Different on every browser, but the lightest option.

Stay on **Video.js** unless you have a reason not to.

***

### Player Skin

Only appears when **Media Player** is Video.js.

**Minimal** — a clean, understated set of controls. The default.

**Standard** — the fuller control bar.

***

### Autoplay Videos

**Disable** — videos wait for the visitor to press play. The default, and the safest.

**Always** — videos start on page load.

**When Visible on Viewport** — videos start when they scroll into view. **This is the one to use** if you want autoplay at all.

{% hint style="warning" %}
**Browsers block autoplay with sound.** Kalium mutes autoplaying media for you so it will actually start — otherwise browsers would simply refuse.

**Always** frequently doesn't work as expected, because a browser may decline to play a video the visitor hasn't scrolled to yet. **When Visible on Viewport** is far more reliable.
{% endhint %}

***

### Auto Repeat

Restarts video or audio from the beginning when it finishes.

Good for a short background clip. Irritating for anything with sound.

***

### Default YouTube Player

Only appears when **Media Player** is Video.js.

**On** — YouTube videos use YouTube's own player, with its branding and suggested videos at the end.

**Off** — YouTube videos use Kalium's player, matching everything else on your site.

***

### Overriding these on one video

The site-wide settings apply everywhere, but **an attribute on an individual shortcode always wins**. So you can autoplay one video without autoplaying all of them:

```
[video src="film.mp4" autoplay="on-viewport" playsinline="yes"]
```

Kalium adds several attributes WordPress doesn't have, including `playsinline` (play inline on iPhone rather than going fullscreen), `object_fit`, and `poster` on audio.

{% content-ref url="shortcodes.md" %}
[shortcodes.md](shortcodes.md)
{% endcontent-ref %}

***

### Common questions

**Every video on my site autoplays.**\
That's **Autoplay Videos** here, not the individual videos.

**A video won't autoplay.**\
Browsers block audible autoplay. Kalium mutes autoplaying media so it can start — unless you've set `muted="false"` yourself. Prefer **When Visible on Viewport**.

**The video looks different in the editor than on the site.**\
Expected. Kalium deliberately leaves the editor's media preview alone, so you see the plain player there and the themed one on your site. Check the front end.

**My audio player is tiny.**\
Without a poster image, audio defaults to a narrow bar. Give it a `width`, or a `poster`.

**Videos are slow to load.**\
Host long videos on YouTube or Vimeo rather than uploading them to your site. Self-hosted video is the heaviest thing most sites serve.

{% content-ref url="performance.md" %}
[performance.md](performance.md)
{% endcontent-ref %}
