# npmrunpodcast website

Hugo website

### Quickstart

```
brew install hugo
git clone git@github.com:runpodcast/website.git runpodcastwebsite
cd runpodcastwebsite
hugo server

# collect static assets for next post
cp ../runpodcastaudio/src/0.1.2-auth-mid.mp3 static/post/
cp ~/Downloads/0.1.2-auth-mid.jpg static/post/

# create next post
hugo new post/e0-1-2-auth-mid.md
vim content/post/e0-1-2-auth-mid.md
```

### Deploy

Install [this tool](https://github.com/bep/bego.io) to make deploy to s3 a snap.

Then use `hugo` to build the static site and `s3deploy` to put it onto s3 (assuming you have permission)

```
hugo && s3deploy -source=public/ -region=us-east-1 -bucket=npmrunpodcast.com -key=****** -secret=******
```
