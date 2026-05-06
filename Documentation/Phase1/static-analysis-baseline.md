# Static Analysis Baseline

Prepared on: 2026-05-06  
Project: UniTime 4.9  
Backend source root: `JavaSource`

## Tool Status

The assignment recommends a static code analysis tool such as SonarQube. The repository now includes `sonar-project.properties` so the project can be scanned with SonarScanner.

At preparation time, the following tools were not available on the local PATH:

- `mvn`
- `ant`
- `sonar-scanner`
- `pmd`
- `checkstyle`
- `spotbugs`

Because the scanner was unavailable locally, this document records a lightweight baseline scan using local PowerShell pattern checks. For final submission, run SonarQube/SonarScanner and attach the generated dashboard/report evidence.

## Baseline Size Metrics

| Metric | Value |
| --- | ---: |
| Java files under `JavaSource` | 2,480 |
| Java source lines under `JavaSource` | 718,358 |

## Lightweight Static Findings

These are not a replacement for SonarQube. They are early indicators to help choose maintenance work and risk areas.

| Check | Result | Risk |
| --- | ---: | --- |
| `TODO` / `FIXME` comments | 152 matches | Deferred maintenance or incomplete work may exist. |
| `System.out.print*` or `printStackTrace()` | 284 matches | Console/debug output may bypass logging and reduce production diagnosability. |
| Empty one-line `catch (...) {}` blocks | 499 matches | Exceptions may be swallowed without recovery or logging. |
| `@SuppressWarnings` or `// NOSONAR` | 480 matches | Some issues may be intentionally suppressed and need careful review before changing. |

## Recommended SonarQube Steps

1. Start a local SonarQube server.
2. Create a project named `unitime-maintenance`.
3. Generate a project token.
4. Run SonarScanner from the repository root:

```powershell
sonar-scanner `
  -Dsonar.projectKey=unitime-maintenance `
  -Dsonar.host.url=http://localhost:9000 `
  -Dsonar.token=<your-token>
```

5. Export screenshots or a PDF report showing at least:
   - Bugs
   - Vulnerabilities
   - Code smells
   - Duplications
   - Security hotspots
   - Maintainability rating

## Static Analysis Conclusion

The codebase is large and mature, so Phase 2 changes should avoid broad refactoring. The safest maintenance strategy is to select narrowly scoped backend changes with clear validation points, such as improving validation messages or adding audit behavior around a single workflow.
