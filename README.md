# hubot-newrelic2-cfpb

New Relic stats from hubot, with CFPB-specific modifications.

This is forked from https://github.com/statianzo/hubot-newrelic2 and modified.

## Why this is forked

We forked this primarily to provide Mattermost-specific customizations

1. Content with Mattermost's 4000-character post limit
1. Use Markdown where suitable, especially for tabular output

## Examples

**Servers**
![newrelic servers](https://raw.githubusercontent.com/cfpb/hubot-newrelic2-cfpb/master/doc/servers.png)

**Deployments**
![newrelic servers](https://raw.githubusercontent.com/cfpb/hubot-newrelic2-cfpb/master/doc/deployments.png)



## Installation

```
npm install --save hubot-newrelic2-cfpb
```

* Add `"hubot-newrelic2-cfpb"` into your hubot project's `external-scripts.json`
* Add `"hubot-newrelic2-cfpb": "^0.4.0"` (or other version) into your `package.json`
* Set `HUBOT_NEWRELIC_API_KEY` to your New Relic API key
* Set `HUBOT_NEWRELIC_API_HOST`. This will default to `api.newrelic.com` if not set

## Usage

*Note*: You can replace 'newrelic' with 'nr' in all these commands.

* List all commands
```
hubot newrelic help
```

#### Application Related Commands

* List all applications
```
hubot newrelic apps
```

* Filtered list of applications
```
hubot newrelic apps name <filter_string>
```

* List of single application's instances
```
hubot newrelic apps instances <app_id>
```

* List of single application's hosts
```
hubot newrelic apps hosts <app_id>
```

* List all deployments for an application
```
hubot newrelic deployments <app_id>
```

* List recent deployments for an application
```
hubot newrelic deployments recent <app_id>
```

#### Key Transaction Related Commands

* List of all key transactions
```
hubot newrelic ktrans
```

* Returns a single key transaction
```
hubot newrelic ktrans id <ktrans_id>
```

#### Server Related Commands

* List all servers
```
hubot newrelic servers
```

* Filtered list of servers
```
hubot newrelic servers name <filter_string>
```

#### User Related Commands

* List all account users
```
hubot newrelic users
```

* Filtered list of account users
```
hubot newrelic user email <filter_string>
```
