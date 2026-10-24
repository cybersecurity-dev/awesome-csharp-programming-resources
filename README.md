<div align="center">
    <p align="center">
        <a href="https://github.com/cybersecurity-dev/awesome-csharp-programming-language">
          <img width="5%" src="https://github.com/cybersecurity-dev/cybersecurity-dev/blob/main/assets/CSharp.svg" />
        </a>
    </p>

```mermaid
flowchart LR
    DEV["Student or Developer"]

    subgraph EDIT["Development<br/>Environment"]
        VS["Visual Studio"]
        VSCODE["Visual Studio<br/>Code"]
        RIDER["JetBrains<br/>Rider"]
        SDK[".NET SDK"]
        CLI["dotnet CLI"]
        NUGET["NuGet"]
    end

    subgraph BUILD["Build Pipeline"]
        SOURCE["C# Source<br/>Files"]
        PROJECT["Project<br/>File"]
        RESTORE["Package<br/>Restore"]
        COMPILER["C#<br/>Compiler"]
        IL["CIL and<br/>Metadata"]
        ASSEMBLY["DLL or<br/>EXE Assembly"]
    end

    subgraph RUNTIME["Execution<br/>Environment"]
        HOST[".NET Host"]
        CLR["Common Language<br/>Runtime"]
        JIT["JIT<br/>Compiler"]
        GC["Garbage<br/>Collector"]
        NATIVE["Native<br/>Machine Code"]
        OS["Operating<br/>System"]
    end

    subgraph ANALYSIS["Development and<br/>Analysis Tools"]
        DEBUGGER["Debugger"]
        TEST["Test Explorer"]
        PROFILER["Performance<br/>Profiler"]
        FORMAT["Code<br/>Formatter"]
        ANALYZER["Roslyn<br/>Analyzers"]
        LOG["Logging<br/>Tools"]
    end

    DEV --> VS
    DEV --> VSCODE
    DEV --> RIDER

    VS --> SDK
    VSCODE --> CLI
    RIDER --> SDK
    NUGET --> RESTORE

    SOURCE --> COMPILER
    PROJECT --> RESTORE
    RESTORE --> COMPILER
    SDK --> COMPILER
    CLI --> COMPILER

    COMPILER --> IL
    IL --> ASSEMBLY

    ASSEMBLY --> HOST
    HOST --> CLR
    CLR --> JIT
    CLR --> GC
    JIT --> NATIVE
    NATIVE --> OS

    SOURCE -.-> FORMAT
    SOURCE -.-> ANALYZER
    ASSEMBLY -.-> DEBUGGER
    ASSEMBLY -.-> TEST
    CLR -.-> PROFILER
    ASSEMBLY -.-> LOG

    DEBUGGER --> DEV
    TEST --> DEV
    PROFILER --> DEV
    ANALYZER --> DEV

    classDef human fill:#263238,color:#fff,stroke:#111,stroke-width:2px
    classDef development fill:#e3f2fd,color:#111,stroke:#1e88e5
    classDef build fill:#e8f5e9,color:#111,stroke:#43a047
    classDef runtime fill:#fff3e0,color:#111,stroke:#fb8c00
    classDef analysis fill:#f3e5f5,color:#111,stroke:#8e24aa

    class DEV human
    class VS,VSCODE,RIDER,SDK,CLI,NUGET development
    class SOURCE,PROJECT,RESTORE,COMPILER,IL,ASSEMBLY build
    class HOST,CLR,JIT,GC,NATIVE,OS runtime
    class DEBUGGER,TEST,PROFILER,FORMAT,ANALYZER,LOG analysis
```

# **`Awesome`** C# Programming Resources [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)
</div>

[![YouTube](https://img.shields.io/badge/YouTube-%23FF0000.svg?style=for-the-badge&logo=YouTube&logoColor=white)](https://youtube.com/playlist?list=PL9V4Zu3RroiWunx1SLqqxg3r-GPrNepeX&si=UaBDdIUmwsR9mgK8) 
[![Reddit](https://img.shields.io/badge/Reddit-FF4500?style=for-the-badge&logo=reddit&logoColor=white)](https://www.reddit.com/r/csharp/)

<p align="center">
    <a href="https://github.com/cybersecurity-dev/"><img height="25" src="https://github.com/cybersecurity-dev/cybersecurity-dev/blob/main/assets/github.svg" alt="GitHub"></a>
    &nbsp;
    <a href="https://www.youtube.com/@CyberThreatDefence"><img height="25" src="https://github.com/cybersecurity-dev/cybersecurity-dev/blob/main/assets/youtube.svg" alt="YouTube"></a>
    &nbsp;
    <a href="https://cyberthreatdefence.com/my_awesome_lists"><img height="20" src="https://github.com/cybersecurity-dev/cybersecurity-dev/blob/main/assets/blog.svg" alt="My Awesome Lists"></a>
</p>

```mermaid
flowchart LR
    SOURCE["C# Source Code<br/>.cs files"]
    PROJECT["Project Configuration<br/>.csproj"]
    PACKAGES["NuGet Packages"]

    SOURCE --> BUILD["dotnet build"]
    PROJECT --> BUILD
    PACKAGES --> RESTORE["Package Restore"]
    RESTORE --> BUILD

    BUILD --> ROSLYN["Roslyn C# Compiler"]

    ROSLYN --> CHECK{"Compilation<br/>successful?"}

    CHECK -->|"No"| ERRORS["Syntax,<br/>type or<br/>reference errors"]
    ERRORS --> SOURCE

    CHECK -->|"Yes"| ASSEMBLY["Managed<br/>Assembly<br/>EXE or DLL"]

    ASSEMBLY --> IL["Common<br/>Intermediate<br/>Language"]
    ASSEMBLY --> META["Type<br/>Metadata"]
    ASSEMBLY --> MANIFEST["Assembly<br/>Manifest"]

    IL --> HOST[".NET Host"]
    META --> CLR["Common<br/>Language<br/>Runtime"]
    MANIFEST --> CLR
    HOST --> CLR

    CLR --> LOAD["Assembly Loading"]
    LOAD --> VERIFY["Type and<br/>Safety Checks"]
    VERIFY --> JIT["JIT<br/>Compilation"]
    JIT --> MACHINE["Native<br/>Machine Code"]
    MACHINE --> CPU["CPU<br/>Execution"]

    CLR --> GC["Garbage<br/>Collection"]
    CLR --> EXCEPT["Exception<br/>Handling"]
    CLR --> THREAD["Thread and<br/>Task Management"]

    GC -.-> MACHINE
    EXCEPT -.-> MACHINE
    THREAD -.-> MACHINE

    classDef source fill:#e3f2fd,color:#111,stroke:#1e88e5
    classDef compiler fill:#e8f5e9,color:#111,stroke:#43a047
    classDef decision fill:#fff3e0,color:#111,stroke:#fb8c00,stroke-width:2px
    classDef assembly fill:#f3e5f5,color:#111,stroke:#8e24aa
    classDef runtime fill:#e0f7fa,color:#111,stroke:#00838f
    classDef error fill:#ffebee,color:#111,stroke:#e53935

    class SOURCE,PROJECT,PACKAGES,RESTORE source
    class BUILD,ROSLYN compiler
    class CHECK decision
    class ASSEMBLY,IL,META,MANIFEST assembly
    class HOST,CLR,LOAD,VERIFY,JIT,MACHINE,CPU,GC,EXCEPT,THREAD runtime
    class ERRORS error
```

## 📖 Contents
- [Books](#books)
- [Videos](#videos)
- [My Other Awesome Lists](#my-other-awesome-lists)
- [Contributing](#contributing)
- [Contributors](#contributors)

##

### Books

### Videos
- [Everything You Need to Know About the Latest in C#](https://youtu.be/jRJa83DeOd8?si=3rWZ-7x3rYqVePnU)
 
##

### My Other Awesome Lists
You can access the my other awesome lists [here](https://cyberthreatdefence.com/my_awesome_lists)

### Contributing
[Contributions of any kind welcome, just follow the guidelines](contributing.md)!

### Contributors
[Thanks goes to these contributors](https://github.com/cybersecurity-dev/awesome-csharp-programming-resources/graphs/contributors)!

### License
[![CC0](http://mirrors.creativecommons.org/presskit/buttons/88x31/svg/cc-zero.svg)](http://creativecommons.org/publicdomain/zero/1.0)

[🔼 Back to top](#awesome-c-programming-resources-)
