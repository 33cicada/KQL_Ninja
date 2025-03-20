# Microsoft Sentinel KQL Repository
 
<p align="center">
  <img src="https://img.shields.io/badge/Azure-KQL-00B2FF.svg?logo=microsoftazure&style=for-the-badge">
  <img src="https://img.shields.io/badge/Sentinel-SIEM-0078D4.svg?logo=microsoftazure&style=for-the-badge">
  <img src="https://img.shields.io/badge/Security-Analytics-FF4500.svg?logo=microsoftsecurity&style=for-the-badge">
</p>

<p align="center">
  <em>A curated collection of powerful KQL (Kusto Query Language) queries for Microsoft Sentinel</em>
</p>

## 🔍 Overview

This repository contains a comprehensive collection of KQL queries designed to enhance your Microsoft Sentinel threat hunting, investigation, and detection capabilities. Each query is carefully crafted and validated to work with Microsoft Sentinel.

## 📚 Categories

- **Threat Hunting**: Queries for proactive threat hunting across your environment
- **Security Monitoring**: Continuous monitoring queries for critical infrastructure
- **Incident Response**: Queries to assist during active security incidents
- **Compliance**: Queries to help with regulatory and compliance requirements
- **Device Security**: Endpoint-focused detection and monitoring
- **Identity & Access**: Authentication and authorization monitoring
- **Network Security**: Network traffic analysis and anomaly detection

## 💡 How to Use

1. Navigate to your Microsoft Sentinel workspace
2. Go to Logs
3. Copy and paste the query of interest
4. Modify parameters as needed for your environment
5. Run the query

## 🚀 Getting Started

```kql
// Example query to get started:
SecurityEvent
| where TimeGenerated > ago(1h)
| where EventID == 4624
| summarize count() by Account, Computer
| order by count_ desc
```

## 🔗 Useful Resources

- [Official KQL Documentation](https://learn.microsoft.com/en-us/azure/data-explorer/kusto/query/)
- [Microsoft Sentinel Documentation](https://learn.microsoft.com/en-us/azure/sentinel/)
- [KQL Cheat Sheet](https://learn.microsoft.com/en-us/azure/data-explorer/kql-quick-reference)

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-query`)
3. Commit your changes (`git commit -m 'Add some amazing query'`)
4. Push to the branch (`git push origin feature/amazing-query`)
5. Open a Pull Request

## 📝 Query Naming Convention

All queries should follow this naming pattern:
- `[Category]_[Threat/Use Case]_[Data Source].kql`

Example: `Hunting_PasswordSpray_AAD.kql`

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.

---

<p align="center">
  Made with ❤️ by security professionals for security professionals
</p>