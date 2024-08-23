<h1 align="center">Message leaderboard</h1>
<p align="center">This set of commands adds a message leaderboard functionality to your server (currently personalized for a specific server, though if you change the database keys it can be quite easily personalized to your server)</p>

<h2 align="center">Setup</h2>
<h4>1. Copy all 4 commands to your server's custom commands</h4>
<p>The setup instructions for each cc are in the first comment, and configurable values (if any) directly below this initial comment</p>
<h4>2. Run this command in discord in the channel you want the auto updating leaderboard to be</h4>

```go
-evalcc channel id: {{.Channel.ID}}
message id: {{sendMessageRetID nil (cembed "title" "Hardmode leaderboard" "description" "No one is on the leaderboard yet" "footer" (sdict "text" "This message updates every 6 hours\nNext update") "timestamp" (currentTime.Add (toDuration "6h")) "color" 14232643)}}
```

<p>This will send the leaderboard message and also a seperate message containing the channel id and message id. you will need these later</p>

<h4>3. Copy the message containing the channel and message ids from the previous step</h4>
<p>In the "auto update leaderboard" command there are two config variables for these ids</p>

> [!IMPORTANT]
> Make sure that you place the correct id in the correct variable or the command wont work
