# wp-cron-bash
Run WP Cron via bash without having to add an entry to your crontab

USAGE: wp_cron --domain <base site url> --interval <delay time> --verbose
	
Possible delay time values:
	s for seconds (default)
	m for minutes
	h for hours
	d for days

Flags:
	--domain (-d)
		Sets the base domain to call wp-cron.php on.
			Note: If DOMAIN_CURRENT_SITE is defined in wp-config.php and you're running this command from your base install directory, --domain can be omitted.
				
	--interval (-i)
		Sets the amount of time between wp-cron.php calls
	
	--verbose (-v)
		Use curl instead of wget to show cron responses
			
EXAMPLE: wp_cron -d msnc.dev -i 60s -v
