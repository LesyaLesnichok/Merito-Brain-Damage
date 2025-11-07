# Contributing to Merito Brain Damage

This document provides the guidelines for contributing to our game. Please take a moment to review it to ensure a smooth and effective workflow for everyone.

## 🚀 The Golden Rule

**DO NOT PUSH TO THE `main` BRANCH.**

All work must be done on a separate branch and submitted as a **Pull Request (PR)** to be reviewed and merged.

## 🛠️ Project Setup

Before you can work on the project, please ensure you have the following tools installed and set up correctly.

1.  **Unreal Engine:**
    * **Version:** **5.6.1**
    * **Source:** Epic Games Launcher
2.  **IDE:**
    * **Visual Studio 2022**
    * **Workload:** You must have the "Game development with C++" workload installed.
3.  **Git LFS:**
    * You **must** have Git LFS installed and configured *before* cloning.
    * Please follow the complete setup instructions in our `README.md` file.

## 🌿 Our Workflow

We use a simple "Branch & Pull Request" model.

1.  **Find a Task:** Pick an task from the GitHub **Issues** tab. If you're starting something new, create an Issue first so we can discuss it.
2.  **Create a Branch:** Create your new branch from the `main` branch.
    * **Naming Convention:** Please use the format `type/short-description`.
    * **Examples:**
        * `feat/player-dash-mechanic`
        * `fix/crash-on-level-load`
        * `asset/sci-fi-crate-model`
        * `refactor/optimize-movement-code`
3.  **Do Your Work:**
    * Write your code, build your assets, and test your changes.
    * Commit your changes locally with clear commit messages (see below).
4.  **Push Your Branch:**
    * `git push -u origin feat/your-branch-name`
5.  **Open a Pull Request:**
    * Go to the repository on GitHub.
    * Click the "New Pull Request" button.
    * **Link the Issue:** In your PR description, write "Closes #123" (replacing `123` with the issue number) to link it.
6.  **Review & Merge:**
    * Your PR must be approved by at least one other person before it can be merged into `main`.
    * Once approved, the person who reviewed the PR is responsible for clicking the "Merge" button.

---

## 📜 Coding Style (C++)

To keep the codebase clean and consistent, we follow the official **[Epic Games C++ Style Guide](https://dev.epicgames.com/documentation/en-us/unreal-engine/unreal-engine-5-6-documentation?application_version=5.6)**.

If you're new to it, here are the **most important** rules:

* **Classes & Structs:** `PascalCase` (e.g., `AMyPlayerCharacter`, `FPlayerData`).
* **Functions & Variables:** `PascalCase` (e.g., `MyFunction`, `MyVariable`).
    * *Note: This is the official UE style. It's different from `camelCase` but is the standard for Unreal.*
* **Pointers:** Place the asterisk next to the type, not the name (e.g., `AActor* MyActor`).
* **`UPROPERTY()` & `UFUNCTION()`:** All member variables and functions that need to be exposed to Blueprints or the engine **must** have the correct `UPROPERTY()` or `UFUNCTION()` macro with appropriate specifiers (e.g., `EditAnywhere`, `BlueprintReadOnly`, `BlueprintCallable`).

## 💬 Commit Message Style

Please follow this simple format for all commit messages. It makes our history much easier to read.

**Format:** `Type: Short description of change`

* **`Feat:`** (A new feature, like adding a new weapon)
* **`Fix:`** (A bug fix, like stopping a crash)
* **`Refactor:`** (Cleaning up code without changing functionality)
* **`Docs:`** (Adding or updating documentation)
* **`Asset:`** (Adding or updating a `.uasset`, `.fbx`, `.png`, etc.)
* **`WIP:`** (Work in Progress - for temporary commits on your branch)

**Examples:**
* `Feat: Implemented basic player dash ability`
* `Fix: Player no longer falls through floor on spawn`
* `Asset: Added T_Rock_N texture and M_Rock material`
* `Refactor: Moved health logic from Character to new HealthComponent`

## 🐞 Reporting Bugs & Issues

* **Use GitHub Issues!**
* **Be clear:** Provide a short, descriptive title.
* **Give details:**
    * What did you do? (Steps to reproduce)
    * What did you expect to happen?
    * What actually happened? (Include error messages, screenshots, etc.)
* **Use Labels:** Add the correct labels (e.g., `bug`, `code: c++`, `priority: high`) so we know what's going on at a glance.
