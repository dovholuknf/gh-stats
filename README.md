# gh-stats
A simple bash script that will output some of your GitHub repo's stats

## Setup
Open the script, change the ORG and REPO to your ORG and REPO. Some of
the scripts will give you ORG stats, some are per REPO. The script clearly
shows you what it's doing...

Set a `Y_U_RATE_LIMIT` environment variable. This is a github "Fine-grained personal access token".
Generate one from here: https://github.com/settings/personal-access-tokens/new

Source this script and get all the functions onto your shell.

## Commands used
`jq` is probably the one you need most which is non-standard but `curl` is also
used extensively.

## General Usage
At some interval issue a command such as `stargazersPerRepo` which will:
* find all the stargazers for your org and output them to 'pages' of json files
* condense the pages of json into a single "${REPO}.stargazers.all.json"
* parse "${REPO}.stargazers.all.json" into a csv
* marvel at all your stargazers

There are other functions to do 'other things' but really that's what you're probably
looking for anyway. Who's stargazing your repo and when and who stopped! You can be a
snoop!