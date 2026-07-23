# Arjun Sood

Atlanta, GA | +1 (267) 903 5103 | asood74@gatech.edu | US Citizen

## Education

**Georgia Institute of Technology** — Atlanta, GA — *Present*
Bachelor of Science in Computer Science — *Expected Graduation, May 2028*
Concentrations: AI + Modeling \& Simulation | GPA 3.55/4.00

## Experience

### Georgia Institute of Technology RICAL Robotics Laboratory — Atlanta, GA

**Robotics Engineer \& Researcher** — *August 2025 – Present*

* Developed reinforcement-learning training pipelines in NVIDIA Isaac Lab for Unitree Go2 locomotion across simulated construction-site terrain, using reward shaping, hyperparameter tuning, and curriculum learning across 4,096 GPU-parallel environments, 17 reward terms, and 5 terrain classes to improve rough-terrain success from approximately 62% to 89%.
* Trained Unitree H1-2 humanoid policies for object pickup, transport, and placement, designing task-specific reward functions and staged curricula for a 3-stage manipulation workflow across 6 object and environment configurations in construction-site manipulation scenarios.
* Replicated 2 robot simulation environments in MuJoCo to support cross-simulator validation and future sim-to-real deployment, while investigating contact-force constraints and wheel-module motor and material requirements across 3 candidate wheel-module configurations.
* Developed an environment-adaptive BLE beacon placement algorithm that parsed floor-plan geometry, room connectivity, signal-blocking obstacles, and task zones to generate zone-specific deployment layouts across 5 environment classifications.
* Applied simulated annealing over approximately 10,000 candidate layout perturbations per optimization run to optimize beacon locations using a 5-term weighted objective for zone and path coverage, adjacent-zone separation, non-line-of-sight penalties, and infrastructure cost.
* Designed placement rules for 5 environment types—warehouses, corridors, partitioned rooms, restricted areas, and metal-obstructed zones—incorporating variable beacon densities and 2 mounting-height strategies to improve indoor worker localization.
* Designing and prototyping a 4-wheel drive module using Arduino Mega and Dynamixel Shield; developing a custom RemoteXY wireless controller supporting real-time control of 4 wheel actuators for manual operation.
* Creating a reusable ROS 2 package with approximately 3 modular nodes for command input, wheel control, and system telemetry to interface wheel controls and make the platform easy to integrate into other robotics projects.
* Physically integrating the 4-wheel drive system with an existing quadruped robot platform, programming approximately 3 wheel-assisted gait and motion behaviors to work with the wheels.
* Implementing computer vision for obstacle detection and adding autonomous path-planning capabilities for navigation across 10+ simulated obstacle and terrain configurations.
* Documenting design, hardware assembly, and software architecture in approximately 25 pages of technical documentation to enable reproducibility and collaboration with future researchers.

### Color Robotics — San Francisco, CA

**Software Engineering Intern** — *March 2025 – October 2025*

* Designed and implemented an AI-powered diagnostic agent system using LLMs, retrieval-augmented generation (RAG), and knowledge graph techniques to support a 5-stage diagnostic workflow that analyzes machine issues, synthesizes maintenance data, recommends solutions, guides users interactively, and generates resolution reports for future use.
* Developed webpages and elements using HTML, CSS, React JS, Python, and Django for a robot monitoring platform that displays 12+ categories of live information from the backend about robot performance, metrics, errors, and deployments.

### The University of Pennsylvania ASSET Laboratory — Philadelphia, PA

**AI/ML Engineer \& Researcher** — *June 2024 – August 2025*

* Collaborated with PhD Students and Undergraduates on 3 AI research projects on LLMs and video foundational models with Professor Mayur Naik.
* Co-led a project where we trained an LLM in PyTorch using Group Relative Policy Optimization to generate Python scripts to search medical databases and make predictions for patient outcomes under 2 treatment conditions—with and without medical treatment.
* Researched, developed, and implemented a new selective LLM fine-tuning and quantization technique in PyTorch and Python for my team's project in efficient LLM training and compression, achieving model performance within approximately 2 percentage points of full fine-tuning despite reducing the number of non-zero bits by 50%.
* Researched and proposed approximately 6 techniques to make video foundational model object action detection system more computationally efficient.
* Developed a prompting interface with approximately 6 configurable input and control elements for machine learning engineers to guide video foundational model in training with HTML, CSS, React JS, and Figma.

### Drive Engineering — Lansdale, PA

**Traffic Engineering and Web Development Intern** — *April 2024 – May 2024*

* Reoptimized traffic light timing systems by modeling and simulating approximately 4 intersections in Synchro 11.
* Improved highway monitoring systems by repositioning approximately 8 CCTV cameras for optimal coverage.
* Enhanced Drive Engineering's website user experience by redesigning approximately 7 webpages with Wix for improved usability.
* Facilitated communication between engineers and clients by making 10+ project reports.

## Selected Projects

### Language-Conditioned Vision-Language-Action Robot Manipulation

Built an end-to-end language-conditioned Vision-Language-Action robot manipulation system (PyTorch, Hugging Face LeRobot, SO-101 arm) spanning teleoperated data collection, dataset curation, policy training, real-time control, and evaluation.

* Trained and benchmarked a four-model ladder — from-scratch behavior cloning, ACT, SmolVLA, and a LoRA/QLoRA fine-tune of the 7B-parameter OpenVLA — on 800 demonstrations across 8 tabletop tasks, improving held-out success from 34% to 76%.
* Designed a reproducible evaluation suite (Wilson 95% confidence intervals over 20 trials/condition) measuring paraphrase generalization, unseen-position and distractor robustness, and end-to-end inference latency across 640 held-out trials.
* Engineered an async policy-inference server and 30 Hz robot client (WebSockets + msgpack) with a hard safety filter — joint/velocity clamps, forward-kinematics workspace bounds, gripper-current cap, and e-stop — enforcing zero unsafe motor commands.
* Delivered a reproducible research stack: fixed seeds, version-controlled YAML configs, Hub-versioned datasets, 47 hardware-free tests covering the full control loop, and a paper-style report with ablations and failure analysis.

### Reinforcement Learning for Robust Quadruped Locomotion

Trained robust quadruped locomotion policies (Unitree Go2) in NVIDIA Isaac Lab with PPO across 4,096 GPU-parallel environments, designing a 17-term shaped reward, procedural terrain curriculum, and full domain randomization (mass, friction, motor strength, sensor noise, actuation latency) for sim-to-real transfer.

* Built an end-to-end vision-based controller: 64×64 egocentric depth images encoded by a custom CNN and fused with proprioception in an asymmetric actor-critic (privileged terrain critic), trained end-to-end with RL to traverse stairs, slopes, and gaps without privileged height maps.
* Engineered a quantitative evaluation harness measuring success/fall rate, velocity-tracking error, cost of transport, and push-recovery rate over 100-episode suites; improved rough-terrain success from 62%→89% and demonstrated domain-randomized policies dominating baselines under perturbation sweeps.
* Validated every reward and randomization component via controlled ablation studies (fixed-seed retraining per term), documenting failure modes — foot-skating, twitching, high-torque gaits — attributable to each removed term.
* Exported policies to TorchScript/ONNX with numerical parity verification and shipped deployment wrappers — a ROS2 inference node and a C++ libtorch 50 Hz control loop — with safety clamps, watchdogs, EMA action filtering, and sub-millisecond p95 inference latency against a 20 ms real-time budget.

### Quant Research Platform \& C++ Event-Driven Backtesting Engine

Built a market-data research platform ingesting exchange L2 order-book/trade feeds into hive-partitioned Parquet with schema validation, sequence-gap detection, and DuckDB SQL achieving 18× faster range queries than a pandas baseline via partition pruning and predicate pushdown.

* Wrote a C++20 limit-order-book replay engine with zero-copy pybind11/NumPy bindings (GIL released in the hot loop), processing 15M events/sec — 30× the pure-Python reference — with bit-identical cross-language parity enforced in CI.
* Developed an event-driven backtester simulating order latency, book-walking market impact, maker/taker fees, and L2 queue-position approximation for limit orders, with portfolio accounting identities verified by property-style tests.
* Implemented leakage-safe evaluation: walk-forward and purged K-fold splits, train-only hyperparameter tuning, stationary-bootstrap Sharpe confidence intervals, and automated lookahead detection (prefix-property checks) that fails CI on contaminated features.
* Shipped production tooling around the research core: FastAPI experiment service, SQLite run registry, Streamlit dashboard, seeded synthetic market simulator for full reproducibility, 60+ tests, GitHub Actions CI, and multi-stage Docker builds.

### Time-Series ML Platform with Distributed Training and Inference for Noisy Market Data

Built a config-driven PyTorch training system (Transformer + TCN with multi-horizon heads, focal loss, mixed precision, gradient accumulation, DDP via torchrun, checkpointing, early stopping) for 3-class return-direction and volatility prediction on simulated limit-order-book data.

* Wrote a C++20 limit-order-book replay engine with zero-copy pybind11/NumPy bindings (GIL released in the hot loop), processing 15M events/sec — 30× the pure-Python reference — with bit-identical cross-language parity enforced in CI.
* Engineered a causal microstructure feature store (order-flow imbalance, book imbalance, realized volatility, rolling z-scores) with machine-checked no-lookahead guarantees: a truncation-invariance test asserts features are bit-identical when future data is removed.
* Designed a leakage-safe evaluation suite — purged/embargoed walk-forward splits, shuffled-label sanity tests, regime-sliced metrics, calibration error, and transaction-cost stress tests reporting the cost level at which the signal's Sharpe crosses zero.
* Benchmarked deep models against logistic-regression/GBDT/naive-rule baselines across 4 market regimes; causality unit tests caught a real bug where TCN normalization leaked future information across the time axis.
* Deployed a versioned model registry (atomic promotion, scaler shipped with weights) behind a FastAPI service with Prometheus histograms; measured \~1.5 ms p50 single-window CPU latency and \~4.1k windows/s batch throughput with a p50/p95/p99 benchmark harness; 43 pytest tests cover data, models, evaluation, and API.

### LLM Pretraining, Post-Training, and High-Performance Inference Engine

Built an end-to-end LLM platform from-scratch BPE tokenizer, LLaMA-style transformer (RoPE/GQA/SwiGLU), and distributed pretraining of 125M models on 2.5B tokens with DDP/FSDP2, bf16, and custom Triton kernels (fused RMSNorm, fused cross-entropy), reaching 36% MFU on A100s with bitwise-deterministic checkpoint resume.

* Ran a 9-run scaling study fitting compute–loss power laws against Chinchilla predictions, with matched-compute architecture ablations (RoPE, SwiGLU, GQA) and a MinHash-deduped, contamination-filtered data pipeline over memory-mapped shards.
* Post-trained via SFT (loss masking, sequence packing) and a from-scratch DPO implementation; evaluated with lm-eval-harness (HellaSwag, ARC, PIQA, WinoGrande, MMLU) and position-debiased LLM-judge win rates with bootstrap CIs across all training stages.
* Engineered a vLLM-style inference engine: paged KV cache with prefix caching and copy-on-write, continuous batching with preemption, speculative decoding (1.8× decode speedup at 72% acceptance), and int8 weight-only quantization — serving 18,000 tok/s with 42 ms p99 TTFT under Poisson load via a streaming SSE server with Prometheus metrics.
* Shipped with 65+ unit tests in CI (logit-parity between engine and reference model, paged-vs-dense attention equivalence, kernel correctness), Docker packaging, a model card, and a full benchmark report vs Hugging Face and vLLM baselines.

### Raft-Replicated Key-Value Store with From-Scratch LSM Engine \& Deterministic Simulation Testing

Built a linearizable distributed KV database from scratch (no DB/consensus/RPC libraries): LSM-tree storage engine (CRC-framed WAL with torn-write recovery, bloom-filtered SSTables, leveled compaction, MVCC snapshots) under a full Raft implementation (pre-vote elections, pipelined replication, InstallSnapshot, membership changes, ReadIndex).

* Engineered a FoundationDB-style deterministic simulator — entire cluster on virtual time with seeded fault injection (partitions, crashes, message loss, forced snapshot transfers) and exact seed replay — executing 11,000+ failure schedules (\~230M events) with a from-scratch Wing-Gong linearizability checker validating every run's client history.
* Caught and documented 6 real bugs pre-release (reproducing seeds preserved as CI regressions), including a snapshot-transfer wedge requiring four rare failures to align — invisible to unit tests and live chaos testing alike.
* Shipped the production layer: tokio server with single-owner event loop, group commit (3.4× write throughput), exactly-once client sessions via replicated dedup, three read-consistency modes priced at 0.55 ms / 0.94 ms / 10 ms p50 (stale / leased / linearizable-write) on a 3-node cluster.
* Measured failure behavior honestly: sub-second leader election under 300,000-op load with zero lost operations, client-observed failover decomposed (election vs. rediscovery) via YCSB-style benchmark suite built for the project.

## Skills

* **Programming Languages:** Python, C/C++, Rust, Java, SQL, Bash, MATLAB, JavaScript, HTML/CSS
* **Machine Learning \& AI:** PyTorch, Hugging Face Transformers, LeRobot, Reinforcement Learning, PPO, Behavior Cloning, ACT, OpenVLA, SmolVLA, LoRA/QLoRA, CNNs, Transformers, Reward Shaping, Curriculum Learning, Domain Randomization, Sim-to-Real Transfer, SFT, DPO, Mixed-Precision Training, DDP, FSDP2, Triton
* **Robotics \& Simulation:** NVIDIA Isaac Lab, MuJoCo, ROS2, Gazebo, RViz, Unitree Go2/H1-2, SO-101 Arm, Vision-Based Control, Robot Manipulation, Quadruped Locomotion, Contact-Force Management, Path Planning (A\*, RRT), SLAM, PID Control, Kalman/Particle Filtering, TorchScript, ONNX
* **Systems \& Distributed Computing:** Raft Consensus, LSM Trees, WAL/SSTables, MVCC, Bloom Filters, Deterministic Simulation, Linearizability Testing, Async Programming, Tokio, pybind11, Zero-Copy NumPy Integration, Multithreading, Real-Time Control, WebSockets, MessagePack
* **Data, Quant \& Model Infrastructure:** NumPy, Pandas, Parquet, DuckDB, SQLite, L2 Order Books, Event-Driven Backtesting, Market Microstructure Features, Walk-Forward Evaluation, Purged Cross-Validation, FastAPI, Streamlit, Prometheus, Model Serving, Model Registries
* **Development \& Infrastructure:** Git, Linux, Docker, GitHub Actions, CI/CD, pytest, YAML, Conda, CMake, REST APIs
* **Embedded Systems \& Hardware:** Arduino and Microcontroller SDKs, Embedded C/C++, SPI, I²C, UART, Dynamixel, Motor Drivers, LoRa/FSK, Sensor Integration, PCB Design, Power Distribution, Soldering, Oscilloscope/Multimeter Debugging
* **CAD \& Design:** Altium Designer, KiCad, AutoCAD, Blender, Mechanical Assembly and Robotics Connectorization

## Activities

### Georgia Tech's RoboJackets RoboCup Team — Atlanta, GA

**Electrical \& Software Subteam Engineer** — *August 2025 – Present*

* Develops the C++/ROS 2 autonomy stack for a six-robot soccer team across 7 major subsystems, including computer vision, state estimation, multi-agent strategy, path planning, motion control, simulation, and wireless robot communication.
* Receiving hands-on training in 3 technical areas—PCB design, circuit analysis, and power system fundamentals for competitive autonomous robots.
* Learning to select and integrate 4 major categories of electrical components, including batteries, motor drivers, microcontrollers, and sensors.
* Gaining experience with soldering, board assembly, and safe handling of high-voltage kicker circuits through multiple prototype assembly and testing sessions.
* Developing introductory skills in embedded firmware programming across 3 communication protocols—SPI, I²C, and serial communication—and 2 diagnostic instruments, multimeters and oscilloscopes.
* Building foundational knowledge in wireless communication protocols and robot power distribution design to prepare for future collaboration across 3 technical groups—mechanical, electrical, and software teams.

### AI @ GT Applied Research Project Team — Atlanta, GA

**AI/ML Engineer \& Researcher** — *August 2025 – Present*

* Collaborating with 1 PhD student and approximately 5 undergraduates on developing lifelong learning frameworks for autonomous household robots, aiming to enable continual skill acquisition and adaptation in open-ended environments.
* Ran baseline experiments using approximately 3 existing Vision Language Action Models across 10 household tasks on humanoid robot household task performance.
* Implementing a 3-component dual-process cognitive architecture that combines fast, reactive neural policies (System 1) with LLM-powered deliberative reasoning (System 2), coordinated by a metacognitive arbitrator that switches based on uncertainty and task novelty.
* Designing a meta-learning loop for agents to self-assess performance, rehearse skills, and prioritize learning based on 3 factors—utility, frequency, and confidence decay.
* Creating uncertainty-aware arbitration mechanisms using 2 primary trigger signals—policy uncertainty and task novelty that trigger LLM reasoning when skill policies are likely to fail, improving sample-efficiency and task success rates.
* Running simulation experiments in SAPIEN Simulator, progressively introducing approximately 5 environmental variation levels, 8 appliance types, and 12 multi-step tasks to benchmark robustness and forward transfer efficiency.
* Tracking performance using 3 advanced lifelong learning metrics, including Forward Transfer Efficiency, Catastrophic Forgetting Index, and Autonomy Index.
* Contributing to research pushing toward AGI-aligned embodied agents capable of self-directed reflection, domain-general skill acquisition, and adaptive behavior in real-world settings across multiple continually expanding household-task domains.

## Awards

* **Computer Science:** 1st place in DVSF Computer Science Research (2025); 1st place in MCSRC Computer Science Research (2025); 1st place in PJAS 1B Computer Science Research (2025); Villanova University Award for Computer Science Research (2025)
* **Engineering:** 1st place in PJAS 1B Engineering Research (2024); U.S. Air Force Special Award "For An Outstanding Science or Engineering Project" (2024); Germantown Academy "Excellence in AP Physics C" (2025); Germantown Academy "Greatest Perseverance in Math and Physics" (2025)
* **General:** National Merit Special Corporate Scholarship (2025)

