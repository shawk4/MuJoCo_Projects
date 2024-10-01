# Compiler and flags
CC = g++
COMMON = -O2 -I../../include -I../../include/mujoco -I../../include/GLFW -L../../bin -mavx -pthread -Wl,-rpath,'$$ORIGIN'
LIBS = -lmujoco200 -lGL -lm -lglew -lglfw

# Source and target
SRC = main_ball.cc
OBJ = $(SRC:.cc=.o)
TARGET = ../../bin/ball_with_drag

# Default target
all: $(TARGET)

# Build target
$(TARGET): $(OBJ)
	$(CC) $(COMMON) $(OBJ) $(LIBS) -o $(TARGET)

# Compile source files into object files
%.o: %.cc
	$(CC) $(COMMON) -c $< -o $@

# Clean target
clean:
	rm -f *.o $(TARGET)

# #LINUX
# COMMON=-O2 -I../../include -I../../include/mujoco -I../../include/GLFW -L../../bin -mavx -pthread -Wl,-rpath,'$$ORIGIN'
# LIBS = -lmujoco200 -lGL -lm -lglew ../../bin/libglfw.so.3
# CC = g++

# #MAC
# # COMMON=-O2 -I../../include -L../../bin -mavx -pthread
# #LINUX
# COMMON=-O2 -I../../include -I../../include/mujoco -I../../include/GLFW -L../../bin -mavx -pthread -Wl,-rpath,'$$ORIGIN'
# LIBS = -lmujoco200 -lGL -lm -lglew ../../bin/libglfw.so.3
# CC = g++



# #MAC
# # COMMON=-O2 -I../../include -L../../bin -mavx -pthread
# # LIBS = -w -lmujoco200 -lglfw.3
# # CC = gcc
# #WINDOWS
# #COMMON=/O2 /MT /EHsc /arch:AVX /I../../include /Fe../../bin/
# #LIBS = ../../bin/glfw3.lib  ../../bin/mujoco200.lib
# #CC = cl

# ROOT = ball_with_drag

# all:
# 	$(CC) $(COMMON) main_ball.cc $(LIBS) -o ../../bin/$(ROOT)

# main.o:
# 	$(CC) $(COMMON) -c main_ball.cc

# clean:
# 	rm *.o ../../bin/$(ROOT)
