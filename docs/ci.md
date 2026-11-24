# CI gates

Every pull request runs these on Node 24 and 26. All must pass.

- `pnpm lint`: oxlint, warnings fail.
- `pnpm format:check`: Prettier (`pnpm format` fixes it).
- `pnpm build`: type-checks with `tsc`.
- `pnpm test`: Node's test runner with coverage. It fails below 75% line coverage. The coverage table goes in the job summary.

Design: [#7](https://github.com/loginllama/clerk-loginllama/issues/7).
