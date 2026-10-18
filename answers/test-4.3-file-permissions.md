# Test 4.3: File Permissions

## 1. Create a file called `test.txt`
```bash
touch test.txt
```
Screenshot: `screenshots/test-4.3-file-permissions/task01.png`

## 2. Display its current permissions
```bash
ls -l test.txt
```
Screenshot: `screenshots/test-4.3-file-permissions/task02.png`

## 3. Set owner = read/write, group = read, others = read
```bash
chmod 644 test.txt
```
Screenshot: `screenshots/test-4.3-file-permissions/task03.png`

## 4. Verify the updated permissions
```bash
ls -l test.txt
```
Result: `-rw-r--r--`

Screenshot: `screenshots/test-4.3-file-permissions/task04.png`

## 5. Create a shell script `deploy.sh`
```bash
touch deploy.sh
```
Screenshot: `screenshots/test-4.3-file-permissions/task05.png`

## 6. Grant executable permission
```bash
chmod +x deploy.sh
```
Screenshot: `screenshots/test-4.3-file-permissions/task06.png`

## 7. Verify `deploy.sh` is executable
```bash
ls -l deploy.sh
```
Result: `-rwxr-xr-x`

Screenshot: `screenshots/test-4.3-file-permissions/task07.png`

## 8. Create a directory `secure_data`
```bash
mkdir secure_data
```
Screenshot: `screenshots/test-4.3-file-permissions/task08.png`

## 9. Owner = full, group = read + execute, others = none
```bash
chmod 750 secure_data
```
Screenshot: `screenshots/test-4.3-file-permissions/task09.png`

## 10. Verify permissions of `secure_data`
```bash
ls -ld secure_data
```
Result: `drwxr-x---`

Screenshot: `screenshots/test-4.3-file-permissions/task10.png`

## 11. Remove `test.txt`, `deploy.sh`, and `secure_data`
```bash
rm -r test.txt deploy.sh secure_data
```
Screenshot: `screenshots/test-4.3-file-permissions/task11.png`

## Permission values used
| Number | Meaning |
|--------|---------|
| 4 | read (r) |
| 2 | write (w) |
| 1 | execute (x) |
