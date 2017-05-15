# Makefile

# Variables
Objs=game.o drawer.o filemanipulator.o format.o timer.o keyboard.o mouse.o ciphers.o font.o sound.o music.o joystick.o \
		vector2.o intvector2.o gameobject.o image.o animation.o floatrectangle.o soundinstance.o
Codes=game.cpp drawer.cpp filemanipulator.cpp format.cpp timer.cpp keyboard.cpp mouse.cpp ciphers.cpp font.cpp sound.cpp \
		music.cpp joystick.cpp vector2.cpp intvector2.cpp gameobject.cpp image.cpp animation.cpp floatrectangle.cpp \
		soundinstance.cpp
Headers=game.h support.h drawer.h filemanipulator.h format.h timer.h keyboard.h mouse.h ciphers.h font.h sound.h \
		music.h joystick.h vector2.h intvector2.h gameobject.h image.h animation.h floatrectangle.h
Libs=-lSDL -lSDL_image -lSDL_mixer -lSDL_ttf

# Build the AGL library
release: $(Objs)
	g++ -shared -o ../lib/libagl.so $(Objs) $(Libs)

# Build the AGL library for debugging
debug:
	g++ -fPIC -c -g game.cpp
	g++ -fPIC -c -g drawer.cpp
	g++ -fPIC -c -g filemanipulator.cpp
	g++ -fPIC -c -g format.cpp
	g++ -fPIC -c -g timer.cpp
	g++ -fPIC -c -g keyboard.cpp
	g++ -fPIC -c -g mouse.cpp
	g++ -fPIC -c -g ciphers.cpp
	g++ -fPIC -c -g font.cpp
	g++ -fPIC -c -g sound.cpp
	g++ -fPIC -c -g soundinstance.cpp
	g++ -fPIC -c -g music.cpp
	g++ -fPIC -c -g joystick.cpp
	g++ -fPIC -c -g vector2.cpp
	g++ -fPIC -c -g intvector2.cpp
	g++ -fPIC -c -g gameobject.cpp
	g++ -fPIC -c -g image.cpp
	g++ -fPIC -c -g animation.cpp
	g++ -fPIC -c -g floatrectangle.cpp
	g++ -shared -g -o ../lib/libagl.so $(Objs) $(Libs)
	
# Build the objects
game.o: game.cpp game.h
	g++ -fPIC -c game.cpp
drawer.o: drawer.cpp drawer.h
	g++ -fPIC -c drawer.cpp
filemanipulator.o: filemanipulator.cpp filemanipulator.h
	g++ -fPIC -c filemanipulator.cpp
format.o: format.cpp format.h
	g++ -fPIC -c format.cpp
timer.o: timer.cpp timer.h
	g++ -fPIC -c timer.cpp
keyboard.o: keyboard.cpp keyboard.h
	g++ -fPIC -c keyboard.cpp
mouse.o: mouse.cpp mouse.h
	g++ -fPIC -c mouse.cpp
ciphers.o: ciphers.cpp ciphers.h
	g++ -fPIC -c ciphers.cpp
font.o: font.cpp font.h
	g++ -fPIC -c font.cpp
sound.o: sound.cpp sound.h
	g++ -fPIC -c sound.cpp
soundinstance.o: soundinstance.cpp sound.h
	g++ -fPIC -c soundinstance.cpp
music.o: music.cpp music.h
	g++ -fPIC -c music.cpp
joystick.o: joystick.cpp joystick.h
	g++ -fPIC -c joystick.cpp
vector2.o: vector2.cpp vector2.h
	g++ -fPIC -c vector2.cpp
intvector2.o: intvector2.cpp intvector2.h
	g++ -fPIC -c intvector2.cpp
gameobject.o: gameobject.cpp gameobject.h
	g++ -fPIC -c gameobject.cpp	
image.o: image.h image.cpp
	g++ -fPIC -c image.cpp
animation.o: animation.cpp animation.h
	g++ -fPIC -c animation.cpp
floatrectangle.o: floatrectangle.cpp floatrectangle.h
	g++ -fPIC -c floatrectangle.cpp

# Build the test application
test: test.cpp
	g++ -fpermissive -g -o test test.cpp -lagl

# Install the AGL library (for debug) on the system
install_debug:
	../install_debug.sh

# Install the AGL library on the system
install:
	../install.sh

# Uninstall the AGL library to the system
remove:
	../remove.sh

# Generates the AGL documentation
doc:
	doxygen doxyfile

# Cleans the directories, removing executables and objects
clean:
	rm $(Objs) test ../lib/*.so
