
gtkwave: test_top.vcd
	gtkwave test_top.vcd

test_top.vcd: test_top.vvp
	vvp -N test_top.vvp +vcd

test_top.vvp: test_top.sv ../../main/top.sv ../../main/prescaler.sv ../../main/cpu.sv
	iverilog -g2012 -o test_top.vvp test_top.sv ../../main/top.sv ../../main/prescaler.sv ../../main/cpu.sv

clean:
	rm -f test_top.vcd test_top.vvp
