# Boolean-Gate-Circuit-Schematic-Simulation-and-Layout

A transistor-level gate that implements the Boolean expression (AB+C)'
![Boolean_gate_schematic](https://github.com/NSaroya/Boolean-Gate-Circuit-Schematic-Simulation-and-Layout/assets/156468713/a050d24f-a459-4273-99c5-a3b908f2bed9)

A testbench with two of the inputs grounded, and vpulse for the remaining input such that toggling this input changes the voltage of the output. 
![Boolean_gate_schematic_TB2](https://github.com/NSaroya/Boolean-Gate-Circuit-Schematic-Simulation-and-Layout/assets/156468713/ceb73451-83e2-489a-877c-7c634fd41f07)

Pulse Source Configuration

- **Voltage 1:** 0V
- **Voltage 2:** 1V
- **Period:** 200p
- **Delay time:** 100p
- **Rise time:** 10p
- **Fall time:** 10p
- **Pulse width:** 100p

### Propagation Delays

Propagation delay for a 1->0 and 0->1 transition with the two inputs grounded as previously the propagation delay for a 1->0 and 0->1 transition 

| Transition | Propagation Delay |
|------------|-------------------|
| 1 to 0     | 11.7982p          |
| 0 to 1     | 10.1248p          |

In Cadence Virtuoso, the optimization of the PMOS width for equal rise and fall times in a CMOS inverter can be achieved by performing a parametric analysis. This involves setting up the simulation to sweep the NMOS and PMOS widths, turning off unnecessary measures, and running transient simulations while sweeping the boolean gate's NMOS and PMOS widths to analyze the output power, rise time, and fall time. 

**Rise and Fall Times with Optimal PMOS width**

| Condition | Rise Time    | Fall Time    |
|-----------|--------------|--------------|
| SS        | 10.551p      | 10.994p      |
| FF        | 7.81126p     | 7.87958p     |
| TT        | 8.9227p      | 8.97476p     |
| FS        | 9.56309p     | 8.35136p     |
| SF        | 8.52932p     | 10.0906p     |

**Rise and Fall Times with propagation delays for different test cases**

![Screenshot from 2024-01-29 10-48-11](https://github.com/NSaroya/Boolean-Gate-Circuit-Schematic-Simulation-and-Layout/assets/156468713/e8634820-5ca6-4f64-a043-b9ad9b085979)

| Node (Signal) | Rise Time           | Fall Time           | Rising Propagation Delay | Falling Propagation Delay |
|---------------|---------------------|---------------------|--------------------------|---------------------------|
| 1 (A)          | 8.9227p             | 8.97476p            | 9.01583p                 | 9.45904p                  |
| 2 (B)          | 17.7278p            | 17.935p             | 19.6061p                 | 19.7966p                  |
| 3 (C)          | 13.196p             | 18.0695p            | 15.8678p                 | 15.8328p                  |

![Screenshot from 2024-01-29 10-49-30](https://github.com/NSaroya/Boolean-Gate-Circuit-Schematic-Simulation-and-Layout/assets/156468713/0a639f5a-9492-43ad-9a4b-a3aab5108ebb)


| Node (Signal) | Rise Time           | Fall Time           | Rising Propagation Delay | Falling Propagation Delay |
|---------------|---------------------|---------------------|--------------------------|---------------------------|
| 1 (D)          | 9.32418p            | 18.0747p            | 13.1305p                 | 19.7824p                  |
| 2 (E)          | 9.2485p             | 5.6004p             | 10.4192p                 | 8.07188p                 |

In comparing the rise times, fall times, and propagation delays across two tables, notable trends emerge. In Table 1, Case 1 (A) exhibits the lowest rise and fall times, while Case 2 (B) shows the highest. In Table 2, Case 2 (E) has the lowest rise time, and Case 1 (D) has the highest fall time. Propagation delays vary across cases, with Case 2 (B) in Table 1 and Case 1 (D) in Table 2 displaying higher values.

### Layout

![lab1_final_layout](https://github.com/NSaroya/Boolean-Gate-Circuit-Schematic-Simulation-and-Layout/assets/156468713/4e6f4ba3-d2b2-4863-8719-8f70ec9fb7bb)

