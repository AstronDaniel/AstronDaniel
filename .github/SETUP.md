# Setting Up WakaTime for GitHub Profile

## ✅ Step 1: Make Your WakaTime Profile Public
1. Go to [WakaTime Settings](https://wakatime.com/settings/profile)
2. Find the "Public Profile" option
3. Toggle it ON
4. Save your changes
5. Verify your profile is public by checking: `https://wakatime.com/@YourWakaTimeUsername`

## ✅ Step 2: Ensure GitHub Action Workflow is Properly Configured

### Check Your Workflow File
The WakaTime workflow file should have these settings:
- Correct WAKATIME_API_KEY reference: `${{ secrets.WAKATIME_API_KEY }}`
- Correct GH_TOKEN reference: `${{ secrets.GH_TOKEN }}`
- Your GitHub username is correctly specified
- The "USERNAME" parameter is set to your GitHub username

### Check GitHub Secrets
1. Go to your repository Settings → Secrets and Variables → Actions
2. Verify these secrets exist:
   - `WAKATIME_API_KEY`
   - `GH_TOKEN`

### Check GitHub Action Permissions
1. Go to repository → Settings → Actions → General
2. Under "Workflow permissions", ensure "Read and write permissions" is selected

## ✅ Step 3: Run the Workflow Manually for Testing
1. Go to repository → Actions → WakaTime Stats workflow
2. Click "Run workflow"
3. Check the workflow logs for any errors 

## ✅ Step 4: Check Your README.md
Ensure the README.md file has the special WakaTime comment tags:
