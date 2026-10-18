# Test 4.2: File and Directory Management

## 1. Create a file called `x`
```bash
touch x
```
Screenshot: `screenshots/test-4.2-file-directory-management/task01.png`

## 2. Create a directory called `content`
```bash
mkdir content
```
Screenshot: `screenshots/test-4.2-file-directory-management/task02.png`

## 3. Move `x` into `content`
```bash
mv x content/
```
Screenshot: `screenshots/test-4.2-file-directory-management/task03.png`

## 4. Create a file `y` inside `content`
```bash
touch content/y
```
Screenshot: `screenshots/test-4.2-file-directory-management/task04.png`

## 5. Create `dir1/dir2/dir3` inside `content`
```bash
cd content
mkdir -p dir1/dir2/dir3
```
`-p` creates the parent directories along the way.

Screenshot: `screenshots/test-4.2-file-directory-management/task05.png`

## 6. Remove `content` with all its contents
```bash
cd ~
rm -r content
```
Screenshot: `screenshots/test-4.2-file-directory-management/task06.png`
