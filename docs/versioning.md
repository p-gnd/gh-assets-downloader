# Version numbering

Versioning is the process of adding unique identifiers to different versions of your package. The unique identifier you use may be name-based or number-based, but most Python packages use [semantic versioning](https://semver.org/). In semantic versioning, a version number consists of three integers A.B.C, where A is the “major” version, B is the “minor” version, and C is the “patch” version. The first version of a software usually starts at 0.1.0 and increments from there. We call an increment a “bump”, and it consists of adding 1 to either the major, minor, or patch identifier as follows:

- Patch release (0.1.0 -> 0.1.1): patch releases are typically used for bug fixes, which are backward compatible. Backward compatibility refers to the compatibility of your package with previous versions of itself. For example, if a user was using v0.1.0 of your package, they should be able to upgrade to v0.1.1 and have any code they previously wrote still work. It’s fine to have so many patch releases that you need to use two digits (e.g., 0.1.27).

- Minor release (0.1.0 -> 0.2.0): a minor release typically includes larger bug fixes or new features that are backward compatible, for example, the addition of a new function. It’s fine to have so many minor releases that you need to use two digits (e.g., 0.13.0).

- Major release (0.1.0 -> 1.0.0): release 1.0.0 is typically used for the first stable release of your package. After that, major releases are made for changes that are not backward compatible and may affect many users. Changes that are not backward compatible are called “breaking changes”. For example, changing the name of one of the modules in your package would be a breaking change; if users upgraded to your new package, any code they’d written using the old module name would no longer work, and they would have to change it.

# Version bumping
[Python Semantic Release (PSR)](https://python-semantic-release.readthedocs.io/en/latest/) is a tool that can automatically bump version numbers based on keywords it finds in commit messages. Relying on the standardization of the commit message format and syntax, PSR can parse to determine how to increment the version number. The default commit message format used by PSR is the Angular commit style, which looks like this:
```json
<type>(optional scope): short summary in present tense

(optional body: explains motivation for the change)

(optional footer: note BREAKING CHANGES here, and issues to be closed)
```
where
<type> refers to the kind of change made and is usually one of:
`feat`: A new feature.
`fix`: A bug fix.
`docs`: Documentation changes.
`style`: Changes that do not affect the meaning of the code (white-space, formatting, missing semi-colons, etc).
`refactor`: A code change that neither fixes a bug nor adds a feature.
`perf`: A code change that improves performance.
`test`: Changes to the test framework.
`build`: Changes to the build process or tools.