CFLAGS = -g -I$(shell $(WASMER_DIR)/bin/wasmer config --includedir)
LDFLAGS = -Wl,-rpath,$(shell $(WASMER_DIR)/bin/wasmer config --libdir)
LDLIBS = $(shell $(WASMER_DIR)/bin/wasmer config --libs)

.SILENT: imports-exports imports-exports.o
imports-exports: imports-exports.o

.PHONY: clean
.SILENT: clean
clean:
	rm -f imports-exports.o imports-exports
