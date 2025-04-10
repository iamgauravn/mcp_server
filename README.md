# MyFirstMCP - Model Context Protocol Server Example

This is a simple C# implementation of a Model Context Protocol (MCP) server using .NET 9. The project demonstrates how to create an MCP server with basic functionality including monkey and selling services.

## Prerequisites

- .NET 9.0 SDK
- Visual Studio Code or Visual Studio 2022

## Project Structure

```
MyFirstMCP/
├── Model/
│   └── Selling.cs
├── Service/
│   ├── MonkeyService.cs
│   └── SellingService.cs
├── Tools/
│   ├── EchoTool.cs
│   ├── MonkeyTools.cs
│   └── SellingTool.cs
└── Program.cs
```

## Configuration

To use this MCP server with Visual Studio Code, add the following configuration to your `./claude/claude_desktop_config.json`:

```json
{
    "mcpServers": {
        "weather": {
            "command": "dotnet",
            "args": [
                "run",
                "--project",
                "F:\\MyFirstMCP\\MyFirstMCP.csproj",
                "--no-build"
            ]
        }
    }
}
```

Make sure to update the project path to match your local environment.

## Features

- MonkeyService: Fetches monkey data from an external API
- SellingService: Manages selling records
- MCP Tools: Provides command interfaces for the services

## Getting Started

1. Clone the repository
2. Open the project in Visual Studio Code
3. Restore NuGet packages
4. Run the project

## References

For more information about Model Context Protocol:

- [Building an MCP Server in C#](https://devblogs.microsoft.com/dotnet/build-a-model-context-protocol-mcp-server-in-csharp/#:~:text=Getting%20Started%20Building%20an%20MCP%20server,-The%20MCP%20C%23&text=The%20ModelContextProtocol%20package%20gives%20access,through%20Microsoft.Extensions.AI%20.)
- [MCP Server Quick Start Guide](https://modelcontextprotocol.io/quickstart/server#windows)

## Dependencies

- Microsoft.Data.Sqlite (9.0.4)
- Microsoft.Extensions.Hosting (9.0.4)
- ModelContextProtocol (0.1.0-preview.7)