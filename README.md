# DHIS2 GitHub Action Metrics

I started this project to analyze the test workflow we use at
[DHIS2](https://dhis2.org/about/). I wanted to know where time was spent, why
some test runs took 15min while others took 23min to finish. How could we get
faster feedback on PRs and reduce this variation in test duration?

Using [GitHub action metrics](https://github.com/teleivo/github-action-metrics)
I

- fetch(ed) [GitHub action data](https://docs.github.com/en/rest/reference/actions) every day using
  [a scheduled GitHub action](./.github/workflows/fetch_actions.yml). The data is
  then stored in this repository. This way I can accumulate a history of our
  workflow runs.
- indexed and analyzed the data using Elasticsearch and Kibana
