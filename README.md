# Scan Docker Images Using Trivy:-

Trivy is a Simple and Comprehensive Vulnerability Scanner for Containers and other Artifacts, Suitable for CI
It is the most popular open source security scanner, reliable, fast, and easy to use.

the below script downloads Trivy binary based on your OS and architecture.
```
curl -sfL https://raw.githubusercontent.com/aquasecurity/trivy/main/contrib/install.sh | sh -s -- -b /usr/local/bin v0.18.3
sudo ln -s /usr/local/bin/trivy /usr/bin/trivy
```
```
trivy image vijay2181/web-amd64:v1
```

```
[root@ip-172-31-25-164 web-server]# trivy image vijay2181/web-amd64:v1
2023-06-20T17:22:12.632Z        INFO    Need to update DB
2023-06-20T17:22:12.633Z        INFO    Downloading DB...
30.57 MiB / 30.57 MiB [-----------------------------------------------------------------------------------------------------] 100.00% 20.79 MiB p/s 1s
2023-06-20T17:22:47.790Z        INFO    Detected OS: amazon
2023-06-20T17:22:47.792Z        INFO    Detecting Amazon Linux vulnerabilities...
2023-06-20T17:22:47.837Z        INFO    Number of PL dependency files: 0

vijay2181/web-amd64:v1 (amazon 2 (Karoo))
=========================================
Total: 0 (UNKNOWN: 0, LOW: 0, MEDIUM: 0, HIGH: 0, CRITICAL: 0)
```
