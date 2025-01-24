# ✨ Build Kivy App to APK using Buildozer ✨

Effortlessly build your Kivy app into an APK with this GitHub Action! 🚀

## Key features:
 * Simple setup: Use the provided code snippet in your workflow.
 * Automates builds: Triggered on every push to the main branch.
 * Customizable: Adjust the buildozer-cmd, python-version and work-dir parameters if needed.

## How to use:
 * Copy the code below into your .github/workflows/ directory.
 * Modify the buildozer-cmd, python-version and work-dir if necessary.
 * Commit and push to your main branch to trigger the build.

### How to use  
```yml
on:
  push:
    branches: [ main ]

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - name: Build APK
        uses: digreatbrian/buildozer-action@v2
        with:
          python-version: 3.8
          buildozer-cmd: buildozer -v android debug

      - name: Upload artifacts
        uses: actions/upload-artifact@v4
        with:
          name: package
          path: ./bin/*.apk
```
[![Ko-fi](./support_me_on_kofi_badge_red.png)](https://ko-fi.com/digreatbrian)  

## Contributions welcome!
Feel free to submit issues, suggestions, or pull requests to improve this action. Let's make it even better together! 🤗  

Happy coding! 😄
