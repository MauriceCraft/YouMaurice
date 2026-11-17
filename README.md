# YouMaurice

<div align="center">
  <h2>A simple place to watch and share videos</h2>
  <p>Browse sample videos, search by title or creator, and publish your own video posts from your browser.</p>
  <p><a href="https://github.com/MauriceCraft/YouMaurice">View the repository</a></p>
</div>

---

## About

YouMaurice is a lightweight, YouTube-inspired video website built with HTML, CSS, and JavaScript. It has a video feed, a watch player, category filters, search, and a form for creating video posts.

The current version is a front-end prototype. It runs in your browser and does not yet have accounts, a server, or a shared online video library.

## Features

| Feature | What it does |
| --- | --- |
| Video feed | Browse the sample videos shown on the home page |
| Video player | Open a video and watch it with the built-in player |
| Search | Find videos by title, creator, or description |
| Categories | Filter videos by Learning, Music, Gaming, or Fun |
| Create videos | Add a title, channel name, description, category, video, and optional thumbnail |
| My videos | See the videos you have saved in your browser |
| Responsive layout | Use the site on desktop, tablet, or mobile screens |

## Getting started

You do not need to install anything.

1. Download or clone this repository.
2. Open `index.html` in a modern web browser.
3. Browse the sample videos or select **Create** to add a video.
4. Open **My videos** to see your saved uploads.

For the best experience, use a recent version of Chrome, Safari, Firefox, or Edge.

## How video uploads work right now

This version stores uploaded videos in your browser using IndexedDB.

- Your uploads are saved on the device and browser where you created them.
- Other people cannot see your uploads.
- Clearing the browser's site data may remove saved videos.
- Keep a separate copy of your original video files.

The current upload limit is 150 MB per video.

## Built with

- **HTML** for the page structure
- **CSS** for the layout and styling
- **JavaScript** for search, filtering, the video player, and uploads
- **IndexedDB** for saving videos locally in the browser

## Project structure

```
YouMaurice/
├── index.html
└── README.md
```

## What's next

YouMaurice is an early prototype. A future version could add user accounts, online video hosting, public creator channels, comments, likes, and a genuinely shared video feed.

## Contributing

Ideas and improvements are welcome. You can open an issue to report a bug or suggest a feature, or submit a pull request with a change.

## License

No license has been specified for this repository yet. Please check with the repository owner before reusing or redistributing the code.
