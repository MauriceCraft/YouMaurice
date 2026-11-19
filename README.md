# YouMaurice

**YouMaurice** is a YouTube-inspired place to watch and share videos.

Live site: https://mauricecraft.github.io/youmaurice

## Features

- Browse community uploads and sample videos
- Watch videos in the built-in player
- Search by video title, creator, or description
- Filter by Learning, Music, Gaming, and Fun
- Create an account and sign in
- Upload videos to shared online storage
- View videos uploaded by the signed-in account
- Responsive layout for desktop, tablet, and mobile

## How it works

The website is hosted with GitHub Pages. Supabase provides accounts, the shared video database, and video storage.

- Supabase Auth handles sign-in and account creation.
- The `public.videos` table stores video details.
- The public Supabase Storage bucket named `videos` stores video files and optional thumbnails.
- Community uploads are loaded from Supabase, so they are not limited to the browser or device that uploaded them.

The current upload limit in the website is **6 MB per video**.

## Supabase setup

The site is configured to use the YouMaurice Supabase project. Its URL and publishable key are in `index.html`. A publishable key is intended for browser use; access must be controlled by Supabase Row Level Security and Storage policies.

The app expects the `public.videos` table to contain these columns:

| Column | Purpose |
| --- | --- |
| `id` | Video row ID |
| `user_id` | ID of the account that uploaded it |
| `title` | Video title |
| `channel_name` | Creator/channel name |
| `description` | Video description |
| `category` | Learning, Music, Gaming, or Fun |
| `video_path` | Path to the video in the `videos` bucket |
| `thumbnail_path` | Optional thumbnail path |
| `created_at` | Upload date |

For uploads and playback to work, configure Supabase so signed-in users can upload to the `videos` bucket, signed-in users can insert their own video rows, and visitors can read community video rows and the public video files. Keep Row Level Security enabled and restrict changes to each user's own rows. Do not put a Supabase service-role key in this website.

## Run locally

1. Clone or download this repository.
2. Open `index.html` in a modern browser, or serve the folder with a local web server.
3. Sign in or create an account.
4. Upload a small test video and check that it appears in the Community feed.

## Project files

```
YouMaurice/
├── index.html
└── README.md
```

## Troubleshooting

- **The page is blank:** check the browser console for JavaScript or network errors.
- **Sign-in fails:** check the Supabase Auth settings and email-confirmation requirements.
- **Videos do not load:** check that the `videos` bucket is public and that the table has a public read policy.
- **Uploads fail:** check the Storage upload policy, the table insert policy, and the 6 MB website limit.

## License

No license has been specified for this repository yet. Please check with the repository owner before reusing or redistributing the code.
