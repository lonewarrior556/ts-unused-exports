## [Unreleased] - ReleaseDate
### Added
- If the option --showLineNumber is given, then output 1 line per unused export, with the location in the file (line number, column)

### Changed
- Fix the --ignorePaths option (it was incorrectly filtering the parsed files, instead of filtering the output)
- Updated TypeScript dependency to 3.6.4

## [2.1.0] - 20 Oct 2019
### Added
- Add comment flag to ignore some exports
- Add tsconfig paths aliases support
- Remove recursive imports check (performance on big projects)
- Use tsconfig 'paths' to resolve import paths
- Print full paths in console, with color highlighting
- Add cmd line option to ignore results from some file paths

### Changed
- By default, the process exit code will be 0 unless there was a critical error (bad arguments or a missing file)
- If the option --exitWithCount is given, then return the count of files that have unused exports