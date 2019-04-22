# cloudshell-tools
Scripts I tend to keep around in my Azure Cloudshell environment.

## Getting Started

This is a collection of scripts meant to be run in an [Azure Cloud Shell][1] environment. There will be some scripts for bash, and some for PowerShell.

To start, this is a collection of my personal tools. If you find some scripts more useful than others or have suggestions, please feel free to [open an issue][2].

## Repository Structure

### <code>[bashrc.d](./bashrc.d/)</code>

All files are meant as examples of things you could append to `~/.bashrc`.

- Files are roughly organized by the frequency I use them or that I think they might be more generally useful.
- Example: <code>[01-add-homelocalbin-to-path](./bashrc.d/01-add-homelocalbin-to-path)</code> is something I find extremely helpful and would not want to use Cloud Shell without.
- Also: <code>[90-autoload-nvm](./bashrc.d/99-autoload-nvm)</code> is maybe fairly useful, but kind of niche, depends on some prior setup, and also expensive to load.
- Where one script might depend on the prior run of another, I order them but don't make any structure to ensure dependencies. Hopefully it's fairly evident though.

### <code>[local/bin](./local/bin/)</code>

Self-contained scripts that are more complicated than an alias, but useful enough that I've found myself using them frequently. Here's a short list of examples.

#### <code>[cpu-usage-for-type](./local/bin/cpu-usage-for-type)</code>

Check the vCPU usage quota in your subscription for a region (default set in script) for a CPU family.

Example

```bash
cpu-usage-for-type D "Central US"
```

Reports the usage and quota for all D, DS, Dv2, DSv2, Dv3, Dsv3 sized vCPUs in the "Central US" region

## Copying

Please refer to the [license file](./LICENSE) for details. If a file does not have a copying or usage guideline in the file, the LICENSE file in the root of this repository should be assumed to apply.

<footer>
maxwellb/cloudshell-tools Tools for use with Azure Cloud Shell. Copyright (C) 2019  Maxwell Bloch
 </footer>

[1]: https://azure.microsoft.com/en-us/features/cloud-shell/
[2]: ../../issues/new?title=[]&body=[]
