Date: 19-02/-2025

Task: Developing the FundooNotes API

Progress:

Redesigned the refresh token implementation. Previously, I was storing the refresh token in the database and retrieving it when generating a new access token. While this approach worked, I felt it was not ideal. Now, I use two JWT tokens with different expiry times—a short-lived access token and a longer-lived refresh token. Instead of storing the refresh token in the database, I now validate it based on its expiry time to issue a new access token.