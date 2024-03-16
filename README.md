# YouTube Video And Channel Archive.

Currently YouTube is the only supported site, but that might change.

this search engine finds all YouTube content ranging from deleted unlisted private current content.

all you have to do is enter a search phrase in the search bar and press search.

it also has a advanced search feature for searching for by year published date and filter by YouTube channel.

the video search engine also has a download feature on every video and channel on the bottom of each 
video and channel account profile avatar logo either way you could download a video or a entire channel
and save it for offline viewing.

Contributions are welcome!

## CLI tool
Currently no documentation exists for the CLI tool.

## Usage as a module
There are docstrings included in the module (it is contained in `lostmediafinder`), but no `setup.py` or PyPI package is currently included. This is because it is not yet 100% stable (and I plan on adding support for more websites soon).

## Frontend
### Running in Docker (recommended):
There is an included Dockerfile. I will figure out publishing to Docker Hub soon enough.

Instead of modiying the Hypercorn config, use `HYPERCORN_<VARIABLE_NAME>` environment variables; the config is setup to work with that.

A command like this should work (runs on port 8000; change the `-p` flag to `<whatever port you want>:8000` to change that):

```
docker run --restart=unless-stopped -p 8000:8000 -e GUNICORN_WORKERS=4 thetechrobo/findyoutubevideo
```

### Running outside of Docker (unsupported)
You should be able to check the Dockerfile for what it is doing during the build (it's a glorified shell script).

## Licence

Copyright (c) 2022-2024 TheTechRobo

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.

You may obtain a copy of the License at http://www.apache.org/licenses/LICENSE-2.0
