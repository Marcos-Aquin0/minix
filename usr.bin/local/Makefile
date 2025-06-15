# Nome do executável do seu programa
EXECUTABLE = teste_processos

# Valores padrão para os argumentos (você pode sobrescrever via linha de comando)
NUM_ITERATIONS ?= 100
ARG2 = 1000000
ARG3 = 100000000

# Nome padrão do arquivo de saída (você pode sobrescrever via linha de comando)
OUTPUT_FILE ?= resultados_01.txt

.PHONY: all run clean

all: $(EXECUTABLE)

$(EXECUTABLE): teste_processos.c
	gcc -o $(EXECUTABLE) teste_processos.c

run: $(EXECUTABLE)
	./$(EXECUTABLE) $(NUM_ITERATIONS) $(ARG2) $(ARG3) > $(OUTPUT_FILE)
	@echo "Execução concluída. Saída salva em $(OUTPUT_FILE)"

clean:
	rm -f $(EXECUTABLE) *.txt