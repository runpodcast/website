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
