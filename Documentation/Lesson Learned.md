Lessons Learned

Issue:
The Domain Controller was configured to use Google's public DNS (8.8.8.8).

Impact:
Active Directory services rely on DNS to locate domain resources. Using an external DNS server can cause authentication, Group Policy, LDAP, and domain service failures.

Resolution:
Configured the Domain Controller to use its own static IP address (192.168.50.10) as the preferred DNS server, then flushed and re-registered DNS records before verifying domain health.