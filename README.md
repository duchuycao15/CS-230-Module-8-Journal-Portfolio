# CS-230-Module-8-Journal-Portfolio

Summarize The Gaming Room client and software requirements?

The client, The Gaming Room, wants to expand their existing game so it can be played by more users across multiple platforms. The main goal is to move from a single-platform implementation to a scalable, networked solution that supports multiple concurrent players and game sessions. Key requirements include:

A centralized server-based design so many users can connect at the same time.

Support for multiple teams/players, organized into game sessions.

Consistent game rules and state management so players see the same results.

A solution that can scale (performance + capacity) as the user base grows.

Basic security and reliability expectations appropriate for an online product (controlled access, stable uptime, and protection of game data/session state).

What you did well in the documentation ?

I did well at organizing the SDD so it reads like a clear decision trail: requirements → constraints → architecture → recommendations. I also did a strong job translating the problem into a domain model (games, teams, players) and describing how the system should manage those objects consistently. Another area I did well was identifying major technical constraints early (platform compatibility, concurrency, scalability, and maintainability) so the design choices were tied to real needs instead of personal preference.

What was helpful about working through the design document when developing code? 

Working through the design document made development more structured because it forced me to define the system boundaries and responsibilities before coding. The domain model and architectural decisions helped me avoid “random implementation,” especially around:

Object ownership and lifecycle (what gets created once vs. per session).

Concurrency concerns (what happens when many users create/join games at the same time).

Consistency rules (unique naming, preventing duplicates, enforcing valid state).
Because those decisions were already written down, coding became more about implementation details and less about constantly re-deciding the architecture.

What you would revise and how you would improve it? 

If I revised the SDD, I would make the technical sections even more actionable for implementation. Improvements I would add:

More detailed API/service interface descriptions (inputs/outputs, error cases, and sample calls).

Expanded security section (authentication approach, basic threat considerations, and data protection expectations).

A clearer data persistence plan (what must be stored, how it’s updated, and what happens on restart/failure).

Additional diagrams (for example: sequence diagrams for “create game,” “join team,” and “start round”) to reduce ambiguity.
These changes would reduce assumptions during coding and make the SDD stronger as a true build guide.

How you interpreted user needs and why user needs matter in design? 

I interpreted user needs by converting the client’s goals into concrete behaviors the software must support (user stories and constraints). For example, if the client expects many users at once, the design must prioritize scalability and concurrency; if the client wants multi-platform access, the architecture should avoid platform-locked decisions. User needs matter because they shape both functional requirements (what the system does) and non-functional requirements (performance, reliability, security, usability). If those needs aren’t captured correctly, the system can be “technically correct” but still fail the client in real use.

Your design approach + techniques/strategies you’d use in the future?

My design approach is to start broad and then tighten: clarify requirements first, choose an architecture that fits the constraints, then validate with small prototypes before full implementation. In the future, I will continue using:

Iterative design (refine in small cycles rather than one big guess).

UML/domain modeling to make relationships and responsibilities explicit.

Architectural decision records (ADRs) to document why key choices were made.

Early planning for concurrency, scaling, and error handling, not as afterthoughts.

Basic testing strategy planning upfront (unit tests for logic + integration tests for workflows).
These techniques reduce rework, make the system easier to maintain, and keep implementation aligned with client outcomes.
