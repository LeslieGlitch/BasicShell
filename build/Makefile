SHELL := /bin/bash

# Executable name
TARGET = my_shell

# Source files
SRCS = ../myshell.c

# Default target
all: $(TARGET)

# Build the executable
$(TARGET): $(SRCS)
	$(CC) $(CFLAGS) -o $(TARGET) $(SRCS)

# Run the application with warning message
run: $(TARGET)
	@echo "Run shell"
	@echo "[ATTENTION: TERMINAL SHOULD PRINT \"500\" BELOW. CANCEL OPERATION AND RUN \"ulimit -u 500\" IF IT SAYS \"unlimited\"!]"
	@bash -c "ulimit -u" && ./$(TARGET)

# Clean build files
clean:
	rm -f $(TARGET)
