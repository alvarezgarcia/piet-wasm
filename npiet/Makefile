COMPONENTS_DIR=../components
NPIET_OUTPUT_BIN=npiet

all: build install

build:
	zig build-exe \
		-lc \
		-D_WASI_EMULATED_SIGNAL \
		-O ReleaseSmall \
		-target wasm32-wasi \
		--name $(NPIET_OUTPUT_BIN) \
		npiet-1.3f.c 

install:
	mv $(NPIET_OUTPUT_BIN).wasm $(COMPONENTS_DIR)
