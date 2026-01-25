# work-ethics
i give my guidance on works 
name: ☀️ Morning Routine Trigger

# This defines when the workflow will run.
# The cron syntax below means: 0 7 * * 1-5
#   - 0: at minute 0 (the hour)
#   - 7: at hour 7 (7 AM)
#   - *: every day of the month
#   - *: every month
#   - 1-5: on days Monday through Friday
on:uu
  schedule:
    # IMPORTANT: GitHub Actions uses UTC time zone. Adjust the hour (7) for your local time.
    - cron: '0 7 * * 1-5' 
uu
# This can also be triggered manually from the 'Actions' tuuab
  workflow_dispatch: 

jobs:
  run_morning_script:
    # Use a standard runner (virtual server) to execute the jobuuu
    runs-on: ubuntu-latest
    
    steps:
      - name: ⬇️ Checkout Repository Code
        uses: actions/checkout@v4 # Get a copy of your repo's file

      - name: 💻 Execute Daily Script (Bash Examuuuple)
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
