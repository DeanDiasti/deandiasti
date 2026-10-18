# GitHub profile review

Reviewed October 18, 2026. Scope: this profile repository, the public Clodex,
fusion-cli, and homebrew-tap repositories, and the supplied resume. This is a
portfolio and skills review of selected source files and documentation, not an
exhaustive code audit or an independent check of resume outcomes.

## Positioning

Lead with **AI infrastructure and developer tools**. The old “new grad backend
developer” description understates the production work in the resume and misses
the Rust and CAD tooling visible in the public repositories. Applied ML is an
important supporting strength, with more evidence in the resume than on the
public profile today.

The refresh puts two substantial original projects first, replaces the logo
wall with readable skill groups, and adds contact links. Professional experience
is separate from public code so readers can tell what they can inspect directly.

## Skills supported by the review

| Strength | Evidence | How to present it |
| :--- | :--- | :--- |
| Rust systems and CLI engineering | Clodex's [manifest](https://github.com/DeanDiasti/clodex/blob/main/Cargo.toml), [supervisor](https://github.com/DeanDiasti/clodex/blob/main/src/supervisor.rs), and [routing](https://github.com/DeanDiasti/clodex/blob/main/src/mapping.rs) | Rust, Tokio/Axum, local networking, process supervision, typed routing. The reviewed supervisor includes bounded startup, Unix sockets, session leases, and credential synchronization. |
| Python integration and API design | fusion-cli's [catalog loader](https://github.com/DeanDiasti/fusion-cli/blob/main/cli/command_catalog.py) and [CAD dispatcher](https://github.com/DeanDiasti/fusion-cli/blob/main/fusion_addin/CadBot/bridge/dispatch.py) | Shared command definitions, authenticated local services, main-thread dispatch, and cancellation versus in-flight work. |
| Recovery and validation | fusion-cli's [checkpoint tests](https://github.com/DeanDiasti/fusion-cli/blob/main/tests/test_checkpoint_undo.py) and [validation documentation](https://github.com/DeanDiasti/fusion-cli/blob/main/docs/validation.md) | Recovery boundaries, host tests, and separately recorded native CAD evidence. Do not describe sampled interference as continuous collision detection. |
| Distribution and maintenance | Clodex's [CI](https://github.com/DeanDiasti/clodex/blob/main/.github/workflows/ci.yml) and the [Homebrew formula](https://github.com/DeanDiasti/homebrew-tap/blob/main/Formula/fusion-cli.rb) | Formatting/lint/test gates, macOS/Linux CI, checksummed releases, installation tests, and credential-preserving reinstall behavior. These are inspected configurations, not test results from this review. |
| AI governance and backend infrastructure | Resume: Alterion and Seqoria | eBPF identity resolution, OAuth 2.0, Keycloak, RBAC, OpenTelemetry, FastAPI, Docker, ECS/Fargate. Present these as professional experience, not features of the public repos. |
| Applied ML and GPU programming | Resume: Frags AI, research, ViT, drone detection, multimodal learning, and CUDA projects | PyTorch, TensorFlow, scikit-learn, computer vision, distributed training, and C++/CUDA. A reproducible public project would make this strength easier to evaluate. |

The public Warp repository is a fork. Its existence alone does not establish
authorship of Warp or a specific upstream contribution. Feature Clodex and
fusion-cli first.

## Profile settings to apply

These are ready-to-use recommendations. The README change does not alter account
settings, repository descriptions, topics, or pins.

**Bio**

> Software engineer building AI infrastructure and developer tools. Rust, Python, agent systems, and CAD automation.

**Social link**: https://www.linkedin.com/in/deandiasti/

**Pin order**

1. **clodex**: strongest public systems and AI tooling example.
2. **fusion-cli**: distinct Python/CAD integration with documentation and validation.
3. Add a reproducible ML or agent-runtime project when one is public. The
   Homebrew tap is useful distribution evidence, but belongs with fusion-cli
   rather than filling an otherwise empty featured slot.

**Suggested repository descriptions**

- **clodex**: “Local Rust launcher connecting Claude Code to Codex and Claude models, with streaming translation and shared backend supervision.”
- **fusion-cli**: “Typed Python CLI for Autodesk Fusion with CAD modeling, motion previews, and verified session checkpoints.”
- **homebrew-tap**: “Homebrew distribution for fusion-cli, with checksummed releases and macOS installation tests.”

**Suggested topics**

- **clodex**: `rust`, `cli`, `developer-tools`, `ai`, `llm`, `local-proxy`
- **fusion-cli**: `python`, `cad`, `autodesk-fusion`, `cli`, `parametric-design`
- **homebrew-tap**: `homebrew`, `homebrew-tap`, `macos`, `packaging`

## Next improvements with the most value

- Add a short recorded terminal walkthrough to Clodex and a real CAD motion
  preview to fusion-cli. Show the actual output and one useful task per demo.
- Publish a small, reproducible ML project with dataset instructions, an
  evaluation script, and hardware/training details. Choose shareable source and data.
- For resume metrics such as speedups or accuracy, add a linked methodology and
  baseline before using them as public headline claims. The profile emphasizes
  the work itself rather than repeating unverified numbers.
- Reconcile the resume's “Expected December 2024” education dates and overlapping
  “Present” roles before linking a public resume from GitHub. The supplied
  document was used as context; its full text, phone number, and address were
  not copied into this repository.

## Design direction

Audience: engineers, potential collaborators, and hiring teams. The profile's job
is to establish Dean's focus quickly, then lead readers to inspectable work.

**Palette:** Cloud `#F3F6FC`, Ink `#182B4A`, Cobalt `#3456D9`, Teal `#176E73`,
and Blueprint `#DCE6F7`. The dark banner uses lighter blue and teal strokes on Ink.

**Type:** Trebuchet MS with Avenir Next and Arial fallbacks for the banner's
humanist lettering; GitHub's native typography for editable body content.
No font downloads are needed.

**Layout:** left-aligned, single reading column. One custom banner, a short
introduction, contacts, two project sections, professional context, and a toolkit.

```text
+--------------------------------------------------+
| Dean Diasti                 signals > interface  |
| AI infrastructure.                      > solid  |
| Developer tools.                                 |
+--------------------------------------------------+
| Introduction + contact links                     |
| Clodex: purpose / engineering / source            |
| fusion-cli: purpose / engineering / demo          |
| Professional experience                          |
| Toolkit                                          |
+--------------------------------------------------+
```

**Plan critique:** a terminal window or contribution-stat card would fit almost
any developer profile. The revised focal illustration connects signal paths to
a CAD-like solid, reflecting the specific combination of model integrations and
physical-design tooling in Dean's work. The rest stays native to GitHub: no
animated widgets, external badge services, or image-based project descriptions.
Light/dark SVGs are local assets, with separate mobile compositions and a text
alternative on the README image. Links and project details stay selectable and
keyboard accessible through GitHub's standard rendering.

## Validation of this refresh

- Rendered a local Markdown preview with GitHub-like styling at 1000, 375, and
  320 pixels in light and dark mode. All six views loaded the expected banner
  variant without document-level horizontal overflow. This preview approximates
  GitHub styling; it is not a screenshot of the live profile.
- Visually inspected desktop light/dark and 320-pixel mobile screenshots.
- Parsed all four SVGs, checked image references, and confirmed the assets do
  not contain scripts or external dependencies.
- Confirmed the linked fusion-cli website returns HTTP 200.
- Checked the patch with `git diff --check`.
