# First In First Out (FIFO) Buffer 
 Asynchronous FIFO implementation

![](https://github.com/seetalpot/Asynchronous-FIFO/blob/main/FIFO-image.jpg)
 
 # Simulation
 Icarus Verilog (iVerilog) was used for simulation.  
 
## Asynchronous FIFO modules

**test_memfifo_tb.v** - Test bench. 

**test_memfifo.v** - The high-level module instantiates the FIFO (below module) along with the boundary logic needed to interface with the memory. <br />

**top_fifo.v** - This module instantiates all the below modules. <br />

**sync_r2w.v** - Synchronizes read pointer to write pointer. <br />

**sync_w2r.v** - Synchronizes write pointer to read pointer. <br />

**rempty.v**  - Checks empty condition. <br />

**fifo_mem.v** - Uses memory for storing values for FIFOs. <br />

**wfull.v**    - Checks full condition. <br />

 
# Simulation Results

iverilog -o test_memfifo_tb test_memfifo_tb.v test_memfifo.v wfull.v rempty.v sync_r2w.v sync_w2r.v top_fifo.v fifo_mem.v<br/>

### Output on Console

vvp test_memfifo_tb

![](https://github.com/MANISHBMK10/FIFO/blob/main/verilog.png)

### GTKWave Waveform

gtkwave fifo3.vcd

![](https://github.com/MANISHBMK10/FIFO/blob/main/gtk_fifofinal.png)


# References

1. [http://www.sunburst-design.com/papers/CummingsSNUG2002SJ_FIFO1.pdf](url)

2. S. R. Hasan, S. F. Mossa, C. Perez and F. Awwad, "Hardware Trojans in asynchronous FIFO-buffers: From clock domain crossing perspective," 2015 IEEE 58th International Midwest Symposium on Circuits and Systems (MWSCAS), Fort Collins, CO, USA, 2015, pp. 1-4.
