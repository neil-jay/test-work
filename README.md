Steps to enable semantic release:

1. Install semantic-release globally
```
npm install -g semantic-release
```

2. Install semantic-release as a dev dependency
```
npm install --save-dev semantic-release @semantic-release/git @semantic-release/changelog
```

3. Create a .releaserc.json file in the root of your project and configure:
```
{
    "branches": ["main"], // Specify your branch(es) for release
    "plugins": [
      "@semantic-release/commit-analyzer", // Analyzes commits to determine the type of release
      "@semantic-release/release-notes-generator", // Generates release notes for each release
      "@semantic-release/changelog", // Updates the CHANGELOG.md file with release notes
      "@semantic-release/github" // Creates a GitHub release
    ]
  }
```

4. Commit and push your changes to the specified branch(es)

5. Run semantic-release
```
npx semantic-release
```

6. Semantic-release will automatically analyze your commit messages, generate release notes, and create a new release on GitHub.
```