# Firewall Configuration Report

## Linux (UFW) Example
### List Rules
```bash
sudo ufw status verbose
```

### Block Port 23 (Telnet)
```bash
sudo ufw deny 23/tcp
```

### Allow SSH (Port 22)
```bash
sudo ufw allow 22/tcp
```

### Delete Rule
```bash
sudo ufw delete deny 23/tcp
```

---

## Windows Firewall Example
### Block Port 23
1. Open **Windows Defender Firewall with Advanced Security**.
2. Click **Inbound Rules → New Rule**.
3. Select **Port**, enter **23**, choose **Block the connection**.
4. Save the rule.

### Allow Port 22 (SSH)
1. Again go to **Inbound Rules → New Rule**.
2. Select **Port**, enter **22**, choose **Allow the connection**.
3. Save the rule.

---

## Summary
- Firewalls filter **inbound** and **outbound** traffic based on rules.
- Blocking Telnet (port 23) prevents insecure connections.
- Allowing SSH (port 22) enables secure remote access.
- Rules can be added, modified, and deleted as per security needs.

---

## Screenshots
Screenshots are in the `screenshots/` folder:
- `ufw-rules.png` → UFW status showing blocked Telnet / allowed SSH.
- `windows-firewall.png` → Windows Firewall inbound rule for port 23.
