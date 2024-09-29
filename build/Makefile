# Variables
CC = gcc
CFLAGS = -Wall -I../include
SRC = ../src
OBJ = ../obj
BIN = battery_saver
OBJS = $(OBJ)/main.o $(OBJ)/cpu_control.o $(OBJ)/brightness_control.o $(OBJ)/service_control.o $(OBJ)/utils.o
DEPS = ../include/cpu_control.h ../include/brightness_control.h ../include/service_control.h ../include/utils.h

# Targets
$(BIN): $(OBJS)
	$(CC) $(CFLAGS) -o $(BIN) $(OBJS)

$(OBJ)/%.o: $(SRC)/%.c $(DEPS)
	mkdir -p $(OBJ)
	$(CC) $(CFLAGS) -c $< -o $@

# Clean up build
clean:
	rm -rf $(OBJ)/*.o $(BIN)

# Phony targets
.PHONY: clean
