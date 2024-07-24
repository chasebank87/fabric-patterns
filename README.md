# fabric-patterns
A custom pattern repository for fabric (Unofficial Fabric Integration plugin for Obsidian) 


# Submittion Instructions

1. Fork the repository
2. Create your own repo to store your patterns (this is the repo you need to enter for pattern_repo)
   - You must put the patterns in a folder called patterns and named patternname.md
   - repo/patterns/pattern.md
3. Update the patterns.json file with your pattern(s) in the forked repo
4. Create a pull request
5. Wait for the changes to be merged
6. Changes to your patterns will not require additional pull requests



## JSON Format

```json
{ "patterns": {
    "pattern_name": {
      "pattern": "name of the pattern (use _ if a divider is needed)",
      "description": "A quick description of the pattern (less than one sentence)",
      "author": "Your name or github username",
      "for_models": "The models this pattern works best with",
      "pattern_repo": "repo where the pattern is stored (chasebank87/fabric-patterns)"
    }
  }
}
```