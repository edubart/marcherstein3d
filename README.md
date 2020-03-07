# Pseudo 3D via 2D Ray Marching

This an experiment to render 3D scenes using ray marching on 2D signed distance fields (SDFs)
in real time using only on the CPU and with some lightning support.

Check this project running on the browser [here](https://edubart.github.io/marcherstein3d/).

This was inspired by [Wolfenstein 3D](https://en.wikipedia.org/wiki/Wolfenstein_3D) rendering technique and [Inigo Quilez](https://www.iquilezles.org/www/index.htm) ray marching articles.

## How it works

The renderer is ray marching on a 2D plane and outputting the scene depth and colors to a single line. Then the line is stretched vertically proportionally to its depth. The lightning
is done in 2D but can be viewed in 3D.

Similar technique was used in the game Wolfenstein 3D back in 1992 to render a
pseudo 3D on low end hardware. However I've introduced ray marching into the idea, this
permits to have some lightning and morph objects across the XZ plane while still
allowing to render in realtime on the CPU.
