CC = gcc
CFLAGS = -Iinclude -Wall -Wextra -O2
SRC = src/canvas.c src/math3d.c src/renderer.c src/soccer_loader.c src/lighting.c src/animation.c demo/main.c
TESTS = tests/test_math.c
TEST_OUT = tests/test_math
OUT = build/demo

all: $(OUT)

$(OUT): $(SRC)
	$(CC) $(CFLAGS) $(SRC) -o $(OUT) -lm

test_math: src/canvas.c src/math3d.c tests/test_math.c
	$(CC) $(CFLAGS) -o $(TEST_OUT) src/canvas.c src/math3d.c tests/test_math.c -lm
RENDER_OUT = build/renderer_demo
render_demo: src/canvas.c src/math3d.c src/renderer.c src/soccer_loader.c src/lighting.c src/animation.c demo/main.c
	$(CC) $(CFLAGS) -o $(RENDER_OUT) \
	src/canvas.c src/math3d.c src/renderer.c \
	src/soccer_loader.c src/lighting.c src/animation.c \
	demo/main.c -lm

clean:
	rm -f $(OUT) $(TEST_OUT)