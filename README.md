- 👋 Hi, I’m @M-Tm
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...

<!---
M-Tm/M-Tm is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
on:
  pull_request: {branches: master}
  push: {branches: master}

jobs:
  test:
    runs-on: ubuntu-latest
    name: Run a Refactr Job
    steps:
      - uses: actions/checkout@v2
      - uses: refactr/action-run-pipeline@master
        with:
          project_id: <project-id>
          job_id: <job-id>
          api_token: ${{ secrets.REFACTR_API_TOKEN }}
          variables: '{ "my_var": "value" }'
