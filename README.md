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
## Asynchronous FIFO testbench results -<br/>
iverilog -o a test_memfifo_tb.v test_memfifo.v wfull.v rempty.v sync_r2w.v sync_w2r.v top_fifo.v fifo_mem.v<br/>
### C:\iverilog\bin>vvp a<br/>
![](https://github.com/MANISHBMK10/FIFO/blob/main/verilog.png)
### GTKWave Results -
![](https://github.com/MANISHBMK10/FIFO/blob/main/gtk_fifofinal.png)


# References
[http://www.sunburst-design.com/papers/CummingsSNUG2002SJ_FIFO1.pdf](url)
