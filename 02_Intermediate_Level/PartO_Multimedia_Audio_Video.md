# 🅾️ PART O: MULTIMEDIA — AUDIO & VIDEO

## 📖 Theory (from PDF)

> The HTML `<audio>` and `<video>` tags are used to embed media (audio and video files) directly into a webpage. They provide a simple way to include multimedia content with **built-in controls** such as play, pause, volume, and more.

## Video (from PDF)

> If you want to add video in HTML page, use `<video>` tag. The **controls** attribute adds video controls like play, pause, and volume. **width** and **height** define video dimensions. **source** allows us to specify video files — we can add alternative files.

### Video Attributes (from PDF):
| Attribute | Description |
|-----------|-------------|
| `controls` | Adds play/pause/volume controls |
| `autoplay` | Starts playing automatically |
| `width/height` | Dimensions |
| `src` (via `<source>`) | Source of video |
| `type` (via `<source>`) | Type of source |

```html
<!-- Video example from PDF -->
<video width="320" height="240" controls>
    <source src="video.mp4" type="video/mp4">
    Your browser does not support the video element.
</video>

<!-- Advanced video with multiple sources -->
<video controls autoplay muted loop poster="thumbnail.jpg"
       width="640" height="360" preload="metadata">
    <source src="video.webm" type="video/webm">
    <source src="video.mp4" type="video/mp4">
    <source src="video.ogg" type="video/ogg">
    <track src="subtitles_en.vtt" kind="subtitles" srclang="en" 
           label="English" default>
    <p>Your browser doesn't support HTML5 video. 
       <a href="video.mp4">Download the video</a>.</p>
</video>
```

## Audio (from PDF)

> If you want to add audio in HTML page, use `<audio>` tag. The **controls** attribute adds audio controls like play, pause, and volume. **source** allows us to specify audio files. To add autoplay, add the `autoplay` attribute.

```html
<!-- Audio example from PDF -->
<audio width="320" height="240" controls>
    <source src="audiofile.mp3" type="audio/mpeg" autoplay>
    <source src="audiofile.ogg" type="audio/ogg">
    Your browser does not support the audio element.
</audio>

<!-- Clean audio example -->
<audio controls preload="metadata">
    <source src="song.ogg" type="audio/ogg">
    <source src="song.mp3" type="audio/mpeg">
    <p>Your browser doesn't support HTML5 audio.</p>
</audio>
```

## All Video/Audio Attributes

| Attribute | Description |
|-----------|-------------|
| `controls` | Show play/pause/volume controls |
| `autoplay` | Start playing automatically |
| `muted` | Mute audio (**required for autoplay** in most browsers) |
| `loop` | Loop the media |
| `poster` | (Video only) Image shown before video plays |
| `preload` | `none`, `metadata`, or `auto` |
| `playsinline` | Play inline on mobile (not fullscreen) |

> ⚠️ **Note from PDF:** To add the autoplay feature, add the `autoplay` attribute. But most modern browsers require `muted` along with `autoplay` for it to work.

---

