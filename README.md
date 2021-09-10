# VC-VIDEO-EDITOR

## Overview

A simple web application can edit videos with features for those who want to create a short video or they are don't have a powerful computer to install a video editor

## How does it work

We can edit the video in the browser then encode it in the server. Also, we are may consider editing and encoding the video
in browser with WebAssembly, I have an example of how it works [ffmpegwasm](https://ffmpegwasm.netlify.app/)

## How does it work in the browser

I have an idea to build multiple layers above the video, one layer can be an element, a text,... To create the layer, I think use canvas instead of virtual DOM

## How does it work in the server

The client sends layers info and the server use layers to encode video with FFmpeg

## Features

- [x] Cut video
- [x] Insert video
- [x] Add image
- [x] Add text
- [ ] Add audio
- [ ] Add filters
- [ ] Add subtitle
- [ ] Add effects

```typescript
interface ILayer {
  coordinates: {
    x: number;
    y: number;
  }[];
  size: {
    width: number;
    height: number;
  };
  time: {
    start: number;
    end: number;
  };
  //  ...
}

interface ITextLayer extends ILayer {
  // .....
}
```
