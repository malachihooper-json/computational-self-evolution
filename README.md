# Self Evolution Via Code Manipulation in C#

Plug-and-play metaprogramming engine for self-modifying code.

## Quick Start

```bash
dotnet build
```

```csharp
using SelfEvolution;

var engine = new SelfModificationEngine("./src");
var analysis = await engine.AnalyzeCodebaseAsync();
await engine.ModifyCodeAsync(new CodeModification {
    FilePath = "MyClass.cs",
    TargetClass = "MyClass",
    Operation = "add_method",
    Code = "public void NewMethod() { }"
});
```

## Components

| File | Purpose |
|------|---------|
| SelfModificationEngine.cs | Codebase analysis and targeted modifications |
| CodeWriter.cs | Programmatic code generation |
| VersionManager.cs | Version tracking and rollback |
| AutonomousExecutor.cs | Self-executing code with sandboxing |
| ContinuousLearningEngine.cs | Learning from execution outcomes |

## Features

- Analyze C# source files and extract metadata
- Insert, modify, or remove code blocks programmatically
- Version-controlled modifications with rollback
- Generate capability code from descriptions

## Requirements

- .NET 8.0+
- Write access to source directory

