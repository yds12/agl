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
sudo apt-get install libsdl1.2-dev
sudo apt-get install libsdl-mixer1.2-dev
sudo apt-get install libsdl-ttf2.0-dev
sudo apt-get install libsdl-image1.2-dev
```

Now we can just compile AGL and put the files in their places.
Clone this repository or download the files. In the terminal, `cd` to the
root directory of the repository and type (this will create some necessary
directories and copy the headers):

```
sudo mkdir /usr/include/agl/
sudo cp -Rap src/*.h /usr/include/agl/
mkdir lib
```

Now `cd` to the `src` directory and type (to compile and install AGL):

```
make agl          (or make debug for a lib prepared for debug)
sudo cp -Rap ../lib/*.so /usr/lib/
```

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
