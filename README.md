# <a href="https://www.givingback.ai" target="_blank"><img src="https://givingback.ai/assets/gblogo.72c0863b.svg"  align="center" height="48" width="48" style="background-color: black;"></a>  GivingbackAI - OpenSourceNepal Blogs
> <div style="background-color: #; border: 1px solid red; padding: 10px; font-weight: bold;">The following content is a property of GivingbackAI.</div>
> <div style="background-color: #; border: 1px solid red; padding: 10px; font-weight: bold;"> Released Under MIT License.</div>

- Audience: Engineers at GivingbackAI.
- Date (YYYY/MM/DD): 2023/08/09
- Version: v1.0.1
---

## OpenSourceNepal Blogs

### Nepali DateTime API

- Problem Statement:
  - Nepal run in [Bikram Sambat](https://en.wikipedia.org/wiki/Vikram_Samvat) calendar.
  - Bikram Sambat calendar is 56 years ahead  of [Gregorian Calendar](https://en.wikipedia.org/wiki/Gregorian_calendar#:~:text=16%20External%20links-,Description,February%20in%20the%20leap%20years.)
  - The number of days in each month in an ascending order does not match to the number of days in the corresponding month of the Gregorian calendar.
For example:
```
Today's date in A.D : 08/16/2023 (June 16th, 2023)
Today's date in B.S : 04/32/2080  (Shrawan 32, 2080)
```
- Simply adding or subtracting number of years or days to correctly represent another calendar does not work.
- In above example, if we consider 04/32/2080 to be an A.D date still representing as `datetime` object, it won't work as it represents April 32 in A.D. calendar. There's no 32nd day in the month of April.
  - Due to this reason, popular datetime libraries such as `datetime` does not represent a Bikram Sambat calendar.

- Solution:
  - [OpenSourceNepal API](https://www.opensourcenepal.com/) provides off the shelf solution to this problem.
  - Simply call the `/api/nepalidatetime` API to get the real-time date and time including *tithi* for Bikram Sambat Calendar.
