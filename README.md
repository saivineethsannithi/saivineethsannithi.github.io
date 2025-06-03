# SIEM Portfolio Project: Deploying ELK Stack with Filebeat on Kali Linux

This project demonstrates how I deployed the **ELK Stack (Elasticsearch, Logstash, Kibana)** and configured **Filebeat** to collect and visualize logs on **Kali Linux**, simulating a basic Security Information and Event Management (SIEM) solution.

---

## Tools Used

- **Kali Linux 2025.1**
- **Elasticsearch 8.18.2**
- **Logstash 8.18.2**
- **Kibana 8.18.2**
- **Filebeat 8.18.2**
- **OpenJDK 11** for Java runtime
- `curl`, `systemctl`, `nano`, `journalctl` and other Linux CLI tools

---

##  Project Setup and Configuration

### Step 1: Installed Java

![install java](https://github.com/user-attachments/assets/5d3a80a0-2c1b-4957-95ce-f002e8611b57)

### Step 2: Added Elastic GPG key and Repository

![updating elastic gpg,repository adn install elasticsearch logstach and kibana](https://github.com/user-attachments/assets/84a3b180-c175-4a23-a459-577daa48dead)

### Step 3: Installed Elasticsearch, Logstash, and Kibana
![updating elastic gpg,repository adn install elasticsearch logstach and kibana](https://github.com/user-attachments/assets/c7f1587d-3d51-4eb2-8f3f-afebfdf182fd)


###  Step 4: Generated Enrollment Token for Kibana
![token enrollment in kibana](https://github.com/user-attachments/assets/7a180b18-d2bd-489c-ac47-0d22841edbcf)

### Step 5: Logged Into Kibana with Token
![logining into elk](https://github.com/user-attachments/assets/c57df9be-3225-4ddb-b993-f319f99aab2d)

###  Step 6: Completed Kibana Setup
![settings up kibana](https://github.com/user-attachments/assets/cfe7a694-8392-4dab-9548-24367f54e5e0)

###  Step 7: Enabled and Started Elastic Services
![creaated filebeat and enable logstach,elasticsearch and kibana](https://github.com/user-attachments/assets/ae84e6a1-f18c-42b6-a86f-712c0a82643b)

###  Step 8: Configured Filebeat to Ship Logs
![configure filebeat](https://github.com/user-attachments/assets/a63d48dc-311d-44a4-b95e-4e751a7745eb)

###  Step 9: Added Sysmon for Linux Integration
![adding systems](https://github.com/user-attachments/assets/85e348e4-7c52-420d-80df-fab7070fd0d3)

###  Step 10: Verified Filebeat Was Running
![checking thefilebeat is active](https://github.com/user-attachments/assets/0f04508f-0b5e-4c6c-8383-1432f3964661)

###  Step 11: Simulated Log Generation
![stimulating the logs](https://github.com/user-attachments/assets/089ef4cb-1f1b-4e25-b4f5-082bd3d7bd6c)

### step12: Sucessfully Generted Timestamp In Kibana
![timestamp of logs](https://github.com/user-attachments/assets/d3fd8eb4-a353-43fd-ac68-22261b0e061b)

---

##  Challenges & Resolutions

| Challenge | Solution |
|----------|----------|
| SSL certificate issue (`curl: (60)` error) | Used `ssl.verification_mode: none` in `filebeat.yml` |
| 401 Unauthorized from Elasticsearch | Reset the `elastic` user password using `elasticsearch-reset-password` |
| Filebeat not shipping logs | Fixed file permissions and ensured log file existed (`/var/log/auth.log`) |
| Kibana not showing logs | Extended the time range and validated `filebeat-*` index |

---

## Results

Logs from Kali Linux (e.g., `/var/log/syslog`, `/var/log/auth.log`) were successfully shipped by Filebeat and visualized in Kibana, completing a full ELK Stack pipeline. This project proves my ability to configure a functional SIEM pipeline using open-source tools.

---

##  How to Run This Setup

1. Clone this repository and install Java.
2. Add the Elastic GPG key and repo.
3. Install Elasticsearch, Kibana, Logstash, and Filebeat.
4. Configure `filebeat.yml` with your system logs and credentials.
5. Enable services with `systemctl enable --now`.
6. Visit `http://localhost:5601` to log in to Kibana.
7. Use the Discover tab to view logs.

---


##  Contact

Feel free to reach out to me on [https://www.linkedin.com/in/saivineeth-sannithi-123278187/vineethsannithi1998@gmail.com].

