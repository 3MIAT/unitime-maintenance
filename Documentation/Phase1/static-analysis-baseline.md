
## Recommended SonarQube Steps

1. Start a local SonarQube server.
2. Create a project named `unitime-maintenance`.
3. Generate a project token.
4. Run SonarScanner from the repository root:


5. Export screenshots or a PDF report showing at least:
   - Bugs
   - Vulnerabilities
   - Code smells
   - Duplications
   - Security hotspots
   - Maintainability rating

## Static Analysis Conclusion

The codebase is large and mature, so Phase 2 changes should avoid broad refactoring. The safest maintenance strategy is to select narrowly scoped backend changes with clear validation points, such as improving validation messages or adding audit behavior around a single workflow.
