# Test 4.4: Users and Groups

## 1. Create a new user `devopsuser`
```bash
sudo useradd devopsuser
sudo passwd devopsuser
```
Screenshot: `screenshots/test-4.4-users-and-groups/task01.png`

## 2. Verify the user was created
```bash
id devopsuser
grep devopsuser /etc/passwd
```
Screenshot: `screenshots/test-4.4-users-and-groups/task02.png`

## 3. Create a new group `devops`
```bash
sudo groupadd devops
grep devops /etc/group
```
Screenshot: `screenshots/test-4.4-users-and-groups/task03.png`

## 4. Add `devopsuser` to `devops`
```bash
sudo usermod -aG devops devopsuser
```
`-a` appends, so existing secondary groups are kept.

Screenshot: `screenshots/test-4.4-users-and-groups/task04.png`

## 5. Verify group membership
```bash
groups devopsuser
```
Screenshot: `screenshots/test-4.4-users-and-groups/task05.png`

## 6. Create directory `project_data`
```bash
mkdir project_data
```
Screenshot: `screenshots/test-4.4-users-and-groups/task06.png`

## 7. Change ownership to `devopsuser`
```bash
sudo chown devopsuser project_data
```
Screenshot: `screenshots/test-4.4-users-and-groups/task07.png`

## 8. Change group ownership to `devops`
```bash
sudo chown :devops project_data
```
Both can be done at once: `sudo chown devopsuser:devops project_data`

Screenshot: `screenshots/test-4.4-users-and-groups/task08.png`

## 9. Verify ownership and permissions
```bash
ls -ld project_data
```
Screenshot: `screenshots/test-4.4-users-and-groups/task09.png`

## 10. Create `project.txt` inside `project_data`
```bash
cd project_data
sudo touch project.txt
```
Screenshot: `screenshots/test-4.4-users-and-groups/task10.png`

## 11. Assign ownership of `project.txt`
```bash
sudo chown devopsuser:devops project.txt
```
Screenshot: `screenshots/test-4.4-users-and-groups/task11.png`

## 12. Verify ownership of `project.txt`
```bash
ls -lh project.txt
```
Screenshot: `screenshots/test-4.4-users-and-groups/task12.png`

## 13. Delete `project.txt`
```bash
sudo rm project.txt
```
Screenshot: `screenshots/test-4.4-users-and-groups/task13.png`

## 14. Remove the `project_data` directory
```bash
cd ~
rmdir project_data
```
Screenshot: `screenshots/test-4.4-users-and-groups/task14.png`

## 15. Delete the user `devopsuser`
```bash
sudo userdel devopsuser
```
Verified with `id devopsuser` (no such user) and `grep devopsuser /etc/passwd` (no output).

Screenshot: `screenshots/test-4.4-users-and-groups/task15.png`

## 16. Delete the group `devops`
```bash
sudo groupdel devops
grep devops /etc/group
```
No output confirms the group is removed.

Screenshot: `screenshots/test-4.4-users-and-groups/task16.png`
