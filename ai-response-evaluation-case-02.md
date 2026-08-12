# AI Response Evaluation Case 02

## Scenario

### Context

In a student progress management project, the Project Instructions defined a specific workflow for processing student data extracted from images.

The instructions required the system to:

- use Project Sources as the primary source;
- map Absen Setoran to Absen Resmi;
- normalize unclear names using the established mapping;
- continue updating the State/List even when some data requires confirmation;
- provide the best prediction for uncertain data and request confirmation when necessary.

### AI Behavior

During one processing session, the AI did not follow the project-specific workflow.

Instead of prioritizing the Project Sources and applying the defined mapping and normalization process, the AI returned to a general OCR-processing approach.

The AI also stopped updating the overall State because some extracted names were uncertain.

Later, the AI acknowledged that this was a failure to follow the existing Project Instructions rather than a lack of clarity in the instructions.

## Evaluation

### Overall Assessment

The response demonstrates a significant instruction-following failure.

The main problem was not the ability to process OCR data, but the failure to apply the project-specific processing hierarchy and workflow that had already been defined.

### Instruction Following

**Rating: Poor**

The AI did not follow several explicit project requirements.

The Project Instructions already established the correct processing order and the required handling of uncertain data.

Returning to a generic OCR workflow ignored those project-specific constraints.

### Reasoning Quality

**Rating: Poor**

The reasoning relied on a general pattern for handling uncertain OCR results instead of applying the rules specific to the project.

This caused the AI to treat uncertainty in some data as a reason to interrupt broader state updates, even though the project instructions explicitly allowed uncertain data to be marked for confirmation while continuing to process reliable data.

### Source Prioritization

**Rating: Poor**

The AI failed to prioritize Project Sources even though they were explicitly defined as the primary source.

For example, when an OCR result contained an unclear student name but the attendance number was available, the correct approach was to use the corresponding identity from Project Sources rather than treating the OCR name as independently uncertain.

### State Management

**Rating: Poor**

The AI incorrectly stopped the broader State/List update because some extracted data required confirmation.

According to the project workflow, uncertain records should be marked as requiring confirmation while reliable records should still be incorporated into the current State/List.

### Corrective Reasoning

The AI later correctly identified its own failure.

It recognized that:

1. Project Instructions had already defined the required workflow.
2. Project Sources should have been used first.
3. Mapping and normalization should have been performed before treating names as uncertain.
4. Uncertain data should not have prevented the rest of the session from being updated.
5. The failure was an instruction-following problem rather than an absence of instructions.

## Key Error

The central error was:

> The AI followed a generic OCR-processing pattern instead of the project-specific algorithm defined in the Project Instructions.

This distinction is important because a response can appear logically reasonable in isolation while still being incorrect within a specific task environment.

## Learning Outcome

This case demonstrates the importance of evaluating an AI response against the actual instructions and workflow of the task rather than judging the response only by whether its general reasoning appears reasonable.

The case demonstrates skills in:

- instruction following;
- source prioritization;
- contextual reasoning;
- workflow compliance;
- handling uncertain information;
- state management;
- identifying reasoning errors;
- distinguishing general best practices from task-specific requirements.
