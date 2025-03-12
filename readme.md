kabutogagne/README.md
Hi there 👋

# Visit https://github.com/lowlighter/metrics#-documentation for full reference
name: Metrics
on:
  # Schedule updates (each hour)
  schedule: [{cron: "0 * * * *"}]
  # Lines below let you run workflow manually and on each commit
  workflow_dispatch:
  push: {branches: ["master", "main"]}
jobs:
  github-metrics:
    runs-on: ubuntu-latest
    permissions:
      contents: write
    steps:
      - uses: lowlighter/metrics@latest
        with:
          # Your GitHub token
          # The following scopes are required:
          #  - public_access (default scope)
          #  - repo
          # The following additional scopes may be required:
          #  - read:org      (for organization related metrics)
          #  - read:user     (for user related data)
          #  - read:packages (for some packages related data)
          #  - repo          (optional, if you want to include private repositories)
          token: ${{ secrets.METRICS_TOKEN }}

          # Options
          user: <div align="center"> <img src="https://metrics.lecoq.io/sun0225SUN?template=classic
          template: classic
          base: header, repositories
          config_timezone: Asia/Shanghai
          plugin_fortune: yes
          plugin_habits: yes
          plugin_habits_charts_type: classic
          plugin_habits_days: 14
          plugin_habits_facts: yes
          plugin_habits_from: 200
          plugin_habits_languages_limit: 8
          plugin_habits_languages_threshold: 0%
          plugin_lines: yes
          plugin_lines_history_limit: 1
          plugin_lines_repositories_limit: 4
          plugin_lines_sections: base
          plugin_stargazers: yes
          plugin_stargazers_charts: yes
          plugin_stargazers_charts_type: classic
          plugin_stargazers_days: 20
          plugin_stargazers_worldmap: yes
          plugin_stars: yes
          plugin_stars_limit: 4
          plugin_steam: yes
          plugin_steam_achievements_limit: 2
          plugin_steam_games_ignored: 81
          plugin_steam_games_limit: 1
          plugin_steam_playtime_threshold: 2
          plugin_steam_recent_games_limit: 1
          plugin_steam_sections: kabutogagne, overwatch, hearthstone
          plugin_steam_user: chen1021667792
          plugin_topics: yes
          plugin_topics_limit: 15
          plugin_topics_mode: starred
          plugin_topics_sort: stars
          plugin_traffic: yes
