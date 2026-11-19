# Windows Monitoring Runbook

## System Information
- Monitoring: Prometheus + Grafana
- Exporter: Windows Exporter
- Operating System: Windows
- Alert threshold: 80%
- Pending period: 5 minutes

---

## CPU_Usage_High

**Problem:** CPU usage exceeds 80%.

**Diagnosis:**
1. Open Task Manager (`Ctrl + Shift + Esc`).
2. Open the Processes tab.
3. Sort processes by CPU usage.
4. Identify applications consuming excessive CPU resources.

**Resolution:**
- Close unnecessary applications.
- Restart applications that are not responding.
- Check suspicious processes.
- Investigate persistent high CPU usage.

---

## RAM_Usage_High

**Problem:** RAM usage exceeds 80%.

**Diagnosis:**
1. Open Task Manager.
2. Open the Processes tab.
3. Sort processes by Memory usage.
4. Identify applications consuming excessive RAM.

**Resolution:**
- Close unnecessary applications.
- Restart applications with unusually high memory consumption.
- Check for possible memory leaks.
- Consider upgrading RAM if usage remains consistently high.

---

## SSD_Usage_High

**Problem:** SSD (C:) usage exceeds 80%.

**Diagnosis:**
1. Open This PC.
2. Check available space on drive C:.
3. Open Settings → System → Storage.
4. Identify files and applications consuming disk space.

**Resolution:**
- Remove unnecessary temporary files.
- Uninstall unused applications.
- Move large personal files to another drive.
- Review old backups and downloads.

**Warning:** Do not manually delete Windows system files.

---

## HDD_Usage_High

**Problem:** HDD (D:) usage exceeds 80%.

**Diagnosis:**
1. Open This PC.
2. Check available space on drive D:.
3. Identify large folders and files.
4. Review old archives and backups.

**Resolution:**
- Remove unnecessary files.
- Move archives to external storage.
- Remove obsolete backups only after verifying that current backups exist.
- Organize stored data.

---

## Verification

After resolving an issue:

1. Open the Grafana dashboard.
2. Check CPU, RAM, SSD and HDD metrics.
3. Verify that the affected metric is below 80%.
4. Confirm that the alert state returns to Normal.
5. Check Telegram for alert recovery notifications.

---

**Monitoring system:** Local Windows PC
