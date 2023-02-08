---
hide:
  - footer
---

# Why can’t Steno.fm display my transcript?

Provided that the publisher [has included a transcript in the RSS feed](https://help.steno.fm/Why-is-this-episode-missing-a-transcript-f5d93c7b7f6e48afaeebf527cacc255b), we do our best to display it on [Steno.fm](http://steno.fm). Occasionally, some issues will prevent us from offering an ideal user experience. If you run into an issue other than the ones below, please reach out to our email address.

## No 'Access-Control-Allow-Origin' header is present on the requested resource.

This error means that the server hosting the transcript lacks [a CORS header](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Access-Control-Allow-Origin) permitting [Steno.fm](http://steno.fm) to request the file from the visitor’s browser. Add a `Access-Control-Allow-Origin: *` header to the server where the transcript file is hosted.
