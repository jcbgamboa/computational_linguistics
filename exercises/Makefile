OUT_DIR=out
.PHONY:=all


all: $(foreach i,01 02 03 04 05 06 07 08 09 10,$(OUT_DIR)/$i_assignment.pdf)


out/%.pdf: %/assignment.tex
	mkdir -p $(OUT_DIR)
	pdflatex -output-directory=$(OUT_DIR) -shell-escape -jobname=$* $<
	pdflatex -output-directory=$(OUT_DIR) -shell-escape -jobname=$* $<
	pdflatex -output-directory=$(OUT_DIR) -shell-escape -jobname=$* $<

clean:
	rm -rf $(OUT_DIR)
