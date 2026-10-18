# Linux Day 5,6,7,8: Machine Tests

DevOps Linux Fundamentals (Day 4) machine tests, completed on Ubuntu (WSL).

## Repository Structure
```
.
├── README.md
├── answers/
│   ├── test-4.1-file-management.md
│   ├── test-4.2-file-directory-management.md
│   ├── test-4.3-file-permissions.md
│   └── test-4.4-users-and-groups.md
└── screenshots/
    ├── test-4.1-file-management/             (task01 ... task07)
    ├── test-4.2-file-directory-management/   (task01 ... task06)
    ├── test-4.3-file-permissions/            (task01 ... task11)
    └── test-4.4-users-and-groups/            (task01 ... task16)
```

## Tests Covered
| Test | Topic | Key Commands | Answers |
|------|-------|--------------|---------|
| 4.1 | File Management | `touch`, `cp`, `mv`, `mkdir`, `rm -r` | [answers](answers/test-4.1-file-management.md) |
| 4.2 | File and Directory Management | `touch`, `mkdir -p`, `mv`, `rm -r` | [answers](answers/test-4.2-file-directory-management.md) |
| 4.3 | File Permissions | `chmod`, `ls -l`, `ls -ld` | [answers](answers/test-4.3-file-permissions.md) |
| 4.4 | Users and Groups | `useradd`, `groupadd`, `usermod`, `chown`, `userdel`, `groupdel` | [answers](answers/test-4.4-users-and-groups.md) |

## Environment
- Ubuntu on WSL (Windows Subsystem for Linux)
- User: `Ajosh`

Each answers file lists the command used for every task, with the matching screenshot path.
