# Watchman API
> An API to gather and display all news released by Zambia's top online newspapers.

#### NB: You need a rapid API account in order to use this API as it provides you with an API key.
https://rapidapi.com/matongomulindi@gmail.com/api/zambian-news/

### Get articles from all sources

### Request

`GET /news/`

### Response
##### The results usually go up > 200

  ```json
  {
    "source": "Daily Mail",
    "title": "Businesses must do the right thing!",
    "link": "http://www.daily-mail.co.zm/businesses-must-do-the-right-thing/",
    "id": 1
  },
  {
    "source": "Daily Mail",
    "title": "Every CDF kwacha must count",
    "link": "http://www.daily-mail.co.zm/every-cdf-kwacha-must-count/",
    "id": 2
  },
  {
    "source": "Daily Mail",
    "title": "Stop the loot",
    "link": "http://www.daily-mail.co.zm/stop-the-loot/",
    "id": 3
  }
  ```


## Get a specific article

### Request
##### `id` is an `int` >= 1

`GET /news/id`

### Response

```json
{
  "source": "Daily Mail",
  "title": "Businesses must do the right thing!",
  "link": "http://www.daily-mail.co.zm/businesses-must-do-the-right-thing/",
  "id": 1
}
```


## Get list of articles from a specific source.
##### Sources
  - Lusaka Times [`lusakatimes`]
  - Daily Mail [`dailymail`]
  - Zambian Watchdog [`zambianwatchdog`]
  - Zambian Observer [`zambianobserver`]

### Request

`GET /news/sources/lusakatimes`

### Response

```json
{
    "source": "Lusaka Times",
    "title": "Muchinga Province Minister assures people after doubt is cast over Government’s ability to implement the 2022 budget",
    "link": "https://www.lusakatimes.com/2021/11/02/muchinga-province-minister-assures-people-after-doubt-is-cast-over-governments-ability-to-implement-the-2022-budget/",
    "id": 1
  },
  {
    "source": "Lusaka Times",
    "title": "Dr. Vongo speak against use of antiseptic stuffs to clean the Vagina",
    "link": "https://www.lusakatimes.com/2021/11/02/dr-vongo-speak-against-use-of-antiseptic-stuffs-to-clean-the-vagina/",
    "id": 2
  },
  {
    "source": "Lusaka Times",
    "title": "Lafarge cement price reduction elates ZACA",
    "link": "https://www.lusakatimes.com/2021/11/02/lafarge-cement-price-reduction-elates-zaca/",
    "id": 3
  }
```

