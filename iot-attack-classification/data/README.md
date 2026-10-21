# Data

`rt_iot2022.csv.gz` is the **RT-IoT2022** dataset from the UCI Machine Learning Repository (CC BY 4.0), compressed. pandas reads the `.gz` file directly, so there's no need to unzip it.

| | |
|---|---|
| Rows | 123,117 network flows (117,940 after removing duplicates and 2 unlabelled rows) |
| Columns | 83 flow features + `target` |
| Classes | 12: 9 attack types and 3 normal IoT device patterns |

**Normal traffic:** `MQTT_Publish`, `Thing_Speak`, `Wipro_bulb`
**Attacks:** `DOS_SYN_Hping`, `DDOS_Slowloris`, `ARP_poisioning`, `Metasploit_Brute_Force_SSH`, `NMAP_UDP_SCAN`, `NMAP_XMAS_TREE_SCAN`, `NMAP_OS_DETECTION`, `NMAP_TCP_scan`, `NMAP_FIN_SCAN` (label spellings kept as in the source)

## Notes
- This copy contains about 300 missing values marked `na` (including 2 missing labels). They're handled in the notebook: unlabelled rows are dropped, and missing feature values are imputed inside the modelling pipeline.
- Features include source and destination ports (`id.orig_p`, `id.resp_p`) and a `service` field inferred from the port. The notebook tests models with and without these, because in this lab capture some attack types always used the same port.

## Source
Sharmila B. S. and Rohini Nagapadma, *RT-IoT2022*, UCI Machine Learning Repository.
