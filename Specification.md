# qAniPlexSync Specification Document

## Project Overview

**qAniPlexSync** is a command-line tool designed to synchronize anime watchlists between AniList and Plex. It aims to provide a seamless integration for users to keep their anime viewing statuses updated across both platforms. By leveraging the AniList API and Plex's unofficial API or third-party libraries, qAniPlexSync ensures that anime fans have a consistent watchlist experience, regardless of the platform they choose to use.

## Objectives

- To fetch the user's anime watchlist from AniList.
- To search for corresponding anime titles in the user's Plex library.
- To update the watch status on Plex based on the status on AniList.
- Optional: To synchronize watch statuses from Plex back to AniList, maintaining bidirectional sync.

## Functionalities

1. **Authentication:**
   - Support OAuth for AniList to access the user's watchlist.
   - Authenticate with Plex using a user's X-Plex-Token.

2. **Watchlist Retrieval:**
   - Fetch the user's anime watchlist from AniList, including titles and watch statuses (e.g., watching, completed).

3. **Title Matching:**
   - Implement a search functionality to find matching titles in the user's Plex library.
   - Optionally, use TheTVDB or similar services for more accurate matching between AniList titles and Plex.

4. **Status Synchronization:**
   - Update the watch status of anime titles in Plex to match the corresponding status on AniList.
   - (Optional) Update AniList watch statuses based on changes in Plex, supporting bidirectional synchronization.

5. **CLI Interface:**
   - Provide a command-line interface for users to execute synchronization manually.
   - Support basic commands for authentication, syncing, and potentially configuration.

## Technical Specifications

- **Language:** Python 3.x, utilizing its rich ecosystem and libraries for API interaction and CLI development.
- **Dependencies:**
  - `python-dotenv` for loading environment variables.
  - `requests` or `graphqlclient` for API requests.
  - `argparse` for parsing command-line arguments.
  - `python-plexapi` for interacting with Plex (if applicable).
- **Platform Compatibility:** The tool should be compatible with major operating systems where Python can run, including Windows, macOS, and Linux.

## Development Milestones

1. **Project Setup:**
   - Initialize the project repository, directory structure, and virtual environment.
   - Setup `.gitignore` and `.env` for sensitive information.

2. **API Integration:**
   - Implement OAuth authentication for AniList.
   - Setup Plex authentication.
   - Develop modules for fetching and parsing data from AniList and Plex.

3. **Core Functionality:**
   - Develop the title matching logic.
   - Implement watch status synchronization from AniList to Plex.
   - (Optional) Implement reverse synchronization from Plex to AniList.

4. **CLI Development:**
   - Create a basic CLI interface for manual execution of the synchronization process.
   - Implement argument parsing for different commands (e.g., sync, configure).

5. **Testing and Debugging:**
   - Perform manual testing of all functionalities.
   - (Optional) Write automated tests for critical components.

6. **Documentation:**
   - Write a comprehensive `README.md` with setup, usage, and configuration instructions.
   - Comment code where necessary for clarity.

7. **Release:**
   - Publish the first working version of qAniPlexSync.
   - Gather feedback from initial users and plan for subsequent updates.

## Contribution Guidelines

- Contributors are encouraged to fork the repository and submit pull requests.
- All contributions should adhere to the project's coding standards and include appropriate tests (if applicable).
- Documentation updates are highly appreciated alongside code contributions.

## License

- qAniPlexSync is licensed under the GPL-3.0 license to ensure that derivatives of the work are also kept open source.
