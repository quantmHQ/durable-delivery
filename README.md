# Durable Delivery: Building Confidence in Distributed Systems

**Executive Summary:**

Deploying distributed systems reliably and predictably remains a significant challenge, with complex failure modes and intricate "table stakes" to manage. This white paper introduces **Durable Delivery**, a set of principles and practices that empower organizations to build robust and resilient delivery pipelines for distributed systems. By adopting these principles, organizations can gain greater confidence in their deployments, minimize disruptions, and ensure rapid recovery from issues.

**Challenges of Distributed System Deployments:**

- **Nuanced Failure Modes:** Complex systems introduce diverse failure possibilities, often requiring specialized expertise to address.
- **Critical "Table Stakes":** Core functionalities like controlled rollouts and reliable rollbacks are essential but challenging to coordinate effectively.
- **Additional Complexities:** Traffic draining, make-before-break strategies, and maintaining safety invariants further complicate the deployment process.
- **Need for Manual Override:** The ability to manually intervene remains crucial for unforeseen circumstances.

**Limitations of Existing Solutions:**

While continuous delivery tools have evolved, they often:

- **Require significant customization**, especially for specialized infrastructure.
- **Primarily focus on Kubernetes deployments**, leaving a large portion of infrastructures unaddressed.

**Introducing Durable Delivery:**

Durable Delivery is a framework built on the following principles.

- **Orderly Code Flow:**
  - FIFO pull request management for predictability and control.
  - Automated validation and testing for early bug detection.
  - Automatic conflict resolution to minimize manual intervention.
- **Unified Stack Management:**
  - Version sets for comprehensive codebase visibility.
  - Effective dependency management for proactive issue identification.
- **Clean Environment Enforcement:**
  - Versioned and Immutable guarantees stable and isolated environments for each deployment.
- **Progressive Rollouts:**
  - Gradual shift of traffic to newly minted infrastructure
  - Investing in monitoring
- **Rapid Recovery:**
  - Keeping one or two older immutable infra-sets warm
  - Manual overrides for quick transfer of traffic to last known good infrastructure from available warm infra-sets.

**Key Components of Durable Delivery:**

**Benefits of Durable Delivery:**

Adopting Durable Delivery offers several benefits, such as:

- **Increased Confidence:** Predictable and reliable deployments lead to greater confidence in the system.
- **Reduced Disruptions:** Structured rollouts and clean environments minimize downtime and impact on users.
- **Faster Recovery:** One-click rollbacks enable swift issue resolution and minimized service interruptions.
- **Improved Operational Efficiency:** Streamlined processes and automated tasks reduce manual intervention and operational overhead.

**Conclusion:**

Durable Delivery empowers organizations to build resilient and reliable delivery pipelines for their distributed systems. By understanding and implementing its principles, organizations can achieve greater confidence in their deployments, minimize disruptions, and ensure rapid recovery from unforeseen issues.

**Additional Notes:**

- [Safe Velocity](https://exp-platform.com/Documents/2019%20TongXiaSumitBhardwajPavelDmitrievAleksanderFabijan_Safe-Velocity-ICSE-SEI.pdf)
- [Keeping the Master Green at Uber Scale](https://dl.acm.org/ft_gateway.cfm?CFID=58774186&CFTOKEN=b4523e763804e44b-116C8152-E1B2-E079-0753A4F82D863A92&dwn=1&ftid=2045461&id=3303970&uclick_id=1ce424ac-ddd3-4bb2-9368-e5ef47020e2b)
- [Amazon's Brazi Build System](https://gist.github.com/terabyte/15a2d3d407285b8b5a0a7964dd6283b0)
