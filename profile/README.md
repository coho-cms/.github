# Welcome to Coho

**Managed content infrastructure, branch-native.**

Coho is a headless CMS that versions your content and your content model together. You
change both on a branch, review the diff, merge it, cut a release, and promote that release
through environments such as `dev`, `qa` and `prod`, with a rollback at every step.

A new field and the forty pages that need it travel together: one branch, one review and
one release, instead of a migration script and a hopeful deploy.

## Start here

The quickest way in is **[coho-samples](https://github.com/coho-cms/coho-samples)**. Begin
with **[Setting up a Next.js blog with the CLI](https://github.com/coho-cms/coho-samples/blob/HEAD/node/cli-next-blog/README.md)**,
which takes you from nothing to a working site in three short steps:

1. **[Set up the content model](https://github.com/coho-cms/coho-samples/blob/HEAD/node/cli-next-blog/01_CONTENT.md)**:
   content types, a few entries, localized text, and references between entries.
2. **[Create the client library](https://github.com/coho-cms/coho-samples/blob/HEAD/node/cli-next-blog/02_CLIENT_LIBRARY.md)**:
   a TypeScript package with a typed API, generated from those content types.
3. **[Build the Next.js blog](https://github.com/coho-cms/coho-samples/blob/HEAD/node/cli-next-blog/03_APPLICATION.md)**:
   pages that read your content through that library.

All you need first is the `coho` command line:

```bash
uv tool install coho-cli      # or: pipx install coho-cli
coho login
```

## What you'll find here

| Repository | What it is |
|---|---|
| [coho-samples](https://github.com/coho-cms/coho-samples) | **Start here.** Tutorials and getting-started projects, by language |
| [coho-cli](https://github.com/coho-cms/coho-cli) | The `coho` command line: sign in, create projects, and manage content types, entries, branches and releases |
| [coho-delivery-sdk-typescript](https://github.com/coho-cms/coho-delivery-sdk-typescript) | Read content from TypeScript and JavaScript, with a code generator and `npm create coho` |
| [coho-template-typescript](https://github.com/coho-cms/coho-template-typescript) | The starting point for a typed TypeScript content library |
| [coho-delivery-sdk-dotnet](https://github.com/coho-cms/coho-delivery-sdk-dotnet) | Read content from .NET *(in testing: alpha packages on NuGet)* |
| [coho-template-dotnet](https://github.com/coho-cms/coho-template-dotnet) | The starting point for a typed .NET content library *(in testing)* |
| [coho-management-sdk-python](https://github.com/coho-cms/coho-management-sdk-python) | Manage Coho from Python: projects, branches, content, releases and delivery keys. The library under the CLI |
| [coho-sdk-spec](https://github.com/coho-cms/coho-sdk-spec) | The shared specification and test material every Coho SDK is built against |

## The ideas in a minute

- **Branches are cheap, so use them.** A branch costs the same in a project of ten entries
  as in one of ten thousand. Make one for every change worth reviewing.
- **Your content model is code.** Content types are JSON you keep in your repository and
  review like any other change. A client library generated from them catches a removed
  field at build time, not in production.
- **Releases are immutable; environments point at them.** Promoting to `prod` moves a
  pointer, and rolling back moves it back.
- **Preview and production read the same way.** The same code reads a branch while you work
  and a release in production, with a different credential.

## Get involved

Found a step that didn't work, or want a sample for your framework? Open an issue on
[coho-samples](https://github.com/coho-cms/coho-samples/issues). Samples for .NET and
Python are on the way 🔜, and requests help decide what comes next.

Bugs in a tool belong in that tool's repository, and its README says how to build and
test it.

Everything here is Apache-2.0 licensed.
