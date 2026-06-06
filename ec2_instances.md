
| EC2 Purchase Option | Commitment | Discount Potential | Flexibility | Interruption Risk | Best For | Key Properties |
|---|---|---:|---:|---:|---|---|
| **On-Demand Instances** | None | Low | High | None | Short-term, unpredictable, or spiky workloads | Pay by the second/minute/hour depending on OS; no upfront commitment |
| **Reserved Instances (Standard)** | 1 or 3 years | High | Low | None | Steady-state workloads with predictable usage | Lower cost than On-Demand; best savings; limited change flexibility |
| **Reserved Instances (Convertible)** | 1 or 3 years | Medium | High | None | Workloads that may change over time | Can exchange for another RI with different attributes if equal or greater value |
| **Savings Plans** | 1 or 3 years | High | High | None | Flexible compute usage across EC2, Lambda, and Fargate | Commit to a spend per hour; simpler than RIs; applies automatically to eligible usage |
| **Spot Instances** | None | Very High | Medium | **Yes** | Fault-tolerant, interruptible, batch, and flexible workloads | Uses spare AWS capacity; can be interrupted with short notice |
| **Dedicated Instances** | None | Low to Medium | Medium | None | Compliance or isolation requirements | Runs on hardware dedicated to your account; AWS manages the host |
| **Dedicated Hosts** | None | Low to Medium | Medium | None | Licensing, compliance, or server-bound software | Physical server dedicated to one customer; visibility into sockets/cores |
| **Capacity Reservations** | None or short-term commitment | No direct discount | Medium | None | Guaranteed capacity in a specific AZ | Reserves EC2 capacity, not necessarily a pricing discount |
| **Scheduled Instances** *(legacy / limited)* | Recurring schedule | Medium | Low | None | Predictable recurring workloads | Runs during specific recurring time windows; limited availability/legacy use |

## Quick notes
- **Cheapest but interruptible**: **Spot Instances**
- **Best for predictable steady use**: **Standard Reserved Instances** or **Savings Plans**
- **Best for changing workloads**: **Convertible RIs** or **Savings Plans**
- **Best for compliance/licensing**: **Dedicated Hosts**
- **Best for guaranteed capacity**: **Capacity Reservations**
- 
