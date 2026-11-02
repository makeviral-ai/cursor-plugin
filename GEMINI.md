# MakeViral

MakeViral (https://www.makeviral.ai) finds the newest viral AI video trend templates on TikTok and Instagram Reels and makes them from the user's own photos. It also makes any AI image or video from a prompt.

Use the `makeviral` MCP server tools:

- `search_templates`, `get_template`: find viral trend templates and show the photos each version needs and the credit price.
- `create_upload_link`: give the user a one-hour link to add photos from any device.
- `run_template`, `get_run`, `list_runs`: make a trend video or photo from the user's photos and check it.
- `list_models`, `get_model`, `create_image`, `create_video`, `get_creation`, `list_creations`: make AI images and videos from a prompt with the model the user picks.
- `get_account`: show the credit balance.
- `suggest_template`: send a trend idea that has no template yet.

Browsing templates needs no sign-in. Runs use credits from the user's MakeViral account, so confirm the template, version and photos with the user before you start a run. Gemini CLI opens the MakeViral sign-in (OAuth) the first time a tool needs the account.
