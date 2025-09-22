# Усложненный make-file.  Введены переменные для параметров компиляции и исполняемых файлов

.PHONY: all debug release clean

RELEASE_FLAGS = -O2 -Wall -DNDEBUG
DEBUG_FLAGS   = -g -O0 -Wall
RELEASE_EXEC  = hello
DEBUG_EXEC    = hello-dbg
SOURCE        = hello.cpp  # <-- ДОБАВЛЕНА ПЕРЕМЕННАЯ ДЛЯ ИМЕНИ ФАЙЛА

all: debug release

debug: $(DEBUG_EXEC)

$(DEBUG_EXEC): $(SOURCE)        # <-- ИСПОЛЬЗУЕМ ПЕРЕМЕННУЮ
	g++ $(DEBUG_FLAGS) $(SOURCE) -o $(DEBUG_EXEC)  # <-- ИСПОЛЬЗУЕМ ПЕРЕМЕННУЮ

release: $(RELEASE_EXEC)

$(RELEASE_EXEC): $(SOURCE)      # <-- ИСПОЛЬЗУЕМ ПЕРЕМЕННУЮ
	g++ $(RELEASE_FLAGS) $(SOURCE) -o $(RELEASE_EXEC)  # <-- ИСПОЛЬЗУЕМ ПЕРЕМЕННУЮ

clean:
	rm -f $(RELEASE_EXEC) $(DEBUG_EXEC)
