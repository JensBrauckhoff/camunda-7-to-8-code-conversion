# Camunda 7 to 8 Code Conversion

As Camunda 8 is a complete rewrite of Camunda 7, you must adjust solutions developed for Camunda 7 to run on Camunda 8.

This project:

-   Describes **[code converstion patterns](patterns/)**, specifically for

    -   [Client API usage](patterns/client.md): Whenever your solutions calls Camunda API, for example to start new process instances.
    -   [Glue code](patterns/glue-code.md): Whenever you define code that is executed when a process arrives at a specific state in the process, e.g. via JavaDelegates.

-   Provides **[OpenRewrite recipes](recipes/)** to automate refactoring of Java solutions.

-   Hosts a **[Camunda 7 API to Camunda 8 API Mapping WebApp (WIP)](https://camunda-community-hub.github.io/camunda-7-to-8-code-conversion/)** to quickly find information about Camunda 7 API endpoints and how they relate to Camunda 8 endpoints. Specifically:
    -   Which Camunda 7 endpoints map to Camunda 8 endpoints directly and how
    -   Which Camunda 7 endpoints are on the roadmap for upcoming Camunda 8 releases
    -   Which Camunda 7 endpoints are handled conceptually differently in Camunda 8
    -   Which Camunda 7 endpoints are discontinued

# Code conversion pattern catalog

> [!NOTE]  
> The pattern catalog was just kicked off and will be filled with more patterns throughout Q2 of 2025. The current patterns are more exemplary to discuss the structure. Feedback of course welcome.

-   Client API
    -   [Process Engine (Spring) &#8594; Zeebe Client (Spring)](patterns/client.md#process-engine-spring--zeebe-client-spring)
-   Glue code
    -   [Java Delegate (Spring) &#8594; Job Worker (Spring)](patterns/glue-code.md#java-delegate-spring--job-worker-spring)
    -   [Java Delegate (Java class) &#8594; Job Worker (Spring)](patterns/glue-code.md#java-delegate-java-class--job-worker-spring)
