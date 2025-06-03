# 📊 SIEM Portfolio Project: Deploying ELK Stack with Filebeat on Kali Linux

This project demonstrates how I deployed the **ELK Stack (Elasticsearch, Logstash, Kibana)** and configured **Filebeat** to collect and visualize logs on **Kali Linux**, simulating a basic Security Information and Event Management (SIEM) solution.

---

## 🛠️ Tools Used

- **Kali Linux 2025.1**
- **Elasticsearch 8.18.2**
- **Logstash 8.18.2**
- **Kibana 8.18.2**
- **Filebeat 8.18.2**
- **OpenJDK 11** for Java runtime
- `curl`, `systemctl`, `nano`, `journalctl` and other Linux CLI tools

---

## ⚙️ Project Setup and Configuration

### ✅ Step 1: Installed Java
![Install Java](install%20java.png)

### ✅ Step 2: Added Elastic GPG key and Repository
![Elastic GPG and Repo Setup](updating%20elastic%20gpg,repository%20adn%20install%20elasticsearch%20logstach%20and%20kibana.png)

### ✅ Step 3: Installed Elasticsearch, Logstash, and Kibana
(See image above)

### ✅ Step 4: Generated Enrollment Token for Kibana
![Enrollment Token](token%20enrollment%20in%20kibana.png)

### ✅ Step 5: Logged Into Kibana with Token
![Kibana Login](logining%20into%20elk.png)

### ✅ Step 6: Completed Kibana Setup
![Kibana Setup](settings%20up%20kibana.png)

### ✅ Step 7: Enabled and Started Elastic Services
![Enable Services](creaated%20filebeat%20and%20enable%20logstach,elasticsearch%20and%20kibana.png)

### ✅ Step 8: Configured Filebeat to Ship Logs
![Filebeat Configuration](configure%20filebeat.png)

### ✅ Step 9: Added Sysmon for Linux Integration
![Sysmon Integration](adding%20systems.png)

### ✅ Step 10: Verified Filebeat Was Running
![Filebeat Active Status](checking%20thefilebeat%20is%20active.png)

### ✅ Step 11: Simulated Log Generation
![Log Simulation](stimulating%20the%20logs.png)

---

## 💡 Challenges & Resolutions

| Challenge | Solution |
|----------|----------|
| SSL certificate issue (`curl: (60)` error) | Used `ssl.verification_mode: none` in `filebeat.yml` |
| 401 Unauthorized from Elasticsearch | Reset the `elastic` user password using `elasticsearch-reset-password` |
| Filebeat not shipping logs | Fixed file permissions and ensured log file existed (`/var/log/auth.log`) |
| Kibana not showing logs | Extended the time range and validated `filebeat-*` index |

---

## 📈 Results

Logs from Kali Linux (e.g., `/var/log/syslog`, `/var/log/auth.log`) were successfully shipped by Filebeat and visualized in Kibana, completing a full ELK Stack pipeline. This project proves my ability to configure a functional SIEM pipeline using open-source tools.

---

## 🚀 How to Run This Setup

1. Clone this repository and install Java.
2. Add the Elastic GPG key and repo.
3. Install Elasticsearch, Kibana, Logstash, and Filebeat.
4. Configure `filebeat.yml` with your system logs and credentials.
5. Enable services with `systemctl enable --now`.
6. Visit `http://localhost:5601` to log in to Kibana.
7. Use the Discover tab to view logs.

---

## 📸 All Screenshots
(Ensure these are added to your GitHub repo)

- `install java.png`
- `updating elastic gpg,repository adn install elasticsearch logstach and kibana.png`
- `token enrollment in kibana.png`
- `logining into elk.png`
- `settings up kibana.png`
- `creaated filebeat and enable logstach,elasticsearch and kibana.png`
- `configure filebeat.png`
- `adding systems.png`
- `checking thefilebeat is active.png`
- `stimulating the logs.png`

---

## 📬 Contact

Feel free to reach out to me on [Your LinkedIn/GitHub Email].

