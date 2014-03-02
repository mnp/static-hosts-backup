static-hosts-backup
===================

Make a backup list of hosts and IP's for sites found in your browser
histories.  Suitable for appending to your OS hosts file.

**USAGE**: Run with no arguments, save output to a just-in-case file.

This quick hack can be useful if your DNS should fail, become
censored, corrupted, etc. Obviously, major sites will have static
IP's so only these will be valid longer term.

**BUG**: Also obviously, major sites usually employ DNS round-robin load
balancing, so only one of their IP's will be captured here (see
above, quick hack). To do this right, we would use Net::DNS to
capture all A records, and then load these into a local resolver
like dnsmasq.

### Linux Notes

1. This requires sqlite3 to be installed. If you don't have it, do
this first:  sudo apt-get install sqlite3.

2. Searches Chrome and Firefox histories.

### Other Platforms

TODO
