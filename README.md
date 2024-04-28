SIMULATION AND IMPLEMENTATION OF MULTIPLIER
**AIM: **
 To simulate and synthesis multiplier using vivado

**APPARATUS REQUIRED:**
vivado 2023.1
  
**PROCEDURE:**
1. Open Vivado: Launch Xilinx Vivado software on your computer.

2. Create a New Project: Click on "Create Project" from the welcome page or navigate through "File" > "Project" > "New".

3. Project Settings: Follow the prompts to set up your project. Specify the project name, location, and select RTL project type.

4. Add Design Files: Add your Verilog design files to the project. You can do this by right-clicking on "Design Sources" in the Sources window, then selecting "Add Sources". Choose your Verilog files from the file browser.

5. Specify Simulation Settings: Go to "Simulation" > "Simulation Settings". Choose your simulation language (Verilog in this case) and simulation tool (Vivado Simulator).

6. Run Simulation: Go to "Flow" > "Run Simulation" > "Run Behavioral Simulation". This will launch the Vivado Simulator and compile your design for simulation.

7. Set Simulation Time: In the Vivado Simulator window, set the simulation time if it's not set automatically. This determines how long the simulation will run.

8. Run Simulation: Start the simulation by clicking on the "Run" button in the simulation window.

9. View Results: After the simulation completes, you can view waveforms, debug signals, and analyze the behavior of your design.
**Logic Diagram**
2 bit Multiplier

![image](https://github.com/navaneethans/VLSI-LAB-EXP-3/assets/6987778/7713750f-65e6-41c0-8082-5005eac4031c)

**4 Bit Multiplier**

![image](https://github.com/navaneethans/VLSI-LAB-EXP-3/assets/6987778/d95215dd-8cf1-4e08-93cc-96adfdd7fbdc)


**Verilog code**
2 bit Multilpier
~~~
module ha(a,b,sum,c);

input a,b;

output sum,c;

xor g1(sum,a,b);

and g2(c,a,b);

endmodule

module bitmultiplier(a,b,c);

input [1:0]a,b;

output[3:0]c;

wire w1;

and g1(c[0],b[0],a[0]);

ha ha1(a[0]&b[1],a[1]&b[0],c[1],w1);

ha ha2(a[1] &b[1],w1,c[2],c[3]);

endmodule
~~~

**Output Waveform**

<<< Simulation output waveform paste it here >>>>>


**Result**



