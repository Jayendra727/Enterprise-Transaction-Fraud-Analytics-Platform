Bronze Layer
bronze_transactions

Raw transaction data ingested from PaySim.
| Column Name         | Data Type     |
| ------------------- | ------------- |
| step                | INT           |
| type                | STRING        |
| amount              | DECIMAL(18,2) |
| nameOrig            | STRING        |
| oldbalanceOrg       | DECIMAL(18,2) |
| newbalanceOrig      | DECIMAL(18,2) |
| nameDest            | STRING        |
| oldbalanceDest      | DECIMAL(18,2) |
| newbalanceDest      | DECIMAL(18,2) |
| isFraud             | INT           |
| isFlaggedFraud      | INT           |
| ingestion_timestamp | TIMESTAMP     |
| source_file_name    | STRING        |

Silver Layer
silver_transactions

Cleaned and standardized transaction data.
| Column Name             | Data Type     |
| ----------------------- | ------------- |
| transaction_id          | BIGINT        |
| step                    | INT           |
| transaction_type        | STRING        |
| amount                  | DECIMAL(18,2) |
| source_account          | STRING        |
| destination_account     | STRING        |
| old_source_balance      | DECIMAL(18,2) |
| new_source_balance      | DECIMAL(18,2) |
| old_destination_balance | DECIMAL(18,2) |
| new_destination_balance | DECIMAL(18,2) |
| fraud_flag              | INT           |
| system_fraud_flag       | INT           |

silver_accounts

Derived from both source and destination accounts.
| Column Name    | Data Type |
| -------------- | --------- |
| account_id     | STRING    |
| account_number | STRING    |

silver_fraud_transactions

Only fraudulent transactions.
| Column Name      | Data Type     |
| ---------------- | ------------- |
| transaction_id   | BIGINT        |
| transaction_type | STRING        |
| amount           | DECIMAL(18,2) |
| fraud_flag       | INT           |

Gold Layer
fact_transactions
| Column Name         |
| ------------------- |
| transaction_id      |
| source_account      |
| destination_account |
| transaction_type    |
| amount              |
| fraud_flag          |

fact_fraud_transactions
| Column Name      |
| ---------------- |
| transaction_id   |
| transaction_type |
| fraud_amount     |

gold_transaction_summary
| Metric            |
| ----------------- |
| transaction_count |
| total_amount      |
| average_amount    |

gold_fraud_summary
| Metric           |
| ---------------- |
| fraud_count      |
| fraud_amount     |
| fraud_percentage |

