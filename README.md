# Aleva Game Library - AGL

AGL is a game library designed to support the task of developing games
in C++. It relies on SDL.

The total AGL is composed of this base lib, plus these other ancilary libs:

- [AGL Graphics](http://github.com/yds12/agl-graphics)
- [AGL Motion](http://github.com/yds12/agl-motion)
- [AGL Mapping](http://github.com/yds12/agl-mapping)
- [AGL Forms](http://github.com/yds12/agl-forms)
- [AGL Text](http://github.com/yds12/agl-text)
- [AGL Net](http://github.com/yds12/agl-net)

## Compiling and Installing AGL

First, install the dependencies (SDL development files): the  
base SDL library (the first version, not SDL 2), SDL mixer, SDL ttf and 
SDL image. In Ubuntu 16.04, for example, you can type this:

```
sudo apt-get install libsdl1.2-dev libsdl-mixer1.2-dev libsdl-ttf2.0-dev libsdl-image1.2-dev
```

Now installing AGL is easy. Just type the following in a terminal 
(from the `src` directory):

```
make install
```

This will install the library for use and development. If you want to use
AGL for development you can type `make install_debug` instead, to install
it with debug symbols.

## Testing

If you have also installed AGL Graphics, you can compile and run a test
program (located in the `src` directory):

```
make test
./test
```

## Notes

Do not use the `sh` files. They are old and consider that the project folder
is `~/aleva/agl/agl`.
