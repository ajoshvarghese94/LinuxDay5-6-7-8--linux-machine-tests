# Test 4.1: File Management

## 1. Create an empty file `x` in `/tmp`
```bash
touch /tmp/x
ls -l /tmp/x
```
Screenshot: `screenshots/test-4.1-file-management/task01.png`

## 2. Copy `x` from `/tmp` to the home directory
```bash
cp /tmp/x ~
ls
```
Screenshot: `screenshots/test-4.1-file-management/task02.png`

## 3. Create a copy of `x` named `y`
```bash
echo "Hello World" > x
cp x y
cat y
```
Screenshot: `screenshots/test-4.1-file-management/task03.png`

## 4. Create directory `files` and move `x` and `y` into it
```bash
mkdir files
mv x y files/
cd files && ls
```
Screenshot: `screenshots/test-4.1-file-management/task04.png`

## 5. Copy the `files` directory as `copy_of_files`
```bash
cp -r files copy_of_files
```
`-r` (recursive) is required to copy a directory.

Screenshot: `screenshots/test-4.1-file-management/task05.png`

## 6. Rename `copy_of_files` to `files2`
```bash
mv copy_of_files files2
```
Screenshot: `screenshots/test-4.1-file-management/task06.png`

## 7. Remove `files` and `files2` with their contents
```bash
rm -r files files2
```
Screenshot: `screenshots/test-4.1-file-management/task07.png`
