# Run commands against results

Run redis command against a redis result set. For example delete a bunch of keys that match a query.

`
redis-cli keys "*worker*" | awk "{print $2}" | xargs redis-cli del
`

This will delete all keys that have the word `worker` somewhere in its name.
