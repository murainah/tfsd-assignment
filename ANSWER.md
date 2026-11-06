## Question 1 — Python Wheel Package 


**File:** `ollama_python-0.1.2-py3-none-any.whl`

The wheel contains 14 files with a total uncompressed size of 49,679 bytes. Excluding the 10 `.py` files, the remaining four files are in the `ollama_python-0.1.2.dist-info` directory.

### 1.1 METADATA (11,822 bytes)

Contains the package information:

- **Name:** `ollama-python`
- **Version:** `0.1.2`
- **Author:** Richard
- **Author email:** `kogunyale01@gmail.com`
- **Metadata-Version:** `2.1`
- **Requires-Python:** `>=3.9,<4.0`
- **Description-Content-Type:** `text/markdown`

It also lists Python 3.9, 3.10, 3.11 and 3.12 classifiers and declares four dependencies:

| Dependency | Version constraint | Purpose |
|---|---|---|
| httpx | `>=0.26.0,<0.27.0` | HTTP communication, including asynchronous requests |
| pydantic | `>=2.5.3,<3.0.0` | Data validation and structured models |
| requests | `>=2.31.0,<3.0.0` | Sending HTTP requests |
| responses | `>=0.24.1,<0.25.0` | Mocking HTTP responses for testing |

The file also contains Markdown documentation with installation instructions, examples of text generation and chat (with and without streaming), image-based chat, embeddings, and model management operations such as creating, listing, pulling, pushing and deleting models.

It documents generation parameters including `temperature`, `top_k`, `top_p`, `num_ctx`, and `num_predict`, and provides contribution instructions using Poetry and pre-commit.

### 1.2 WHEEL (88 bytes)

Contains four fields:

- `Wheel-Version: 1.0` — identifies the wheel format version.
- `Generator: poetry-core 1.8.1` — identifies the build backend used.
- `Root-Is-Purelib: true` — indicates that the package is installed in Python's pure-library directory.
- `Tag: py3-none-any` — indicates that the wheel targets Python 3 without a specific Python ABI or operating-system requirement. The supported Python versions are further restricted by `Requires-Python` in METADATA.

### 1.3 RECORD (1,224 bytes)

Contains an inventory of all 14 files in the wheel. Each entry normally consists of the file path, SHA-256 hash and size in bytes.

The hashes allow verification of file integrity. The `RECORD` file's own entry (`RECORD,,`) has no hash or size.

### 1.4 LICENSE (11,350 bytes)

Contains the Apache License, Version 2.0 (January 2004).

The license permits using, modifying and redistributing the software, including commercially, subject to its conditions. It requires retaining applicable copyright and license notices, includes patent provisions and provides the software without warranties.

**Output:** [Task 1 — Wheel Contents](Outputs-Logs-Screenshots/task1_wheel_content.txt)


## 2. npm Package Analysis

**File:** `ollama-0.5.18.tgz`

The archive is a compressed npm package for the Ollama JavaScript library. Excluding the `dist` and `src` directories, three files remain in the `package` directory: `package.json`, `README.md`, and `LICENSE`.

### 2.1 package.json

Contains the package configuration and metadata:

- **Name:** `ollama`
- **Version:** `0.5.18`
- **Description:** Ollama Javascript library
- **Author:** Saul Boyd
- **License:** MIT
- **Repository:** https://github.com/ollama/ollama-js

**Module entry points:**

- `main: dist/index.cjs` — CommonJS entry point.
- `module: dist/index.mjs` — ES module entry point.
- `types: dist/index.d.ts` — TypeScript type declarations.
- `exports` — defines entry points for CommonJS (`require`), ES modules (`import`), TypeScript types, and a separate browser module (`ollama/browser`). It also includes a wildcard export (`./*`).

**Scripts:**

| Script | Command | Purpose |
|---|---|---|
| format | `prettier --write .` | Formats project files |
| test | `vitest --run` | Runs tests |
| build | `unbuild` | Builds the package |
| lint | `eslint ./src/*` | Checks source files for linting issues |
| prepublishOnly | `npm run build` | Builds the package before publishing |

**Dependencies:**

The package declares one runtime dependency, `whatwg-fetch (^3.6.20)`, which provides Fetch API functionality.

It also declares nine development dependencies:

- `@swc/core` — JavaScript/TypeScript compilation and transformation.
- `@types/whatwg-fetch` — TypeScript type definitions for Fetch.
- `@typescript-eslint/eslint-plugin` — TypeScript linting rules.
- `@typescript-eslint/parser` — allows ESLint to parse TypeScript.
- `eslint` — static code analysis.
- `vitest` — testing framework.
- `prettier` — code formatting.
- `typescript` — TypeScript compiler.
- `unbuild` — package build tool.

The `^` version prefix allows compatible updates within the specified major version for these dependencies.

### 2.2 README.md

Contains documentation for installing and using the Ollama JavaScript library.

It includes:

- **Installation:** `npm i ollama`.
- **Basic usage:** examples of sending chat requests to models such as `llama3.1`.
- **Browser usage:** importing the library through `ollama/browser`.
- **Streaming:** receiving generated responses incrementally using `stream: true` and an `AsyncGenerator`.
- **API reference:** documents `chat`, `generate`, `pull`, `push`, `create`, `delete`, `copy`, `list`, `show`, `embed`, `ps`, and `abort`, including their request parameters and response types.
- **Model configuration:** parameters for models, prompts, messages, images, tools, thinking, response formatting, streaming and runtime options.
- **Custom client:** configuring the Ollama server address, Fetch implementation and custom HTTP headers.
- **Building:** Provides the npm run build command for building the project files.

The documentation also explains that `abort()` stops all active streamed generations associated with a client instance, and that the `files` parameter is not supported by the library's `create` API in this version.

### 2.3 LICENSE

Contains the MIT License, with the copyright notice `Copyright (c) 2023 Saul`.

The license allows users to use, copy, modify, merge, publish, distribute, sublicense and sell the software.

The copyright and permission notices must be included in copies or substantial portions of the software. The software is provided without warranties, and the authors are not liable for damages arising from its use.

**Output:** [Task 2 — npm Contents](Outputs-Logs-Screenshots/task2_npm_contents.txt)



## 3. Maven Package Analysis 



### 3.1 Description of the Files

| File | Description |
|---|---|
| `ollama4j-1.1.0.jar` | Compiled Java library containing the classes needed to use Ollama4j. |
| `ollama4j-1.1.0-sources.jar` | Java source code archive, useful for debugging and understanding the implementation. |
| `ollama4j-1.1.0-javadoc.jar` | Generated Java API documentation for the library. |
| `ollama4j-1.1.0.pom` | Maven Project Object Model file containing project metadata, dependencies, build configuration, and publishing settings. |
| `*.asc` | PGP signature files used to verify the authenticity of the published artifacts. |
| `*.md5` | MD5 checksums for integrity checking. |
| `*.sha1` | SHA-1 checksums for integrity checking. |
| `*.sha256` | SHA-256 checksums for integrity checking. |
| `*.sha512` | SHA-512 checksums for integrity checking. |

Each of the four main artifacts (`.jar`, `-sources.jar`, `-javadoc.jar`, and `.pom`) has one signature file and four checksum files, giving 24 artifact-related files in total.

The downloaded `index.html` is the repository directory listing, while `robots.txt` contains crawler instructions and is not part of the Maven artifact.

### 3.2 Detailed Description of ollama4j-1.1.0.pom

**Project information**

- **Model version:** `4.0.0`
- **Group ID:** `io.github.ollama4j`
- **Artifact ID:** `ollama4j`
- **Version:** `1.1.0`
- **Name:** Ollama4j
- **Description:** Java library for interacting with Ollama API.
- **Packaging:** `jar`
- **Project URL:** https://github.com/ollama4j/ollama4j
- **Developer:** Amith Koujalgi
- **License:** MIT License

**Properties**

The project targets Java 11 using `maven.compiler.release` and specifies UTF-8 source encoding. It defines Lombok version `1.18.38`, Surefire and Failsafe plugin versions `3.0.0-M5`, and a build output timestamp derived from Git commit information.

**Dependencies**

The POM declares 11 direct dependencies:

| Dependency | Version | Scope | Purpose |
|---|---|---|---|
| lombok | 1.18.38 | provided | Reduces Java boilerplate through annotations |
| jsoup | 1.18.1 | compile (default) | HTML parsing |
| jackson-databind | 2.17.1 | compile (default) | JSON serialization and deserialization |
| jackson-datatype-jsr310 | 2.17.1 | compile (default) | Java date/time support for Jackson |
| logback-classic | 1.5.6 | test | Logging during tests |
| slf4j-api | 2.0.9 | compile (default) | Logging API |
| junit-jupiter-api | 5.10.0 | test | Unit testing |
| mockito-core | 4.1.0 | test | Mock objects for testing |
| json | 20240205 | test | JSON handling during tests |
| testcontainers-ollama | 1.20.2 | test | Ollama container-based testing |
| testcontainers-nginx | 1.20.0 | test | Nginx container-based testing |

The `provided` scope indicates that Lombok is expected to be available during compilation but is not packaged as a runtime dependency. Dependencies with `test` scope are used for testing rather than normal application execution.

**Build plugins**

- `maven-compiler-plugin` — compiles the Java code, with Lombok configured as an annotation processor.
- `maven-source-plugin` (3.3.1) — generates and attaches the source JAR.
- `maven-javadoc-plugin` (3.11.2) — generates and attaches the Javadoc JAR.
- `maven-surefire-plugin` (3.0.0-M5) — executes unit tests.
- `maven-failsafe-plugin` (3.0.0-M5) — executes integration tests and verification.
- `maven-gpg-plugin` (1.5) — signs artifacts during the verify phase.
- `git-commit-id-maven-plugin` (9.0.1) — retrieves Git commit information for build metadata.

The `pluginManagement` section also specifies compiler plugin version `3.14.0` and JAR plugin version `3.4.2`.

**Source control and distribution**

The `scm` section specifies the GitHub repository, developer connection and Git tag `1.1.0`. The `distributionManagement` section identifies the publishing repository as `central`.

**Build profiles**

The POM defines four profiles:

- `ossrh` — active by default; configures artifact publishing to Maven Central using the Sonatype Central Publishing plugin.
- `unit-tests` — enables unit tests, skips integration tests, and configures JaCoCo code coverage reporting.
- `integration-tests` — enables integration tests while skipping unit tests.
- `ci-cd` — configures automated builds, GPG signing, Sonatype staging and JaCoCo coverage reporting, while skipping unit and integration tests.

These profiles allow the project to use different configurations for testing, publishing and continuous integration.

**Output:** [Task 3 — Maven Files and POM](Outputs-Logs-Screenshots/task3_maven_content.txt)


## 4. Dependency Tree and Security Audit

**Project:** `dependency_project`  
**Package manager:** npm  
**Package:** `ollama@0.5.18`

### 4.1 Dependency Tree

```text
dependency_project@1.0.0
└── ollama@0.5.18
    └── whatwg-fetch@3.6.20
```

The project has 2 installed dependency packages:

- `ollama@0.5.18` — direct dependency.
- `whatwg-fetch@3.6.20` — transitive dependency required by Ollama.

### 4.2 Security Audit

The `npm audit` command reported:

**0 vulnerabilities found.**

### 4.3 Packages installed

**2 packages are installed:** `ollama@0.5.18` (direct) and `whatwg-fetch@3.6.20` (transitive), plus the root project itself. `ollama` also declares nine development dependencies, but npm does not install a dependency's dev dependencies, so they are not in the tree.

### 4.4 What the audit reported and what I would do

`npm audit` reported **0 vulnerabilities** (info, low, moderate, high and critical were all 0) for the 2 installed packages. The tree is small, so there is little attack surface.

Because nothing was reported, no fix is needed now. What I would do is:
- keep `package-lock.json` committed, so the versions that were audited are the ones that get installed;
- re-run `npm audit` regularly (for example in CI, or with Dependabot alerts), because new vulnerabilities can be disclosed later for versions that are clean today;
- if a vulnerability appears, first try `npm audit fix` or update `ollama`; if it comes from `whatwg-fetch`, check whether a newer `ollama` release depends on a fixed version.

A clean audit only covers vulnerabilities that are already publicly known. It does not prove the packages are free from security issues.

**Outputs:**

- [Dependency Tree](Outputs-Logs-Screenshots/task4_dependency_tree.txt)
- [Security Audit](Outputs-Logs-Screenshots/task4_audit.json)



## 5. Software Bill of Materials (SBOM)

**Project:** `dependency_project`  
**Format:** CycloneDX JSON  
**Specification version:** 1.6

The generated SBOM contains two dependency components:

| Component | Version | Type |
|---|---|---|
| ollama | 0.5.18 | library |
| whatwg-fetch | 3.6.20 | library |

The SBOM was generated with `@cyclonedx/cyclonedx-npm` 6.0.1 in CycloneDX 1.6 JSON format and lists 2 components plus the root project.

### Description of Three SBOM Entries

**1. ollama 0.5.18 (direct dependency)**

- **What it is:** a JavaScript client library for the Ollama API (MIT license).
- **Where it came from:** the npm registry. The SBOM records the tarball URL `https://registry.npmjs.org/ollama/-/ollama-0.5.18.tgz`, the package URL `pkg:npm/ollama@0.5.18`, and a SHA-512 hash of the tarball, so the exact file can be verified. It is installed at `node_modules/ollama`.
- **Why it is there:** my project depends on it directly. In the `dependencies` section of the SBOM, the root component `dependency_project` lists `ollama` in its `dependsOn`.

**2. whatwg-fetch 3.6.20 (transitive dependency)**

- **What it is:** a `window.fetch` polyfill (MIT license) that provides the Fetch API where it is not available.
- **Where it came from:** also the npm registry (`pkg:npm/whatwg-fetch@3.6.20`, with its own SHA-512 hash), installed at `node_modules/whatwg-fetch`. Its upstream repository is `github.com/github/fetch`.
- **Why it is there:** I did not ask for it. It is there only because `ollama` depends on it. The dependency graph shows `ollama@0.5.18` depending on `whatwg-fetch@3.6.20`, and no direct link from my project.

**3. dependency_project 1.0.0 (the root component)**

- **What it is:** my own project, recorded in `metadata.component` as an application with the ISC license.
- **Where it came from:** it is not downloaded. It is the local project the SBOM was generated for (`pkg:npm/dependency_project@1.0.0`).
- **Why it is there:** an SBOM needs a root to describe. Everything else in the file hangs from this component, so `ollama` and `whatwg-fetch` are listed as what it depends on, directly and indirectly.

**Output:** [Task 5 — CycloneDX SBOM](Outputs-Logs-Screenshots/task5_sbom.json)


## 6. GitHub Profile

**GitHub Profile:** https://github.com/murainah 


## Question 7 — GitHub SSH Authentication and Push

I registered my public key with GitHub and successfully authenticated using SSH over port 443.

I configured the repository's remote using SSH and successfully pushed `question7_push.txt` to GitHub.

**Repository:** https://github.com/murainah/tfsd-assignment

**Evidence:**
- [SSH public key registered on GitHub (settings/keys)](Outputs-Logs-Screenshots/task7_github_ssh_key.png)
- [Terminal: SSH authentication, remote check printing OK, and push to GitHub](Outputs-Logs-Screenshots/task7_ssh_push.png)
- [SSH authentication and push log](Outputs-Logs-Screenshots/task7_ssh_push.txt)

Note: the terminal screenshot was taken after the later Question 8 commit (`9f4db04`), so it shows that commit as `HEAD`. The Question 7 push itself is commit `323525d`, shown in the log above.


## Question 8 — GPG-Signed Commit

I generated an Ed25519 GPG key, registered its public key with GitHub, and configured Git to sign commits. I then created and pushed a GPG-signed commit, which GitHub marked as **Verified**.

**Verified commit:** https://github.com/murainah/tfsd-assignment/commit/9f4db043909b41a1b3ee632cdeb35c2a6361c482

**Evidence:**
- [Registered GPG key screenshot](Outputs-Logs-Screenshots/task8_github_gpg_key.png)
- [Verified commit screenshot](Outputs-Logs-Screenshots/task8_verified_commit.png)


## Question 9 — GitHub Pages

I created and published a personal website using GitHub Pages. I verified its accessibility using the required `curl` command, which returned HTTP status code `200`.

**Website:** https://murainah.github.io

**Evidence:** [GitHub Pages HTTP 200 screenshot](Outputs-Logs-Screenshots/task9_github_pages.png)


## Question 10 — GitHub Issues

### GitHub issues on projects I did not create

1. **pandas** — [ENH: DataFrame.merge raises bare KeyError without saying which DataFrame is missing the key column](https://github.com/pandas-dev/pandas/issues/71819)  
   `merge(on=...)` raises `KeyError: 'customer_id'` without saying whether the left or the right DataFrame is missing the column. I reproduced it on pandas 2.3.3, included a minimal example, the code location, a suggested error message, and explained how it differs from the related closed issue #65553.

2. **requests** — [Invalid `params` type (e.g. int) raises misleading "TypeError: Cannot mix str and non-str arguments"](https://github.com/psf/requests/issues/7642)  
   Passing `params=5` raises an error that comes from `urllib.parse` and never mentions `params`. I reproduced it on requests 2.31.0, included expected vs. actual output and system information, and explained how it differs from the related fixed issue #2844.