# Waveform Analysis Start

## Partitions

```
tb
|
|-dut
| |-cpu
| |-mem
|-clock_gen
|-APB_vip
```

## clock

following is a list of clock signals there frequencies and duration time (start time to end time)

|clock signal name| path | Frequency | Start time | End time |
|-----------------|------|-----------|------------|----------|
| cpu_clk         | tb   | 1Ghz      | start at 10ns | simulation end  |
tb.mem_clk 500Mhz start at 100ns to end  
tb.clock_gen.cpu_clk 1Ghz start at 10ns to end  
tb.clock_gen.mem_clk 500Mhz start at 100ns to end  
tb.dut.cpu_clk 1Ghz start at 10ns to end  
tb.dut.mem_clk 500Mhz start at 100ns to end  

## Reset

tb.cpu_rst_n 1Ghz start at 1`b0, deassert to 1'b1 at 100ns  
tb.mem_rst_n 500Mhz start at 1`b0, deassert to 1'b1 at 100ns  
tb.clock_gen.cpu_rst_n start at 1`b0, deassert to 1'b1 at 100ns  
tb.clock_gen.mem_rst_n start at 1`b0, deassert to 1'b1 at 100ns  
tb.dut.cpu_rst_n start at 1`b0, deassert to 1'b1 at 100ns  
tb.dut.mem_rst_n start at 1`b0, deassert to 1'b1 at 100ns  

## Constants

tb.dut.cpu.interrupt_vec 0xFFFF0000  

### Wires that are constant 1`b0

tb.dut.cpu.irq  

### Wires that are constant 1`b1

tb.dut.cpu.pc_en  

### Wires that are constant 1`bX

tb.dut.gpio0  



# Waveform Analysis End
