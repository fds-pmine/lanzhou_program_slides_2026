# Slides for Lanzhou University 2026 

Professor: Prof. Dr. Aquil Mirza Mohammed 

Mentor: Suyu Jiang, Haozhe Ruan 

# Code repo 

https://github.com/fds-pmine/Lanzhou_Student_Starter_Bundle 

# GitHub Instructions 

https://github.com/Field-of-Dreams-Studio/FDS0/tree/master/Seminar_07-Git_Basics 

https://github.com/Field-of-Dreams-Studio/FDS0/tree/master/Seminar_08-GitHub_Cooperation 

---

# Book Chapters

### Chapter 1. Digital Twins for Reproducible Robot-Arm Experiments

**Core claim:** A deliberately simple but deterministic arm twin can provide the shared,
reproducible experimental substrate for the entire book.

**Signature subsection:** **4.4 Deterministic Replay Contract**

**In scope:** kinematic model, state/command representation, joint limits, fixed-step
updates, known trajectories, repeatability, and runtime cost.

**Out of scope:** camera calibration, network delivery, learned dynamics, controller
training, and claims of physical-arm fidelity.

#### Customized Subsections

##### 2. Background and Related Work

- **2.1 Reproducible Simulation in Robotics**
- **2.2 Kinematic Abstractions for Robot Arms**
- **2.3 Determinism Gaps in Educational Robot Experiments**

##### 3. Problem Formulation and System Model

- **3.1 Manipulator and Environment Scope**
- **3.2 Coordinate Frames, Units, and Joint-Limit Contract**
- **3.3 Fixed-Step Temporal Model**
- **3.4 Determinism Requirements and Acceptance Criteria**

##### 4. Design and Method

- **4.1 Robot State and Command Representation**
- **4.2 Forward Kinematics and Fixed-Step Update**
- **4.3 Known-Pose and Trajectory Fixtures**
- **4.4 Deterministic Replay Contract**

##### 6. Experimental Methodology

- **6.1 Analytical Known-Pose Tests**
- **6.2 Repeated-Run and Cross-Build Replay Protocol**
- **6.3 Joint-Boundary and Workspace Workloads**
- **6.4 Correctness, Repeatability, and Runtime Metrics**

##### 7. Results

- **7.1 Known-Pose and Kinematic Correctness**
- **7.2 Same-Seed Trace Reproducibility**
- **7.3 Joint-Limit and Workspace Boundary Behavior**
- **7.4 Fixed-Step Runtime Cost**

##### 8. Discussion and Limitations

- **8.1 Suitability as the Book's Shared Experimental Substrate**
- **8.2 Model-Fidelity and Dynamics Limitations**
- **8.3 Simulator-Only Validity Boundary**

**Required evidence:** twin architecture figure, known-pose table, replay hash/trace,
boundary-test table, and runtime summary.

---

### Chapter 2. Calibrated State Estimation for Networked Robot Arms

**Core claim:** Coordinate-frame, calibration, and sensing-time errors must be represented
explicitly because they can become incorrect robot motion downstream.

**Signature subsection:** **4.4 Calibration Error and Uncertainty Propagation**

**In scope:** pose adapter, frame transformations, state-time alignment, simulated or
camera-derived calibration fixtures, uncertainty, noise, and occlusion.

**Out of scope:** deterministic plant simulation, MQTT delivery semantics, full computer
vision pipelines, and neural state estimation.

#### Customized Subsections

##### 2. Background and Related Work

- **2.1 Robot Pose, Calibration, and Frame Graphs**
- **2.2 Temporal Alignment of Sensed State**
- **2.3 Uncertainty Representation for Networked Control**

##### 3. Problem Formulation and System Model

- **3.1 Sensor or Pose-Adapter Boundary**
- **3.2 Frame Graph and Transformation Chain**
- **3.3 Sensing-Clock and Timestamp Model**
- **3.4 Geometric, Temporal, Noise, and Occlusion Errors**

##### 4. Design and Method

- **4.1 Pose-Adapter Contract**
- **4.2 Calibration and Transformation Composition**
- **4.3 State-Time Alignment**
- **4.4 Calibration Error and Uncertainty Propagation**
- **4.5 State-Quality Output for Downstream Gates**

##### 6. Experimental Methodology

- **6.1 Reference-Pose and Transform-Closure Tests**
- **6.2 Clock-Offset and Jitter Injection**
- **6.3 Noise and Occlusion Workloads**
- **6.4 Pose, Time, Uncertainty, and Rejection Metrics**

##### 7. Results

- **7.1 Transformation and Reference-Pose Error**
- **7.2 Sensitivity to Clock Offset and Jitter**
- **7.3 Sensitivity to Noise and Occlusion**
- **7.4 Effect of State Quality on Downstream Acceptance**

##### 8. Discussion and Limitations

- **8.1 When Calibrated State Is Trustworthy Enough to Use**
- **8.2 Separation of Sensing Age from Network Freshness**
- **8.3 Calibration-Fixture and Sensor Limitations**

**Required evidence:** frame-graph figure, transform-closure table, pose/time-error plots,
noise/occlusion sensitivity plot, and downstream rejection table.

---

### Chapter 3. Reliable Binary Protocols for Robotic Actuation

**Core claim:** Corrupt, truncated, disordered, or unrecoverable frames must be detected
before they can trigger an actuator action.

**Signature subsection:** **4.5 Resynchronization State Machine**

**In scope:** binary frame format, CRC, sequence and frame-level timestamp validation,
ACK/NACK, parser recovery, and communication-fault injection.

**Out of scope:** MQTT QoS, broker congestion, semantic safety constraints, and physical
command validity.

#### Customized Subsections

##### 2. Background and Related Work

- **2.1 Binary Framing for Robotic Actuation**
- **2.2 Error Detection and Sequence Control**
- **2.3 Parser Recovery after Stream Corruption**

##### 3. Problem Formulation and System Model

- **3.1 Communication Fault and Actuation-Risk Model**
- **3.2 Wire Contract and Payload Budget**
- **3.3 Frame Acceptance and Rejection Semantics**
- **3.4 Integrity Boundary versus Physical-Safety Boundary**

##### 4. Design and Method

- **4.1 Binary Frame Layout**
- **4.2 CRC-Based Integrity Validation**
- **4.3 Sequence and Frame-Time Validation**
- **4.4 ACK/NACK Behavior**
- **4.5 Resynchronization State Machine**

##### 6. Experimental Methodology

- **6.1 Correct Round-Trip Baseline**
- **6.2 Bit-Flip and Burst-Corruption Injection**
- **6.3 Truncation, Drop, Duplication, and Reordering**
- **6.4 Detection, False-Rejection, Recovery, and Cost Metrics**

##### 7. Results

- **7.1 Corruption-Detection Effectiveness**
- **7.2 Recovery after Truncated or Misaligned Frames**
- **7.3 Sequence and Reordering Verdicts**
- **7.4 Retransmission and Recovery Cost**
- **7.5 Verification of Zero Corrupt Actuation**

##### 8. Discussion and Limitations

- **8.1 Integrity Guarantees Provided by the Frame Layer**
- **8.2 What CRC and Sequence Checks Cannot Guarantee**
- **8.3 Stream and Fault-Model Limitations**

**Required evidence:** wire-layout figure, recovery-state-machine figure, injected-fault
table, detection/false-rejection table, and corrupt-actuation count.

---

### Chapter 4. Time-Synchronized MQTT for Fresh Robot Commands

**Core claim:** Robot control requires the latest still-useful command, not merely eventual
message delivery.

**Signature subsection:** **4.4 Freshness Semantics under MQTT QoS**

**In scope:** MQTT topics, QoS policy, time synchronization, multi-stage timestamps,
latest-value semantics, age cutoff, and emergency-message transport behavior.

**Out of scope:** byte-level frame corruption recovery, event-loop dispatch guarantees,
and end-to-end actuator safety.

#### Customized Subsections

##### 2. Background and Related Work

- **2.1 Publish–Subscribe Communication for Robot Systems**
- **2.2 MQTT Quality of Service**
- **2.3 Freshness, Age, and Deadline Semantics**

##### 3. Problem Formulation and System Model

- **3.1 Topic Graph and Message Flow**
- **3.2 Four-Point Timestamp and Clock Model**
- **3.3 Command-Age and Freshness Definitions**
- **3.4 Delivery Guarantee versus Execution Usefulness**

##### 4. Design and Method

- **4.1 Binary-Frame-to-MQTT Bridge**
- **4.2 Topic and QoS Policy**
- **4.3 Latest-Value Queue and Age Cutoff**
- **4.4 Freshness Semantics under MQTT QoS**
- **4.5 Disconnect, Reconnect, and Emergency Path**

##### 6. Experimental Methodology

- **6.1 QoS 0/1/2 under Controlled Load**
- **6.2 Duplicate, Stale, Delayed, and Disconnected Workloads**
- **6.3 Clock-Offset and Timestamp-Trace Protocol**
- **6.4 RTT, Tail, Stale-Drop, Deadline, and E-Stop Metrics**

##### 7. Results

- **7.1 QoS Delivery and Latency Trade-Offs**
- **7.2 End-to-End Message-Age Distribution**
- **7.3 Stale and Duplicate Command Rejection**
- **7.4 Deadline Misses under Broker Load**
- **7.5 Emergency-Message Transport Latency**

##### 8. Discussion and Limitations

- **8.1 When Delivery Reliability Conflicts with Freshness**
- **8.2 Separation of Transport Delay from Runtime Dispatch Delay**
- **8.3 Broker, Clock, and Network-Topology Limitations**

**Required evidence:** topic-flow figure, four-timestamp diagram, QoS comparison table,
RTT/age distribution plot, stale-drop table, and emergency-latency result.

---

### Chapter 5. Nonblocking Multi-Client Robot Control in C

**Core claim:** A slow, blocked, or flooding client must not delay fast clients or the
safety path.

**Signature subsection:** **4.4 Backpressure and Client Fairness**

**In scope:** blocking failure, nonblocking I/O, `poll()`, partial I/O, per-client buffers,
backpressure, fairness, and multi-client workloads.

**Out of scope:** `epoll`-based emergency cancellation, mutex correctness, and physical
safety policy.

#### Customized Subsections

##### 2. Background and Related Work

- **2.1 Blocking and Nonblocking Server I/O**
- **2.2 Head-of-Line Blocking in Robot-Control Services**
- **2.3 Readiness Multiplexing with `poll()`**

##### 3. Problem Formulation and System Model

- **3.1 Fast, Slow, and Flooding Client Model**
- **3.2 Reproducible Blocking Failure**
- **3.3 Service, Fairness, and Safety-Path Objectives**
- **3.4 User-Space and Kernel-Space Queue Locations**

##### 4. Design and Method

- **4.1 Nonblocking Connection Lifecycle**
- **4.2 `poll()` Event-State Machine**
- **4.3 Partial Reads, Partial Writes, and Per-Client Buffers**
- **4.4 Backpressure and Client Fairness**
- **4.5 Safety-Path Isolation**

##### 6. Experimental Methodology

- **6.1 Blocking Server Baseline**
- **6.2 One-, Ten-, and Fifty-Client Workloads**
- **6.3 Fast, Slow, and Flood Client Mixtures**
- **6.4 Latency, Throughput, Fairness, and HOL Metrics**

##### 7. Results

- **7.1 Reproduction of Head-of-Line Blocking**
- **7.2 Blocking-versus-`poll()` Tail Latency**
- **7.3 Throughput and Fairness across Client Counts**
- **7.4 Slow/Flood Client Isolation**
- **7.5 Safety-Path Responsiveness**

##### 8. Discussion and Limitations

- **8.1 Scalability and Fairness of the `poll()` Design**
- **8.2 Separation of Readiness from Deadline Guarantees**
- **8.3 Workload and File-Descriptor Limitations**

**Required evidence:** blocking-failure timeline, event-state-machine figure,
latency-versus-clients plot, fairness table, and slow/flood isolation trace.

---

### Chapter 6. Deadline-Aware Event Loops and Emergency Cancellation

**Core claim:** Readiness alone is insufficient; queue age, deadlines, cancellation, and
emergency response must be explicit and measurable.

**Signature subsection:** **4.4 Emergency Cancellation and Deadline Enforcement**

**In scope:** `epoll`, timer-driven wake-up, queue age, dispatch deadlines, cancellation,
watchdog behavior, overload, and emergency preemption.

**Out of scope:** MQTT transport latency, arbitration among command owners, safety-limit
selection, and hard real-time certification.

#### Customized Subsections

##### 2. Background and Related Work

- **2.1 Event Notification and Deadline-Aware I/O**
- **2.2 Cancellation and Watchdog Mechanisms**
- **2.3 Emergency Response in Soft Real-Time Systems**

##### 3. Problem Formulation and System Model

- **3.1 Event Sources and End-to-End Runtime Budget**
- **3.2 Queue-Age and Dispatch-Deadline Model**
- **3.3 Cancellation and Emergency Semantics**
- **3.4 Normal-Load and Overload Assumptions**

##### 4. Design and Method

- **4.1 `epoll` Runtime Architecture**
- **4.2 Timer and Self-Pipe Wake-Up Paths**
- **4.3 Deadline-Aware Dispatch**
- **4.4 Emergency Cancellation and Deadline Enforcement**
- **4.5 Watchdog and Stalled-Task Recovery**

##### 6. Experimental Methodology

- **6.1 `poll()` Runtime Baseline**
- **6.2 Normal, Burst, and Sustained-Overload Workloads**
- **6.3 Repeated Emergency-Stop and Cancellation Trials**
- **6.4 p99, Maximum, Deadline-Miss, Queue-Age, and Starvation Metrics**

##### 7. Results

- **7.1 `poll()`-versus-`epoll` Dispatch Behavior**
- **7.2 Queue Age under Normal and Overload Conditions**
- **7.3 Emergency-Cancellation Worst Case**
- **7.4 Deadline Miss and Watchdog Recovery**
- **7.5 Starvation Analysis**

##### 8. Discussion and Limitations

- **8.1 What Deadline Awareness Adds beyond Nonblocking I/O**
- **8.2 Soft Real-Time versus Hard Real-Time Claims**
- **8.3 Kernel, Scheduler, and Hardware Limitations**

**Required evidence:** event-loop architecture figure, cancellation timeline, queue-age
plot, repeated e-stop worst-case table, deadline-miss table, and starvation result.

---

### Chapter 7. Concurrency-Safe Arbitration of Shared Actuators

**Core claim:** Multiple producers may compute commands concurrently, but the actuator
must observe one valid, non-interleaved writer decision at a time.

**Signature subsection:** **4.2 Single-Writer Invariant**

**In scope:** command ownership, arbitration, single-writer queue, mutexes, lock ordering,
races, deadlocks, priority inversion, and unique actuation.

**Out of scope:** deciding whether a uniquely selected command is physically safe,
controller-quality assessment, and transport freshness.

#### Customized Subsections

##### 2. Background and Related Work

- **2.1 Shared-Actuator Concurrency**
- **2.2 Mutual Exclusion, Deadlock, and Priority Inversion**
- **2.3 Arbitration versus Safety Supervision**

##### 3. Problem Formulation and System Model

- **3.1 Command Producers and Actuator Ownership**
- **3.2 Race, Interleaving, Deadlock, and Inversion Model**
- **3.3 Arbitration Invariants and Linearization Point**
- **3.4 Producer Priority and Rejection Semantics**

##### 4. Design and Method

- **4.1 Command-Arbitration Policy**
- **4.2 Single-Writer Invariant**
- **4.3 Mutex Scope and Lock Ordering**
- **4.4 Priority Handling and Bounded Wait**
- **4.5 Deadlock Detection or Recovery Strategy**

##### 6. Experimental Methodology

- **6.1 Concurrent-Producer Baseline**
- **6.2 Frame-Interleaving and Race Fixtures**
- **6.3 Deadlock and Priority-Inversion Fixtures**
- **6.4 Unique-Writer, Lock-Wait, NACK, and Recovery Metrics**

##### 7. Results

- **7.1 Verification of Unique, Non-Interleaved Actuation**
- **7.2 Arbitration Verdicts under Competing Producers**
- **7.3 Lock-Wait Distribution**
- **7.4 Deadlock Reproduction and Mitigation**
- **7.5 Priority-Inversion Behavior**

##### 8. Discussion and Limitations

- **8.1 Concurrency Correctness Delivered by Arbitration**
- **8.2 Why Unique Ownership Does Not Imply Physical Safety**
- **8.3 Threading and Scheduling Limitations**

**Required evidence:** ownership/arbitration figure, interleaving trace, unique-writer
table, lock-wait distribution, and deadlock/inversion before–after result.

---

### Chapter 8. Fail-Closed Safety Supervisors for Robot Arms

**Core claim:** Every command, regardless of whether it comes from a human, script, or
learned controller, must pass a non-bypassable and auditable safety gate.

**Signature subsection:** **4.5 Hazard-to-Gate Traceability**

**In scope:** joint, velocity, workspace, freshness, confidence, watchdog, emergency-stop,
verdict, reason code, audit completeness, and fail-closed behavior.

**Out of scope:** command-producer arbitration, controller training, formal safety
certification, and unsupervised high-speed physical-arm experiments.

#### Customized Subsections

##### 2. Background and Related Work

- **2.1 Runtime Safety Supervision for Robot Arms**
- **2.2 Fail-Closed Design and Safety Invariants**
- **2.3 Runtime Checks versus Formal or Certified Safety**

##### 3. Problem Formulation and System Model

- **3.1 Hazards, Assets, and Trust Boundaries**
- **3.2 Safety Invariants and Instructor-Frozen Thresholds**
- **3.3 Verdict and Reason-Code Model**
- **3.4 Fail-Closed Assumptions**

##### 4. Design and Method

- **4.1 Pure Safety-Gate Pipeline**
- **4.2 Joint, Velocity, and Workspace Checks**
- **4.3 Freshness, Confidence, and State-Quality Checks**
- **4.4 Watchdog, Emergency Stop, and Audit Trail**
- **4.5 Hazard-to-Gate Traceability**

##### 6. Experimental Methodology

- **6.1 Normal and Unsafe Command Matrix**
- **6.2 Stale, NaN, Out-of-Range, and Disconnect Faults**
- **6.3 Individual-Gate Ablation**
- **6.4 Unsafe-Actuation, False-Rejection, Audit, and Coverage Metrics**

##### 7. Results

- **7.1 Unsafe-Command Rejection**
- **7.2 False-Rejection Analysis on Normal Commands**
- **7.3 Watchdog and Emergency-Stop Verdicts**
- **7.4 Audit Completeness and Fault Coverage**
- **7.5 Safety-Gate Ablation**

##### 8. Discussion and Limitations

- **8.1 Safety Implications of Fail-Closed Runtime Checks**
- **8.2 Threshold Provenance and Sensitivity**
- **8.3 Simulator-Only and Non-Certification Limitations**

**Required evidence:** hazard-to-gate table, safety-pipeline figure, command-verdict
matrix, false-rejection result, audit-coverage table, and gate-ablation figure.

---

### Chapter 9. Safely Hosting Learned Controllers in Real-Time Robot Systems

**Core claim:** A learned controller is one replaceable controller implementation; the
host must contain its timing and output failures and provide a safe fallback.

**Signature subsection:** **4.5 Controller Containment and Safe Fallback**

**In scope:** unified controller contract, PID/script baseline, professor-provided
black-box controller, runtime measurement, timeout, sanitization, confidence handling,
and fallback.

**Out of scope:** neural-network architecture, dataset preparation, training,
hyperparameter tuning, convergence proof, and claims about model novelty.

#### Customized Subsections

##### 2. Background and Related Work

- **2.1 Hosting Controllers in Robot Runtime Systems**
- **2.2 Learned Controllers as Untrusted Components**
- **2.3 Runtime Containment, Sanitization, and Fallback**

##### 3. Problem Formulation and System Model

- **3.1 Unified Black-Box Controller Contract**
- **3.2 Runtime, Output, Confidence, and Stall Failures**
- **3.3 Control-Cycle Time Budget**
- **3.4 PID or Scripted Baseline and Trust Assumptions**

##### 4. Design and Method

- **4.1 Controller Adapter**
- **4.2 Runtime Measurement and Timeout Isolation**
- **4.3 Finite, Range, and Rate Sanitization**
- **4.4 Confidence Handling and Fallback Trigger**
- **4.5 Controller Containment and Safe Fallback**

##### 6. Experimental Methodology

- **6.1 PID/Script Baseline and Provided-Controller Workloads**
- **6.2 Normal Tracking-Proxy Scenario**
- **6.3 NaN, Out-of-Range, Low-Confidence, Timeout, and Stall Faults**
- **6.4 Runtime-Jitter, Blocking, Fallback, and Recovery Metrics**

##### 7. Results

- **7.1 Runtime Jitter and Tracking-Proxy Behavior**
- **7.2 Rejection of Invalid Controller Output**
- **7.3 Timeout and Stall Containment**
- **7.4 Fallback Activation and Recovery**
- **7.5 Behavior after Removing the Learned Controller**

##### 8. Discussion and Limitations

- **8.1 Reliability of the Controller-Hosting Boundary**
- **8.2 Why Controller Quality Does Not Replace Safety Supervision**
- **8.3 No-Training and Black-Box Evaluation Limitations**

**Required evidence:** adapter/containment figure, controller-fault table, runtime-jitter
plot, fallback timeline, and controller-removal result.

---

### Chapter 10. An Audited Gatekeeper for Sim-to-Real Robot Actuation

**Core claim:** An actuator write is permitted only after the command passes integrity,
freshness, arbitration, safety, and audit stages in one traceable end-to-end chain.

**Signature subsection:** **4.5 Cross-Layer Claim–Evidence Traceability**

**In scope:** end-to-end composition, gatekeeper pipeline, verdict trace, fixture runner,
fault replay, deadline budget, release evidence, and optional transport swap from
simulator to instructor-supervised arm.

**Out of scope:** repeating every upstream chapter's unit experiment, controller training,
and claiming physical validation when only simulator evidence exists.

#### Customized Subsections

##### 2. Background and Related Work

- **2.1 End-to-End Assurance in Robotic Middleware**
- **2.2 Runtime Gatekeepers and Auditable Actuation**
- **2.3 Traceability across Communication, Runtime, and Safety Layers**

##### 3. Problem Formulation and System Model

- **3.1 End-to-End Actuation Architecture**
- **3.2 Cross-Layer Trust Boundaries**
- **3.3 End-to-End Deadline Budget**
- **3.4 Simulator-to-Arm Transport Boundary**

##### 4. Design and Method

- **4.1 Decode→Freshness→Arbitration→Safety→Write Pipeline**
- **4.2 Unified Verdict, Reason Code, and Audit Trace**
- **4.3 Canonical Fixture and Replay Runner**
- **4.4 Simulator and Optional Arm Transport Adapters**
- **4.5 Cross-Layer Claim–Evidence Traceability**

##### 6. Experimental Methodology

- **6.1 End-to-End Happy-Path Baseline**
- **6.2 Corrupt, Stale, Unsafe, Reordered, and Overloaded Scenarios**
- **6.3 Controller-Failure and Emergency-Stop Scenarios**
- **6.4 Cross-Layer Gate Ablation and Trace Replay**
- **6.5 End-to-End Deadline, Verdict, Audit, and Reproducibility Metrics**

##### 7. Results

- **7.1 End-to-End Happy-Path Execution**
- **7.2 Cross-Layer Fault Rejection**
- **7.3 End-to-End Latency and Deadline Compliance**
- **7.4 Gate-Ablation Contribution**
- **7.5 Independent Trace-Replay Reproduction**
- **7.6 Simulator-to-Transport-Swap Boundary**

##### 8. Discussion and Limitations

- **8.1 What the Integrated Evidence Supports**
- **8.2 Failure Dependencies across Chapter Boundaries**
- **8.3 Simulator-to-Arm Generalization Limits**
- **8.4 Remaining Work toward Deployment or Certification**

**Required evidence:** end-to-end pipeline figure, deadline-budget table, canonical
scenario matrix, cumulative latency plot, gate-ablation result, traceability matrix,
and replay report.

---

## 9. Signature Subsection and Evidence Index

| Chapter | Signature subsection                            | Evidence that must remain unique to the chapter              |
| ------: | ----------------------------------------------- | ------------------------------------------------------------ |
|     Ch1 | Deterministic Replay Contract                   | Same-seed trace identity, known-pose correctness, and boundary behavior |
|     Ch2 | Calibration Error and Uncertainty Propagation   | Pose/time error under noise and occlusion                    |
|     Ch3 | Resynchronization State Machine                 | Detection, recovery cost, false rejection, and zero corrupt actuation |
|     Ch4 | Freshness Semantics under MQTT QoS              | Stale-drop behavior, RTT/message-age tail, and deadline misses |
|     Ch5 | Backpressure and Client Fairness                | Slow/flood-client HOL behavior, fairness, and tail latency   |
|     Ch6 | Emergency Cancellation and Deadline Enforcement | Repeated e-stop worst case, deadline misses, and starvation result |
|     Ch7 | Single-Writer Invariant                         | No interleaving, unique writer, lock wait, and deadlock/inversion evidence |
|     Ch8 | Hazard-to-Gate Traceability                     | Unsafe actuation, false rejection, audit coverage, and gate ablation |
|     Ch9 | Controller Containment and Safe Fallback        | Timeout, NaN, range, confidence, stall, fallback, and controller removal |
|    Ch10 | Cross-Layer Claim–Evidence Traceability         | End-to-end scenario matrix, trace replay, gate ablation, and transport boundary |

---

## 10. Five-Day Hands-On to Chapter-Writing Map

The five one-hour sessions produce an evidence-backed chapter skeleton, not ten finished
long-form manuscripts.

| Day                                | Chapter sections advanced                                | Minimum writing and evidence output                          |
| ---------------------------------- | -------------------------------------------------------- | ------------------------------------------------------------ |
| **Day 1 — State + Frame**          | 1.2–1.4 and Section 3                                    | Chapter charter, research questions, contributions, system model, assumptions, shared interface, baseline, and one minimal failure case |
| **Day 2 — MQTT + Freshness**       | Section 4 and 5.3                                        | Design/method v1, instrumentation, timestamp/log schema, first raw data, and method bullets |
| **Day 3 — Nonblocking + `poll()`** | Section 6 and result-table skeleton                      | Baseline-versus-method protocol, workload, seed, repetition count, metrics, and planned figures/tables |
| **Day 4 — Locking + Safety**       | Section 7 fault/ablation and Section 8 limitations       | At least one failure or ablation per chapter, safety implication, preliminary result, limitations, and validity boundary |
| **Day 5 — Async + Release**        | Remaining Section 7, Section 8, Section 9, then Abstract | Main results, RQ answers, integration trace, conclusion skeleton, claim–evidence table, evidence index, and internal/external review |

Related-work collection continues throughout the course through each evidence pack, but a
complete literature review and full prose expansion are post-course activities.

---

## 12. Chapter Skeleton Completion Checklist

A chapter skeleton is complete only when all applicable items are present:

- [ ] One chapter-specific research gap and two or three measurable research questions
- [ ] A claim that does not duplicate its paired chapter
- [ ] Explicit `In scope` and `Out of scope` boundaries
- [ ] Inputs inherited from earlier chapters and outputs consumed by later chapters
- [ ] A chapter-specific system or failure model
- [ ] A baseline, proposed mechanism, workload, fault set, and metric definition
- [ ] One signature subsection that no other chapter reuses
- [ ] At least one chapter-specific figure and one chapter-specific result table
- [ ] Raw data, seed, parameters, compiler, container identity, commit, and command
- [ ] At least one negative, failure, or ablation result
- [ ] A claim→test/trace/table/figure evidence mapping
- [ ] Safety implications and threats to validity
- [ ] Explicit simulator-only boundary unless supervised physical-arm evidence exists
- [ ] Internal cross-review and review-ring comments

---

## 13. Editorial Consistency Rules

- Use the common terminology and interfaces; do not redefine them chapter by chapter.
- Use chapter-specific technical result headings rather than generic repeated headings.
- Report p50/p95/p99/maximum or another justified distribution summary; do not rely only
  on means.
- Separate transport latency, runtime-dispatch latency, lock wait, controller runtime, and
  end-to-end actuation latency.
- Distinguish syntactic validity, freshness, ownership, physical safety, and final
  actuation permission.
- Do not claim real-robot validation from simulator-only evidence.
- Do not describe the provided learned controller as a contribution of the student team.
- Do not invent or duplicate references; every citation must be verified and relevant to
  the specific chapter claim.
- Write the abstract after results are available, even though it appears first in the
  finished chapter.
