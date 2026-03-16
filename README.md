# A Refinement and Verification Pipeline for Learning-Based Planning: Temporal Consistency, Dynamic Feasibility, and Comfort

**Paper:** [A Refinement and Verification Pipeline for Learning-Based Planning: Temporal Consistency, Dynamic Feasibility, and Comfort]

**Authors:** Seungwoo Heo, Seheon Ha, Jahyun Koo, Jiwon Seok, Yuseung Na, and Kichun Jo

**Affiliation:** Hanyang University

**YouTube:** [Real-Vehicle Comfort Demo Supplementary Videos] (https://www.youtube.com/TBD)

## Abstract

Learning-based motion planners infer driving behavior from data, reducing reliance on hand-crafted rules. However, closed-loop deployment remains difficult because their outputs can fluctuate across planning cycles, violate vehicle dynamics and friction limits, and degrade ride comfort through unnecessary acceleration and steering oscillations. Prior safety filters and low-level control corrections can mitigate immediate violations, but they do not provide a unified mechanism that enforces trajectory-level consistency, executability, and risk-aware validation at the planner output. This paper proposes a refinement-and-verification trajectory processing pipeline that improves closed-loop execution without replacing the underlying planner. The pipeline combines a Kalman filter--based consistency refinement across planning cycles, an NMPC-based Dynamic--Safety--Comfort refinement that enforces vehicle dynamics together with safety and comfort constraints, and a risk-aware verification and selection stage based on friction limits, collision risk, and driving-quality metrics. On the NuPlan closed-loop benchmark, the full pipeline improves ride-comfort metrics by more than 10\% and increases collision- and TTC-related safety metrics by about 4\%, yielding a consistent gain in the overall planning score. Additional evaluation in CarMaker and real-vehicle experiments shows that the refined trajectories remain dynamically feasible and can be stably tracked without sacrificing task-level driving performance. These results support the role of a structured trajectory-level intermediate layer for bridging learning-based planning and real-world execution.


## Real-Vehicle Comfort Demo Supplementary Videos

The real-vehicle experiments were conducted at **K-City**, the autonomous driving proving ground operated by the Korea Transportation Safety Authority (KATRI).
The experimental platform was a research-grade **Hyundai IONIQ 5** equipped with a **128-channel LiDAR, blind-spot LiDARs, a MEMS LiDAR, RTK-GNSS, and an onboard PC with a CAN interface**. The full planning and refinement pipeline was deployed onboard and operated in closed loop at **10 Hz**.
For real-vehicle comfort evaluation, two representative scenarios from the paper are shared in this repository. Each video is presented in a side-by-side format for qualitative comparison, with **ML on the left** and **Refined on the right**.

### Scenario 4: Arterial Driving
This scenario evaluates ride comfort during arterial-road driving with lane changes under the condition of **ego speed below 50 km/h**.
** YouTube Link:** [Scenario 4 Video](https://www.youtube.com/TBD)

### Scenario 5: Urban Driving with Stop-and-Gp
This scenario evaluates ride comfort during urban driving with repeated stop-and-go behavior under the condition of **ego speed below 30 km/h**.** YouTube Link:** [Scenario 5 Video](https://www.youtube.com/TBD)
