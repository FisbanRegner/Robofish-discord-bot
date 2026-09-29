# RoboFish Command Documentation

Generated from the current uploaded RoboFish source. This document covers commands located under `Commands/GlobalSlashCommands/` and `Commands/prefixCommands/`.

## Command Counts

- Global slash/chat-input commands: **36**
- Global message context commands: **2**
- Prefix commands: **3**
- Total documented command files: **41**

## Slash Command Option Types

- `String` = typed text
- `Integer` = whole number
- `Boolean` = true/false toggle
- `User` = Discord user selector
- `Channel` = Discord channel selector
- `Role` = Discord role selector
- `Attachment` = uploaded file
- `Subcommand` / `Subcommand Group` = nested slash command actions

## Quick Index

### Global Slash / Application Commands

| Category | Command | Description |
|---|---|---|
| Admin | `/prefix` | Change the command Prefix. |
| Admin | `/setavatar` | Set the bot's avatar (for authorized user only) |
| Admin | `/setup` | RoboFish setup |
| Bugreports | `/bug` | Submits a bug report. |
| ContextCommands | `approve suggestion` | context menu command for approve suggestion. |
| ContextCommands | `deny suggestion` | context menu command for deny suggestion. |
| Dev | `/convert` | RoboFish setup |
| Dev | `/findguild` | RoboFish setup |
| Dev | `/rolelist` | list current roles in the guild. **depreciated** |
| Fun | `/8ball` | Tells you a fortune |
| Fun | `/fliptext` | flips your message. |
| Fun | `/clap` | Add clap emoji between each word. |
| Fun | `/dab` | Adds dab emoji after each word. |
| Fun | `/dadjoke` | Sends a random joke |
| Fun | `/fact` | Sends a random fact. |
| Fun | `/hack` | Another Fun Command. |
| Fun | `/reverse` | Flips your message. |
| Games | `/counting` | Config Command for Counting game |
| Games | `/counting_wars` | Config Command for Counting wars game |
| Games | `/fourletterword` | Config Command for Four Letter Word game |
| Games | `/onewordstory` | config for one-word story game. |
| Info | `/help` | Help file for commands. |
| Info | `/invite` | Get RoboFish's invite link. |
| Info | `/ping` | Check RoboFish's ping. |
| Moderation | `/role` | Manage roles of the server or members. |
| RoleMenus | `/embed_sample` | Show a sample embed with labeled customizable sections |
| RoleMenus | `/role_menu` | Create, edit, or delete self-assign role menus. |
| Suggestions | `/approve` | Marks a suggestion as approved. |
| Suggestions | `/configbroken` | RoboFish old setup setup |
| Suggestions | `/consider` | Marks a suggestion as considered. |
| Suggestions | `/deny` | Marks a suggestion as denied. |
| Suggestions | `/implemented` | Marks a suggestion as implemented. |
| Suggestions | `/suggest` | Suggest <something>. |
| Suggestions | `/suggestions` | Suggestions admin command. |
| Suggestions | `/vote` | Adds voting reactions to a suggestion. |
| Utility | `/add_word` | Add a word to the list of four-letter words. |
| Utility | `/avatar` | Display user's avatar |
| Utility | `/stickyroles` | RoboFish setup 2 |

### Prefix Commands

| Category | Command | Description |
|---|---|---|
| Admin | `say` | Have the RoboFish say something! guild admin use only. |
| Info | `invite` | Get the bot's invite link |
| Info | `ping` | Check bot's ping. |

## Global Slash and Application Commands

### Admin

#### `/prefix`

- **File:** `Commands/GlobalSlashCommands/Admin/prefix.js`
- **Type:** Slash command
- **Description:** Change the command Prefix.
- **Help text:** allows you to set a new prefix for prefix commands.
- **Syntax:** `/prefix <prefix>`
- **Cooldown:** `3000` ms
- **User permissions:** `Administrator`
- **Bot permissions:** None listed
- **Notes:** Changes the guild prefix used by prefix commands. This does not affect slash commands.
- **Options:**
  - `prefix` — **String**, required. New prefix

#### `/setavatar`

- **File:** `Commands/GlobalSlashCommands/Admin/setavatar.js`
- **Type:** Slash command
- **Description:** Set the bot's avatar (for authorized user only)
- **Syntax:**
  - `/setavatar <image>`
- **User permissions:** None listed
- **Bot permissions:** None listed
- **Notes:** Owner-only command. Upload an image attachment to set RoboFish's avatar. Validates common image MIME types.
- **Options:**
  - `image` — **Attachment**, required. Upload an image to set as the bot's avatar.

#### `/setup`

- **File:** `Commands/GlobalSlashCommands/Admin/setup.js`
- **Type:** Slash command
- **Description:** RoboFish setup
- **Help text:** Usage: /config Follow prompts to setup suggestions.
- **Syntax:**
  - `/setup`
- **User permissions:** `ManageGuild`
- **Bot permissions:** `ManageGuild`
- **Notes:** Starts the interactive RoboFish setup panel using buttons/select menus. Requires guild management permissions.
- **Options:** None

### Bugreports

#### `/bug`

- **File:** `Commands/GlobalSlashCommands/Bugreports/bug.js`
- **Type:** Slash command
- **Description:** Submits a bug report.
- **Help text:** Submits a bug report. be sure to include the command if any, the bug, and all steps needed to recreate it.
- **Syntax:** `Usage: /bug <command name> <the bug> <how to recreate>`
- **User permissions:** None listed
- **Bot permissions:** None listed
- **Notes:** Sends a bug report to the configured bug-report system/channel. Users should include the command, what went wrong, and steps to recreate the issue.
- **Options:**
  - `bugreport` — **String**, required. New bugreport

### ContextCommands

#### `approve suggestion`

- **File:** `Commands/GlobalSlashCommands/ContextCommands/approveContext.js`
- **Type:** Message context command
- **Help text:** context menu command for approve suggestion.
- **Syntax:** Message context command; use Discord’s message context menu / Apps menu on a message.
- **User permissions:** `ManageGuild`
- **Bot permissions:** None listed
- **Notes:** Message context command. Right-click/use Apps on a saved suggestion message to approve it with an optional comment.
- **Options:** None

#### `deny suggestion`

- **File:** `Commands/GlobalSlashCommands/ContextCommands/denyContext.js`
- **Type:** Message context command
- **Help text:** context menu command for deny suggestion.
- **Syntax:** Message context command; use Discord’s message context menu / Apps menu on a message.
- **User permissions:** `ManageGuild`
- **Bot permissions:** None listed
- **Notes:** Message context command. Right-click/use Apps on a saved suggestion message to deny it with an optional reason.
- **Options:** None

### Dev

#### `/convert`

- **File:** `Commands/GlobalSlashCommands/Dev/convert.js`
- **Type:** Slash command
- **Description:** RoboFish setup
- **Help text:** used by owner
- **Syntax:**
  - `/convert`
- **User permissions:** None listed
- **Bot permissions:** None listed
- **Notes:** Developer/owner utility command. The source marks this as owner-use.
- **Options:** None

#### `/findguild`

- **File:** `Commands/GlobalSlashCommands/Dev/findguild.js`
- **Type:** Slash command
- **Description:** RoboFish setup
- **Help text:** used by owner
- **Syntax:**
  - `/findguild`
- **User permissions:** None listed
- **Bot permissions:** None listed
- **Notes:** Developer/owner utility command. The source marks this as owner-use.
- **Options:** None

#### `/rolelist`

- **File:** `Commands/GlobalSlashCommands/Dev/rolelist.js`
- **Type:** Slash command
- **Description:** list current roles in the guild. **depreciated**
- **Help text:** /rolelist
- **Syntax:**
  - `/rolelist`
- **User permissions:** `ManageRoles`
- **Bot permissions:** `ManageRoles`
- **Notes:** Deprecated role listing utility. Kept in the Dev folder.
- **Options:** None

### Fun

#### `/8ball`

- **File:** `Commands/GlobalSlashCommands/Fun/8ball.js`
- **Type:** Slash command
- **Description:** Tells you a fortune
- **Help text:** Different from normal 8bal responses.
- **Syntax:** `/8ball <question>`
- **User permissions:** None listed
- **Bot permissions:** None listed
- **Notes:** Replies with a magic-8-ball style answer to the supplied question.
- **Options:**
  - `question` — **String**, required. The question you want to ask the magic 8ball

#### `/fliptext`

- **File:** `Commands/GlobalSlashCommands/Fun/Fliptext.js`
- **Type:** Slash command
- **Description:** flips your message.
- **Help text:** flips your message. ǝƃɐssǝɯ ldɯɐs ɐ sᴉ sᴉɥʇ
- **Syntax:** `/fliptext <message>`
- **User permissions:** None listed
- **Bot permissions:** None listed
- **Notes:** Transforms the supplied text into upside-down/flipped text.
- **Options:**
  - `message` — **String**, required. Usage: /fliptext <message>

#### `/clap`

- **File:** `Commands/GlobalSlashCommands/Fun/clap.js`
- **Type:** Slash command
- **Description:** Add clap emoji between each word.
- **Help text:** Add clap emoji between each word. This 👏 is 👏 a 👏 sample 👏 message.
- **Syntax:** `/clap <message>`
- **User permissions:** None listed
- **Bot permissions:** None listed
- **Notes:** Adds clap emoji between words in the supplied message.
- **Options:**
  - `message` — **String**, required. Usage: /clap <message>

#### `/dab`

- **File:** `Commands/GlobalSlashCommands/Fun/dab.js`
- **Type:** Slash command
- **Description:** Adds dab emoji after each word.
- **Help text:** Adds dab emoji after each word. This <a:emoji_9:726786422866182186> is <a:emoji_9:726786422866182186> a <a:emoji_9:726786422866182186> sample <a:emoji_9:726786422866182186> message.
- **Syntax:** `/dab <message>`
- **User permissions:** None listed
- **Bot permissions:** `UseExternalEmojis`
- **Notes:** Adds the configured dab emoji after words in the supplied message. Requires external emoji permission when using external animated emoji.
- **Options:**
  - `message` — **String**, required. Usage: /dab <message>

#### `/dadjoke`

- **File:** `Commands/GlobalSlashCommands/Fun/dadjoke.js`
- **Type:** Slash command
- **Description:** Sends a random joke
- **Help text:** pick a random joke from over 400 jokes.
- **Syntax:** `/dadjoke`
- **User permissions:** None listed
- **Bot permissions:** None listed
- **Notes:** Replies with a random dad joke from RoboFish data.
- **Options:** None

#### `/fact`

- **File:** `Commands/GlobalSlashCommands/Fun/fact.js`
- **Type:** Slash command
- **Description:** Sends a random fact.
- **Help text:** Sends a random fact from over 400 facts.
- **Syntax:** `/fact`
- **Cooldown:** `300000` ms
- **User permissions:** None listed
- **Bot permissions:** None listed
- **Notes:** Replies with a random fact. The command file has a longer cooldown than most fun commands.
- **Options:** None

#### `/hack`

- **File:** `Commands/GlobalSlashCommands/Fun/hack.js`
- **Type:** Slash command
- **Description:** Another Fun Command.
- **Help text:** Fake hacking command.
- **Syntax:** `/hack <User>`
- **User permissions:** None listed
- **Bot permissions:** None listed
- **Notes:** Runs a fake hacking animation/message for the selected user.
- **Options:**
  - `user` — **User**, required. The User you want to hack

#### `/reverse`

- **File:** `Commands/GlobalSlashCommands/Fun/reversetext.js`
- **Type:** Slash command
- **Description:** Flips your message.
- **Help text:** flips your message. ǝƃɐssǝɯ ldɯɐs ɐ sᴉ sᴉɥʇ
- **Syntax:** `/reverse <message>`
- **User permissions:** None listed
- **Bot permissions:** None listed
- **Notes:** Reverses/flips the supplied message text.
- **Options:**
  - `message` — **String**, required. Usage: /reverse <message>

### Games

#### `/counting`

- **File:** `Commands/GlobalSlashCommands/Games/counting.js`
- **Type:** Slash command
- **Description:** Config Command for Counting game
- **Help text:** use this command to setup the counting game in a specified channel.
- **Syntax:** `/counting`
- **User permissions:** `ManageChannels`
- **Bot permissions:** None listed
- **Notes:** Starts or configures the Counting game setup flow for a selected channel.
- **Options:** None

#### `/counting_wars`

- **File:** `Commands/GlobalSlashCommands/Games/countingWars.js`
- **Type:** Slash command
- **Description:** Config Command for Counting wars game
- **Help text:** use this command to setup the Counting wars game in a specified channel.
- **Syntax:** `/counting_wars`
- **User permissions:** `ManageChannels`
- **Bot permissions:** None listed
- **Notes:** Starts or configures the Counting Wars game setup flow for a selected channel.
- **Options:** None

#### `/fourletterword`

- **File:** `Commands/GlobalSlashCommands/Games/fourLetterWord.js`
- **Type:** Slash command
- **Description:** Config Command for Four Letter Word game
- **Help text:** use this command to setup the Four Letter Word game in a specified channel.
- **Syntax:** `/fourletterword`
- **User permissions:** `ManageChannels`
- **Bot permissions:** None listed
- **Notes:** Starts or configures the Four Letter Word game setup flow for a selected channel.
- **Options:** None

#### `/onewordstory`

- **File:** `Commands/GlobalSlashCommands/Games/oneWordStory.js`
- **Type:** Slash command
- **Description:** config for one-word story game.
- **Help text:** use this command to setup one word stories in a specified channel.
- **Syntax:** `/onewordstory`
- **User permissions:** `ManageChannels`
- **Bot permissions:** None listed
- **Notes:** Starts or configures the One Word Story game setup flow for a selected channel.
- **Options:** None

### Info

#### `/help`

- **File:** `Commands/GlobalSlashCommands/Info/help.js`
- **Type:** Slash command
- **Description:** Help file for commands.
- **Help text:** Help file for commands or command.
- **Syntax:** `/help or /help <command> with out the prefix or /`
- **User permissions:** None listed
- **Bot permissions:** None listed
- **Notes:** Shows help for commands. Can be used without arguments for general help or with a command name for command-specific help.
- **Options:**
  - `command` — **String**, optional. additional help for a command

#### `/invite`

- **File:** `Commands/GlobalSlashCommands/Info/invite.js`
- **Type:** Slash command
- **Description:** Get RoboFish's invite link.
- **Help text:** Usage: /invite or <prefix>invite shows the invite url for RoboFish.
- **Syntax:**
  - `/invite`
- **Cooldown:** `3000` ms
- **User permissions:** None listed
- **Bot permissions:** None listed
- **Notes:** Shows RoboFish's invite link.
- **Options:** None

#### `/ping`

- **File:** `Commands/GlobalSlashCommands/Info/ping.js`
- **Type:** Slash command
- **Description:** Check RoboFish's ping.
- **Help text:** ping returns the Ping in ms.
- **Syntax:** `/ping or <prefix>.`
- **Cooldown:** `3000` ms
- **User permissions:** None listed
- **Bot permissions:** None listed
- **Notes:** Shows RoboFish latency/ping.
- **Options:** None

### Moderation

#### `/role`

- **File:** `Commands/GlobalSlashCommands/Moderation/role.js`
- **Type:** Slash command
- **Description:** Manage roles of the server or members.
- **Help text:** Add a role to a user.
- **Syntax:** `/role add <role> <user> or /role remove <role> <user>`
- **Cooldown:** `3000` ms
- **User permissions:** `ManageRoles`
- **Bot permissions:** `ManageRoles`
- **Notes:** Adds roles to users. The current slash payload exposes the add subcommand in the uploaded code.
- **Options:**
  - `add` — **Subcommand**, required. Add role to a user.
    - `role` — **Role**, required. The role you want to add to the user.
    - `user` — **User**, required. The user you want to add role to.

### RoleMenus

#### `/embed_sample`

- **File:** `Commands/GlobalSlashCommands/RoleMenus/embedSample.js`
- **Type:** Slash command
- **Description:** Show a sample embed with labeled customizable sections
- **Syntax:**
  - `/embed_sample`
- **User permissions:** None listed
- **Bot permissions:** None listed
- **Notes:** Shows a sample embed with labeled/customizable sections for Role Menu/embed design work.
- **Options:** None

#### `/role_menu`

- **File:** `Commands/GlobalSlashCommands/RoleMenus/roleMenu.js`
- **Type:** Slash command
- **Description:** Create, edit, or delete self-assign role menus.
- **Help text:** Opens the role-menu manager.
- **Syntax:** `/role_menu`
- **User permissions:** `ManageGuild`
- **Bot permissions:** `ManageGuild`
- **Notes:** Opens the Role Menu manager for creating, editing, or deleting self-assign role menus.
- **Options:** None

### Suggestions

#### `/approve`

- **File:** `Commands/GlobalSlashCommands/Suggestions/approve.js`
- **Type:** Slash command
- **Description:** Marks a suggestion as approved.
- **Help text:** Usage: /approve <suggestion#> Opens a comment modal and marks a suggestion as approved.
- **Syntax:**
  - `/approve <suggestionid>`
- **User permissions:** `ManageGuild`
- **Bot permissions:** `ManageGuild`
- **Notes:** Marks a suggestion as approved and opens a comment modal.
- **Options:**
  - `suggestionid` — **Integer**, required. Suggestion id#

#### `/configbroken`

- **File:** `Commands/GlobalSlashCommands/Suggestions/configold.js`
- **Type:** Slash command
- **Description:** RoboFish old setup setup
- **Help text:** Usage: /config Follow prompts to setup suggestions.
- **Syntax:**
  - `/configbroken`
- **User permissions:** `ManageGuild`
- **Bot permissions:** `ManageGuild`
- **Notes:** Old/broken suggestions config command retained in the source. Prefer the current setup/suggestions flows.
- **Options:** None

#### `/consider`

- **File:** `Commands/GlobalSlashCommands/Suggestions/consider.js`
- **Type:** Slash command
- **Description:** Marks a suggestion as considered.
- **Help text:** Usage: /consider <suggestion#> Opens a comment modal and marks a suggestion as considered.
- **Syntax:**
  - `/consider <suggestionid>`
- **User permissions:** `ManageGuild`
- **Bot permissions:** `ManageGuild`
- **Notes:** Marks a suggestion as considered and opens a comment modal.
- **Options:**
  - `suggestionid` — **Integer**, required. Suggestion id#

#### `/deny`

- **File:** `Commands/GlobalSlashCommands/Suggestions/deny.js`
- **Type:** Slash command
- **Description:** Marks a suggestion as denied.
- **Help text:** Usage: /deny <suggestion#> Opens a reason modal and marks a suggestion as denied.
- **Syntax:**
  - `/deny <suggestionid>`
- **User permissions:** `ManageGuild`
- **Bot permissions:** `ManageGuild`
- **Notes:** Marks a suggestion as denied and opens a reason/comment modal.
- **Options:**
  - `suggestionid` — **Integer**, required. Suggestion id#

#### `/implemented`

- **File:** `Commands/GlobalSlashCommands/Suggestions/implemented.js`
- **Type:** Slash command
- **Description:** Marks a suggestion as implemented.
- **Help text:** Usage: /implemented <suggestion#> Opens a comment modal and marks a suggestion as implemented.
- **Syntax:**
  - `/implemented <suggestionid>`
- **User permissions:** `ManageGuild`
- **Bot permissions:** `ManageGuild`
- **Notes:** Marks a suggestion as implemented and opens a comment modal.
- **Options:**
  - `suggestionid` — **Integer**, required. Suggestion id#

#### `/suggest`

- **File:** `Commands/GlobalSlashCommands/Suggestions/suggest.js`
- **Type:** Slash command
- **Description:** Suggest <something>.
- **Help text:** Usage: /suggest <suggestion> Creates a new suggestion.
- **Syntax:**
  - `/suggest <suggestion>`
- **User permissions:** None listed
- **Bot permissions:** `ManageMessages`
- **Notes:** Creates a new suggestion in the configured suggestions channel.
- **Options:**
  - `suggestion` — **String**, required. New suggestion

#### `/suggestions`

- **File:** `Commands/GlobalSlashCommands/Suggestions/suggestions.js`
- **Type:** Slash command
- **Description:** Suggestions admin command.
- **Help text:** Usage: /suggestions help help file for suggestions, /suggestions is used to set up suggestions channels and options, however it is recommended you run /config for quick setup
- **Syntax:**
  - `/suggestions channel suggestions <channel>`
  - `/suggestions channel decision <channel>`
  - `/suggestions userrole <userrole>`
  - `/suggestions adminrole <adminrole>`
  - `/suggestions voting <enabled>`
  - `/suggestions help`
  - `/suggestions anonymous <enabled>`
  - `/suggestions dm <enabled>`
  - `/suggestions moveondecision <enabled>`
  - `/suggestions enabled <enabled>`
- **User permissions:** `ManageGuild`
- **Bot permissions:** `ManageGuild`
- **Notes:** Admin command for suggestion settings, including channels and toggles such as voting, anonymous, DMs, move-on-decision, and enabled state.
- **Options:**
  - `channel` — **Subcommand Group**, required. channel settings for suggestions
    - `suggestions` — **Subcommand**, required. Channel for new suggestions.
      - `channel` — **Channel**, required. Select a channel for suggestions
    - `decision` — **Subcommand**, required. Decision channel
      - `channel` — **Channel**, required. Channel to move suggestions to after a decision is made.
  - `userrole` — **Subcommand**, required. Not used yet
    - `userrole` — **User**, required. /Suggest user Role
  - `adminrole` — **Subcommand**, required. Role for admin settings(not used yet)
    - `adminrole` — **User**, required. Suggestion admin role
  - `voting` — **Subcommand**, required. turn on and off suggestion vote reactions
    - `enabled` — **Boolean**, required. Turn suggestion voting on by default?
  - `help` — **Subcommand**, optional. Help for suggestions commands
  - `anonymous` — **Subcommand**, required. Turn on anonymous suggestions.
    - `enabled` — **Boolean**, required. Turn on anonymous suggestions.
  - `dm` — **Subcommand**, required. Toggles between sending the person who suggested something upon a decision.
    - `enabled` — **Boolean**, required. turn on decision DM's
  - `moveondecision` — **Subcommand**, required. Toggles between moving suggestions that admins have approved/denied.
    - `enabled` — **Boolean**, required. enable suggestion moving.
  - `enabled` — **Subcommand**, required. allows you to enable or disabled suggestions.
    - `enabled` — **Boolean**, required. Enable suggestions, make sure to select a suggestions channel!

#### `/vote`

- **File:** `Commands/GlobalSlashCommands/Suggestions/vote.js`
- **Type:** Slash command
- **Description:** Adds voting reactions to a suggestion.
- **Help text:** Usage: /vote <suggestion#> Opens a suggestion for voting.
- **Syntax:**
  - `/vote <suggestionid>`
- **User permissions:** `ManageGuild`
- **Bot permissions:** `ManageMessages`
- **Notes:** Adds voting reactions to an eligible suggestion and opens it for voting.
- **Options:**
  - `suggestionid` — **Integer**, required. Suggestion id#

### Utility

#### `/add_word`

- **File:** `Commands/GlobalSlashCommands/Utility/add_word.js`
- **Type:** Slash command
- **Description:** Add a word to the list of four-letter words.
- **Syntax:**
  - `/add_word <word>`
- **User permissions:** `ManageGuild`
- **Bot permissions:** None listed
- **Notes:** Owner-only utility in code; adds a new four-letter word to the Four Letter Word word list after validation.
- **Options:**
  - `word` — **String**, required. The word to add to the list.

#### `/avatar`

- **File:** `Commands/GlobalSlashCommands/Utility/avatar.js`
- **Type:** Slash command
- **Description:** Display user's avatar
- **Help text:** display the avatar of select user.
- **Syntax:** `Usage: /avatar <user> displays a users avatar.`
- **Cooldown:** `3000` ms
- **User permissions:** None listed
- **Bot permissions:** None listed
- **Notes:** Shows a user's avatar and adds buttons for available image formats.
- **Options:**
  - `user` — **User**, optional. The avatar of the user you want to display.

#### `/stickyroles`

- **File:** `Commands/GlobalSlashCommands/Utility/stickyRoles.js`
- **Type:** Slash command
- **Description:** RoboFish setup 2
- **Help text:** sets the status of sticky roles. enabled member Roles don't reset when leaving and rejoining guild.
- **Syntax:** `/stickyroles`
- **User permissions:** `ManageRoles`
- **Bot permissions:** `ManageRoles`
- **Notes:** Opens a setup selector for Sticky Roles, which controls whether members keep roles after leaving and rejoining.
- **Options:** None

## Prefix Commands

### Admin

#### `say`

- **File:** `Commands/prefixCommands/Admin/say.js`
- **Type:** Prefix command
- **Description:** Have the RoboFish say something! guild admin use only.
- **Help text:** have RoboFish say something! guild admin use only.
- **Syntax:** `!say <message>`
- **Cooldown:** `3000` ms
- **User permissions:** None listed
- **Bot permissions:** None listed
- **Notes:** Prefix admin command. Deletes the user's message and makes RoboFish repeat the provided message.
- **Options:** None

### Info

#### `invite`

- **File:** `Commands/prefixCommands/Info/invite.js`
- **Type:** Prefix command
- **Description:** Get the bot's invite link
- **Syntax:** `<prefix>invite`
- **Cooldown:** `3000` ms
- **User permissions:** `Administrator`
- **Bot permissions:** `Administrator`
- **Notes:** Shows RoboFish's invite link.
- **Options:** None

#### `ping`

- **File:** `Commands/prefixCommands/Info/ping.js`
- **Type:** Prefix command
- **Description:** Check bot's ping.
- **Syntax:** `<prefix>ping`
- **Cooldown:** `3000` ms
- **User permissions:** None listed
- **Bot permissions:** None listed
- **Notes:** Shows RoboFish latency/ping.
- **Options:** None

## Expanded Notes: `/suggestions` Admin Command

`/suggestions` is a grouped admin command for configuring the suggestion system. The uploaded slash payload includes these actions:

- `channel` — channel settings for suggestions
  - `channel suggestions` — Channel for new suggestions.
    - `channel`: Channel, required — Select a channel for suggestions
  - `channel decision` — Decision channel
    - `channel`: Channel, required — Channel to move suggestions to after a decision is made.
- `userrole` — Not used yet
  - `userrole`: User, required — /Suggest user Role
- `adminrole` — Role for admin settings(not used yet)
  - `adminrole`: User, required — Suggestion admin role
- `voting` — turn on and off suggestion vote reactions
  - `enabled`: Boolean, required — Turn suggestion voting on by default?
- `help` — Help for suggestions commands
- `anonymous` — Turn on anonymous suggestions.
  - `enabled`: Boolean, required — Turn on anonymous suggestions.
- `dm` — Toggles between sending the person who suggested something upon a decision.
  - `enabled`: Boolean, required — turn on decision DM's
- `moveondecision` — Toggles between moving suggestions that admins have approved/denied.
  - `enabled`: Boolean, required — enable suggestion moving.
- `enabled` — allows you to enable or disabled suggestions.
  - `enabled`: Boolean, required — Enable suggestions, make sure to select a suggestions channel!

## Maintenance Notes

- Some commands in `Dev` or with owner checks are intended for bot-owner/testing use only.
- `configbroken` is documented because it exists in the uploaded GlobalSlashCommands folder, but the name indicates it should not be the preferred configuration command.
- Prefix command syntax uses the guild prefix. Your default/example prefix has historically been `!`, but `/prefix` can change it per guild.
- This documentation reflects the command metadata in the uploaded source; if command behavior changes inside `run()`, update this file together with the command.