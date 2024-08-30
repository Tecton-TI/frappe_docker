Everything about [Frappe](https://github.com/frappe/frappe) and [ERPNext](https://github.com/frappe/erpnext) in containers.

## Getting Started

This is for develop purposes and add new features to the erp

1.- copy the backup from host to container
2.- execute
  
  ```bash
  gzip -d <filepath of sql-gz file>
  bench restore <filepath of the decompressed sql file>
  ```

3.- after this you need to get the apps for the erp in these cases you need to use one repo and the following apps:
      - https://github.com/tonicanada/tecton_erpnext_endpoints
      - hrms
      - payments
      - insights
    and then execute the following command with each app  
  
  ```bash
  bench get-app <app-name or repo>
  ```

4.- finally use
  
  ```bash
  bench migrate
  ```

and you are good to go
