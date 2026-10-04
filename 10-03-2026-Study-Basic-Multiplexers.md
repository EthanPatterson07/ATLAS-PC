# Purpose
MUX (Multiplexers) are used to turn multiple inputs into a single output line, saving money, wiring, and improving efficiency

# Concept
- A 2:1 MUX is a gate that picks one input from 2 possible inputs to pass its signal to the output
- If we call the picking variable Sel ("Sel" is just convention)
- We can say that when Sel is 0, the output will be A, and when Sel is 1, the output will be B
- We can call this output F

# Model
- We can then establish a truth table that represents this logical relationship

![2:1 MUX](https://github.com/EthanPatterson07/ATLAS-PC/blob/media/MUX10-03-2026.png)
- We can then use a K-map to simplify the expression

![MUX K-map](https://github.com/EthanPatterson07/ATLAS-PC/blob/media/MUXK-map10-03-2026.png)
- In POS form, the expression would then become:

$$
F = Sel'A + SelB
$$

- Now, we can draw a basic circuit diagram to show the logical gates in the expression

![MUX Circuit](https://github.com/EthanPatterson07/ATLAS-PC/blob/media/MUXCircuitCorrect-10-03-2026.png)

- Since our final gate before F is an OR gate (SOP form), we can now make the circuit much cheaper to make by turning all gates into NAND gates per De Morgan's Law

![MUX Circuit NAND](https://github.com/EthanPatterson07/ATLAS-PC/blob/media/MUXCircuitNAND-10-03-2026.png)

# Apply
- We can't practically use a similar method to make a 4:1 MUX because the truth table would contain 6 inputs, meaning 64 different combinations of 1s and 0s
- However, we can construct a 4:1 MUX out of 2:1 MUXes
