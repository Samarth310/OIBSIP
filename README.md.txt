
1. Install UFW:
   Command: sudo apt update
            sudo apt install ufw -y
   - Updates the package list and installs UFW (Uncomplicated Firewall).
   - '-y' automatically confirms the installation.

2. Check UFW status:
   Command: sudo ufw status
   - Displays whether UFW is active or inactive.
   - Shows any existing firewall rules.

3. Enable UFW:
   Command: sudo ufw enable
   - Turns on the firewall and starts applying rules.

4. Allow SSH:
   Command: sudo ufw allow ssh
   - Opens port 22 (default SSH port).
   - Important for remote access so you don’t lock yourself out.

5. Allow HTTP:
   Command: sudo ufw allow 80/tcp
   - Opens port 80 (TCP).
   - Used by web servers for regular HTTP traffic.

6. Allow HTTPS:
   Command: sudo ufw allow 443/tcp
   - Opens port 443 (TCP).
   - Used for secure HTTPS traffic.

7. Allow custom port:
   Command: sudo ufw allow 8080/tcp
   - Opens port 8080 (TCP).
   - Often used for testing web servers or proxy services.

8. Deny a port:
   Command: sudo ufw deny 23/tcp
   - Blocks port 23 (TCP).
   - Telnet runs on this port, which is insecure, so blocking it is good practice.

9. Delete a rule:
   Command: sudo ufw delete allow 8080/tcp
   - Removes the rule that allowed port 8080.
   - Useful for correcting mistakes or removing unneeded rules.

10. Set default policies:
    Command: sudo ufw default deny incoming
             sudo ufw default allow outgoing
    - Deny all incoming traffic by default (extra security).
    - Allow all outgoing traffic (so your system can make requests).

11. Reload UFW:
    Command: sudo ufw reload
    - Reloads UFW to apply new or modified rules.
    - Doesn’t disable the firewall.

12. Check detailed status:
    Command: sudo ufw status verbose
    - Shows active rules with more details.
    - Helpful for troubleshooting and verifying configuration.

13. Disable UFW:
    Command: sudo ufw disable
    - Completely turns off the firewall.
    - Rules will not be enforced until re-enabled.

