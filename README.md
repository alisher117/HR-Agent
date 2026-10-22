# HR Agent

A simple, self-hosted tool for small companies to see who is at work, who is on leave, and whose birthday is coming up. The Telegram bot is the "agent": it posts a daily summary, takes leave requests, and answers "who's out today".

Built for small teams (5 to 50 people) in Kazakhstan and the CIS. Russian, Kazakh and English out of the box.

Status: early development. Version 1 is in progress, nothing to install yet.

## What it does

- Employee directory with CSV import and export
- Leave requests: an employee asks, their manager approves or rejects
- Today page: who is in, who is out, what's coming up (birthdays, work anniversaries, end of probation, end of contract)
- Daily summary in Telegram at a time you choose
- Notification settings per person
- Kazakhstan holiday calendar, including moved days off
- Interface in Russian, Kazakh and English

## What it does not do

Version 1 stays small on purpose.

- No clock-in/clock-out or time tracking
- No salary or payroll
- No recruiting
- No performance reviews
- No 1C integration (CSV only)

After v1: a dashboard with charts, 1C export, and asking the bot questions in plain language.

## Quick start (target for v1)

You need Docker and a Telegram bot token from @BotFather.

```
git clone https://github.com/<you>/hr-agent.git
cd hr-agent
cp .env.example .env   # add your bot token and a database password
docker compose up
```

Open http://localhost:3000. The first run creates the admin user. The demo seed adds a fake company with 25 employees so you can click around.

## Stack

Next.js, TypeScript, Prisma, Postgres, Auth.js, Zod, grammY for the Telegram bot, next-intl for translations. Runs with Docker Compose.

## Team

Alisher Maxutov: development. Azamat: desktop design. Nurdana: mobile design and Telegram messages.

## License

MIT
