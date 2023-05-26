SOURCE=tickets
TARGET=$(SOURCE)
ENGINE=pdflatex

all: $(TARGET)

$(TARGET): *.tex preamble.sty
	pdflatex -jobname=$(TARGET) $(SOURCE)
	pdflatex -jobname=$(TARGET) $(SOURCE)

clean:
ifeq ($(OS),Windows_NT)
	del /F /S /Q $(TARGET).pdf $(wildcard *.toc) $(wildcard *.synctex.gz) $(wildcard *.out) \
	$(wildcard *.log) $(wildcard *.aux)
else
	rm -rf $(TARGET).pdf $(wildcard *.toc) $(wildcard *.synctex.gz) $(wildcard *.out) \
	$(wildcard *.log) $(wildcard *.aux)
endif