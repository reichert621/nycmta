# nycmta

The goal of this app is to provide an easy way for New Yorkers to quickly view the upcoming trains for their "favorite" subway stations. It will use the [MTA API](https://api.mta.info/#/landing) to provide this data. It will be fairly similar to [this website](https://wheresthefuckingtrain.com/), but provide a bit more granularity.

### What problem does this solve?

This is a fairly minor annoyance, but when I'm trying to figure out when e.g. the next Q train is arriving at DeKalb station, I usually just open up Google Maps or Citymapper and enter a location to preview the route. But since I already know the route I need to take and all I care about is when the next northbound Q train is coming, I would prefer to just see that immediately.

### Goals

- I can find my favorite stations and add them to my dashboard
- I can view when certain trains will be arriving at my favorite stations
- I don't have to log in or create an account to do this
- I can view status alerts if there are delays on the routes I care about

### Technical breakdown

This will just be a simple React/NextJS/TypeScript web app with TailwindCSS for styling. It will use a Python backend (strongly borrowing from https://github.com/jonthornton/MTAPI) to handle wrapping the MTA API.

No database will be necessary, since I plan on using something like [`localStorage`](https://developer.mozilla.org/en-US/docs/Web/API/Window/localStorage) to manage each user's favorite stations.

Since this will be a NextJS app, I'll use Vercel to deploy and host it.

### Demo

https://mta-ui.vercel.app/
