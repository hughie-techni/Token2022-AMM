# Instructions for Agent: Token-2022 AMM Integration Project

This document outlines the instructions for the agent to work on the Token-2022 AMM integration project, ensuring effective documentation, changelog maintenance, version control with Git, and visual system design logging.

## Documentation
- **Format**: Write all documentation in Markdown (`*.md`) for compatibility with GitHub and other platforms.
- **Structure**: Follow a clear structure with the following sections:
  - Overview
  - Installation
  - Usage
  - Examples
  - API Reference
  - Troubleshooting
  - Changelog
- **Code Examples**:
  - Include examples for Solana/Anchor (smart contracts) and TypeScript (UI/SDK) with inline comments explaining each step.
  - Example:
    ```rust
    // Initialize a Token-2022 with Transfer Hook
    pub fn initialize_token(ctx: Context<InitializeToken>) -> Result<()> {
        // Logic to set up token with Transfer Hook extension
        Ok(())
    }
    ```
- **Visual Aids**: Embed Mermaid diagrams in Markdown to illustrate system flows and architecture (e.g., token creation, AMM trading process).
- **Usability**:
  - Ensure documentation is beginner-friendly by defining technical terms (e.g., Transfer Hooks, AMM).
  - Design modular sections and templates for reusability (e.g., a template for creating a liquidity pool).

## Changelog
- **File**: Maintain a `CHANGELOG.md` file in the project root, following the [Keep a Changelog](https://keepachangelog.com/en/1.0.0/) format.
- **Format**:
  - Use Markdown with sections for each version (e.g., `## [1.0.0] - 2025-07-06`).
  - Categorize changes under: `Added`, `Changed`, `Deprecated`, `Removed`, `Fixed`, `Security`.
  - Include unreleased changes under `## [Unreleased]`.
  - Link changes to GitHub commits or pull requests for traceability.
- **Versioning**: Use [Semantic Versioning (SemVer)](https://semver.org/) with the format `MAJOR.MINOR.PATCH`:
  - `MAJOR`: Increment for incompatible changes (e.g., breaking API changes).
  - `MINOR`: Increment for backward-compatible features (e.g., new Transfer Hook support).
  - `PATCH`: Increment for backward-compatible bug fixes (e.g., fixing a UI bug).
  - Use `0.y.z` for pre-1.0 releases (e.g., `0.1.0` for initial development).
- **Updates**: Update `CHANGELOG.md` with every significant change, linking to the corresponding Git commit hash.

## Git Instructions
- **Commits**:
  - After each significant change (e.g., new feature, bug fix), stage and commit with a descriptive message:
    ```bash
    git add .
    git commit -m "Add feature X to Token-2022 AMM"
    ```
  - Ensure commit messages are clear and linked to changelog entries (e.g., `Fixes #123: UI bug`).
- **Changelog Updates**:
  - Update `CHANGELOG.md` before tagging a release:
    ```bash
    git add CHANGELOG.md
    git commit -m "Update CHANGELOG for feature X"
    ```
- **Releases**:
  - Tag releases with SemVer versioning:
    ```bash
    git tag v0.1.0
    git push origin v0.1.0
    ```

## Visual Design
- **Diagrams**:
  - Use Mermaid for inline diagrams in Markdown to represent system flows and architecture (e.g., sequence or flowchart for AMM interactions).
  - Example:
    ```mermaid
    sequenceDiagram
        participant User
        participant UI
        participant AMM
        User->>UI: Create Token-2022
        UI->>AMM: Initialize Pool
        AMM-->>UI: Pool Address
    ```
- **Storage**:
  - Store diagrams in a `diagrams/` folder in the repository.
  - Commit diagrams with descriptive messages:
    ```bash
    git add diagrams/architecture.mmd
    git commit -m "Add system architecture diagram"
    ```
- **Changelog Integration**:
  - Log diagram updates in `CHANGELOG.md` with commit references.
  - Example:
    ```markdown
    ### Added
    - System architecture diagram for Token-2022 AMM (`diagrams/architecture.mmd`).
      - Commit: `git commit -m "Add architecture diagram" -a && git push`
    ```