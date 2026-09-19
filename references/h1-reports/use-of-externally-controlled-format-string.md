# Use of Externally-Controlled Format String

_5 reports — High/Critical, disclosed_

- **CVE-2022-40604: Apache Airflow: Format String Vulnerability** — `Internet Bug Bounty` · `Critical` [↗](https://hackerone.com/reports/1707287)
  - `CVE-2022-40604` There is a Format String Vulnerability in src/airflow/utils/log/file_task_handler.py In the above code, I can control some part of the log_relative_path, because log_relative_path is made up of run_id and other things.
- **Exploitable Format String Vulnerability in curl_mfprintf Function** — `curl` · `High` [↗](https://hackerone.com/reports/2819666)
  - The curl_mfprintf function in the curl_printf.h file contains a format string vulnerability that allows an attacker to inject arbitrary format specifiers.
- **███ ████████ running a vulnerable log4j** — `U.S. Dept Of Defense` · `Critical` [↗](https://hackerone.com/reports/1438393)
  - Probably arbitrary code execution Observe that a request was made to your DNS server.
- **██████████ running a vulnerable log4j** — `U.S. Dept Of Defense` · `Critical` [↗](https://hackerone.com/reports/1423496)
  - `CVE-2021-44228` Probably arbitrary code execution Observe that a request was made to your DNS server.
- **Format String Vulnerability in the EdgeSwitch restricted CLI** — `Ubiquiti Inc.` · `High` [↗](https://hackerone.com/reports/311884)
  - In EdgeSwitch 1.7.3 and prior, an user with admin credentials can make use of specially crafted commands to execute arbitrary shell instructions, bypassing the SSH/TELNET CLI interface.
