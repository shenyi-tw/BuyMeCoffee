# BuyMeCoffee

- [demo](https://www.youtube.com/shorts/TWmtCKO6BIg)
- Designed and implemented an end-to-end [checkout](https://app.bloomingrice.com/menu_order/c5b52e3b-3dee-488d-bebd-f9e216547d68) workflow, including order creation, payment initiation, idempotent processing, transactional consistency, webhook signature verification, and asynchronous payment confirmation
- Designed and implemented production and staging traffic routing architecture using Cloudflare DNS and Traefik
- Improved overall security posture by separating public and private network boundaries, implementing VPC peering, configuring firewall / Traefik rules, and applying Cloudflare anti-bot protection
- Implemented a centralized [logging](img/logscreen.png) pipeline, notification(firebase), [SliderCaptcha](https://app.bloomingrice.com/login), i18n and timezone

## Security Testing & Hardening

### 🔍 Penetration Testing
**Burp Suite - IDOR (Insecure Direct Object Reference) Testing**
![Burp Test 1](security/Burp/1.png)
![Burp Test 2](security/Burp/2.png)

### 🛡️ Web Security Headers
**HSTS (HTTP Strict Transport Security) Implementation**
![HSTS Configuration](security/HSTS/1.png)

### 🔒 SSL/TLS Security
**SSL Labs Security Assessment**
![SSL Labs Test](security/ssllabs/1.png)

### 🚨 Automated Security Scanning
**OWASP ZAP Security Analysis**
![ZAP Overview](security/zap/1.png)

### 🔍 Network Vulnerability Scanning
**OpenVAS (Greenbone Vulnerability Management)**
![OpenVAS Scan 1](security/OpenVAS/01.png)
![OpenVAS Scan 2](security/OpenVAS/02.png)
![OpenVAS Scan 3](security/OpenVAS/03.png)
![OpenVAS Scan 4](security/OpenVAS/04.png)
![OpenVAS Scan 5](security/OpenVAS/05.png)
![OpenVAS Scan 6](security/OpenVAS/06.png)
![OpenVAS Scan 7](security/OpenVAS/07.png)
![OpenVAS Scan 8](security/OpenVAS/08.png)
![OpenVAS Scan 9](security/OpenVAS/09.png)
![OpenVAS Scan 10](security/OpenVAS/10.png)

### 🐳 Container & Infrastructure Security
**Trivy Vulnerability Scanner**
![Trivy Scan Results](security/trivy/1.png)

### Observability
- By correlating logs and traces with the same Trace ID, we can navigate from a log entry directly to the full trace, inspect the request execution path, and identify performance bottlenecks across services.
![Observability 1](observability/1.png)
![Observability 2](observability/2.png)
- A client request passing through the BFF service to the Blog service, completing successfully with a 200 OK response in 13.17 ms.
![Observability 3](observability/3.png)
- Similar idea with a more complex scenario.
![Observability 5](observability/5.png)
- Dashboard correlates metrics, traces, and logs, allowing us to follow a request across multiple services and inspect the related logs using the same Trace ID.
![Observability 4](observability/4.png)
- Querying OpenTelemetry span metrics to show the top API calls by service and endpoint traffic rate.
![Observability 6](observability/6.png)
- Tempo is querying distributed traces to show API request rates, latency (p90), and service relationships.
![Observability 7](observability/7.png)
- Grafana SRE Service Detail dashboard shows a service's traffic, API performance, and latency metrics using Prometheus and Tempo data.
![Observability 8](observability/8.png)
