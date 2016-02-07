## meteor-client-refresh

Since `beta.8`, a change in client code also causes a server restart.

## beta.7

*meteor --release METEOR@1.3-modules-beta.7*

Client mod w/o ultimate code change (no hcp, as expected):

```
echo >> client/client.js
=> Client modified -- refreshing
```

Client code change (hcp, as expected):


```
echo "console.log('client load $RANDOM');" >> client/client.js
=> Client modified -- refreshing
```

## beta.8

*meteor --release METEOR@1.3-modules-beta.8*

Client mod w/o ultimate code change (no hcp, as expected):


```
echo >> client/client.js
=> Meteor server restarted
```

Client code change (hcp, as expected):

```
echo "console.log('client load $RANDOM');" >> client/client.js
=> Meteor server restarted
```
