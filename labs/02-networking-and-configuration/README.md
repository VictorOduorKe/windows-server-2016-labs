# Network Architecture

This repository documents the structural layout and virtualized environment setup for the network topology.

## Table of Contents
- [Overview](#overview)
- [Topology Diagram](#topology-diagram)
- [Component Specifications](#component-specifications)
- [Getting Started](#getting-started)

---

## Overview

The network is deployed on a physical host utilizing virtualization software to isolate and manage guest operating systems through a shared internet gateway.

---

## Topology Diagram

```text
         [ PHYSICAL MACHINE ]
                  |
           INTERNET ACCESS
                  |
          [ VIRTUAL BOX ]
                  |
    -----------------------------
    |                           |              
[ WINDOW-SERV01 ]         [ WINDOWS 10 ]
(Windows Server 2016)     (Windows 10)
    (VM1)                     (VM2)