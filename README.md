# Business-Process-Modeling-Internship-Workflow-Analysis


## BPMN Collaboration Model
The repository provides BPMN diagrams depicting how the **Intern**, **Supervisor**, and **Project Leader** exchange messages and coordinate tasks. The diagrams show the core workflow and the extended variant with an optional internship extension.

## Petri Net Models
Each role (Supervisor, Intern, Project Leader) is modeled as an individual **Workflow Net (WF-net)**. Additionally, there is an **integrated system** that combines all three roles into a single Petri net, capturing message-passing and synchronization points.

- **Base Models**: Capture the standard internship lifecycle.  
- **Variant Models**: Add the internship extension mechanism, requiring additional tasks and synchronization steps.

## Analysis and Properties
A thorough analysis was conducted to verify critical properties:

- **Soundness**: Every net has a unique start place and end place, ensuring the process terminates properly without leaving tokens in intermediate places.  
- **Boundedness**: No unbounded accumulation of tokens is possible, guaranteeing that the reachability space is finite.  
- **Liveness**: Every transition can eventually fire under some valid execution sequence, indicating no deadlocks.  
- **Well-structuredness, Free-choice, PT/TP-handles**: The final integrated model is sound and bounded but contains PT/TP-handles and free-choice violations, indicating it is not fully well-structured.


## How to Use

1. **View BPMN Models**  
   Open the files in any BPMN-compatible tool (e.g., Camunda Modeler, Bizagi, etc.) to visualize the collaboration flows.

2. **Examine Petri Nets**  
   Use Petri net analysis tools like **WoPeD** or **ProM** to load the `.pnml` files. You can verify soundness, liveness, and other properties yourself.


## Key Highlights

### Internship Extension Mechanism
Introduces a feedback loop where the supervisor decides to extend the internship, demonstrating how a real-life process change can be incorporated into an existing model.

### Structured Approach
The methodology follows a typical flow: start with BPMN diagrams → transform them into Petri nets → perform soundness and liveness checks → discuss well-structuredness and free-choice properties.

### Robustness and Flexibility
Despite PT/TP-handles and free-choice violations in the integrated system, the final workflow remains sound, bounded, and live, reflecting real-world complexities where perfect structural simplicity is not always feasible.

## License
Feel free to explore, adapt, and reuse these models and the accompanying report content for **academic or research purposes**. If you extend or modify the models, please credit the original work.
