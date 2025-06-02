| Package | Version age | PAT.url | Adoption | Passing | Confidence |
|---|---|---|---|---|---|
| [transformers](https://redirect.github.com/huggingface/transformers) | `==4.52.3` -> `==4.52.4` | [![age](https://developer.mend.io/api/mc/badges/age/pypi/transformers/4.52.4?slim=true)](https://docs.renovatebot.com/merge-confidence/) | [![adoption](https://developer.mend.io/api/mc/badges/adoption/pypi/transformers/4.52.4?slim=true)](https://docs.renovatebot.com/merge-confidence/) | [![passing](https://developer.mend.io/api/mc/badges/compatibility/pypi/transformers/4.52.3/4.52.4?slim=true)](https://docs.renovatebot.com/merge-confidence/) | [![confidence](https://developer.mend.io/api/mc/badges/confidence/pypi/transformers/4.52.3/4.52.4?slim=true)](https://docs.renovatebot.com/merge-confidence/) |
[![Dependabot compatibility score](https://dependabot-badges.githubapp.com/badges/compatibility_score?dependency-name=actions/checkout&package-manager=github_actions&previous-version=2&new-version=4)](https://docs.github.com/en/github/managing-security-vulnerabilities/about-dependabot-security-updates#about-compatibility-scores)


# Hello there! If you want to have a school website where you can run a server, you have found just the place!
# STEPS:
  # 1. Fork this repository
  # 2. create a `deploy.yml` in a `.github/workflows/deploy.yml` path! Put the following code:


```YAML
     name: Deploy website

on:
  push:
    branches: ["main"]
  workflow_dispatch:
  
permissions:
  contents: read
  pages: write
  id-token: write

concurrency:
  group: "pages"
  cancel-in-progress: false

defaults:
  run:
    shell: bash

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - name: Checkout
        uses: actions/checkout@v4
      - name: Upload artifact
        uses: actions/upload-artifact@v4
        with:
          path:
            data
      - name: Setup Node
        uses: actions/setup-node@v4
        with:
          node-version: "20"
      - name: Setup Pages
        id: pages
        uses: actions/configure-pages@v5
        with:
          # Automatically inject pathPrefix in your Gatsby configuration file.
          #
          # You may remove this line if you want to manage the configuration yourself.
          static_site_generator: gatsby
      - name: Install dependencies
        run: ${{ steps.detect-package-manager.outputs.manager }} ${{ steps.detect-package-manager.outputs.command }}
      - name: Checkout
        uses: actions/checkout@v4
      - name: Setup Pages
        uses: actions/configure-pages@v5
      - name: Build with Jekyll
        uses: actions/jekyll-build-pages@v1
        with:
          source: ./
          destination: ./_site
      - name: Upload artifact
        uses: actions/upload-pages-artifact@v3
      - name: Deploy to GitHub Pages
        id: deployment
        uses: actions/deploy-pages@v4
```

  # 3. Then, wait for it to deploy. And test out the website! You can tweak the `index.html` file if you want.
  # 4. Open up the `Server` branch and make a codespaces on that branch.
  # 5. See the `README.md` [preview] in the codespaces (OR) go to [This file](https://github.com/Gamer-friend/googlecom/blob/server/text/instructions.md)
# hello school staff, feel free to block this
