# retention-policy-azure-storage-account
retention-policy-azure-storage-account


```
{
  "rules": [
    {
      "enabled": true,
      "name": "data-retention",
      "type": "Lifecycle",
      "definition": {
        "actions": {
          "version": {
            "delete": {
              "daysAfterCreationGreaterThan": 7
            }
          },
          "baseBlob": {
            "delete": {
              "daysAfterModificationGreaterThan": 30
            }
          },
          "snapshot": {
            "delete": {
              "daysAfterCreationGreaterThan": 7
            }
          }
        },
        "filters": {
          "blobTypes": [
            "blockBlob",
            "appendBlob"
          ]
        }
      }
    }
  ]
}

```
