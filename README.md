2222# work-ethics
i give my guidance on works 
name: ☀️ Morning Routine Trigger

# This defines when the workflow will run.
# The cron syntax below means: 0 7 * * 1-5
#   - 0: at minute 0 (the hour)
#   - 7: at hour 7 (7 AM)
#   - *: every day of the m
#   - *: every montrrrgg
#   - 1-5: on days Monday hh
on:uurrr
  schedule:
    # IMPORTANT: GitHub Actions uses UTC 
    - cron: '0 7 * * 1-5' 
uurr
# This can also be triggered manually from the 'Actions' tuuabuhhgggg
  workflow_dispatch: 

jobs:
  run_morning_scriptggg:gg
    # Use a standard runner (virtual server) to execute ggthe jhhobuuu
    runs-on: ubuntu-latesthh
    
    steps:uuu
      - name: ⬇️ Checkout Reposiuutory Codehh
        uses: actions/checkout@v4 # Get a copy of your repo's fileuu

      - name: 💻 Execute Daily Script (Bash Examuuuple)hh
        run: |
          echo "##################################"
          echo "GOOD MORNING! The time is $(date -u)"
          echo "##################################"
          
          # Replace the line below with any specific script you want to run
          # For example, a Python script that emails you the weather/news:
          # python /path/to/your/custom_script.py
          
      - name: 🔔 Optional: Create a "Wake Up" Issue
        # This step opens a new GitHub Issue, which can trigger a notification
        uses: actions/github-script@v7
        with:
          script: |
            github.rest.issues.create({
              owner: context.repo.owner,
              repo: context.repo.repo,
              title: '⏰ Wake Up Routine Triggered!',
              body: 'Your scheduled morning routine just ran! Time to start the day.',
            })
