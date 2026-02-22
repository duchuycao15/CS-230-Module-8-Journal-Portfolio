# CS-230-Module-8-Journal-Portfolio

1. Summarize The Gaming Room client and software requirements?

The client, The Gaming Room, wants to expand their existing game into a solution that can support more users and operate across multiple platforms. The core requirement is to move toward a scalable, networked design that allows multiple users to play at the same time while keeping the game state consistent. This includes supporting multiple game sessions and organizing players (and teams, if applicable) in a structured way. The system should be reliable and maintainable, and it should be designed with performance and basic security expectations in mind, since it will be accessed by many users through a shared online environment.

2. What you did well in the documentation ?

I did well at organizing the SDD so it reads like a clear decision trail: requirements → constraints → architecture → recommendations. I also did a strong job translating the problem into a domain model (games, teams, players) and describing how the system should manage those objects consistently. Another area I did well was identifying major technical constraints early (platform compatibility, concurrency, scalability, and maintainability) so the design choices were tied to real needs instead of personal preference.

3. What was helpful about working through the design document when developing code? 

Working through the design document made development easier because it forced me to plan system responsibilities and behaviors before writing code. By defining the system architecture, the relationships between key objects, and the flow of major actions ahead of time, I reduced confusion during implementation and avoided redesigning core ideas mid-way through development. It was especially helpful for planning how the system should manage shared game state, how it should handle multiple users at the same time, and how it should enforce consistent rules (such as preventing duplicate entities and maintaining valid game/session state).

4. What you would revise and how you would improve it? 

If I could revise the design document, I would make it more implementation-ready by adding more concrete technical details. For example, I would expand the security portion by outlining a clearer approach for access control and data protection, and I would include more details about how game/session data should be stored and recovered if the system restarts or fails. I would also improve the document by adding more diagrams or sequence-style descriptions for key workflows like creating a game, joining a session, and starting gameplay, because those details reduce ambiguity and make the design easier to implement consistently.

5. How you interpreted user needs and why user needs matter in design?

I interpreted user needs by translating what the client wants into specific functional and non-functional requirements. For example, if users need to access the game from different platforms and play concurrently, the design must prioritize compatibility, scalability, and consistent performance. User needs matter because they directly determine whether the software succeeds in real usage; even a well-coded system can fail if it doesn’t meet the expectations of the people using it. Designing around user needs also helps ensure the system is reliable, intuitive, and aligned with the business goals of the client.

6. Your design approach + techniques/strategies you’d use in the future?

My design approach is to start by clarifying requirements and constraints, then select an architecture that matches those needs, and finally refine the solution in iterations. In the future, I will continue using strategies such as domain modeling (to clearly define objects and responsibilities), documenting key architectural decisions (so choices are justified and easy to maintain), and planning early for scalability, concurrency, and error handling. I also want to include a clearer testing strategy earlier in the design process, because it improves reliability and makes it easier to validate that the implementation matches the design.
