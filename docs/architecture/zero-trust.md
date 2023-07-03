# Zero-Trust

## Why Zero-Trust?
**Before** 

Nginx Reverse-Proxy relying on Cloudflare's blocking services to filter out bad actor traffic.

This Allowed For:

  * Centralised Connectivity Control - Expose Ports via Nginx config files, reload Nginx
  * Provider Flexibility - No walled-garden with one hosting provider
  * Self-Managed SSL Certificates

But it caused issues with:

  * Dynamic DNS on Domestic Broadband
  * Complexity - Nginx and complex configuration files, Public IP watcher (and preferably updater), Keeping SSL Certificates Updated
  * Requires Port-Forwarding on Router

**After**

Zero-Trust Externally Available Apps, with Internal Tunnelled connections relying on the WARP infrastructure to reduce complexity in connectivity maintenance.

Which reduced any issues with:

  * Dynamic DNS - Manged network via a Tunnel
  * Certificates - Generated and Managed by Cloudflare
  * Complexity - Add new External Service by pointing new sub-domain to the local IP and post number. Or keep it only accessible via a WARP connection using local IP
  * No Port Forwarding Required
  * More security at first-access - Access only if matching rules (e.g., emails), before reaching my Server


Concerns still apply with:

  * Fair-Use Policy with Cloudflare - Plex
  * Vendor-Lock in - Cloudflare is now a requirement which could cost in the future
  * Rule Overlap - Domain-Wide Rules + Zero Access Rules need to be considered

## Zero-Trust Configuration

Checklist in force for making an Application Accessible via Domain Name:

  * Does it require Access beyond just myself? E.g., Google Assistant for Home Assistant, Partner for Mealie etc.
  * What Sort of Access is required? E.g., Apps can have issues with initial Log-in, External Servers will not log in as require open access, just myself accessing or others?
  * Is there a need further than the above two points? E.g, Password Manager requires SSL for app-logic to work and so needs a sub-domain
  * If WARP connectivity could not be established, would it be useful to fall-back to domain + log in?


Everything else will be kept as locally accessible (including via WARP Tunnelling)