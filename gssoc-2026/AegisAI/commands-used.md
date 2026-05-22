# Commands Used

## Sync fork

git fetch upstream

## Rebase

git rebase upstream/main

## Continue rebase

git rebase --continue

## Force push after rebase

git push origin fix-information-exposure --force

## Check conflict markers

Select-String "<<<<<<" backend/app/api/v1/guard.py

## Python syntax check

python -m py_compile backend/app/api/v1/guard.py