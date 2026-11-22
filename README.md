# sila-config

Occasion messages for the Sila prayer app. The app reads `campaigns.json` anonymously (at most
twice a day, and only if the person turned on "Occasion messages") and schedules each message as
a local notification on their own phone. Nothing about the reader is sent or stored here.

## Format

```json
{
  "version": 1,
  "messages": [
    {
      "id": "ramadan-1448",
      "date": "2027-02-07",
      "time": "17:00",
      "title": { "ar": "رمضان مبارك", "en": "Ramadan Mubarak" },
      "body":  { "ar": "تقبّل الله منا ومنكم.", "en": "May Allah accept from us and you." }
    }
  ]
}
```

- `date` and `time` are local to each person's phone ("5 pm wherever you are").
- Only messages due in the next 14 days are used; at most 30 per file.
- Limits: id up to 60 characters, title up to 80, body up to 240. Plain text only.
- Keep messages rare and religious in tone; review each one before publishing.
