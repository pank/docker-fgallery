docker-fgallery
===============

A Dockerfile for installing fgallery.

fgallery is a static image gallery generation script, it takes images from a directory and generates a static HTML page
with the images displayed in a slideshow. It can be found at:

http://www.thregr.org/~wavexx/software/fgallery/

Usage
-----

To use this image, just do:

    docker build -t stavrosk/fgallery .
    docker run -i -v <mountpath>:/fgallery/gallery/ -t stavrosk/fgallery

That will mount "mountpath" in the container and allow you to run fgallery on it. Just move the output directory to
mountpath when done, and you'll have the resulting gallery ready to use.

Initially based on
the [image](https://github.com/skorokithakis/docker-fgallery) by
skorokithakis. 

I use it to create galleries
via [Gitlab Pages](https://gitlab.com/pank/sample-fgallery).  Thus, I
have tried to minimize the size (I welcome tips to make it smaller).
