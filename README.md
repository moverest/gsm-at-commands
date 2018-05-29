# GSM AT Commands

### `AT+CMGL` - List SMS Messages from Preferred Store

#### Test command
`AT+CMGL=?` lists supported status.

##### Exemple in text mode

```
AT+CMGL=?
+CMGL: ("REC UNREAD","REC READ","STO UNSENT","STO SENT","ALL")

OK
```

#### Write command

`AT+CMGL=<status>,<mode>`

Arguments:

- status:
    - 0 = `REC UNREAD` (default)
    - 1 = `REC READ`
    - 2 = `STO UNSENT`
    - 3 = `STO SENT`
    - 4 = `ALL`
- mode:
    - 0 = change status, e.g. unread message becomes read (default)
    - 1 = don't change status

#### Execution command

`AT+CMGL` is the same as `AT+CMGL="REC UNREAD"` or `AT+CMGL=0`.
