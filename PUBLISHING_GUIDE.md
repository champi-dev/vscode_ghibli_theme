# Publishing Guide for Studio Ghibli Theme

## Prerequisites

1. **Install vsce** (Visual Studio Code Extension Manager):
   ```bash
   npm install -g vsce
   ```

2. **Create a Publisher Account**:
   - Go to https://marketplace.visualstudio.com/manage
   - Sign in with your Microsoft account
   - Create a new publisher ID (e.g., "ghibli-themes")

3. **Generate Personal Access Token**:
   - Visit https://dev.azure.com/
   - Click on your profile → Personal access tokens
   - Create new token with:
     - Organization: All accessible organizations
     - Scopes: Marketplace (Publish)
   - Save the token securely

## Packaging the Extension

1. **Navigate to the theme directory**:
   ```bash
   cd ghibli-theme
   ```

2. **Install dependencies** (if any):
   ```bash
   npm install
   ```

3. **Package the extension**:
   ```bash
   vsce package
   ```
   This creates a `.vsix` file (e.g., `ghibli-theme-1.0.0.vsix`)

## Publishing to VS Code Marketplace

1. **Login to vsce**:
   ```bash
   vsce login [your-publisher-id]
   ```
   Enter your Personal Access Token when prompted

2. **Publish the extension**:
   ```bash
   vsce publish
   ```

   Or publish a specific version:
   ```bash
   vsce publish 1.0.0
   ```

   Or publish from a packaged .vsix file:
   ```bash
   vsce publish -p ghibli-theme-1.0.0.vsix
   ```

## Publishing Checklist

Before publishing, ensure:

- [ ] All colors have been tested for readability
- [ ] README.md is complete and accurate
- [ ] CHANGELOG.md is up to date
- [ ] package.json has correct information:
  - [ ] Publisher ID matches your marketplace account
  - [ ] Repository URL is correct
  - [ ] Version number is appropriate
  - [ ] Description is clear and concise
- [ ] Icon.png exists (128x128px PNG)
- [ ] Theme works in latest VS Code version
- [ ] No console errors when theme is active
- [ ] Screenshots are ready (optional but recommended)

## Post-Publishing

1. **Verify on Marketplace**:
   - Visit https://marketplace.visualstudio.com/
   - Search for your theme
   - Check that all information displays correctly

2. **Create GitHub Release**:
   - Tag the repository with the version number
   - Upload the .vsix file to the release
   - Add release notes from CHANGELOG.md

3. **Monitor Feedback**:
   - Check reviews and ratings
   - Respond to issues on GitHub
   - Plan updates based on user feedback

## Updating the Theme

1. **Update version** in package.json
2. **Update CHANGELOG.md** with changes
3. **Test all changes thoroughly**
4. **Package and publish**:
   ```bash
   vsce publish patch  # for 1.0.0 → 1.0.1
   vsce publish minor  # for 1.0.0 → 1.1.0
   vsce publish major  # for 1.0.0 → 2.0.0
   ```

## Common Issues

### "Error: Missing publisher name"
Update package.json with your publisher ID:
```json
"publisher": "your-publisher-id"
```

### "Error: Make sure to edit the README.md file before you package or publish"
Remove the default VS Code extension README content and ensure your README is customized.

### "Personal Access Token verification failed"
- Ensure the token has Marketplace (Publish) scope
- Check token hasn't expired
- Verify you're using the correct organization

## Resources

- [VS Code Publishing Extensions](https://code.visualstudio.com/api/working-with-extensions/publishing-extension)
- [Extension Manifest](https://code.visualstudio.com/api/references/extension-manifest)
- [Theme Color Reference](https://code.visualstudio.com/api/references/theme-color)