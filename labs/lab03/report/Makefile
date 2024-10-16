# Определяем файлы, которые будут конвертированы
FILES := $(patsubst %.md, %.docx, $(wildcard *.md)) \
         $(patsubst %.md, %.pdf, $(wildcard *.md))

# Определяем формат для LaTeX и фильтр
LATEX_FORMAT := --pdf-engine=lualatex --pdf-engine-opt=--shell-escape
FILTER := --filter pandoc-crossref

# Правила для конвертации .md в .docx
%.docx: %.md
	pandoc "$<" $(FILTER) -o "$@"

# Правила для конвертации .md в .pdf
%.pdf: %.md
	pandoc "$<" $(LATEX_FORMAT) $(FILTER) -o "$@"

# Основная цель, которая запускает конвертацию всех файлов
all: $(FILES)
    @echo "Скомпилировано: $(FILES)"

# Очистка сгенерированных файлов
clean:
	rm -f $(FILES)
	@echo "Очистка завершена."
