Backup dir
=========

Роль для резервирования файлов и директорий

Variables
--------------
```yaml
# backup name postfix
dump_name: $(date '+%A')_dir
dump_dirs: []
# cron time 
dump_hour: 0
dump_minute: 30
dump_file_name: /var/dumpdir.sh
dump_attempt: 5
dump_attempt_interval: 5  # in seconds
dump_cron_task_name: backup dir
```

Example Playbook
----------------

    - hosts: apps
      roles:
        - role: CourseOrchestra.backup_dir
          dump_dirs: [/var/app]
