# PID Tank Level Control System with HMI

A PLC-based tank level control system developed in **Siemens TIA Portal** using Factory I/O as a simulation environment.
The system uses a **PID controller** to automatically regulate tank liquid level based on a user-defined setpoint.
An HMI provides real-time visualization, manual parameter adjustment, and trend monitoring of the control process.

## System Overview
- The system controls the liquid level of a simulated tank process.
- The operator can enter a desired level setpoint via the HMI.
- The current tank level is read from an analog input coming from Factory I/O.
- Control behavior and system response are visualized in real time.

## PID Control
- A PID controller regulates the filling process to maintain the desired tank level.
- **Automatic PID fine-tuning** is performed directly in **TIA Portal** during runtime.
- The tuning process generates optimized **Proportional, Integral, and Derivative** values.
- Tuned PID parameters are mapped to HMI tags.
- The operator can manually adjust **Kp, Ki, and Kd** via the HMI if further tuning is required.
- The controller output drives the filling actuator proportionally.

## Analog Signal Handling
- Raw tank level data is acquired from Factory I/O via an analog input.
- The signal is normalized and scaled into engineering units for visualization on the HMI.

## HMI Features
- Input fields for:
  - Tank level setpoint
  - PID parameters (Kp, Ki, Kd)
- Numeric display of the current tank level.
- Bar indicator showing real-time liquid level.
- Trend visualization displaying:
  - Setpoint level
  - Actual tank level
- Trends allow observation of system response, overshoot, and steady-state behavior.

## Tools & Technologies
- Siemens TIA Portal
- Siemens WinCC Advanced
- Factory I/O
- PLCSIM

## What I Learned
- Implementing closed-loop PID control in PLC systems
- Using TIA Portal’s automatic PID fine-tuning tools
- Adjusting PID parameters manually via HMI
- Visualizing control performance using trends
- Processing and scaling analog process signals

## Possible Improvements
- Alarm handling for high and low-level limits
- Data logging for long-term trend analysis
