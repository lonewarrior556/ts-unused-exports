## [6.1.0] - 4 Mar 2020

### Added

- Add an option to allow maximum number of issues: --maxIssues

### Changed

- Fix to support destructuerd exports like 'export const { a, b }'
- Handle dynamic imports that use dereferencing

## [6.0.0] - 24 Jan 2020

### Added

- Add options to ignore imports from certain files: --ignoreFiles, --ignoreProductionFiles, --ignoreTestFiles

### Changed

- BREAKING CHANGE: renamed the option --ignorePaths to be --excludePathsFromReport

## [5.5.0] - 20 Jan 2020

### Added

- Add option --allowUnusedTypes to skip unused types or interfaces.

## [5.4.0] - 19 Jan 2020

### Added

- Support exports destructured from array (issue #31)

## [5.3.0] - 04 Jan 2020

### Added

- Handle exports from within a namespace. Disabled by default, unless option --searchNamespaces is given. Note: this can affect performance on large codebases.

## [5.2.0] - 23 Dec 2019

### Changed

- (Internal) Update dependency TypeScript to 3.7.3
- (Internal) Simplify some logic, using the new optional chaining operator (?.)
- (Internal) Increase code coverage and simplify code (baseUrl defaults to '.')

## [5.1.0] - 26 Nov 2019

### Added

- Detect dynamic imports, to avoid false reports of unused exports
- Handle the alias from 'export default as', to avoid false positives.

### Changed

- (Internal) Update dependencies (except for TypeScript)

## [5.0.0] - 22 Nov 2019

### Added

- Include `.d.ts` files when searching for unused exports. This can be disabled via the --excludeDeclarationFiles option.

## [4.0.0] - 07 Nov 2019

### Changed

- use eslint-style exit code (0 = no issues, 1 = unused exports found, 2 = exception occurred)
- (Internal) add code coverage via nyc
- (Internal) code coverage and linting are included in `npm test`
- (Internal) add more unit tests, increasing the code coverage
- Limit max exit code when --exitWithCount option is used (max is 127, a signed byte)
- (Internal) add badges including: code coverage, npm package version, license, dependency status.

## [3.0.3] - 30 Oct 2019

### Changed

- (Internal) Add eslint with default rules (via typescript-eslint)
- (Internal) Fix all the linting issues

## [3.0.2] - 28 Oct 2019

### Changed

- (Internal) Replaced jasmine tests with cucumber tests
- Fix handling of import from index files, like "." or "./index.ts"

## [3.0.1] - 28 Oct 2019

### Changed

- Fix bug introduced by --showLineNumber option, where analysis throws error on more complex projects.

## [3.0.0] - 27 Oct 2019

### Changed

- Updated TypeScript dependency to 3.6.4

## [2.2.0] - 27 Oct 2019

### Added

- If the option --showLineNumber is given, then output 1 line per unused export, with the location in the file (line number, column)

### Changed

- Fix the --ignorePaths option (it was incorrectly filtering the parsed files, instead of filtering the output)

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
