# Ansys Meshing Prime

> Runs Ansys Meshing Prime through this assistant instead of you opening the Ansys application by hand — it breaks a 3D model into the mesh (grid) that other simulation tools need in order to run. Needs Ansys Meshing Prime installed and licensed on this computer; the first time you use it, point it at your Ansys install folder.

The bundle zip (**43 MB**) is stored in this repository at **`2c2ce129-d545-428a-a76e-bc881e80a513.zip`**.

This repository is part of the **Forjinn-Desk** MCP bundle collection. An MCP bundle is a self-contained server that a host application launches and communicates with over the MCP (Model Context Protocol) protocol.

## Repo metadata

| Field | Value |
| --- | --- |
| Registry ID | `2c2ce129-d545-428a-a76e-bc881e80a513` |
| Status in registry | active |
| Bundle size | 43 MB |
| Distribution | committed to this repo |

## Environment variables

| Variable | Value / note |
| --- | --- |
| `ANSYS_ROOT` | `C:\ANSYS\v252\ansys_inc` |

## MCP launch configuration

The host replaces `__INSTALL_DIR__` (install dir) and `__PYTHON__` (bundled Python) at runtime.

```json
{
  "command": "__PYTHON__",
  "args": [
    "server.py"
  ],
  "cwd": "__INSTALL_DIR__",
  "env": {
    "ANSYS_ROOT": "",
    "ANSYS_WORKDIR": "__INSTALL_DIR__",
    "AEDT_NO_GUI": "1"
  }
}
```


## Install / usage

1. Get the bundle:
   - download `2c2ce129-d545-428a-a76e-bc881e80a513.zip` from this repo (Code → Download ZIP, or `git clone`).
2. Extract to your target installation directory (config paths expect contents at the install-dir root).
3. Set the environment variables listed above.
4. Launch using the MCP config JSON (or let a host client manage it automatically).

> Bundles may include vendored runtimes (bundled Python, Node, or native executables). Builds are Windows x64.
