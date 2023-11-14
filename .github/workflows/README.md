## WinGet Publish Workflow

- Pull Request: <https://github.com/microsoft/winget-pkgs/pull/126347> for the WinGet repository

- Workflow Source: <https://github.com/The-Running-Dev/Winget-Updates/blob/main/.github/workflows/sidequest.easyinstaller.internal.yml>

- Workflow Results: <https://github.com/The-Running-Dev/Winget-Updates/actions/runs/6864444163/job/18666214326>

What this workflow does:

1. Runs every time there is a new release pushed
2. Gets the published version from WinGet
3. Gets the latest published version from the current repository
4. If the latest version is different than the WinGet version, submits an update to the WinGet repository

## HowTo Setup

1. Generate a new personal access token at <https://github.com/settings/personal-access-tokens/new>, and give it 'Public Repositories' access, and copy it.
2. Create a new repository secret at <https://github.com/SideQuestVR/EasyInstallerReleases/settings/secrets/actions>, with the name ```PublicAccessToken```
3. The workflow will run when a new release is published