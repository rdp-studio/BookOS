X_LIBS		+= libxlibc.a \
			libuview.a libzlib.a libpng.a libjpeg.a \
			libxtk.a libfreetype.a libcairo.a libpixman.a

NAME		:= xtk
SRC			+= main.c

define CUSTOM_TARGET_CMD
echo [APP] $@; \
$(LD) $(X_LDFLAGS) $(X_OBJS) -o $@ $(patsubst %, -L%, $(X_LIBDIRS)) --start-group $(patsubst %, -l:%, $(X_LIBS)) --end-group; \
cp $@ $(srctree)/../develop/rom/usr/local
endef
