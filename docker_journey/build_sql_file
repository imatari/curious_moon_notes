# build.sql section
## the file content (produce the `build.sql` file)
_review content and continue reading after_
```sql
create schema if not exists import;

DROP TABLE IF EXISTS import.master_plan;

CREATE TABLE import.master_plan
  (
     start_time_utc     TEXT,
     duration           TEXT,
     date               TEXT,
     team               TEXT,
     spass_type         TEXT,
     target             TEXT,
     request_name       TEXT,
     library_definition TEXT,
     title              TEXT,
     description        TEXT
  );

\copy import.master_plan from 'C:\Users\matari\docker\volumes\master_plan.csv' with DELIMITER ',' HEADER CSV
```
### **what i did different from the book for the `build.sql` file**
- The book uses `copy` but i needed to use `\copy` for it to work  
- Additionally, what spanned as three lines starting with `copy` in the book won't work with the `\copy` command. The three lines instead had to be written as one contiguous line.
- Lastly, it's worth noting that when entering the directory path to the `master_plan.csv` it is okay to use how Windows notes a file path with backslashes.

### **To run the `build.sql` file on the `enceladus` database**
- in order to execute  
`psql -h localhost -U postgres -d enceladus < build.sql`  
with a minimum of fuss,  
start the `bash.exe` found here  
`C:\Program Files\Git\bin`  
_the source:_  
**https://superuser.com/questions/1011597/what-does-an-output-is-not-a-tty-error-mean**  
![use bash.exe][bash]
I found this source because when I tried to execute the above command/instruction, I tried it in Git Bash and it gave me this error: **`output is not a tty`**  
I considered trying the command in Git Bash because when I tried in Powershell, it was not happy with the **`<`** symbol.

this is what it looked like for me.
![running of script][results]



[bash]:https://i.imgur.com/ra9loan.png?1
[results]:https://i.imgur.com/tpTw2oY.png
