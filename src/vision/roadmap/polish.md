# Polish

## Impact

* Users can predict and understand why the compiler raises error messages. Errors are aligned with an experienced user's intuition about how Rust works.
* Error messages identify common misconceptions, suggest solutions, and are generally on par with sync Rust.
  * Errors not only show that there is a problem, they help the user to fix it and to learn more about Rust (possibly directing the user to other documentation).
  * The compiler may suggest crates from the ecosystem to help solve problems when appropriate.
* Lints guide the user away from common errors and help them both to get started with async Rust and to maintain async Rust programs over time.
* Rust's async implementation is high quality and reflects an attention to detail.
  * No internal compiler errors
  * Compiler analysis and code generation passes are precise and not unnecessarily conservative.
  * Integration with low-level tooling and the like is high-quality.
  * The generated code from the compiler is high quality and performant.

## Milestones

| Milestone                                  | State | Key participants |
| ---                                        | ---   | ---              |
| Precise generator captures                 | 🦀    | [eholk]          |
| ↳ Prototyped                               | 🦀    | [eholk]          |
| ↳ Documented in Rust Reference             | 🦀    | [eholk]          |
| ↳ [Lang team] initiative proposal          | 💤    | [eholk]          |
| ↳ [Lang team] signoff                      | 💤    | [Lang team]      |
| ↳ Stabilized                               | 💤    | [eholk]          |
| Lint: [Large copies], large generators     | 💤    | |
| ↳ [Lang team] initiative proposal          | 💤    | |
| ↳ Implementated                            | 💤    | |
| Lint: [Must not suspend]                   | 💤    | |
| ↳ Implemented the [RFC]                    | 💤    | |
| Lint: [Blocking in async context]          | 💤    | |
| ↳ RFC proposed and accepted                | 💤    | |
| ↳ Implementated                            | 💤    | |


[eholk]: https://github.com/eholk/
[Lang team]: https://www.rust-lang.org/governance/teams/lang
[Blocking in async context]: ./polish/lint_blocking_fns.md
[Large copies]: ./polish/lint_large_copies.md
[Must not suspend]: ./polish/lint_must_not_suspend.md
[RFC]: https://rust-lang.github.io/rfcs/3014-must-not-suspend-lint.html