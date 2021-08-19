
Script to poll schedule in https://mymedical.iom.int and notify via Telegram when there is a new free slot.

#Requirements
Make sure you've installed newman
```
npm install -g newman
```

# Execute
To start the infinite polling process :

```
./run.sh
```
Pass parameters `botId` and `chatId` for telegram messaging
# Logs
To see last log look into `log` file

# Details
Core logic implemented as a postman collection.
Postman collection executed once in a minute.
It consists of 3 steps:
- first and second steps are receiving necessary tokens
- the last one gets information about the schedule and check if there are any free slots before the required date.
  If there are free slots it sends a telegram message