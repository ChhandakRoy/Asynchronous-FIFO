# Asynchronous-FIFO
Verilog Implementation of Parameterized and Synthesizable Asynchronous FIFO

The FIFO has been parameterized in DEPTH and WIDTH dimension.
     The Asynchronous FIFO does Read and Write ops in 2 different clock cycles, rd_clk and wr_clk, because of this Clock Domain crossing techniques use to update FULL and EMPTY condition, here we have employed the following parameters to avoid metastability and corrupt result due to domain crossing:
            1.  Binary to Gray converter .
           2.  2-Flop synchronizer.
We have transferred wr_ptr to read domain to generate Empty and rd_ptr to write domain to generate Full condition.

