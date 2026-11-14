
# Week 02 - Linux Commands Practice

## 1. Working with Files

### List files
```bash
ls -lh
```

### Count lines in a file
```bash
wc -l module-01/data/app_2026-10.log
```

## 2. Searching Logs with grep

### Count ERROR logs
```bash
grep -c "ERROR" module-01/data/app_2026-10.log
```

### Find authentication errors
```bash
grep "auth" module-01/data/app_2026-10.log | grep -c ERROR
```

### Find errors on a specific date
```bash
grep "2026-10-10" module-01/data/app_2026-10.log | grep ERROR
```

## 3. Using cut, sort and uniq

### Extract dates
```bash
grep "ERROR" module-01/data/app_2026-10.log | cut -d' ' -f1
```

### Count errors by date
```bash
grep "ERROR" module-01/data/app_2026-10.log | cut -d' ' -f1 | sort | uniq -c
```

### Find the date with the fewest errors
```bash
grep "ERROR" module-01/data/app_2026-10.log | cut -d' ' -f1 | sort | uniq -c | sort -n | head -1
```

## 4. Redirecting Output

### Save output to a file
```bash
echo "Linux Practice" > assignment-02.txt
```

### Append output
```bash
echo "Practiced grep and sort" >> assignment-02.txt
```

## What I Learned

- Searching log files using grep
- Extracting data using cut
- Sorting data using sort
- Counting occurrences using uniq
- Displaying results using head
- Saving command output into files

