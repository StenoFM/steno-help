---
hide:
  - footer
---

# Podcasters

## Adding your show to Steno.fm

Our directory is powered by the [Podcast Index](https://podcastindex.org/). If your show isn’t already in the Index, [submit your feed here](https://podcastindex.org/add). There’s no separate submission process to be included in our directory.

## Adding transcripts

To display transcripts on your episode pages, we rely on the [`<podcast:transcript>`](https://github.com/Podcastindex-org/podcast-namespace/blob/main/docs/1.0.md#transcript) tag in your RSS feed. If your current host doesn’t support the transcript tag, switch to [one that does](https://blog.steno.fm/hosts/)!

## Getting featured in Explore

The homepage features collections of podcasts that support the transcript tag. Please submit your show for an existing collection or propose a new collection by emailing [hello@steno.fm](mailto:hello@steno.fm).

## Getting featured in Trending

The Trending page only includes episodes with a transcript tag in the feed and [the OP3 prefix](https://op3.dev/setup).


## Promoting your podcast

### Icon and Badges
You may use or adapt the Steno.fm [icon](https://nathangathright.github.io/podcast-badges/icons/stenofm.svg) and/or badges ([light](https://nathangathright.github.io/podcast-badges/badges/stenofm-light.svg) & [dark](https://nathangathright.github.io/podcast-badges/badges/stenofm-dark.svg)) to promote your podcast on Steno.fm.

### Linking
Steno.fm’s URLs rely on the show’s [`<podcast:GUID>`](https://github.com/Podcastindex-org/podcast-namespace/blob/main/docs/1.0.md#guid) and the episode’s `<guid>`. The episode GUID is hashed with a URL-safe variant of base64 encoding.
```
https://www.steno.fm/show/<podcastGUID>/episode/<episodeGUID>
```

## Technical Issues

### CORS

If you’re hosting your own transcripts, please ensure that `Access-Control-Allow-Origin: *` is present on the requested resource. Otherwise, browsers will not permit us to request the transcript.

### HTTPS

Browsers like Chrome refuse to serve mixed HTTP and HTTPS content. When we request an HTTP resource, the browser will try to retrieve it with HTTPS. If the feed refuses HTTPS connections, the audio won't play.
