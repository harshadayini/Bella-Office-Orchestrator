# Business Process Automation Platform

A Streamlit-based application that automates various business processes including PR reviews, CI/CD deployments, release notes generation, and data refresh operations.

## Features

1. **PR Reviewer Round-Robin**
   - Automatically assigns PR reviewers based on team roster
   - Ensures fair load balancing
   - Sends notifications via Slack
   - Tracks review history

2. **CI/CD Auto-Deploy**
   - Monitors GitHub Actions
   - Automatically deploys to staging/production
   - Handles rollbacks
   - Provides deployment status updates

3. **Release Notes Generator**
   - Fetches merged PRs since last release
   - Uses AI to categorize changes
   - Posts formatted changelog to Slack
   - Maintains release history

4. **Data Refresh & Dependency Check**
   - Hourly HubSpot data refresh
   - Weekly dependency checks
   - Vulnerability scanning
   - Automated Jira ticket creation

## Setup

1. Clone the repository:
   ```bash
   git clone <repository-url>
   cd <repository-name>
   ```

2. Create a virtual environment:
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

4. Create a `.env` file with the following variables:
   ```
   # OpenAI Configuration
   OPENAI_API_KEY=your_openai_api_key

   # GitHub Configuration
   GITHUB_TOKEN=your_github_token
   GITHUB_REPO=your_repo_name
   GITHUB_OWNER=your_github_username

   # Slack Configuration
   SLACK_BOT_TOKEN=your_slack_bot_token
   SLACK_CHANNEL_ID=your_channel_id

   # AWS Configuration
   AWS_ACCESS_KEY_ID=your_aws_access_key
   AWS_SECRET_ACCESS_KEY=your_aws_secret_key
   AWS_REGION=your_aws_region
   S3_BUCKET=your_bucket_name

   # HubSpot Configuration
   HUBSPOT_API_KEY=your_hubspot_api_key

   # Jira Configuration
   JIRA_API_TOKEN=your_jira_token
   JIRA_EMAIL=your_jira_email
   JIRA_URL=your_jira_url
   ```

5. Run the application:
   ```bash
   streamlit run app.py
   ```

## Usage

1. **PR Reviewer**
   - Add team members in the interface
   - Enter PR number and author
   - System will automatically assign reviewers

2. **CI/CD Deployer**
   - Monitor deployment status
   - Trigger manual deployments
   - Handle rollbacks if needed

3. **Release Notes**
   - Generate release notes for new versions
   - View previous releases
   - Get AI-categorized changes

4. **Data Refresh**
   - Trigger manual data refresh
   - Check dependency updates
   - View refresh history

## Contributing

1. Fork the repository
2. Create a feature branch
3. Commit your changes
4. Push to the branch
5. Create a Pull Request

## License

This project is licensed under the MIT License - see the LICENSE file for details. 