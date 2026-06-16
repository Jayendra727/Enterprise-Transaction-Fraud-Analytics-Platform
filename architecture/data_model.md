bronze_transactions
| Column              |
| ------------------- |
| step                |
| type                |
| amount              |
| nameOrig            |
| oldbalanceOrg       |
| newbalanceOrig      |
| nameDest            |
| oldbalanceDest      |
| newbalanceDest      |
| isFraud             |
| isFlaggedFraud      |
| ingestion_timestamp |
| source_file_name    |

silver_transactions
| Column              |
| ------------------- |
| transaction_id      |
| step                |
| transaction_type    |
| amount              |
| source_account      |
| destination_account |
| fraud_flag          |

silver_accounts
nameOrig
nameDest
| Column         |
| -------------- |
| account_id     |
| account_number |
| account_type   |

silver_fraud_transactions
| Column         |
| -------------- |
| transaction_id |
| amount         |
| fraud_flag     |

Gold Layer
fact_transactions
| Column              |
| ------------------- |
| transaction_id      |
| source_account      |
| destination_account |
| amount              |
| transaction_type    |
| fraud_flag          |

fact_fraud_transactions
| Column           |
| ---------------- |
| transaction_id   |
| fraud_amount     |
| transaction_type |

gold_transaction_summary
| Metric             |
| ------------------ |
| Total Transactions |
| Total Amount       |
| Average Amount     |

gold_fraud_summary
| Metric       |
| ------------ |
| Fraud Count  |
| Fraud Amount |
| Fraud Rate   |

