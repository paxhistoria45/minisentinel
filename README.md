# MiniSentinel

**An eBPF-based Linux Runtime Monitoring and Process Provenance System**

MiniSentinel is an experimental Linux runtime security monitoring project built around eBPF. It aims to observe process lifecycle activity, reconstruct process relationships and identify potentially suspicious behaviour through configurable detection rules.

The project focuses on understanding how process activity can be monitored and analysed efficiently from the Linux kernel.

> **Project status:** Under development  
> **Project type:** Systems Programming | Linux Security | eBPF | Runtime Monitoring

## 1. Motivation

Understanding runtime process behaviour is an important part of Linux security monitoring. Process creation, execution and termination events can provide useful information about how applications interact and how potentially suspicious activity develops.

MiniSentinel explores how eBPF can be used to collect this information with low monitoring overhead and how collected events can be transformed into meaningful process relationships.

## 2. Objectives

- Monitor selected process lifecycle events using eBPF.
- Reconstruct parent-child process relationships.
- Maintain process provenance information.
- Observe selected pathname-related activity.
- Apply predefined rules to identify suspicious behaviour.
- Measure event loss, monitoring overhead and detection latency.

## 3. Proposed Architecture

The system is organised around the following conceptual components:

1. **Kernel Event Collection** — Observe selected process events using eBPF.
2. **Event Transport** — Transfer collected events to user space.
3. **Process Tracking** — Maintain process identities and reconstruct process relationships.
4. **Rule Engine** — Evaluate observed activity against predefined detection rules.
5. **Evaluation** — Measure reliability, performance and detection behaviour.

## 4. Evaluation

The project will evaluate:

- Event collection reliability and event loss.
- Monitoring overhead.
- Detection latency.
- Correctness of process relationship reconstruction.
- Behaviour under different process workloads.

## 5. Scope and Limitations

MiniSentinel is an experimental monitoring and detection prototype. It is not intended to be a complete Endpoint Detection and Response (EDR) platform.

Its initial scope is focused on process activity observation, provenance reconstruction and rule-based detection. It does not claim to prevent attacks or provide comprehensive system-wide security coverage.

## 6. Technology

- Linux
- eBPF
- C / systems programming
- User-space event processing

Specific implementation details and dependencies will be documented as development progresses.

## 7. Repository Structure

The repository will progressively organise kernel-side programs, user-space components, documentation, tests and evaluation tools.

## 8. Development Roadmap

- [ ] Establish the Linux development environment.
- [ ] Implement process lifecycle event collection.
- [ ] Develop user-space event processing.
- [ ] Implement process
