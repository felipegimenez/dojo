.PHONY: tests clean

tests: tests/check
	@./tests/check

clean:
	@rm -f tests/*.o src/*.o tests/check

src/stack.o: src/stack.c src/stack.h
	gcc -c $< -o $@

tests/check_stack.o: tests/check_stack.c
	gcc -c $< -o $@

tests/check: src/stack.o tests/check_stack.o
	gcc $^ -lcheck -o tests/check
