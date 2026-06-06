# mental-help

A tool that helps caregivers navigate the mental health treatment system during a crisis — orienting them to care levels, surfacing real facilities, and preparing them for conversations with providers.

## Language

**Caregiver**:
The person using this tool. Typically a family member or close friend seeking help for someone else. In rare cases, may be the person themselves.
_Avoid_: Family member, user, relative

**Person**:
The individual experiencing the mental health crisis that the caregiver is seeking help for.
_Avoid_: Patient, loved one, individual, client

## Care

**Care Level**:
The type and intensity of treatment recommended for the person. One of five values: Inpatient, Residential, Partial Hospitalization Program (PHP), Intensive Outpatient Program (IOP), or Outpatient.
_Avoid_: Care type, treatment level, recommendation type

**Care Level Recommendation**:
The output of the Orient phase. The specific care level determined by the decision tree based on the caregiver's answers.
_Avoid_: Assessment result, suggestion, diagnosis

**Decision Tree**:
The JSON data structure that defines the questionnaire's branching logic — nodes, conditions, and care level outcomes. Distinct from the code that evaluates it.
_Avoid_: Rules engine, algorithm, logic, flowchart

**Questionnaire**:
The guided step-by-step flow in the Orient phase that collects the caregiver's answers and produces a care level recommendation.
_Avoid_: Form, survey, assessment, intake form

**Question**:
A single screen within the questionnaire that presents a prompt and collects an answer from the caregiver.
_Avoid_: Step, prompt, item, screen

**Node**:
A single unit in the decision tree data structure. May be a question node (collects input) or an outcome node (produces a care level recommendation or safety escalation).
_Avoid_: Step, item, leaf, state

**Facility**:
A treatment organization returned by the FindTreatment.gov API. A facility may offer multiple care levels. Not modelled at the program level in Phase 1.
_Avoid_: Provider, program, center, clinic, treatment center

**FindTreatment.gov API**:
The public SAMHSA API that provides facility-level records for all known substance use and mental health treatment facilities in the United States. The sole external data source for the Locate phase.
_Avoid_: SAMHSA API, N-SUMHSS, SAMHSA data

**Safety Escalation**:
An outcome node in the decision tree that bypasses the rest of the questionnaire and surfaces emergency resources (988, 911). Triggered when an immediate safety risk is detected.
_Avoid_: Crisis redirect, emergency path, danger flag

**Immediate Safety Risk**:
The condition where the person is a danger to themselves or others right now. The trigger for a safety escalation.
_Avoid_: Crisis, emergency, danger, red flag

**Crisis**:
An acute, immediate safety situation requiring emergency intervention (911 or 988). Distinct from a mental health emergency.
_Avoid_: Emergency, breakdown, incident

**Mental Health Emergency**:
The serious but non-immediately-dangerous situation that brings a caregiver to this tool — a loved one has reached a point where treatment is urgently needed. Does not necessarily require 911.
_Avoid_: Crisis, breakdown, episode

## Phases

**Orient**:
The first phase. A guided questionnaire that determines what level of care the person needs right now.
_Avoid_: Step 1, assessment, intake

**Locate**:
The second phase. Surfaces real treatment facilities filtered to the recommended care level and the caregiver's state.
_Avoid_: Step 2, search, find, browse

**Prepare**:
The third phase. Gives the caregiver questions to ask facilities and red flags to watch for, framed around the specific care level.
_Avoid_: Step 3, guide, checklist
