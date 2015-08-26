# Install instructions

1. Go to Slack and set up an incoming webhook integration:
https://yourslackteam.slack.com/services/new/incoming-webhook

2. Clone this repo with:
> git clone git@github.com:hbbtstar/parsely-slack-integration.git

3. install requirements:
> cd parsely-slack-integration
> pip install -r requirements.txt

4. In config.py enter your webhook URL you received above, your Parse.ly apikey, shared secret, and channel you want to send the results to

5. Run the command with the arguments you want (sample commands shown below) or set up a cron job to have them sent automatically
> python parsely_slack.py --help


## Sample Commands
> python parsely_slack.py realtime --mention bob alice --limit 10 --shares --time 1h
Returns the top 10 posts in the last hour with shares and notifies bob and alice

> python parsely_slack.py analytics --mention sue george david --limit 15 --shares --days 7
Returns the top 15 posts over the past 7 days with shares and notifies sue, george, and david
