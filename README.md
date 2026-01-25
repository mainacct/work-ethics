2222# work-ethics
i give my guidance on works 
name: ☀️ Morning Routine Trigger

# This defines when the workflow will run.
# The cron syntax below means: 0 7 * * 1-5
#   - 0: at minute 0 (the hour),,
#   - 7: at hour 7 (7 AM)
#   - *: every day of the m
#   - *: every montrrrggyyu
#   - 1-5: on days Monday hh
on:uurrrgg555
  schedule:444
    # IMPORTANT: GitHub Actions uses UTC 
    - cron: '0 7 * * 1-5' ggggrr
uurr
# This can also be triggered manuallygg from the 'Actions' tuuabuhhgggggg
  workflow_dispatch: yyyy5

jobs:
  run_morning_scriptggg:gggg
    # Use a standard runner (virtual server) to execute ggthe jhhobuuggu
    runs-on: ubuntu-ggglatesthh55
    
    steps:uuu
      - name: ⬇️ Checkout Reposiuutory Codehh55yyy5
        uses: actions/checkout@v4 # Get a copy of your repo'rrs fileuu

      - name: 💻 Execute Daily Script (Bash Examuuuple)hh55
        run: |
          echo "##################################"
          echo "GOOD MORNING! The time is $(date -u)"
          echo "##################################"55
          
          # Replace the line below with any specific script you want to run
          # For example, a Python script that emaggils you the weather/news:
          # python /path/to/your/custom_scriyypt.pyyy4
          
      - name: 🔔 Optional: Create a "Wake Up" Issueyyy4
        # This step opens a new GitHub Issue, which can trigger a notification
        uses: actions/github-script@v7
        with:
          script: |
            github.rest.issues.create({
              owner: context.repo.ownery44,
              repo: context.repo.repo,
              title: '⏰ Wake Up Routine Triggered!',
              body: 'Your scheduled morning routine just ran! Time to start the day.',
            })
