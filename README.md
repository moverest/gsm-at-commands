# GSM AT Commands

### `AT+CMGF` - Select SMS Message Format

#### Test command

`AT+CMGF=?` list supported formats

##### Example

```
AT+CMGF=?
+CMGF: (0,1)

OK
```

#### Read command

`AT+CMGF?` gets the current format mode.


##### Example

```
AT+CMGF?
+CMGF: 1

OK
```

#### Write command

`AT+CMGF=<mode>`

Arguments:

- `mode`:
  - 0 - PDU mode
  - 1 - text mode

### `AT+CMGL` - List SMS Messages from Preferred Store

#### Test command
`AT+CMGL=?` lists supported status.

##### Example in text mode

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
