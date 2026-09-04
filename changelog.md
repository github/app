# Changelog

## v1.1.15

### Highlights

- Added a `/goal` command to set a persistent objective for autopilot to work towards in local sessions.
- Editing and saving files, including whole-file diff changes, now works in WSL, Direct, and Mission Control workspaces, with conflict detection.
- You can now attach images and videos to pull request descriptions by pasting, dragging, or selecting files.
- You can now install MCP servers via a deep link, which opens a prefilled review form for confirmation before adding the server.
- Added a Power BI MCP server to the connector catalog, supporting both a hosted remote connection and a local server option.

### Added

- Added a "Show in Finder"/"Show in Explorer" action for local chat session paths in the session header menu.
- Added a `/goal` command to set a persistent objective for autopilot to work towards in local sessions.
- Added a None option for session complete and needs-input sounds, so each can be muted independently.
- Added a Pinned filter and column to Manage sessions, so you can find, review, and safely bulk-delete pinned sessions.
- Added a Power BI MCP server to the connector catalog, supporting both a hosted remote connection and a local server option.
- Added a remappable keyboard shortcut to start screenshot capture in the browser preview, and updated the Pick & Polish tooltip to show both the shortcut and the Shift-click gesture.
- Added a right-click context menu to the prompt composer with paste, paste without formatting, and a toggle to view or edit the raw text of your prompt.
- Added a way to resume a session by pasting its session ID into Quick Open or via the sidebar's new menu.
- Added an inline archive action to custom sidebar groups that contain merged or closed pull request sessions.
- Added Azure CLI authentication as an option for Microsoft Foundry model providers, letting you connect using your existing `az login` session instead of an API key.
- Assistant messages can now include links to other sessions, letting you navigate directly between related sessions.
- Attach images and videos to pull request descriptions by pasting, dragging, or selecting files, alongside the existing link action.
- Code review agents now let you configure reasoning effort in addition to the model.
- Editing and saving files, including whole-file diff changes, now works in WSL, Direct, and Mission Control workspaces, with conflict detection if a file changes remotely before you save.
- Featured extension, skill, and MCP sections now show a looping carousel with chevron and keyboard navigation when more than three items are available.
- Pasting a GitHub issue or pull request URL into the relation picker (sub-issues, blocking/blocked-by, linked issues, and linked PRs) now switches to that repository and surfaces the matching item ready to select.
- Pull request numbers in the merge stack card now open in your browser, and a copy-link button appears on hover or keyboard focus.
- Selecting text in a pull request or issue description now offers Quote and Add to Side chat actions when viewing it in a chat session, in addition to Copy.
- Session IDs shown in Chronicle results are now clickable, letting you open or resume that session directly.
- Shift-click the Pick & Polish button to jump straight into screenshot selection, which stays active after you release Shift.
- Show before/after image previews for changed PNG, JPG, and SVG files in the diff view
- The composer's "+" menu now lists project files/folders, issues/PRs, and sessions as quick-insert shortcuts alongside the file attachment options.
- The pull request stack menu and merge drawer now show the stack's number (e.g. "Stack #123") alongside its position.
- You can now install MCP servers via a deep link, which opens a prefilled review form for confirmation before adding the server.
- You can now jump to or create a session for another pull request in a stack directly from the merge box.
- You can now open a `session/new` link with an `issue` parameter to create an issue-linked session directly.
- You can now view schedule details and cancel a scheduled automation directly from its pill in the composer.

### Changed

- Agents can now create new top-level sessions directly instead of always nesting them under the current session.
- Clicking a commit in the commits menu now selects only that commit; hold Shift and click to select a range of commits.
- Conversation transcripts that load after the initial paint now fade in smoothly instead of appearing abruptly.
- Conversation views now default to Balanced verbosity, which groups settled tool calls into a collapsible panel while keeping active tool work visible.
- Deep links now show a clear error message with a way to view details and copy the error when the link's target can't be found or an action from the link fails.
- Improved accessibility of required fields in workflow forms, with clearer screen reader announcements and more consistent required-field labeling.
- Landmark navigation (F6 / Shift+F6) now shows a visible focus indicator when it moves between the sidebar, main content, and view header, and appears in the keyboard shortcuts dialog and Settings > Accessibility.
- Made the enable/disable toggle switches in the Customize lists more compact.
- Made the feedback input in the plan review composer more compact and kept the model picker available while reviewing a plan.
- Markdown source mode now uses a code editor with line numbers and syntax highlighting.
- Moved the Azure DevOps MCP server to the Development category in the MCP catalog.
- Redesigned the Environments settings page to show a single deduplicated list of connected and available environments, keep stopped WSL environments visible and connectable, and collapse long offline environment history.
- Refined My Work list rows at narrow widths to keep the title and status readable, with author or assignee avatars shown in a trailing column.
- Removed the single-key "R" retry shortcut on the onboarding repositories error screen and announced the load error to screen readers.
- Renamed remaining "Quick Chat" labels to "Chat" in the tray menu, sidebar, and Accessibility settings.
- Renamed the "Extensions" submenu in the right sidebar's add-tab menu to "Canvas".
- Renamed the Atlassian featured canvas to Jira and updated its icon in Customize.
- Required fields are now clearly marked and optional fields are labeled "(optional)" in the create repository, publish to GitHub, add MCP server, feedback survey, and skill editor forms, improving clarity for screen reader and keyboard users.
- Screenshot annotation arrows now scale proportionally to their length with a tapered body, so arrows look more consistent regardless of size.
- Screenshot annotations are now enabled by default after capturing a browser region.
- Session titlebars now show the project name alongside the branch name (e.g. `project/branch`) for easier context when working across repositories.
- Session titles are now generated in the background after your first message, instead of delaying the assistant's initial response.
- Shell read rows in the conversation now show the originating task, live elapsed time and status, and can be expanded to reveal the captured output.
- Simplified collapsed file view rows in the conversation to show just the file name, without the line range or line count.
- Simplified the empty and error states in the Changes panel with more concise messaging.
- Simplified the notice shown when some skills fail to load into a single row, with details, retry, and dismiss actions.
- Standardized the Installed and Add server states in the MCP extensions list so they look and read the same across categories and search results.
- The create issue dialog no longer shows red asterisks on required fields; optional fields like description and assignee are now labeled "(optional)" instead.
- The Run menu now names the active script in its running-state actions, so it's clear which script Stop, Restart, and View logs apply to.
- Tool calls from the Computer Use tool now show a mouse-pointer icon instead of a generic MCP icon.
- Updated the Power BI MCP server description in the recommended server catalog to better describe its semantic model authoring capabilities.
- When a session referenced from Chronicle or a deep link can no longer be resumed, you're now shown a confirmation dialog to start a fresh session on the same branch instead of an error message.
- Wide markdown tables in the chat transcript now expand to use available horizontal space instead of squeezing into the narrow reading column, only scrolling once they've grown too wide.

### Fixed

- Automations with a manual trigger no longer show a non-functional "Disable automation" command, since manual automations can't be disabled.
- Built-in canvases now appear before installed extension canvases in Customize.
- Built-in canvases now show their tailored icon in the Installed inventory instead of a generic fallback icon.
- Cancelled checks on a pull request are now grouped as skipped instead of being counted as failures.
- Clicking a check row in the pull request checks list now opens the actual check run instead of sometimes going to the reporting app's generic details page.
- Completed sessions no longer jump out of the Working section in the sidebar while you're viewing them; they move to Done after you navigate away.
- Copilot code review severity badges in review summaries now render as sharp icons instead of blurry images.
- Diagnostic output dialogs now use the selected theme's background instead of a fixed muted surface.
- Extension canvases now track the panel smoothly while resizing the window instead of jumping to their final size after you stop dragging.
- Fixed a bug where a Copilot "pick one" question prompt would repeatedly steal keyboard focus, dropping or misplacing keystrokes typed elsewhere on the page.
- Fixed a bug where a remote session could remain stuck showing as busy after the app restarted while a tool was still running.
- Fixed a bug where approving a plan in a Side chat would switch the workspace away from its main conversation and open the Plan tab unexpectedly.
- Fixed a bug where starting a new chat could occasionally be replaced by an empty session instead of continuing the one you started.
- Fixed a chat session becoming disconnected and unable to accept new prompts right after restoring an archived workspace.
- Fixed a completed automation run incorrectly showing a session unavailable error and blocking the composer when switching to chat.
- Fixed a duplicate attachment chip appearing when adding a folder or non-image file to the prompt composer.
- Fixed a flicker and choppy arrow movement when hovering over home page suggestion cards.
- Fixed a message sometimes appearing twice in the conversation, once in the transcript and once in the queue.
- Fixed a misleading message that claimed you had used 100% of your allowance for any unrecognized rate limit; it now shows a neutral "You've hit a limit" message instead.
- Fixed a pasted issue or pull request reference in the message composer spinning forever when it couldn't be loaded; it now shows a clear "Couldn't load" state instead.
- Fixed a race condition where Agent Merge could interrupt an active turn instead of waiting for it to finish.
- Fixed a rare issue where sending a message could leave the conversation stuck with no response; you'll now see a clear error and can retry.
- Fixed a session sometimes appearing idle or complete, releasing keep-awake, or missing notifications while it was still waiting on a background subagent task.
- Fixed a session sometimes appearing stuck as running after sending a message that the runtime never acknowledged.
- Fixed a session sometimes remaining stuck showing as loading after the backend had already finished responding.
- Fixed a transient error and duplicate prompt that could appear when a queued follow-up message started after a remote session's turn completed.
- Fixed a workspace briefly appearing to have uncommitted changes and showing a Create PR button right after it was created.
- Fixed a workspace that could remain stuck showing as initializing after it had actually finished setting up.
- Fixed accessibility issues on the onboarding Health Check step: copying results now announces success to screen readers, and the Check again and Export logs buttons keep keyboard focus while busy.
- Fixed accessible names for the sidebar's back, forward, new, and user menu buttons so screen readers and voice control announce the visible label first.
- Fixed agent merge action settings so enabling it in one session no longer overwrites or hides another session's saved choices.
- Fixed Agent Merge getting stuck without acting when it couldn't verify whether a pull request still had unresolved review comments.
- Fixed an error that could occur when pasting text while a horizontal rule was selected in the message composer
- Fixed an issue where a closed dropdown panel could leave an invisible overlay in place that blocked clicks anywhere in the window.
- Fixed an issue where connecting to a WSL environment could fail to register or start the managed daemon depending on the user's shell configuration.
- Fixed an issue where deleting a session could sometimes fail with a "Directory not empty" error while its workspace was still being set up.
- Fixed an issue where opening the same browser preview in multiple sessions could cause the app to freeze.
- Fixed an issue where pull request and issue conversations could show fewer comments than actually loaded after the conversation stream reconnected.
- Fixed an issue where quickly switching between chats could show the wrong scroll position or message content briefly.
- Fixed an issue where recovering a stalled chat session could leave it permanently stuck instead of restarting cleanly.
- Fixed an issue where resuming or reopening a chat could briefly make its tools unavailable, or interrupt tools in other open chats.
- Fixed an issue where sending a follow-up message right after reconnecting to or resuming a session could start a duplicate response instead of queuing against the one already in progress.
- Fixed an issue where the message composer could steal keyboard focus away from Quick Open.
- Fixed an issue where your initial prompt could be lost from the composer if a session restarted before it was sent.
- Fixed an unintended horizontal scrollbar appearing in the feedback textarea when sharing feedback.
- Fixed archiving or deleting a remote workspace failing after restarting the app or host.
- Fixed assistant responses briefly appearing incomplete when they contained a GitHub pull request or issue link
- Fixed authentication for private GitHub plugin marketplace sources that specify a branch or ref
- Fixed automatic session update notifications sometimes being shown as a queued message waiting to be sent, even though nothing was queued.
- Fixed automation cards with multiple triggers crowding or overflowing by showing a compact "Multiple" badge that reveals the full trigger list on hover.
- Fixed background shell details sometimes showing "No output was captured" even after output had been read.
- Fixed background task activity sometimes appearing stuck on "Waiting for activity…" even while the task was actively running.
- Fixed background tasks sometimes staying stuck showing "Working" even after the task had actually finished.
- Fixed being signed out of Copilot entirely when only a secondary GitHub account's token expired, instead of only prompting to reauthorize that account.
- Fixed browser previews on Windows sometimes showing a blank placeholder instead of the requested page.
- Fixed cloud automation pull request triggers so selecting multiple events keeps all of them instead of replacing the previous selection.
- Fixed collapsed "N unmodified lines" rows in the diff view shifting out of alignment when opening a comment on a diff.
- Fixed collapsed file headers growing taller than expected when the diff pane was narrowed with line wrapping enabled.
- Fixed completed background tasks sometimes getting stuck in the composer and failing to clear.
- Fixed conversation compaction getting stuck showing "Compacting conversation..." indefinitely when the session was interrupted; it now shows a clear failure message instead.
- Fixed Copilot CLI processes sometimes continuing to run in the background after closing or quitting the Windows app.
- Fixed Customize discarding an unsaved skill draft without warning when a deep link opened a different tab or dialog; you'll now be prompted to keep editing or discard.
- Fixed deep links that open a new session scoped to a repository that isn't already attached, and error dialogs for a failed repository add now name the repository.
- Fixed delegated sessions sometimes never notifying you when their task finished.
- Fixed diff code text running against the right edge of the diff view, so wrapped lines no longer look clipped.
- Fixed disabled custom cron scheduled workflows being unexpectedly re-enabled after restarting the app.
- Fixed disabled danger buttons showing a red border on hover, which made them look interactive.
- Fixed dragging a tab along the tab bar sometimes accidentally splitting the pane.
- Fixed extra padding around short completed messages in the chat conversation.
- Fixed featured cards in Customize appearing with uneven heights when their descriptions wrapped to different numbers of lines.
- Fixed find in Markdown files failing to highlight any matches, and sometimes throwing an error, when the file contained a dotted capital İ.
- Fixed find-in-file jumping to the next or previous match freezing the app briefly when searching large files.
- Fixed git operations using the wrong GitHub account's credentials when multiple accounts share the same host, causing failures on repos owned by a non-default account.
- Fixed GitHub Enterprise Cloud address errors during onboarding relying on color alone; error messages are now labeled with text so they're clear regardless of color perception.
- Fixed image thumbnails in background task tabs not opening the full-size preview
- Fixed images sent earlier in a conversation sometimes failing to display after resuming a session
- Fixed images shown in tool results disappearing after the original file was deleted or when reopening a chat.
- Fixed inconsistent vertical spacing around "file deleted" and other no-diff notices in the diff view.
- Fixed issue and pull request creation failing on GitHub Enterprise Server repositories when the linked account was lost; the agent now guides you to complete the creation with the local GitHub CLI instead.
- Fixed keyboard focus being lost after removing an advanced filter pill in the My work filter bar.
- Fixed keyboard focus being lost after renaming a file or folder in the Files tree
- Fixed keyboard focus jumping away from the selected plan option when returning to a session with a pending exit-plan decision.
- Fixed keyboard/screen reader focus sometimes moving away from the step heading when navigating between onboarding steps.
- Fixed linked identifiers in Markdown tables (like PR numbers) wrapping character by character instead of keeping a readable column width.
- Fixed long chat histories with subagent activity sometimes loading incompletely or out of order.
- Fixed Markdown content shifting position (tables, checkboxes, code blocks, headings, and lists) when switching between editing and reading a document
- Fixed markdown rendering incorrectly hiding a leading horizontal rule and the content after it as frontmatter.
- Fixed Markdown task lists rendering duplicate checkboxes for items with extra paragraphs or content
- Fixed MCP servers provided by a plugin showing an empty or misleading configuration editor. They now show as read-only, with enable/disable, connection status, and OAuth sign-in still available.
- Fixed Mermaid diagrams keeping their old colors when switching the app theme, instead of updating to match.
- Fixed messages sometimes getting stuck without starting instead of sending right away
- Fixed new sessions sometimes taking a very long time to start when many workspaces were being cleaned up in the background.
- Fixed Overview reporting the wrong Git version on macOS when a different Git install is used for repository operations
- Fixed PageDown and PageUp in the prompt composer moving the background view instead of scrolling within a long prompt.
- Fixed queued follow-up messages disappearing from the composer when a busy session's runtime restarts.
- Fixed Quick Open sending a cancelled private preview code to GitHub's search after dismissing the private preview page.
- Fixed repository configuration trust prompts failing to apply for WSL-hosted sessions when accepted right after the session started.
- Fixed screen readers not announcing option position, count, and selection state in dropdown pickers with unlabeled groups.
- Fixed screen readers not announcing the selected provider or the "Add provider" option in model provider and MCP server pickers.
- Fixed screenshot annotations showing resize handles and staying selected while drawing, and fixed resizing the capture region distorting existing arrows, rectangles, and comments.
- Fixed searching for a pull request or issue by number with a leading "#" (e.g. "#3026") in Create from
- Fixed session creation failing for GitHub Enterprise Server repositories when using a GitHub.com or GitHub Enterprise Cloud account for Copilot.
- Fixed session creation failures and hangs silently discarding your prompt and error details; failures now stay visible and can be retried.
- Fixed sessions incorrectly showing as still working after their background tasks had already finished.
- Fixed sessions sharing a CLI process getting stuck appearing to run after that process failed; affected sessions now show as interrupted and resume successfully on a new process.
- Fixed sessions sometimes staying stuck in a running state after delegating work to a background session.
- Fixed sessions using a custom agent without branch/session rename tools getting instructions that required those tools
- Fixed sessions with inherited auto-approval unexpectedly reverting to manual approval and prompting for command tools after a permissions refresh.
- Fixed shapes in the PowerPoint canvas that take their fill color from the slide theme not rendering.
- Fixed slash command cards losing their rich formatting and showing raw reference markup instead of readable labels.
- Fixed Streamer Mode hiding the Environments settings tab, which blocked access to WSL hosts.
- Fixed suggestion menus (like @-mentions, emoji, and slash commands) not reopening after being dismissed and then retyping the same text.
- Fixed suggestion popovers (like @file or @session mentions) staying visible on top of dialogs such as Settings when opened via keyboard shortcut.
- Fixed the app crashing when opening certain malformed Excel (.xlsx) files, showing a file-open error instead.
- Fixed the app failing to start on some older macOS versions.
- Fixed the app not picking up an updated GitHub Copilot plan or access until you signed out and back in.
- Fixed the browser preview sometimes appearing over the wrong session after switching sessions.
- Fixed the bulk-delete dialog so sub-sessions of a pinned session are also protected from accidental deletion.
- Fixed the Cancel button in the skill editor dialog not closing the dialog when no changes were made.
- Fixed the changed files view losing resolved conflict files and going blank while validation ran during a merge or rebase, instead of showing live progress until the operation completes.
- Fixed the chat composer replacing an entire bracketed token (e.g. a file path) when clicking or arrowing into it to edit a single character.
- Fixed the composer not showing skill suggestions when typing "/" right after starting a new line with Shift+Enter.
- Fixed the Create skill dialog incorrectly warning about unsaved changes when reopened with an empty form.
- Fixed the Customize view's category tabs disappearing or becoming unreadable at narrow window widths
- Fixed the diff view scrolling to the wrong position when expanding or collapsing a review thread.
- Fixed the Extensions "Plan, build, and ship" cards prematurely stacking into a single column at moderate window widths.
- Fixed the featured Figma MCP server preset to pre-fill the correct remote HTTP endpoint instead of a stale local address.
- Fixed the GitHub authorization banner sometimes showing no explanation when your authorization was rejected.
- Fixed the MCP server editor dialog resizing and the server list shifting while opening, and prevented a stray tooltip from appearing over the extensions carousel after closing the dialog with Escape.
- Fixed the model picker briefly showing a raw model ID or an error state when resuming a session
- Fixed the model picker occasionally failing to load models with a "catalog unavailable" error on a cold app start.
- Fixed the model picker showing a "Retry loading models" error when reopening a session that needed to reconnect its runtime.
- Fixed the New Issue dialog briefly showing "No assignees found" while assignee search results were still loading, and improved assignee search to include all repository collaborators.
- Fixed the palette search box in Settings > Themes so leading or trailing spaces no longer hide matching palettes.
- Fixed the pull request Files view getting stuck scrolled to the top after returning from a commit view, so scrolling and navigating to other changed files works normally again.
- Fixed the quota gauge sometimes showing stale usage for the previous account or project after quickly switching between them.
- Fixed the recommended Fabric IQ MCP server preset, which pointed to an endpoint that returned an error when connecting.
- Fixed the right-click context menu on an inactive tab sometimes appearing in the corner of the window instead of at the click location.
- Fixed the scheduled session indicator in the sidebar disappearing or replacing the session status icon; it now stays visible alongside the status for every session state.
- Fixed the send and queue icons in the compact composer button appearing offset when the operating system text size is increased.
- Fixed the session usage pane showing a sub-agent's context breakdown instead of the main session's while sub-agents were running.
- Fixed the Steer and Queue shortcut tooltip in the message composer showing an extra keycap and incorrect spacing.
- Fixed the Windows app becoming unresponsive after a WebView2 crash by automatically restarting instead of leaving a black window.
- Fixed typing in the prompt composer sometimes appearing reversed or showing an unexpected gray suggestion on macOS.
- Fixed uneven spacing and an extra divider between the My work header and its filter tabs, and aligned them with the pull request and issue detail tabs.
- Fixed workspaces sometimes getting stuck on "Preparing workspace" when branch list refreshes queued ahead of workspace startup.
- Fixed WSL worktrees using directory names that could be misread by editors, which sometimes caused an integrated terminal to open in the wrong folder.
- Forked sessions now correctly receive their own workspace context instead of continuing to reference the original session's worktree.
- Improved accessibility of model provider setup and settings forms by clearly marking required and optional fields for screen readers, and showing an "(optional)" label only on fields that can actually be left blank.
- Improved contrast of placeholder text in message and search fields.
- Mathematical formulas and equations now render correctly in chat responses, including inline math inside list items.
- MCP server connection failures now show the underlying error details when available, instead of just a generic "Connection failed" status.
- Nested sessions started from a session in a manual sidebar group now inherit that group instead of appearing outside it.
- Pressing Escape while filter query suggestions are open now dismisses just the suggestions, so it no longer also closes a surrounding dialog or panel.
- Pull and Sync are now unavailable when local changes are present, with guidance to commit, stash, or resolve them first.
- Questions asked by the agent, along with any draft answer you were typing, are now restored if the app or session is restarted before you answer.
- Quoting selected text in Side chat now inserts it into the Side chat composer instead of the main composer.
- Reduced jank and flickering placeholders when scrolling through comment-dense pull request diffs
- Removed the `&` session mention option from the prompt composer on cloud sessions, since those references couldn't be resolved there.
- Restored the branch name next to the session title in the workspace titlebar.
- Resuming a chat by session ID (or clicking its reference in a message) now reopens the existing chat instead of mistakenly adopting it into a new project and workspace.
- Screen readers now announce the API key and model ID field hints on the model provider setup screen during onboarding.
- Sessions that got permanently stuck failing to resume with remote control enabled now automatically resume with remote control turned off, with a toast explaining what happened and how to turn it back on.
- Show a clear "Worktree missing" message and recovery option when a session's linked local worktree can no longer be found, instead of silently replacing the session or losing conversation history.
- Sidebar group headers no longer show a pointer cursor or reveal the collapse/expand arrow when hovering elsewhere in the group; the arrow now only appears when hovering the header itself.
- The branch picker no longer appears for Workspace sessions on a remote host, since remote workspaces always use the host checkout's current branch.
- The composer now shows when Copilot is running commands in a sandbox because it couldn't confirm your organization's policy, instead of incorrectly reporting the sandbox as off.
- The loading indicator now shows "Resuming session" while a previous session is resuming, instead of a stale or misleading status.
- The model picker now keeps your configured provider models selectable and shows a clear, retryable message when Copilot's model list temporarily fails to load, instead of getting stuck loading or prompting you to sign in again.
- The Run button's tooltip and accessible name now show the default script it will run when multiple run scripts are configured.
- Typing `/fleet` in front of a prompt in a new, unsent chat no longer refuses the message with a remote-host error — it starts the chat as a Fleet, matching Home and workspace drafts.
- WSL connection and project errors now show clear recovery guidance naming the affected distribution instead of raw internal error details.

## v1.1.14

### Highlights

- Model, reasoning effort, and context window selection are now combined into a single menu in the message composer.
- Added an "Open in external browser" option to the context menu for browser preview tabs.
- Fixed Agent Merge sometimes treating a pull request's reviews as fully resolved when it had only checked the first page of review comments.
- Fixed automations discarding the selected agent when saved, so scheduled and manual runs now use the agent chosen in the automation editor.
- Fixed the # mention picker so pull requests and discussions can be found on repositories with many issues, instead of only ever showing issues.

### Added

- Added an "Open in external browser" option to the context menu for browser preview tabs.

### Changed

- Model, reasoning effort, and context window selection are now combined into a single menu in the message composer.
- Moved the Open in menu back to the session titlebar.
- Skill load failures now show as a neutral, dismissible notice instead of replacing the entire skills list.

### Fixed

- Fixed Agent Merge sometimes treating a pull request's reviews as fully resolved when it had only checked the first page of review comments.
- Fixed an issue on the Home screen where pasting a GitHub URL into the prompt could switch the selected project away from the one you explicitly chose.
- Fixed an issue where a resume failure could replace a session with an empty one even though its conversation history still existed.
- Fixed automations discarding the selected agent when saved, so scheduled and manual runs now use the agent chosen in the automation editor.
- Fixed browsing public marketplaces on Windows, where loading would fail before cloning.
- Fixed missing accessible names for issue and pull request sidebar controls (type, labels, reviewers, assignees), so screen readers now announce them correctly.
- Fixed the `#` mention picker in the prompt composer so pull requests and discussions can be found on repositories with many issues, instead of only ever showing issues.
- Your prompt now stays visible and selectable in the conversation if session creation fails, instead of being replaced by a full-page error.

### Removed

- Removed the "Uncommitted work preserved" toast when archiving sessions; uncommitted work is restored automatically with the session.

## v1.1.13

### Highlights

- Customize is now available to everyone, letting you browse and manage plugins, skills, MCP servers, and canvases in one place, and even create your own personal skills.
- Pull request overviews now show and let you edit closing issues, and you can link pull requests to issues right from the header menu.
- Azure DevOps is now available to install and open from Customize > Featured.
- You can now toggle worktrees on or off for all repositories at once when starting a new session across a repository collection.
- Added an opt-in setting to stabilize screen reader transcript navigation while a response streams.

### Added

- Added 180-day and 360-day options to the Copilot CLI session history picker in Settings.
- Added a "Reset zoom level" action to the command palette to quickly return the app to its default zoom.
- Added a checkbox to toggle worktrees on or off for all repositories at once when starting a new session across a repository collection.
- Added an opt-in setting to stabilize screen reader transcript navigation while a response streams.
- Azure DevOps is now available to install and open from Customize > Featured.
- Customize is now available to everyone, letting you browse and manage plugins, skills, MCP servers, and canvases in one place, and create, edit, or remove your own personal skills.
- Pull request overviews now show and let you edit closing issues; link pull requests to issues from the header overflow menu.

### Changed

- Alternate GitHub accounts now live in a "Switch account" submenu, keeping the account menu simpler when you have several accounts.
- Check runs in the pull request checks panel now show elapsed or total runtime instead of relative timestamps like "just now" or "1h ago".
- Improved canvas discovery and management in Customize: featured canvases now show clearer Install/Installing states and update automatically once installed, canvas details show provider and requirements with a New session action, and canvas context menus offer New session, View details, and provider management actions.
- Made loading, retry, and empty-state messaging in the Customize view clearer and more consistent, and stopped background refresh indicators from shifting content.
- Moved the client protocol and agent daemon version details from Settings > Environments to the Health check dialog.
- Pinned sessions can now be selected and deleted in Manage sessions, just like other sessions.
- Pull request activity feeds now show the title, status, and an actionable reference card when an issue or pull request is linked or unlinked.
- Refined tooltip open and close animations with a smoother, snappier motion.
- Refreshed artwork in the Customize view, adding featured card images and tailored icons for built-in canvases like the editor, browser, terminal, Word, Excel, and PowerPoint.
- Reorganized the Customize > Featured tab so Azure DevOps is highlighted in Editor's picks, Figma appears alongside planning and shipping tools, and connected-work integrations are reordered.
- Session automations are now available by default, so scheduled prompts run without needing to be enabled first.
- Shortened the descriptions on featured extension cards so they display without truncation.
- Simplified and standardized the source labels shown for installed skills, plugins, canvases, agent extensions, and MCP servers in Customize > Installed.
- Simplified the queued message menu to Move up, Move down, Edit, and Copy, removing duplicate send/discard actions already available on the row.
- Standardized fallback icons for MCP servers, skills, plugins, connectors, and canvases in the Customize view so each resource type shows a consistent, distinct icon.
- The account switcher now shows just the username for accounts on the same host, only showing the full host/username when you have accounts on multiple hosts.
- The checks panel on pull requests now shows contextual check names (like workflow and job) and matches GitHub.com's status wording and durations for running, successful, failing, and other check states, with skipped checks grouped separately from neutral checks.
- The plan pill in the composer now keeps a stable "Plan" label as items complete, showing progress only through its count.
- When adding a repository fails, you now see specific guidance about why (like needing to sign in to another account) instead of a generic error, with quick actions to add an account or open the health check.

### Fixed

- A project's selected custom agent is now remembered across app restarts instead of resetting to the default agent.
- Collapsing a sidebar group for a session or chat you're currently working in no longer automatically re-expands it.
- Conversation history now stays visible and readable if a session temporarily can't reconnect, with a retry action to reconnect.
- Creating a Local session without picking a branch no longer forces an unexpected checkout, preserving your current branch instead.
- Dropdown menus now block clicks on background elements until the menu is dismissed, preventing accidental actions while a menu is open.
- Fixed a brief freeze and loss of keyboard focus that occurred when a long streaming response finished.
- Fixed a bug where a session running a long command could be shut down mid-task, losing track of its progress, before the command finished.
- Fixed a bug where rapid file changes in a collection workspace could spawn many overlapping Git processes and make the app unresponsive.
- Fixed a bug where the queued messages count could show entries with no visible content when expanded.
- Fixed a crash that could occur when deleting a column from a table in the composer.
- Fixed a crash that could occur when sorting files in the diff view for repositories with directory names that differ only by casing.
- Fixed a crash when opening certain malformed Excel files, which now show an error instead.
- Fixed a folder session getting stuck showing a spinner with no way to view files.
- Fixed a Linux crash where running git commands after the app auto-updated or restarted itself could fail with a library-loading error.
- Fixed a memory leak on macOS where repeatedly opening and closing canvases left background processes running.
- Fixed a race condition where restoring an archived session while archiving was still in progress could orphan its conversation history and create empty duplicate sessions.
- Fixed a session sometimes getting stuck showing as running indefinitely after a tool finished.
- Fixed a session's pull request link getting permanently stuck on a closed or merged pull request instead of updating to a new one opened on the same branch.
- Fixed a Windows UI freeze that could occur when loading MCP app content.
- Fixed activity row labels being misaligned with their leading icons.
- Fixed an issue on Linux where the app could show a phantom media player entry with no title and, over time, cause the app to freeze or use excessive CPU.
- Fixed an issue on Windows and Linux where relaunching GitHub Copilot while it was already running could sometimes start a duplicate copy of the app instead of bringing the existing window to the front.
- Fixed an issue on Windows where archiving a session could fail and leave the archived session reappearing after restart.
- Fixed an issue on Windows where the app could occasionally crash with a "This page is having a problem" error.
- Fixed an issue where archiving a session could fail with an "Access is denied" error if files in the workspace were still locked by another process.
- Fixed an issue where closing Quick Open could leave keyboard focus on the message composer instead of a newly opened question that needed a response.
- Fixed an issue where directly installed plugins could fail to uninstall with a "not installed" error.
- Fixed an issue where restoring an archived workspace could let you send a prompt before the session was fully ready, causing it to appear sent but never reach Copilot.
- Fixed an issue where sending a follow-up message while background agents were still finishing up could be rejected instead of being queued and sent once they settled.
- Fixed archiving a session from a worktree that lost its git link, so it no longer fails with an "Archive failed" error.
- Fixed background subagent task details getting slower to update the longer a running message streamed in.
- Fixed Computer Use settings sometimes showing permissions as ready before they were actually granted, and made dependent controls clearly disabled until permission status is confirmed.
- Fixed extra visual spacing from repeated blank lines in the Markdown editor, so blank runs now render with consistent spacing while still showing exact blank-line markers when your cursor is nearby.
- Fixed GitHub alert callouts (e.g. Note, Tip, Warning) not rendering correctly in the plan panel and canvas markdown preview when the alert body started with plain text.
- Fixed high CPU usage and laggy typing on the Home screen caused by Mona's animation reacting to prompt input.
- Fixed keyboard focus disappearing after dismissing a chat confirmation dialog, so keyboard navigation continues from where you left off.
- Fixed keyboard focus dropping out after confirming removal of an account in Settings -> Accounts, so it now moves to a neighboring account instead.
- Fixed keyboard shortcuts and menu navigation silently discarding an unsaved New issue draft instead of prompting to confirm.
- Fixed links in chat references and the right-click Open link menu silently doing nothing when they failed to open, showing an error message instead.
- Fixed math expressions using different delimiter styles right next to each other (e.g. `\(a\)$$b$$`) showing a parse error instead of rendering correctly.
- Fixed MCP server entries in Customize opening with an empty configuration form; they now open pre-filled with the correct command, arguments, and environment fields.
- Fixed messages sent by a coordinated session sometimes not appearing in the conversation while the queue count still included them.
- Fixed misaligned icons and toggles for installed skill rows in Customize > Installed.
- Fixed multi-paragraph LaTeX display expressions (delimited by \[ ... \]) not rendering correctly when separated by blank lines.
- Fixed newly created sub-issues sometimes not appearing in the sub-issues list until the issue was reloaded.
- Fixed onboarding sometimes skipping past the repositories step before its choices were visible when pressing Continue's keyboard shortcut twice quickly.
- Fixed opening a WSL project failing when the shell prompt printed extra output after the git repository info.
- Fixed pasting a copied table from apps like Numbers or Excel into the prompt composer, which previously attached a broken image and dropped the table content.
- Fixed Pick & Polish so it works when previewing local HTML files in the browser preview.
- Fixed pull request checks incorrectly showing obsolete, cancelled reruns as failing instead of reflecting the latest check attempt.
- Fixed Quick Open and other command palettes not responding to Enter after clearing the search query with the keyboard.
- Fixed Quick Open losing keyboard focus when a permission or decision prompt appeared
- Fixed repository and session-picker popups (like the GitHub repository selector and "Start session in repository") not announcing their title to screen readers.
- Fixed responses blocked by content filtering appearing to complete silently; the conversation now explains that the response was blocked and announces it for screen readers.
- Fixed review comment navigation in diffs so jumping to a comment reliably expands the right file and context, avoids duplicate comment panels, and keeps line gutters aligned.
- Fixed session creation being incorrectly blocked for repositories whose remote URL includes a GitHub username matching a signed-in account, such as when multiple GitHub accounts are configured on the same machine.
- Fixed session creation failing for repositories cloned over SSH with a custom username, such as GitHub's SSH certificate authority clone format.
- Fixed setup scripts sometimes failing on newly created workspaces before the workspace files were fully available.
- Fixed slash commands for personal skills not being invoked correctly.
- Fixed streamed chat answers containing a line break inside a table becoming progressively slower and janky the longer the answer got.
- Fixed system prompt cards overflowing or getting cut off in narrow chat panes by wrapping long labels and subtitles.
- Fixed task completion summaries getting an extra scrollbar and height cap instead of flowing normally in the conversation.
- Fixed the app freezing briefly when copying a long assistant response
- Fixed the Changes view incorrectly showing no changes for a workspace whose branch had already been merged into the base branch.
- Fixed the comment editor's formatting toolbar being cut off and unclickable at narrow window widths.
- Fixed the composer's model picker not announcing the selected model to screen readers when Auto mode is on.
- Fixed the conversation view briefly freezing when moving the pointer over long answers containing code blocks.
- Fixed the Dim theme option appearing active in light appearance even though it only applies in dark appearance.
- Fixed the dock/taskbar badge count to match the sessions actually showing an attention indicator in the sidebar, so it no longer overcounts sessions that are working again after being unread.
- Fixed the environment variables reference table in project Settings > Scripts being clipped and unreadable at narrow window widths.
- Fixed the filter buttons in Automations, Appearance settings, and Keyboard shortcuts settings being too small to click reliably.
- Fixed the fix-checks and resolve-comments slash commands so they are available when reviewing a pull request, not just one you created.
- Fixed the Installed tab in Customize so refreshing MCP servers and plugins no longer shifts content; loading status now shows as a small indicator next to the header actions.
- Fixed the keyboard focus indicator not being visible on the selected day (or range endpoints) in the date picker.
- Fixed the keyboard focus ring in the Settings navigation being clipped at the top, bottom, and off-screen edges.
- Fixed the local sandbox toggle incorrectly showing in the new session composer when Cloud was selected.
- Fixed the model selector (and other composer menus/popovers) getting stuck open in the corner of the window when the agent asks a follow-up question while the panel is open.
- Fixed the onboarding logo wave animation continuing to render in the background when the app was minimized, reducing unnecessary CPU usage.
- Fixed the onboarding theme picker losing the selected palette from the grid when clearing search, filtering by color, or returning to the step.
- Fixed the project Settings tab clipping the "Create config file" button and overflowing horizontally at high zoom or narrow window widths.
- Fixed the session timeline's time axis being announced as an interactive control with no action for screen reader and keyboard users.
- Fixed the sidebar context menu sometimes acting on a stale multi-selection instead of the session that was right-clicked.
- Fixed the Stop button in the message composer becoming hard to see when focused with the keyboard.
- Fixed the Stop button sometimes disappearing (and Esc no longer working to stop a turn) in GitHub-hosted sessions while the agent was still working.
- Fixed the sub-agent activity view losing the latest streamed output while it was updating, so it now stays scrolled to the bottom automatically.
- Fixed tool call results showing "No output" when an MCP tool returned its result as an embedded resource instead of plain text.
- Fixed VoiceOver not announcing the position of rows in the Run options menu's Running, Recents, and Automations sections.
- Fixed Word documents using excessive CPU while idle with the cursor placed but no typing happening.
- Fixed WSL sessions failing to start or falling back incorrectly when a configured workspace folder no longer existed.
- Markdown documents with YAML frontmatter no longer show the metadata as visible content in the document body.
- Pinned sessions now stay in their own Pinned section when the sidebar is grouped by status, instead of being mixed into the status groups.
- Restored the row dividers in the available MCP server list on the Customize page.
- Restored the Show submenu in Configure sessions, letting you display project and branch info under session names, and fixed a small jitter when hovering over sidebar rows.
- Submitting a slash command that isn't currently available now shows an error explaining why, instead of silently doing nothing (or, in some cases, sending the command text as a plain chat message).
- The `/pr-approve` and `/pr-request-changes` commands are now disabled with an explanation when you try to review your own pull request, instead of submitting a verdict GitHub always rejects.
- The plan panel no longer shows view options that could hide the task list when a plan contains only tasks.
- The Skills list now explains when a skill file couldn't be loaded, instead of leaving that skill silently missing from the list.
- Tooltips with long text now wrap within a consistent maximum width instead of growing unbounded, and keyboard shortcut hints stack neatly below wrapped labels.
- Typing an issue or pull request number in the `#` mention picker now always resolves it, even if the item is older than the picker's recently prefetched suggestions.
- When an MCP server disconnects mid-session, its reference chip now explains why it failed instead of just showing "failed".

## v1.1.12

### Highlights

- You can now use /ask and /btw to ask a side question without interrupting the current response.
- The pull request Files view now lets you expand the diff to see more surrounding code, matching the controls already available in Compare changes.
- Fixed a security issue where tool approval prompts requested by a hook could be skipped instead of always requiring your explicit approval.
- Active agent sessions now pick up the latest pull request state, like a merge or ready-for-review change, instead of reasoning from stale information.

### Added

- Added a Copy > Session ID action to session context menus in the sidebar.
- The pull request Files view now lets you expand the diff to see more surrounding code, matching the expand up/down/whole file controls already available in Compare changes.
- You can now use /ask and /btw to ask a side question without interrupting the current response.

### Changed

- Moved Search into the sidebar header next to Back and Forward, and moved Open in from the workspace header into the Files and Changes toolbars.
- Refined the command palette's selection styling with a more compact row height and a full-width highlight showing a Return icon for the active item.
- Sidebar archive actions now distinguish merged and closed pull requests, and merged pull requests are included for archiving even after their worktree is cleaned up.
- Widened the plan view so plan content is easier to read.

### Fixed

- Active agent sessions now pick up the latest pull request state (like a merge or ready-for-review change) instead of continuing to reason from stale information.
- Assistant responses using LaTeX delimiters like \( ... \) and \[ ... \] now render as math instead of showing raw brackets and commands.
- File tab close buttons in chat are now always visible and easier to reach with touch or keyboard, instead of only appearing on hover.
- Fixed a security issue where tool approval prompts requested by a hook could be skipped instead of always requiring an explicit approval from you.
- Fixed a skill load failure incorrectly showing "Loaded skill" instead of "Failed to load skill".
- Fixed Agent Merge sometimes taking much longer than expected to re-check a pull request after your computer wakes from sleep.
- Fixed Ctrl/Cmd+T not opening the Add to panel picker for a workspace whose right panel had never been opened.
- Fixed dragging and dropping files onto the app on Linux, which previously did nothing.
- Fixed keyboard focus and screen reader announcements when confirming account removal in Settings > Accounts.
- Fixed pull request checks incorrectly showing as failed to load when some check details were restricted by organization security settings.
- Fixed repositories disappearing from the onboarding "Connect your repositories" step after navigating back from a later step.
- Fixed rows in the command palette shifting position when highlighted while arrowing through results.
- Fixed screen readers announcing a generic label instead of the actual question when navigating confirmation prompts (permissions, rate limits, browser sharing, repository setup, and similar dialogs).
- Fixed several terminal commands that could silently write files or change system settings without asking for approval; these now require confirmation like other non-read-only commands.
- Fixed the "Started" and "Last read" timestamps in the shell task detail panel so they can be revealed with the keyboard and are announced correctly by screen readers.
- Fixed the Add MCP Server form's error message to mention that server names can't contain a closing brace (}).
- Fixed the Changes panel showing raw Git error output when a workspace's checkout was missing or invalid; it now shows a clear, actionable error message with retry and details options.
- Fixed the Files tab becoming slow and unresponsive when filtering large repositories.
- Fixed the model picker trigger being announced as a combobox by screen readers instead of a button.
- Fixed the model picker's "Retry loading models" button so it actually retries instead of doing nothing when models failed to load.
- Non-openable file and MCP references in chat can now be revealed and read with the keyboard and screen readers, not just by hovering.
- The Updated, Created, and Location details in the Manage sessions table can now be revealed and read by keyboard and screen reader users, not just with a mouse hover.
- When a cloud session can't be created because cloud sandboxes aren't enabled for your organization or enterprise, you now see a clear explanation with the option to view detailed logs, instead of a generic failure or being sent to the Health check.
- Workflow run rows now announce the full date and time to screen readers, instead of only showing it in a hover tooltip.

## v1.1.11

### Highlights

- Added a branch update strategy setting in project settings, letting you choose whether session branches are updated by merge commit or rebase.
- Added a Session cleanup section to Sessions settings, letting you enable automatic archiving of inactive sessions and permanent deletion of archived sessions on separate schedules.
- You can now select a range of commits in the Changes commit picker to view their combined diff.
- When switching to Autopilot mode with tool permissions set to Always ask, Copilot now recommends a permission mode that lets it keep working unattended, with a one-click option to apply it.
- The sidebar now has a configuration menu for grouping and ordering sessions, filtering by status/PR/environment/source, collapsing all groups, and marking all as read.

### Added

- Added a "Plan" option to the right panel's "+" menu in chat sessions, so you can open the plan tab from there instead of only from the plan pill above the composer.
- Added a branch update strategy setting in project settings, letting you choose whether session branches are updated by merge commit or rebase.
- Added a Session cleanup section to Sessions settings, letting you enable automatic archiving of inactive sessions and permanent deletion of archived sessions on separate schedules.
- Outdated pull request comments that aren't tied to a file are now collapsible on their own and collapse together with the "Collapse all files" action.
- Overflowing code blocks now support keyboard scrolling (Tab in, then use arrow keys, Home, End, Page Up/Down), and macOS shows a draggable scrollbar on hover for mouse users.
- Right-click a recent automation run to stop it or open its session, without opening the run details first.
- Starting a new session from an issue now prefills a fix command and keeps the linked issue visible while the workspace is created.
- The command palette now includes quick actions for managing sessions, keyboard shortcuts, accounts, health check, help center, and app updates.
- When switching to Autopilot mode with tool permissions set to Always ask, Copilot now recommends a permission mode that lets it keep working unattended, with a one-click option to apply it.
- You can now enable Canvas Dev Mode from the command palette on extension canvases to switch to a read-only developer view and refresh the canvas.
- You can now select a range of commits in the Changes commit picker to view their combined diff, instead of only one commit at a time.
- You can now Shift-click checkboxes in Manage sessions to select or deselect a range of sessions at once.

### Changed

- Autopilot mode in the prompt composer now uses a rocket icon instead of the robot icon, making it easier to distinguish from the agent picker.
- Clarified the description of the Assisted tool approval mode to explain that requests are automatically approved only after passing an LLM safety check.
- Clarified the warning message shown for unsupported media previews in the files view.
- Exported session gists now include the full conversation detail—reasoning, tool activity, and timing—matching what you see in the app.
- Linked and unlinked issues and pull requests now show consistent icons and reference cards in the issue timeline.
- Reduced padding on user chat message bubbles for a more compact conversation view.
- Refined home page suggestion cards with simpler icons and responsive layouts.
- Removed Draft from the sidebar's Status filter (draft pull requests remain available under the PR filter), and merge-ready pull requests no longer count toward sessions needing attention.
- Removed the redundant branch label from the completed pull request widget, showing only the title, draft badge, and diff stats.
- Renamed the side panel toggle, resize, and width controls to use panel-neutral wording instead of "review panel".
- Shortened chat and session context menu actions to Pin, Archive, and Delete, and grouped copy actions into a new Copy submenu with Branch and Pull request. My Work tabs now stay highlighted while their context menu is open.
- Shortened the placeholder text shown in the message box across chat, plan, and autopilot modes.
- The "Ask in Side chat" action on question prompts now stays visible instead of only appearing on hover.
- The pull request view now shows every status check instead of stopping at the first 100.
- The sidebar now has a configuration menu for grouping and ordering sessions, filtering by status/PR/environment/source, collapsing all groups, and marking all as read.
- The Stop/Stop all button in the workspace header is now icon-only for a more compact toolbar.
- Tightened spacing in menus, context menus, and selection popovers for a more compact feel.
- Updated Manage sessions menus to match My Work's sizing and density, removed the redundant heading, shortened Archive and Delete labels, and improved ellipsis-button menu placement and visibility.
- Updated the queued message label to use sentence case.
- Widened workspace tabs so labels and close controls have more breathing room.

### Fixed

- Expanding the sidebar no longer briefly freezes the app, and opening feedback from a collapsed sidebar now reliably opens the feedback dialog instead of doing nothing.
- Files tabs now show the selected file's name and file-type icon again instead of a static "Files" label.
- Find in a diff now searches text revealed by expanding a collapsed section or the full file, instead of reporting no results for content that's visible on screen.
- Fixed a brief input lag when switching between mouse and keyboard while typing.
- Fixed a bug on Windows where archiving a session could fail permanently, leaving it stuck and unable to be archived.
- Fixed a closed session's tab strip sometimes appearing at the bottom of the conversation panel.
- Fixed a crash on Windows that could occur when the app's tray menu was rebuilt while it was being closed.
- Fixed a duplicate divider appearing in the Run options menu.
- Fixed a duplicate tooltip appearing on the Update branch action in the diff toolbar when its label was already visible.
- Fixed a misleading error when an extension's MCP server was blocked by an organization policy; the app now explains that the server is disallowed by policy and directs you to your administrator.
- Fixed a phantom media player entry appearing in the system media controls on Linux while playing videos in the app
- Fixed Agent Merge getting stuck and not resuming when a pull request's mergeability status was temporarily unknown, such as right after a conflicting base update.
- Fixed an issue on Linux where a leftover copy of the app's bundle could interfere with git operations, causing fetch failures and blocking session creation.
- Fixed an issue on Windows where the app update could fail because the installer started before the previous app process had fully exited.
- Fixed an issue where an in-progress diff comment could be silently lost when selecting text on a diff or switching to comment on a different line.
- Fixed an issue where archiving a workspace could fail if the workspace folder was only partially removed.
- Fixed archived sessions sometimes briefly reappearing in the session list while cleanup was still in progress.
- Fixed archiving a workspace sometimes failing on Windows when a file in the workspace was briefly locked by another process.
- Fixed archiving or deleting a workspace sometimes failing with a git error when its files had already been partially cleaned up.
- Fixed automation run pills and generated cards so plans, background tasks, widgets, factories, and GitHub references open in the run sidebar without losing pending plan approvals.
- Fixed avatar fallback initials being announced by screen readers as part of surrounding labels, such as repository filter options.
- Fixed background agent task labels not showing which model was used when no specific model was requested.
- Fixed C4 diagrams (C4Context, C4Container, C4Dynamic) failing to render with a "Failed to load rendered diagram" error.
- Fixed chat progress indicators freezing after collapsing and reopening a sidebar repository group.
- Fixed clearing an automation's project in the automation editor not actually removing it, and added an error message when saving an automation fails.
- Fixed collapsed sidebar sections re-expanding and losing their collapsed state when they contained the active session.
- Fixed connecting a GitHub repository by URL when signed in with multiple accounts on the same GitHub host — it now resolves the account that actually has access instead of failing or opening the wrong project.
- Fixed corrupted terminal glyphs that could appear after switching away from a terminal tab and back.
- Fixed crashes that could occur when browsing very deep folder trees in the directory picker, when opening malformed external links, and when using code block controls in the composer.
- Fixed deleted sessions reappearing after restarting the app.
- Fixed empty sessions appearing on the Agents page after launching the app with remote access disabled.
- Fixed extra spacing above the first line and mismatched gutter background color when editing a code file.
- Fixed generated files in the Changes view snapping back to collapsed after you expanded them, whenever the diff was recomputed.
- Fixed globally installed plugin canvases showing up as duplicate entries once per project in the Canvases and Installed tabs.
- Fixed Go To File returning no results when typing a file path with backslash separators.
- Fixed hard-wrapped list items in the Markdown editor showing broken-looking line breaks instead of flowing together as one item.
- Fixed Home not allowing session submission for remote-only projects, such as Codespaces, that have no local checkout.
- Fixed hover-revealed row controls (selection checkboxes and overflow menus) in Manage sessions and My work so they're no longer invisibly clickable on touch devices, and are now visible at rest for touch input.
- Fixed keyboard focus being lost after closing a tab in the right panel
- Fixed keyboard focus jumping out of the MCP servers list in Settings after canceling or confirming a server removal; focus now stays on a sensible control in the list.
- Fixed keyboard navigation getting stuck when tabbing through action buttons on sidebar chat and repository rows
- Fixed MCP servers that require sign-in getting stuck on a loading spinner instead of showing a sign-in prompt.
- Fixed misaligned action rows (like Clone repository and Open folder) in the project picker dropdown
- Fixed misaligned labels and fields for the custom CRON expression in the automation dialog.
- Fixed Mona being clipped or hidden behind the composer on the new session page as it grows.
- Fixed My work inbox items not showing when the window is narrower than about 965px by switching to a single-pane layout instead of clipping the detail view.
- Fixed notification sounds sometimes not playing over Bluetooth speakers on Linux
- Fixed Pick & Polish screenshot region capture by selecting from a static browser preview without including the picker highlight or guidance in the captured image.
- Fixed Quick Open's "Keyboard shortcuts" entry, and the toggle thinking/file edits entries, advertising the wrong or a stale default key after a shortcut was remapped or cleared.
- Fixed relaunching the app on Windows sometimes leaving it hidden and unresponsive instead of restoring and focusing the existing window.
- Fixed repository search and Add GitHub Repository incorrectly matching a repository to the wrong signed-in account when multiple accounts had access to a repository with the same name.
- Fixed scheduled automations continuing to run and fail after their chat session was archived.
- Fixed screen readers announcing the selected repository instead of the search field when opening the My Work repository filter.
- Fixed screen readers not announcing which repositories are selected in the repository filter on the My work view.
- Fixed screen readers not reading the helper text next to toggles and fields in Settings > Projects, giving each script's Edit/Remove buttons a distinct name, and fixed the branch prefix validation error not being announced while the dialog was open.
- Fixed session titles overlapping the macOS window controls in the session grid view.
- Fixed sessions created automatically from a GitHub issue losing the selected context window size.
- Fixed skipped checks incorrectly showing as failed in the pull request checks panel
- Fixed slash commands completed with Tab in the Automation editor not being saved correctly.
- Fixed terminals sometimes getting stuck using slower rendering instead of GPU-accelerated rendering.
- Fixed the "Delete sessions without confirmation" setting also silencing the archive confirmation dialog. Archiving now has its own "Archive sessions without confirmation" setting.
- Fixed the "Find in workspace" position menu in Settings truncating longer option labels.
- Fixed the `/pr-fix-checks` and `/pr-resolve-comments` slash commands incorrectly reporting no failing checks or unresolved comments while a pull request's checks or comments were still loading.
- Fixed the app hanging for about 10 seconds on startup when launched from a terminal.
- Fixed the Changes view losing its file list after a pull request's session was merged.
- Fixed the commits menu in the Changes view losing its scroll position and selected row when selecting the first commit of a range.
- Fixed the Continue button staying disabled after typing feedback on a plan review, so it can be clicked to submit.
- Fixed the file-mention picker and Go-to-File suggesting ".git" as a file to reference
- Fixed the Files tab flickering and briefly hiding expanded folders while it refreshed in the background.
- Fixed the Files, Changes, and Commits tabs for workspaces created from a project containing multiple Git repositories, which previously failed to load or showed incorrect data.
- Fixed the final completion summary sometimes disappearing behind the collapsed activity when using Minimal verbosity.
- Fixed the loading timer resetting to 0s when starting a new session without a project selected.
- Fixed the Markdown canvas becoming read-only when it contained a Mermaid diagram; text before and after the diagram now stays editable.
- Fixed the model promotion banner's dismiss button text overflowing and getting clipped on narrow windows.
- Fixed the panel toggle keyboard shortcut not working in standalone chat sessions.
- Fixed the Run control not showing a newly added run script until the workspace was refreshed.
- Fixed the Settings dialog staying open when pressing Escape on the MCP "Add custom server" form while keyboard shortcuts were disabled in Settings > Accessibility.
- Fixed the side chat panel not opening when adding selected text to a side chat from a general chat.
- Fixed the side-panel resize splitter highlight and tooltips being hidden behind native browser previews and extension canvases.
- Fixed the sidebar layout pushing content off-screen on Linux when using GNOME's Large Text setting or certain tiling window managers.
- Fixed the stop/cancel button on background task and shell rows sometimes being covered by overflowing task text.
- Fixed the toolbar in the inline message editor so its buttons respond where they appear instead of being offset.
- Fixed the workspace popover showing the wrong Session ID; it now shows the actual Copilot CLI session ID and stays hidden until a session exists.
- Fixed typing or pasting in a session grid cell sometimes landing in a different cell's composer instead of the one you clicked.
- Fixed window resizing feeling janky by removing an unnecessary full-window restyle on each resize.
- Improved screen reader support for plan review, question, and input request prompts, and fixed the selected option losing its highlight when focus moved away.
- Improved screen reader support in the My Work list: rows now announce repo, author, updated time, labels, checks, changes, comments, and assignee names, and row checkboxes have clear, consistent labels.
- Links to specific issue or pull request comments now open in-app and scroll to the referenced comment instead of just opening the parent issue or pull request.
- Local repository projects now detect missing, changed, or unreadable origin remotes before session creation. Safe origin mismatches can be restored automatically, while other problems include repair or re-add guidance.
- Project MCP servers settings now show a distinct message when a config file exists but loaded no servers, instead of the same empty state as having no config file at all.
- Quota usage percentages no longer round up, so displayed usage matches the actual remaining quota.
- Removed the duplicate "Remove app" menu row for custom apps in the "Open in" menu, keeping a single inline remove action that remains keyboard accessible.
- Renaming a branch now preserves letter case in the name you type, so case-sensitive ticket references like TICKET-123 are no longer lowercased.
- Screen readers now announce only the model name when opening the model information dialog in the model picker.
- The origin recovery notification for a failed session now updates to match the current problem and offers the right fix instead of showing stale guidance after you retry.
- The plugin details dialog now lists the MCP servers a plugin provides alongside its skills, so it's clear what installing or uninstalling the plugin adds or removes.
- Use the pull request icon for the Copy > Pull request action in the session menu.
- Videos now play inline in the Files tab instead of showing a "can't be previewed" message.
- Voice dictation now shows a clear error and a way to retry or open settings when the speech-to-text model list fails to load, instead of silently doing nothing when you click the mic button.
- When starting a session fails because a repository's remote origin is missing, mismatched, or can't be verified, your prompt, attachments, and settings are now preserved with a notification offering to fix the origin or retry, instead of losing your work.

## v1.1.10

### Highlights

- Background items and queued message management are now available to everyone, enabled by default.
- You can now repair a saved diff for a merged pull request session when it can no longer be loaded.
- Plugins can now be updated automatically, including their extensions, from Customize → Plugins.
- Right-click a side panel tab to close it, close others, or close tabs to the right.
- You can now remove a pending queued or steering message directly from the conversation transcript.

### Added

- Added a way to repair a saved diff for a merged pull request session when its saved diff can no longer be loaded.
- Added an option in Customize → Plugins to update installed plugins and their extensions automatically.
- Background items and queued message management are now available to everyone and enabled by default.
- Right-click a tab in the side panel to close it, close other tabs, or close tabs to the right.
- You can now remove a pending queued or steering message directly from the conversation transcript in local sessions.

### Changed

- Copilot work events in the pull request timeline now show a small Copilot icon instead of an avatar.
- Deleting or automatically cleaning up sessions with uncommitted work no longer shows a recovery toast; the work is still backed up before deletion.
- Made composer list panel titles match the sidebar's group header styling.
- Opening an issue or pull request link for a repository you haven't added now offers to add it and opens the link automatically once it's ready.
- Refreshed the question prompt shown when the agent asks you a question, with a more compact layout and a collapsible details view.
- Returning to a session's Files tab now shows the previously loaded file tree immediately instead of rebuilding it, and switching between files no longer briefly flashes the previous file's content.

### Fixed

- Copy buttons in Add Account and the device code screen now announce success to screen readers, and the "Copy link" button no longer changes its label after copying.
- Emoji are now only inserted when you select one from the suggestions menu, so typing or pasting a shortcode like `:rocket:` keeps it as literal text.
- Fixed "Repair saved diff" not being able to recover the diff for a merged pull request whose source branch had been deleted.
- Fixed "Reply to thread" cards not navigating to their inline diff thread when the card lacked workspace information.
- Fixed a brief console window flash on Windows when opening a workspace.
- Fixed a brief visual jump in the conversation transcript after dismissing the repository configuration prompt.
- Fixed a bug where app updates could delete user-added skills, such as migrated slash commands.
- Fixed a rare crash on Linux where the app could abort without a crash dialog while updating the tray menu.
- Fixed an issue on the Home view where tapping near a discovery card's hidden dismiss button on a touch device could accidentally dismiss the card.
- Fixed automation runs loading forever when their chat had been deleted or archived; these now show a clear unavailable state instead.
- Fixed crashes that could occur when editing tables or selecting typeahead suggestions in the chat composer.
- Fixed new worktree sessions sometimes running outdated repository setup scripts and skipping the trust prompt instead of using the worktree's own configuration.
- Fixed opening a new session deep link sometimes starting two sessions instead of one.
- Fixed pull request descriptions sometimes incorrectly showing as empty when they actually failed to load, and added a retry option to recover them.
- Fixed repository configuration approval being forgotten and re-prompted when switching between worktrees of the same project.
- Fixed right-panel tabs so moving and splitting them (via drag or the tab context menu) works consistently, and the Changes tab no longer renders blank when split alongside the pull request overview.
- Fixed screenshot and file links in chat losing their preview; clicking a linked screenshot now opens it in the image viewer, and other file links open in the artifact viewer.
- Fixed the "Off" CLI session retention setting so it actually stops automatically importing CLI sessions instead of still retaining them for seven days, and sped up startup for accounts with many stored sessions.
- Fixed the copy logs button in the setup script logs dialog rendering smaller than the adjacent edit script button.
- Fixed the cursor getting stuck showing the wrong icon when moving over embedded content in the browser preview panel.
- Fixed the diff view not auto-collapsing generated build output (like dist/ or build/ folders) when it appeared at the top level of the repository.
- Fixed the Manage sessions table freezing or lagging when many sessions were shown at once.
- Fixed the pull request sidebar to show successful checks before neutral checks and to display skipped checks with a distinct icon instead of the generic neutral dot.
- Fixed the review panel resize handle so it can be dragged reliably across its full grab area.
- Fixed the run browser sometimes opening a server's login page instead of the URL containing the auth token, and fixed browser popup links doing nothing in chat sessions.
- Improved loading and scrolling performance on the Files tab for very large pull requests, keeping the file tree stable while it refreshes.
- Made the Manage sessions status filter respond immediately when toggling it with a large number of sessions
- Restarting a session no longer loses a queued prompt — it is restored to the composer instead.
- The model picker now shows the provider name next to duplicate custom models with the same name, so they can be told apart and found when searching by provider.

## v1.1.9

### Highlights

- You can now create, edit, and remove personal skills directly from Customize, with Markdown preview and validation.
- You can now update installed plugins from Customize or Settings, individually or all at once, and see each plugin's installed version.
- Files marked as generated are now automatically collapsed in the diff view and labeled with a Generated tag.
- Agents can now attach screenshots, diagrams, and recordings to pull request descriptions and comments without requiring staff access.
- Added the Shades of Purple color theme, available in both dark and light variants.

### Added

- Added the Shades of Purple color theme, available in both dark and light variants.
- Background agents now show their requested model, reasoning effort, and context size in the Background activity panel.
- Completed automation runs now show their duration alongside the timestamp.
- Files marked as generated are now automatically collapsed in the diff view and labeled with a Generated tag, so machine-generated changes don't bury the rest of the review.
- You can now create, edit, and remove personal skills directly from Customize, with Markdown preview and validation.
- You can now remove a queued follow-up message directly from the conversation.
- You can now update installed plugins from Customize or Settings, individually or all at once, and see each plugin's installed version.
- You can now use the Left and Right arrow keys to move between images when previewing an image attachment.

### Changed

- Agents can now attach screenshots, diagrams, and recordings to pull request descriptions and comments without requiring staff access.
- Aligned the session status indicators and empty-value placeholders in the My work table for a more consistent look.
- Moved the context window size next to the reasoning effort control instead of showing it on the model picker.
- Re-authorizing an existing GitHub account now uses a device code instead of an automatic browser sign-in: copy the code shown and paste it into the browser page that opens to finish signing in.
- Restored a compact "Last commit" option in the Changes commit dropdown, with the full commit history available on demand.
- Simplified the bulk delete sessions confirmation dialog with clearer, more compact copy and storage estimates.
- Simplified the warning text in the delete sessions dialog when deleting multiple sessions.
- Simplified trigger selection when creating automations that run in the cloud, grouping related triggers by subject with the specific event shown inline.
- Smoothed the open/close transition for menus, submenus, and popovers.
- Tables now scroll horizontally using the operating system's native scrollbar instead of a custom one.
- The model picker now shows all available context sizes for a model in one row, with token prices reflecting your currently selected context option.
- The pull request activity feed now merges related timeline events into a single row and collapses long runs of low-signal activity behind a disclosure.
- Workspaces now use a redesigned full-height right panel layout with compact titlebar actions and updated panel tabs by default.

### Fixed

- Automatic branch sync now honors the project's "update with rebase" setting instead of always creating a merge commit.
- Clicking a factory-owned agent now opens its full prompt and response history in the side panel.
- Collapsed sessions with nested sub-sessions now keep their activity indicator visible until you hover or focus the row.
- Fixed "Create PR" staying hidden for the rest of a session after its pull request was merged or closed, even after making further changes.
- Fixed a bug where a failed workspace session could silently retry and create a new session in the wrong directory instead of showing an error.
- Fixed a bug where accepting a session switch in one app window could navigate other open windows as well
- Fixed a bug where creating a new session on a remote environment (like WSL) without an initial prompt would incorrectly create the workspace locally instead.
- Fixed a duplicate "Review inline code" entry appearing in the conversation after posting an inline diff comment.
- Fixed a rare issue where the diff view could display the wrong line of code (and copy the wrong text) after re-rendering a file.
- Fixed an issue where a newly created pull request's description could be silently overwritten by a follow-up edit.
- Fixed automation gallery cards showing stray backslashes instead of the automation's prompt as written.
- Fixed Cmd+A (Select All) not working correctly in the integrated browser on macOS.
- Fixed completed background activity items sometimes failing to clear or clearing the wrong item after a session restart.
- Fixed diff search to correctly match queries with leading or trailing spaces and to stop returning matches from hidden hunk metadata.
- Fixed duplicate results appearing when searching for a pull request by number using "#" in the prompt box.
- Fixed find-in-page not finding text below the viewport in long markdown responses on macOS and Linux.
- Fixed Git operations failing on Windows when Git is installed via Scoop.
- Fixed GitHub issue and pull request links in a conversation appearing unresponsive when the workspace's local files were unavailable; they now open in your browser instead.
- Fixed in-document markdown links (like a table of contents) so clicking them scrolls to the linked section instead of doing nothing.
- Fixed inline review comments briefly disappearing, the viewport jumping, or an empty row flashing while new comments and replies loaded.
- Fixed issue and pull request pickers (like adding a sub-issue, dependency, or closing as a duplicate) sometimes showing "No matching issues." after searching in Quick Open.
- Fixed keyboard focus getting lost from the model picker's retry button when the window is resized
- Fixed muted text losing its color and becoming hard to read in some cases.
- Fixed onboarding's theme and sample repository suggestions being unevenly randomized, so all options now have a fair chance of showing up.
- Fixed pasted plain text (like Windows file paths) losing backslashes when pasted into the message composer.
- Fixed project changes (creating, renaming, or deleting a project) not always showing up in other open windows
- Fixed pull request review comments occasionally drifting, stacking at the top of a file, or overlapping diff rows when the diff updated while reviewing.
- Fixed pull request stack ordering and position indicator to match the order shown on GitHub.com.
- Fixed Quick Open so untitled chats, shown as "New chat", can now be found by typing that name.
- Fixed remote session diffs sometimes being clipped instead of filling the Changes view.
- Fixed repositories with an unusual or broken HEAD reference sometimes being treated as empty when added as a project, so sessions now correctly start with the repository's existing commits and files.
- Fixed run date headings on the Automations page showing the wrong day around daylight saving time transitions
- Fixed screen readers announcing extra button names when navigating skill rows in project settings.
- Fixed session titles automatically changing again after being renamed by the agent.
- Fixed sessions with a merged or closed pull request incorrectly showing as "Working" in the sidebar until clicked; they now appear under "Done" right away.
- Fixed sharing a secret gist showing a misleading "sign out and sign back in" message when GitHub actually refused for another reason, such as gists being disabled for Enterprise Managed User accounts; the app now shows GitHub's actual explanation.
- Fixed sign-in getting stuck when entering www.github.com or api.github.com:443 on the GitHub Enterprise Cloud sign-in screen.
- Fixed starting a session for a repository whose HEAD points at a missing branch, which previously created an empty session workspace instead of using the repository's existing commits.
- Fixed text selection in the diff view starting from the wrong spot in spaced file cards, and added Quote and Copy actions plus hoverable, modifier-clickable links for selected diff text.
- Fixed the "Add project" control being cut off the edge of the new session composer and impossible to click at narrow window widths.
- Fixed the add-account dialog hanging on "Copying code to clipboard..." when re-authenticating after a GitHub sign-in expired or was revoked.
- Fixed the app window rendering incorrectly after waking macOS with an external display connected.
- Fixed the automatic browser preview opening the wrong port (or nothing) when a Run script's dev server printed its address in less common formats.
- Fixed the Automations view freezing briefly when opening it with many workflows, each with several runs.
- Fixed the bookmark button shifting position in the response toolbar when bookmarking or unbookmarking a message.
- Fixed the chat composer dropping the first character and getting stuck when typing with certain IME input methods (e.g. Chinese, Japanese, Korean).
- Fixed the conversation view lagging briefly behind the composer when shrinking it, such as after deleting lines of text.
- Fixed the diff view so collapsing a file no longer causes an unexpected scroll jump, and a file revealed by search navigation stays open until you navigate to another match.
- Fixed the focus accent bar on comboboxes (command palette, autocomplete, and select menus) appearing on mouse hover; it now shows only during keyboard navigation.
- Fixed the integrated terminal failing to start Microsoft Store PowerShell on Windows
- Fixed the keyboard shortcut for selecting an option on a question so it works no matter which button in the prompt has focus.
- Fixed the keyboard shortcuts for switching between the Overview and Changes tabs in the pull request view, which never worked despite being advertised in the tab tooltips.
- Fixed the Local workspace branch picker to show all of the repository's branches instead of only the default branch.
- Fixed the markdown editor rewriting indentation of fenced code blocks you never touched when saving a file.
- Fixed the Markdown preview in the Files view losing its scroll position when the underlying file was refreshed in the background.
- Fixed the onboarding welcome and theme steps still responding to keyboard shortcuts (like starting sign-in or changing the theme) after keyboard shortcuts were turned off in Settings.
- Fixed the worktree location example in Settings > Sessions to correctly show a repository-relative path for custom templates anchored at the repository.
- Improved keyboard and screen reader support for expanding and collapsing items in the inbox.
- Outdated inline review comments in diffs can now be replied to and resolved instead of only offering delete, and stay anchored near their original content as the diff changes.
- Projects no longer disappear from the sidebar when all of their sessions are pinned.
- Quick Open no longer loses focus when a question from Copilot arrives while it's open; the first Escape now closes Quick Open instead of accidentally answering the question.
- Restored word-level highlighting for changed words on long lines in the diff view
- Screen readers now announce keyboard shortcuts for buttons like Comment, Reply, Save, and Create, instead of just the button name.
- Scrolling up to read earlier messages while a response is still streaming now stays in place, instead of being pulled back to the bottom.
- Softened the text selection highlight color in light GitHub themes so it no longer appears too strong.
- The Compare Changes view now shows a clear recovery action (Restore session or Retry) when a diff can't load because its underlying Git ref was changed or deleted outside the app, instead of a generic error.
- The Share as secret gist action is now shown as inactive with an explanation for Enterprise Managed User accounts, which cannot create gists.

## v1.1.8

### Highlights

- Chats now support Files, Plan, and background task tabs, with terminals and file mentions using the chat's actual working directory.
- Error toasts now include a View logs action that opens the full error details with a copy button.
- You can now configure supported reasoning effort levels for custom provider models in Settings, enabling the reasoning effort control for those models.
- A new keyboard shortcut (Cmd/Ctrl+Shift+.) jumps focus to the selection actions bar when items are selected in My Work or the sessions list.
- The conversation timeline now shows a "will change" notice as soon as you switch models or reasoning effort mid-turn.

### Added

- Added a keyboard shortcut (Cmd/Ctrl+Shift+.) to jump focus to the selection actions bar when items are selected in My Work or the sessions list, with Escape returning focus to where you started.
- Chats now support Files, Plan, and background task tabs, and terminals and file mentions use the chat's actual working directory.
- Error toasts now include a View logs action that opens a dialog with the full, selectable error details and a copy button.
- The conversation timeline now shows a "will change" notice as soon as you switch models or reasoning effort mid-turn, so your selection is confirmed before the agent finishes.
- You can now configure supported reasoning effort levels for custom provider models in Settings → Model providers, enabling the reasoning effort control in the composer for those models.

### Changed

- Made the file tree toggle icon-only and aligned it to the same side as the file tree in the Changes, Files, PR files, and file/Markdown editor views
- Renamed the "Cached" row in response details to "Context", which now clearly shows whether a response reused context, rebuilt the cache, or used no caching.
- Session startup now shows clearer progress, distinguishing repository preparation from starting the Copilot session.
- The trusted-source guidance in the Manage marketplaces dialog now uses the same visual style as the Add canvas from URL dialog.
- When mentioning someone in an issue or pull request comment, people already participating in the conversation (author, reviewers, commenters) are now suggested first, ahead of other repository members.

### Fixed

- Agent Merge now always replies to pull request review feedback inside the reviewer's comment thread and resolves it, instead of sometimes posting a separate top-level comment and leaving the thread unresolved.
- Cancelling a plan review (or pressing Escape) now stops the current turn without approving the plan.
- Clicking a plan action now submits it immediately instead of requiring a separate Continue click.
- Clicking Try again on a pull request description that failed to load now shows loading feedback instead of appearing unresponsive.
- Custom apps in the "Open in" menus can now be removed using only the keyboard.
- Fixed "/fork" discarding a trailing prompt — any text after "/fork" is now sent to the newly created forked session.
- Fixed "Delete empty sessions" not removing placeholder sessions whose local checkout folder was already missing.
- Fixed a bug where creating a new session could get stuck indefinitely if the connection was briefly interrupted; session creation now fails clearly and can be retried instead of hanging.
- Fixed a crash that could occur when opening the home view.
- Fixed a crash that could occur when pressing Enter inside a code block in the message composer.
- Fixed a deleted chat sometimes reappearing as a blank chat if it was deleted while it was still starting.
- Fixed a freeze on Linux where the app could hang indefinitely after certain crashes instead of closing.
- Fixed a message sent while reconnecting sometimes not showing session activity until a later event, which could make it look ignored.
- Fixed a misleading error when reopening a conversation failed but the conversation was still saved on your device — you'll now see a clearer message telling you to retry instead of a message that suggested it was lost.
- Fixed a session sometimes losing its history and turning into a new empty session when resuming it failed, instead of showing an error and keeping the history recoverable.
- Fixed a visual artifact where scrolling a list, such as My Work, showed a small notch next to the scrollbar on macOS.
- Fixed adding an enterprise account with a GitHub.com URL getting stuck on the device code screen instead of showing the code.
- Fixed an issue where a quick chat could repeatedly duplicate itself into new empty sidebar chats when it failed to resume.
- Fixed an issue where submitting a pull request review with a staged inline comment on a single line could fail and post none of the comments.
- Fixed coordinated sessions appearing stalled by notifying the parent session as soon as a child session's plan needs approval.
- Fixed crashes related to the file editor cursor position and keyboard shortcut handling.
- Fixed crashes that could occur when browsing extensions in the plugin catalog or filtering a large folder in the directory picker.
- Fixed custom keyboard shortcuts with Shift and punctuation (like Ctrl+Shift+,) being recorded and displayed incorrectly.
- Fixed deleting a session sometimes failing to fully clean up its workspace directory, particularly on Windows.
- Fixed dragging from a line number in the diff view or pull request Files view to start a line selection and open the "Ask about these lines" composer.
- Fixed file mentions with bracketed path segments (e.g. Next.js dynamic routes) getting truncated instead of resolving to the full path.
- Fixed find highlights flickering off and on with every keystroke while searching in a workspace conversation.
- Fixed focus outlines showing up during mouse use in menus, the command palette, autocomplete, and the select panel, and when opening Settings with a mouse click. The outline now only appears for keyboard navigation.
- Fixed forking a session in a project whose repository has no commits, which previously failed with a raw git error.
- Fixed Keep Awake sometimes not actually preventing the computer from sleeping while a session was running, even though the setting appeared enabled.
- Fixed large token counts overflowing outside the session information popover.
- Fixed Markdown file tabs sometimes showing stale content after an agent edits the file.
- Fixed MCP servers disabled in mcp-config.json incorrectly showing as enabled in Settings; affected servers now show their configuration state and can be edited to enable them.
- Fixed MCP servers in Customize briefly flashing a sign-in or error status on startup before reconnecting with cached credentials
- Fixed MCP servers that use OAuth sometimes not being available to the agent right after starting a new chat, even when already signed in.
- Fixed model selection in active sessions not reflecting repository allowlists; unavailable selections now switch to an allowed model and let you know when this happens.
- Fixed neutral surfaces (disabled controls, muted text, overlays, secondary buttons) rendering with an unintended pink tint in some themes.
- Fixed pull requests sometimes failing to load from a locally saved snapshot, and sped up issue descriptions appearing while the rest of the issue details continue loading.
- Fixed Quick Open and pull request/issue link resolution sometimes matching the wrong pull request or issue when a pasted URL contained hidden invisible characters in its number.
- Fixed reasoning effort unexpectedly changing when switching models
- Fixed remapped keyboard shortcuts using Space, plus, greater-than or asterisk so they work correctly instead of never firing (or, for asterisk, firing on every keystroke).
- Fixed restoring an archived workspace sometimes leaving the session stuck showing "Setting up workspace…" instead of becoming ready to use.
- Fixed selecting a range of lines in the diff view when the selection spans expanded context lines
- Fixed session and workspace names you renamed being overwritten by automatic title updates.
- Fixed sessions sometimes showing a stuck "Answer required" badge after finishing, most noticeably on agent-created child sessions.
- Fixed sign-in occasionally failing with a "Failed to fetch user info" error after a successful GitHub authentication.
- Fixed submitted pull request review comments reappearing as a pending review after reloading the app.
- Fixed the "Merge when ready" button showing a perpetual spinner when auto-merge could be enabled, now showing a stable merge icon instead.
- Fixed the /fleet command being unavailable when composing a new session; it now starts Fleet as soon as the session is created.
- Fixed the agent silently overwriting a pull request description that had changed since it last read it, so a conflicting edit now fails with a clear retry message instead of reporting false success.
- Fixed the app crashing on Linux when previewing a local file:// page in the embedded browser preview.
- Fixed the app window reopening at a smaller default size on macOS after quitting while maximized, instead of restoring maximized at the saved size.
- Fixed the Changes pill above the composer not reopening the Changes panel after it had been dismissed.
- Fixed the Changes view in linked worktrees not updating immediately after committing from a terminal or IDE outside the app.
- Fixed the conversation view sometimes staying scrolled away from the latest message after new content loaded, instead of automatically returning to the bottom.
- Fixed the Customize search box carrying over its query when switching between tabs.
- Fixed the expanded (fullscreen) view of a Mermaid diagram closing unexpectedly while chat content kept streaming in.
- Fixed the keyboard focus outline on the "Select all" checkbox in table headers being clipped and hard to see.
- Fixed the message composer losing focus when returning to a session that had a markdown file open.
- Fixed the model-change indicator so it stays pending until the current response truly finishes, instead of appearing to switch mid-turn.
- Fixed the pull request checks panel showing cancelled or skipped check suites as failures when they had no check runs.
- Fixed the pull request merge status to clearly show pending or awaiting required checks as a merge blocker instead of an endless loading state, and clarified the required checks summary text.
- Fixed the pull request timeline so Copilot code review activity is labeled as reviewing instead of appearing identical to Copilot coding work.
- Fixed the reviewers, assignees, and labels pills briefly disappearing and reappearing in the pull request view while details were still refreshing.
- Fixed visual artifacts appearing next to the scrollbar in the Manage Sessions table, and the My Work table cutting off columns instead of letting you scroll sideways to reach them.
- Fixed workspace auto-sync creating unnecessary merge commits and repeated sync loops after rewriting local commit history (e.g. amending or rebasing).
- Improved text selection contrast when using external color themes
- New sessions for multi-repository folder projects now include repositories added after the project was created.
- Newly pinned sessions now appear at the top of the pinned list instead of the bottom.
- Reduced the delay before large sessions become visible when resuming them locally by loading the most recent messages first and streaming older history in the background.
- Show the Outdated badge before the Resolved indicator in grouped pull request review thread headers
- Smoothed out Mermaid diagram previews while a diagram is still being generated, and fixed the expanded diagram view occasionally showing a diagram whose source didn't match its rendered image.
- The merge panel now explains when a pull request's required merge rules could not be verified, instead of showing an indefinite "Checking merge status" spinner.

## v1.1.7

### Highlights

- Ask a question in Side chat during a session to explore options without answering the original question yet.
- My Work now automatically detects when a repository was renamed or transferred on GitHub and updates your local project to match.
- Orchestrators can now create child sessions in a project's existing local checkout instead of always creating a new isolated worktree.
- PR creation now finds pull request templates in more locations, including the repository root and docs folder, not just .github/.
- Composer status pills (plan, background tasks, factories, loading widgets) no longer shimmer, keeping labels static while counts still update.

### Added

- Added an "Ask in Side chat" action to questions asked during a session, letting you explore the options in a Side chat without answering the original question yet.
- My Work now automatically detects when a repository was renamed or transferred on GitHub and updates the local project to match, so a stale repo name heals without reopening the branch picker.
- Orchestrators can now create child sessions that run in a project's existing local checkout instead of always creating a new isolated worktree.

### Changed

- Added visual separators to group related tabs in the Customize view for easier scanning.
- PR creation now finds pull request templates in more locations, including the repository root and docs folder, not just .github/
- Removed the shimmering animation on composer status pills (plan, background tasks, factories, and loading widgets) so labels stay static while counts and completion states still update.

### Fixed

- Copilot no longer navigates you to an archived chat that opens as a blank "New chat"; it now tells you the chat is archived and needs to be restored first.
- Fixed "Merge when ready" and "Queue when ready" incorrectly appearing on pull requests in repositories where auto-merge is disabled, which caused merging to fail.
- Fixed a bug where sending a message to an archived session could resume it outside its original project directory instead of prompting you to restore it first.
- Fixed a crash that could occur when the agent opened the browser preview with a malformed URL containing quotation marks.
- Fixed a crash when browsing a workspace containing recursive directory links, and stopped a spurious error from appearing after closing an Excel spreadsheet.
- Fixed a restored chat staying stuck with an "Answer required" badge after being archived while waiting on a response.
- Fixed adding private plugin marketplaces so you can sign in or switch GitHub accounts when authentication is needed, instead of the add hanging or failing with a generic error.
- Fixed an error when accepting a repository's configuration file from a new session's trust prompt before the session had been created.
- Fixed an issue where background updates to an open canvas document could steal keyboard focus away from the chat composer while typing.
- Fixed an issue where switching to or adding an account whose organization disabled the Copilot app could bypass the access restriction; the app now correctly blocks access whenever any signed-in account is restricted.
- Fixed an issue where the slash-command menu could briefly lose plugin commands right after a session started.
- Fixed buttons with a keyboard shortcut tooltip (like New chat, Send, Stop, and tab controls) not announcing the shortcut to screen readers.
- Fixed cloud task transcripts rendering the final answer above the tool calls that produced it instead of below them.
- Fixed committing changes when a branch workspace's checkout is in a detached HEAD state.
- Fixed completion summaries sometimes rendering as part of preceding tool activity instead of as their own row.
- Fixed copies made with Ctrl+C on Windows not appearing in the Windows clipboard history (Win+V).
- Fixed crashes that could occur when browsing very deeply nested directory trees or during onboarding on some browsers.
- Fixed editing and saving an MCP server in Settings from silently resetting its tool allowlist and working directory.
- Fixed Find (Cmd+F) not searching the pull request diff when opening a pull request's Changes tab from My Work without first clicking a file.
- Fixed image attachment thumbnails collapsing to an unreadably small size in some chat messages.
- Fixed keyboard focus in menus and pickers being nearly invisible by showing the standard accessible focus ring instead of a faint grey highlight.
- Fixed keyboard navigation in the My Work inbox becoming slow and dropping keypresses after loading more rows.
- Fixed Markdown previews (including Mermaid diagrams and read-only file previews) so their text can be selected and copied.
- Fixed middle-click paste (PRIMARY selection) on Linux for text selected in the diff view
- Fixed My Work briefly flashing a "Refreshing..." banner and shifting the layout during background data refreshes.
- Fixed opening a document canvas for a missing file silently creating a blank file instead of showing a load error.
- Fixed opening a plain folder that contains a single nested Git repository incorrectly using the nested repository as the project instead of the folder you selected.
- Fixed plan review feedback being lost when switching to another chat before sending it.
- Fixed pull requests disappearing from My Work when a background refresh moved them up the list.
- Fixed pull requests merged via the merge queue incorrectly showing a "closed this" event in the activity feed.
- Fixed reasoning effort and context window controls disappearing when the recommended model is shown instead of a previously selected one
- Fixed renaming a branch to a nested path (e.g. "feature/foo/bar") collapsing it into a single dash-separated name, and updated the rename branch action to show the branch name actually used.
- Fixed skills saved with a UTF-8 byte order mark not appearing in Automations or in workflow prompt autocomplete.
- Fixed submitting feedback from the app failing for accounts without permission to add labels, both when submitting directly and when using the prefilled GitHub issue fallback.
- Fixed the "What's new" card on Home getting stuck showing an old release after a failed refresh, instead of updating once the network recovered.
- Fixed the command palette becoming slow to respond when typing a search with a large number of workspaces or sessions.
- Fixed the Files pane not updating when the agent created, moved, or deleted files, so changes now show up without switching tabs.
- Fixed the Files tab changing its label and icon to match the selected file instead of staying labeled "Files" with a consistent folder icon.
- Fixed the focused view tab in My work scrolling out of view when reordering it with the keyboard.
- Fixed the hover highlight on extension rows in Customize so it no longer obscures the icon, name, description, and actions in high-contrast mode.
- Fixed the Markdown editor carrying over bold, italic, or code formatting when using the arrow keys to move out of a blockquote or code block
- Fixed the Markdown editor's Raw mode rendering source lines with extra spacing between them
- Fixed the merge button and merge drawer showing a generic "Merge blocked" state for pull requests that are behind their base branch, instead of offering the "Update branch" action.
- Fixed the merged pull request icon disappearing from a session in the sidebar once the session was no longer actively working and its local checkout had been removed.
- Fixed the message box to respect native spelling and text replacement preferences, so configured text replacements (like macOS shortcuts) now expand correctly.
- Fixed the mode selector icon overlapping the model icon in the composer toolbar at narrow window widths.
- Fixed the stop and cancel controls for background tasks and shells looking like checkboxes in some themes by using a filled stop icon.
- Fixed the terminal's text-selection highlight (and scrollbar) becoming invisible when the terminal's light/dark tone is set differently from the app's.
- Fixed the worktree branch picker not showing local branches created outside the shared clone, such as branches checked out in another editor or tool
- Fixed web search being unavailable in app sessions.
- Reopening a file tab now shows the file's latest content instead of a stale cached preview.
- Restored the native right-click menu (e.g. Paste) when right-clicking inside text inputs and rich text editors.
- Screen readers now announce the selected item count when selecting multiple items in My Work and Manage sessions
- Show an error message with a retry option in the sidebar when the session list fails to load, instead of leaving it blank.
- The pull request review panel no longer offers Approve or Request changes on your own pull requests, since GitHub doesn't allow authors to use those verdicts on their own work.
- Triple-clicking a line in the diff view now selects the whole line instead of a single word.
- Unsent prompts on the Home screen are no longer lost when the app restarts.
- Updated the search placeholder in Customize's All tab to indicate it searches MCP servers.

## v1.1.6

### Highlights

- Added controls to delete outdated local review comments and conversations from the Changes view without affecting GitHub review data.
- Pull request review comments now show an Outdated badge when their original code has changed, with a simplified file path label.
- Improved the Manage marketplaces dialog with clearer source rows, in-dialog error and progress feedback, and better focus handling.
- Sidebar and right-side panels now open and close instantly, without animation, keeping your conversation scroll position stable.
- Bulk-archiving sessions now prioritizes closed and merged pull request sessions first before archiving everything in a section.

### Added

- Added controls to delete outdated local review comments and conversations from the Changes view without affecting GitHub review data.
- Show an Outdated badge on pull request review comments whose original code has since changed, and simplify the location label to just the file path.

### Changed

- Archiving closed or merged pull request sessions from the sidebar now happens immediately, without a confirmation dialog.
- Bulk-archiving sessions grouped by date or status now prioritizes archiving closed and merged pull request sessions first, only falling back to archiving all sessions in a section when there is nothing completed to clean up.
- Improved the Manage marketplaces dialog with clearer source rows, in-dialog error and progress feedback, and better focus handling when removing marketplaces or their plugins.
- Issue and pull request timeline events now show clearer per-event icons, including a distinct closed icon for pull requests that were closed without merging.
- Moved the context window (long context) option into the reasoning picker in the composer, keeping the model details view focused on informational pricing details.
- Sidebar and right-side panels now open and close instantly, without animation, and keep your conversation scroll position stable.
- Simplified merge blocker messages for repository rules, required checks, and approvals to be more concise.
- Simplified the wording and layout of the storage and worktree location settings.

### Fixed

- "Open in Visual Studio" now opens the workspace's solution file instead of landing on the folder view.
- Editing a Markdown file with nested lists indented using something other than four spaces no longer rewrites the whole file's list indentation and adds stray backslashes on save.
- Fixed a blank conversation view when opening a child session immediately after creating it; a "Creating worktree..." progress indicator now shows until the session is ready.
- Fixed a bug in the Files tab where right-clicking a nested folder and choosing New file, New folder, Rename folder, or Delete folder could unexpectedly collapse its parent folder, hiding the resulting input field.
- Fixed a bug where enabling or refreshing plugins during an active session could break the session and cause subsequent messages to fail.
- Fixed a bug where the new automation dialog could get stuck showing "Loading tools…" indefinitely when cloud automation tools failed to load; it now shows the error with a retry option.
- Fixed a crash that could occur when attaching a file while the cursor was in certain positions in the prompt box.
- Fixed a double scrollbar in the outdated comments panel and improved spacing between comment groups from different files.
- Fixed a failed session archive removing the session from the sidebar even though it was never actually archived.
- Fixed a failing check's "Open on GitHub" action not opening when its log link couldn't be resolved safely, falling back to the pull request's checks page instead.
- Fixed a phantom media player showing up in the system tray/notification area on Linux.
- Fixed a session's sidebar status staying stuck on Done when the agent resumed work on its own without a new message from you.
- Fixed an issue on macOS where a file change in one folder could incorrectly be reported for a same-named file in a different folder.
- Fixed an issue on Windows where the app could fail to recover its local data after an unexpected shutdown or corruption.
- Fixed an issue where long-running responses could be stopped unexpectedly after conversation compaction happened multiple times in a row.
- Fixed an issue where switching models or manually compacting a conversation could incorrectly trigger the "compaction repeated too quickly" safety message on the next response.
- Fixed archiving or deleting a workspace on Windows sometimes failing because an open terminal was still using the workspace's folder
- Fixed crashes that could occur in markdown rendering, the Invertocat animation, and tab navigation.
- Fixed duplicate/ghost file headers appearing in the diff view around review threads until scrolling.
- Fixed extension canvas content in the right panel sometimes staying misaligned over the conversation after resizing the sidebar or panel layout.
- Fixed external links on Windows re-prompting after you dismissed a shell-open prompt, and added a copyable error toast when a link genuinely fails to open.
- Fixed external links sometimes silently failing to open on Windows by falling back to the system file explorer when the default launch method fails.
- Fixed GitHub issue and pull request links in automation run transcripts so they open in the run's side panel instead of doing nothing.
- Fixed inbox widget links pointing to github.com instead of the correct GitHub Enterprise URL for PRs and issues.
- Fixed issue and pull request labels sometimes showing the wrong color family (e.g. a pale yellow label appearing auburn).
- Fixed local-only branches not appearing as selectable base branches when creating a new workspace from an existing branch.
- Fixed removing a project appearing to do nothing while it deletes, which could let a second confirmation trigger duplicate deletion attempts. The project now disappears immediately with a status toast, and reappears automatically if removal fails.
- Fixed reopening a pull request that was previously closed getting stuck with a broken session instead of starting a fresh one.
- Fixed the bottom fade in the conversation view overlaying the last message when the transcript is scrolled to the bottom.
- Fixed the changed-files list briefly showing an empty state instead of loading while file changes were still being loaded.
- Fixed the chat transcript getting stuck and unable to scroll while text was selected.
- Fixed the cloud automation dialog blocking creation when no optional tools were selected, so automations relying only on built-in tools can now be created.
- Fixed the composer's slash-command skill menu getting permanently stuck and no longer showing newly available skills after a failed skill list refresh.
- Fixed the conversation and composer shifting and getting clipped when changing the app's zoom level on Linux.
- Fixed the Enterprise Cloud server address field getting stuck after a failed sign-in attempt, so you can correct and resubmit the address.
- Fixed the environment picker sometimes hiding "This machine" as an option after attaching an existing project's checkout on another environment.
- Fixed the header corners of a collapsed inline comment thread appearing disconnected from an open reply draft.
- Fixed the in-app feedback form incorrectly staying unavailable after switching from a managed account to a personal account.
- Fixed the Insights tab not appearing when clicking "View session insights" from the session title popover.
- Fixed the Manage sessions title overlapping the sidebar toggle when collapsed.
- Fixed the markdown editor endlessly widening a code span that contains only spaces every time the file was saved or reopened.
- Fixed the message edit box scrolling out of view or being hidden behind the composer when editing a chat message.
- Fixed the model picker sometimes resetting to "Select model" and losing the session's reasoning effort and context tier after switching models while a turn was in progress.
- Fixed the outdated comments panel overlapping or duplicating content in the diff view, and grouped multiple outdated comments for the same file under one heading.
- Fixed the plugin details dialog sometimes showing skills from the previously-viewed plugin when switching between plugins.
- Fixed the Terminal tab being unusable in a new local folder session until the first message was sent.
- Fixed unpublished pull request and issue comments being lost when navigating away and back.
- Launching the app again while it's already running now focuses the existing window instead of opening a duplicate instance.
- Links in assistant responses that point to files in your project now open in the Files panel instead of being stripped as invalid links.
- MCP server statuses in Settings no longer flicker to unauthenticated or failed while reconnecting after opening MCP settings or changing a server. Failed connections now show a clearer "Connection failed" message with full, readable error details.
- Screen readers now announce the default timeout hint when adding or editing MCP servers
- Uninstalling or disabling a plugin now stops its extension process instead of leaving it running in the background.
- When a commit fails or appears to hang because your signing key can't prompt for a passphrase, the app now explains what happened and how to fix it, instead of showing a raw git error or seeming to do nothing.
- WSL environment settings no longer appear on macOS and Linux, where they can't be used.

## v1.1.5

### Highlights

- Added a Resume button to the sidebar hover preview so you can resume interrupted or errored sessions without opening them.
- Closing the main window now keeps the app running in the background instead of quitting, with tray/dock support to bring it back.
- Pinned sessions in the sidebar can now be dragged into a custom order that persists across restarts.
- Hovering a link in a chat message now shows its full destination URL.
- Permission modes are now aligned with the CLI while keeping the app's existing slash commands like /permissions and /yolo.

### Added

- Added a Resume button to the sidebar hover preview for interrupted or errored sessions, so you can resume them without opening the session.
- Closing the main window now keeps the app running in the background instead of quitting. On macOS, closing hides the window and the Dock or tray restores it. On Windows/Linux, this is on by default when the system tray is enabled, with an opt-out setting under the tray settings.
- Hovering a link in a chat message now shows its full destination URL.
- Pinned sessions in the sidebar can now be dragged into a custom order that is remembered across restarts.
- Settings now has a skip link: tabbing from the search field reveals a control that moves keyboard focus past the navigation list straight to the panel content.

### Changed

- Aligned permission modes with the CLI while preserving the app's existing slash commands: use `/permissions manual|assisted|allow-all|show`, `/allow-all-tools on|off|show`, `/yolo on|off|show`, or `/reset-allowed-tools`.
- Improved the sidebar disk space banner so its graph segments and legend labels clearly match, with per-segment tooltips and a tighter compact layout.
- Permission prompts now show the specific reason a command wasn't automatically approved, instead of a generic message.
- The disk space banner's "Manage sessions" button now shortens to "Manage" at narrow sidebar widths so it stays legible alongside "Not now".

### Fixed

- Adding a local clone during onboarding now links the project to the repository you selected, instead of defaulting to your fork when it happens to be named 'origin'.
- Adding multiple projects at once (like selecting several repositories during onboarding) no longer navigates away from what you're working on as each one finishes importing.
- Chat sessions can now add Insights and installed extension canvases from the panel's Add tab menu, matching the workspace view.
- Custom worktree location settings that are rejected now show an inline error instead of failing silently.
- Expanding a message or tool row inside a background task's details no longer jumps the scroll position of the main conversation.
- Fixed a bug where certain shell commands with quoted flags could run without showing the expected permission prompt when "Always ask" was set.
- Fixed a bug where opening the terminal canvas with a command could run it without asking for permission.
- Fixed Agent Merge treating a required check that hasn't reported yet as passing, which could let merges proceed too early; it's now correctly treated as still pending.
- Fixed an intermittent issue on macOS where copying text, code, or images could occasionally fail or crash the app.
- Fixed background shells incorrectly showing as still running with a non-functional Stop action after restarting the app.
- Fixed crashes in the message composer that could occur when pressing Enter inside a code block or when switching away from a tab while editing a table.
- Fixed Ctrl+Arrow (Windows/Linux) not moving the caret by word inside composer code blocks
- Fixed extension canvases sometimes staying frozen behind a screenshot after closing a dialog like Settings.
- Fixed forking a conversation in a folder-based project, which previously failed.
- Fixed forking a session losing or corrupting changes to files tracked with Git clean filters (such as Git LFS).
- Fixed git clone and fetch failures on Fedora, RHEL, and other non-Debian Linux distributions by falling back to the system git when the bundled git can't load its libraries.
- Fixed keyboard focus being lost from the model or branch picker in the prompt composer toolbar when resizing the window or toggling the sidebar caused the toolbar to switch to its compact layout.
- Fixed Markdown images with explicit width/height being resized incorrectly, and images using legacy alignment attributes no longer appearing misaligned with adjacent text.
- Fixed missing tooltips on the "Change view" and "Filter actions" buttons in My Work when hovering or navigating with the keyboard.
- Fixed My Work list rows not opening when clicking the diff stats, comment count, or assignee avatars at the right edge of a row.
- Fixed nearly-invisible text selection highlighting in the GitHub dark theme.
- Fixed right-click selection menu not appearing when selecting text in background task details, so Copy selection works there like it does in the main conversation.
- Fixed Run scripts not being detected when a session's branch adds repository configuration that the default checkout doesn't have, and improved the empty-state message to explain why no Run scripts are available.
- Fixed starting a pull request or issue session for a repository accessed through a configured upstream remote, so it reuses the existing fork checkout instead of reporting the repository hasn't been added.
- Fixed switching the composer mode (e.g. from Autopilot to Plan) unexpectedly submitting the draft message instead of preserving it for editing.
- Fixed the AppImage failing to launch on some Wayland desktops.
- Fixed the composer occasionally showing the wrong permission mode (autopilot/ask before every action) right after resuming a session.
- Fixed the conversation view drifting away from the bottom after zooming out while pinned to the latest message.
- Fixed the conversation view getting out of sync when editing a message failed, so the message history now correctly reflects the actual state and an error is shown.
- Fixed the Files tab context menu so using "Copy path" on a nested file no longer collapses its parent folder.
- Fixed the home page's animated logo continuing to redraw indefinitely while idle, which caused unnecessary CPU and battery usage.
- Fixed the sidebar lagging behind the cursor while dragging its resize divider, so resizing now tracks the pointer smoothly.
- Fixed the sidebar stuttering and lagging behind the keyboard while its resize divider is adjusted with a held arrow key, so keyboard resizing is now as smooth as dragging.
- Fixed video previews getting stuck on Linux by showing a clear message with an option to open the file in your default app instead.
- Improved screen reader support for environment variable and header rows in MCP server settings, so each row is announced as a group and named after its variable or header.
- Restored the ability to fix unresolved review comments directly from a pull request's conversation tab.
- Screen readers now announce what each toggle in Settings > Accessibility controls (e.g. "Reasoning announcements") instead of just its bare name, even when the toggle is reached directly via Tab or a deep link.

## v1.1.4

### Highlights

- Navigate between related pull requests in a stack with a new stack menu, plus a stack summary in the merge drawer.
- Copilot can now create GitHub issues in a different repository than the current session.
- Customize where new session worktrees are created with a new Worktree location setting.
- Control whether agent-authored commits include a Co-authored-by trailer with a new Commit attribution setting.
- View and edit the milestone on issues and pull requests directly in the app.

### Added

- Added a Commit attribution setting under Sessions settings to control whether agent-authored commits include a Co-authored-by trailer.
- Added a one-click copy button for the session name in workspace and chat session information popovers.
- Added a stack menu next to a pull request's status to navigate between related pull requests in a stack, plus a stack summary in the merge drawer showing which pull requests will be included.
- Added a Worktree location setting in Settings > Sessions to customize where new session worktrees are created, using a path template with repository, branch, and name placeholders.
- Added an "Enable sound" toggle to the onboarding accessibility preferences dialog, so you can turn on notification sounds during setup.
- Cmd/Ctrl+click a quick chat in the sidebar to add it alongside sessions in the session grid.
- Copilot can now create GitHub issues in a different repository than the current session, not just the session's own repository.
- Right-clicking a session you've selected in the grid view now shows bulk actions (send, mark read/unread, archive, delete) for the whole selection.
- Settings > Sessions now shows file-backed instructions discovered from your system alongside the app-managed instructions, including their source path with copy and reveal-in-file-manager actions.
- The model-change notice can now be expanded to show which model you switched from and how much context was reused from cache.
- You can now view and edit the milestone on issues and pull requests in the app.

### Changed

- Forked sessions now appear as independent top-level entries in the sidebar instead of being nested under their source session.
- Improved the plan review experience: newly created plans now open automatically with the approval prompt focused, the plan panel shows a rendered checklist with search and an easy switch to edit the raw Markdown, and completed plans are clickable in chat history to reopen them.
- In the sidebar's group-by-project view, top-level sessions no longer show a redundant repository label on hover since they already inherit it from their project header. Nested sessions still show their repository label.
- Increased the contrast of selected-state backgrounds for a clearer visual highlight.
- Session history now loads faster by reading the transcript from disk immediately instead of waiting for the agent to resume.
- Smoothed out scrolling while tool calls stream in with Balanced verbosity, so the view stays anchored to the bottom, scrolling up to review earlier tools isn't interrupted, and edge fades transition more gradually.
- The composer's empty placeholder text now mentions typing "&" to reference other sessions.
- The credits usage notification is no longer shown when you have a bring-your-own-key or local model configured.
- The Plan tab now uses the standard plan review experience by default; you can still opt into the canvas rich text editor for plan.md in settings.

### Fixed

- Agent merge now shows a status message when it's paused waiting on a commit status check, instead of silently parking with no explanation.
- Archived pull request diffs that were previously blank or missing now show correctly when possible, or a clear explanation when the underlying changes can no longer be recovered.
- Checking for updates in Settings > General now announces status to screen readers, and the check button stays keyboard-reachable while a check is running.
- Comment boxes (like inline review replies and draft review threads) now correctly receive keyboard focus when they open, so typing immediately after opening no longer gets lost.
- Completed pull requests and issues no longer linger in the home page's Up next section.
- Expanding a composer pill panel (like queued messages or background activity) no longer shifts the chat history.
- Fixed a bug in the canvas editor where saving a file containing an image with backslashes in its alt text (such as a Windows-style path) would corrupt the alt text a little more with every save.
- Fixed a bug where a custom storage location directory named "worktrees" or "copilot-worktrees" could be incorrectly altered when saved.
- Fixed a bug where clicking the model picker could submit your draft message instead of opening the picker.
- Fixed a bug where commands run through `env` could bypass the shell command permission prompt.
- Fixed a bug where newly added skills didn't show up in the `/` autocomplete menu until a session started or the app was restarted.
- Fixed a bug where sending a message while the assistant was responding could leave your message displayed below the assistant's reply instead of in chronological order.
- Fixed a confusing browser permission prompt that could appear when reading the clipboard on Windows.
- Fixed a crash in the terminal that could occur after the graphics context was lost.
- Fixed a crash that could occur when resuming a session with very large files in its artifacts; oversized files now show a clear "file too large" message instead.
- Fixed a crash that could replace the entire app with an error screen when typing certain search terms (like "constructor:") into a filter query, such as in My work or the cloud automation trigger filter.
- Fixed an issue where pressing Stop while a follow-up message was queued sometimes required pressing Stop a second time before the session became idle.
- Fixed archived workspaces sometimes showing a file count with a diff that never loads by falling back to the last saved diff when it can no longer be reconstructed.
- Fixed branch renaming so the configured branch prefix is no longer applied twice when Copilot renames a session's branch.
- Fixed child sessions sometimes showing an incorrect model, reasoning effort, or context size in the composer instead of the configuration inherited from the parent session.
- Fixed clones of the same repository sharing sidebar labels and settings, which could merge their sessions or route actions to the wrong clone. Clones with the same name now show distinct, path-qualified labels.
- Fixed collapsed resolved and staged review comment threads showing an unnecessary "Outdated location" banner, keeping the collapsed row compact.
- Fixed conversation compaction sometimes getting stuck in a repeating loop that could run indefinitely; affected turns now stop automatically with guidance to resend the message.
- Fixed copying selected text in the read-only file viewer, which previously copied nothing to the clipboard.
- Fixed emoji in the integrated terminal being measured too narrow, which shifted the rest of the line and broke alignment in tables, box-drawing layouts, and similar output.
- Fixed extra vertical spacing on session communication entries like "Received message" and "Read session" in the conversation view.
- Fixed keyboard and screen reader navigation for clickable list rows so their action buttons can be reached and activated independently.
- Fixed keyboard shortcuts silently stopping when focus was on a tab's close button, such as switching tabs or submitting a pull request review.
- Fixed noticeable lag when viewing diffs containing very long lines (like long strings or near-minified code), which could take over a second to syntax highlight.
- Fixed pasted URLs with underscores being incorrectly converted to Markdown emphasis in the composer
- Fixed plugin-provided skill slash commands failing with an "Unknown slash command" error
- Fixed pressing Escape to close the provider dropdown during onboarding's model provider setup from discarding the whole form, including a typed API key.
- Fixed pull requests incorrectly showing as mergeable when they actually had merge conflicts.
- Fixed reasoning effort incorrectly defaulting to "None" for some models when starting a new session.
- Fixed right-click context menus not appearing for files and folders in the Files tab
- Fixed screen readers announcing extra button text when navigating the notification sound picker and the "Open in" app menus, so each option is now announced clearly.
- Fixed screen readers not reading the helper text next to the auto-update toggle and the Suggestion cards Restore button in Settings, and fixed focus loss and missing confirmation when restoring suggestion cards.
- Fixed shell commands sometimes never running in terminals using a customized shell prompt.
- Fixed skill directories configured in config.json or settings.json being ignored when the file contained comments or trailing commas
- Fixed skill directories from config.json or settings.json not being recognized when the file started with a UTF-8 byte order mark.
- Fixed stuttering when scrolling wide file diffs sideways in the conversation view.
- Fixed the "Add Enterprise account" form in Settings so an invalid server address is announced to screen readers, and an empty submission now explains what to fix instead of doing nothing.
- Fixed the /compact command sometimes showing no progress or result, or requiring a second run to display feedback.
- Fixed the app launching to a blank window on some Linux systems due to a font-rendering crash triggered by certain color emoji or monospace fonts.
- Fixed the completion summary at the end of a task being incorrectly grouped with the preceding tool call.
- Fixed the conversation view growing and jumping when a long sequence of tool calls runs in Balanced verbosity mode by keeping the live tool list scrollable until it settles.
- Fixed the find-in-chat popup overlapping and covering the chat header buttons.
- Fixed the Fix action getting stuck on "Working on a fix..." for pull request review comments authored under your own account, including feedback from your review agent.
- Fixed the Markdown file editor sometimes overwriting newer changes made to a file on disk while the editor still held older content; it now shows the reload-or-keep-local-changes prompt instead.
- Fixed the merge drawer sometimes hiding auto-merge and showing a direct merge action instead while merge requirements were still loading.
- Fixed the model picker sometimes showing the wrong model after a switch failed while a session was reconnecting.
- Fixed the onboarding Repositories step's Retry keyboard shortcut so it no longer intercepts letters typed into search or dialog fields, disappears once the Retry button is gone, and respects the "Use keyboard shortcuts" accessibility setting.
- Fixed the pull request tab not resolving correctly for sessions linked to a private security advisory fork.
- Fixed the resize divider between split panes so dragging anywhere along it resizes the split, instead of only the top half responding.
- Fixed the scroll wheel not scrolling the command menu (/, @, #, or session) when the pointer stayed over the prompt composer's text box.
- Fixed the Up Next list on Home sometimes showing the same pull request twice.
- Fixed workspace/worktree setup failures (such as a failing Git command) being mislabeled as an "invalid argument" error, so the message now correctly describes it as a workspace initialization failure.
- Long branch names in the pull request header no longer wrap to a second line; they now truncate with the full name available on hover.
- Pinned sessions are now protected in Manage sessions: their checkbox is disabled and "select all" no longer includes them, preventing accidental bulk archive or delete. Also added a "Manage sessions" launcher in Settings > Sessions.
- Scheduled workflows no longer fail permanently when a transient network error occurs while starting the session; they now retry briefly before giving up.
- Sessions stopped by a network or service error now show a Failed status in the sidebar instead of appearing idle.
- Settings > Skills now lists skills defined in your repository's .github/skills/ directory instead of showing them as not found.
- Show a clear error message when creating a session from a pull request fails because GitHub couldn't be reached or the pull request couldn't be loaded.
- Typed answers to agent questions are no longer lost when navigating away from and back to a session.
- Use a stop icon for the button that stops a running background shell, so it no longer looks identical to the panel collapse action.
- Windows integrated terminals now pick up PATH and environment changes from your PowerShell profile, so tools like fnm-managed Node versions work without restarting the app.

## v1.1.3

### Highlights

- You can now request Copilot code reviews and re-request reviews from reviewers who have already responded.
- Pull requests that are part of a stack now show stack status and can be merged together as a stack from the merge drawer.
- Pull request views now show when a pull request is in the merge queue, including its queue position, with the option to remove it.
- A new `/side` slash command lets you open a side chat for a parallel question without interrupting the main conversation.
- When using Auto, completed responses now show which model was actually used, plus AI credits and cache details when available.

### Added

- Add a `/side` slash command to quickly open a side chat for a parallel question without interrupting the main conversation.
- Added a setting to control whether Shift+Tab cycles agent modes in the composer, so screen reader and keyboard users can restore native backward focus navigation.
- GitHub Copilot now appears automatically as a read-only model provider in the Model Providers settings when you're signed in with an active Copilot seat.
- If GitHub Copilot fails to start, it now shows a diagnostics dialog letting you copy details or open the log file instead of leaving you with a blank window.
- Local repository text and code files opened in a file tab or the Files viewer can now be edited directly, with changes automatically saved.
- Plan tabs can now be closed and restored from the Add tab menu in the full-height right panel layout, matching Changes and pull request tabs.
- Precise cross-row text selection and copying in diffs is now enabled by default, with an option to fall back to native browser selection if diff scrolling or selection feels slow.
- Pull request views now show when a pull request is in the merge queue, including its queue position, and let users with write access remove it from the queue.
- Pull requests that are part of a stack now show stack status and can be merged together as a stack from the merge drawer.
- When using Auto, completed responses now show which model was actually used, plus AI credits and cache details when available.
- You can now request Copilot code reviews and re-request reviews from reviewers who have already responded.

### Changed

- @-mention suggestions in comments now prioritize people already participating in the issue or pull request, such as the author and commenters.
- Cancelled checks now show a muted alert icon instead of a red failure icon, matching GitHub.
- Collapsed tool call groups no longer show a failed-call count in the summary; failure details still appear when the group is expanded.
- Files now open immediately when clicked, without a delay. Use Cmd/Ctrl-click to open a file in a new tab.
- Issue conversations now load progressively, with comments and timeline events streaming in as they arrive instead of waiting for everything at once. Issues with very large comment threads no longer get cut off.
- Large sessions now open faster by showing the most recent messages first while older history streams in the background.
- Pull request file diffs now appear progressively as they load, instead of waiting for the entire diff to be ready before showing anything.
- Removed the dropdown caret from the project, workspace type, and branch selectors in the new session composer for a cleaner look.
- Removed the metadata status bars (start time, duration, output summary) shown below tool calls and reasoning steps in the conversation timeline.
- Right panel tabs are easier to scan, close, and restore, with clearer close controls, adaptive label widths, and support for a narrower panel.
- SQL tool calls now show a human-readable summary in the conversation timeline instead of the raw query, which remains available in the expanded details.
- The Changes tab now uses a simpler diff icon in the full-height right panel layout.
- The file tree in the Files tab now starts at its minimum width by default, leaving more room for file content.
- The review panel can now be resized down to 25% of the workspace width, and the 25% width preset now works correctly.
- Updated the icon for Interactive mode in the prompt composer to a conversation glyph.

### Fixed

- Automations now correctly use the saved Long Context model setting when they run on schedule.
- Copying a selection from inside a code block now copies the raw text instead of converting it to markdown links.
- Ctrl+Enter now submits the kickoff prompt in the Sessions widget on Windows and Linux, matching Cmd+Enter on macOS.
- Fixed "Copy path" on files in the artifact tree copying only the file name instead of the full file path.
- Fixed "Create PR + agent merge" sometimes creating the pull request without actually turning on agent merge, especially when navigating away while the PR was being created.
- Fixed @ file mentions showing "No matching files" on Home and other pre-session composers when a project's files had loaded.
- Fixed a brief "Thinking" row flashing and disappearing in the conversation timeline before an agent's response started streaming.
- Fixed a brief flash of "No changes to compare" before a session's diff finished loading.
- Fixed a brief layout jump when responding to a permission prompt or resuming an interrupted session, so the composer settles into its final size immediately.
- Fixed a bug where a background session delivering a message could switch your active chat or side chat and steal focus while you were typing elsewhere.
- Fixed a bug where deleting a project while one of its sessions was still starting up could leave the app unable to close, stuck warning about an agent working in a project that no longer existed.
- Fixed a bug where deleting a session or workspace could silently discard uncommitted work in certain repository setups instead of preserving it.
- Fixed a bug where editing a markdown file could unintentionally remove backslash escapes on unrelated lines, causing escaped characters like headings, lists, quotes, and HTML tags to render incorrectly after saving.
- Fixed a bug where entering a branch name starting with a dash (e.g. "-D") when creating a worktree could silently delete an existing local branch instead of creating the new one.
- Fixed a bug where toggling a skill in Settings could silently re-enable a different skill you had previously disabled.
- Fixed a crash that could occur in the diff view when reviewing changes with an open comment draft while the diff was still updating.
- Fixed a crash that could occur when a message arrived while closing a session.
- Fixed a crash that could occur when deleting a table from the rich text composer.
- Fixed a crash that could replace the whole app window with an error screen when a code block's language label was "__proto__".
- Fixed a layout shift when a session loaded file-edit rows, where the row now appears in its final position immediately instead of shifting after diff stats loaded.
- Fixed a rare issue on Linux where the app could crash or hang and require a full relaunch to reconnect.
- Fixed a rare issue where the first message in a new session could fail to send, requiring you to manually resend it to continue the conversation.
- Fixed a small layout shift in sent user messages as they transitioned from pending to sent.
- Fixed adding two repositories with the same name from different organizations so each gets its own checkout instead of one add failing or pointing at the wrong repository.
- Fixed Agency falling out of date for users who don't run it directly in a terminal, by keeping it updated in the background when Agency mode is enabled.
- Fixed an issue where pressing Escape while typing in a Settings field (such as custom instructions, the branch prefix template, or the environments base path) could discard your edit instead of saving it.
- Fixed an issue where responding to certain agent prompts (choice selections or custom text answers) could leave the conversation stuck instead of resuming.
- Fixed an issue where sessions could get stuck asking for approval on every tool call instead of remembering your auto-approve preference.
- Fixed an issue where the "Expand up"/"Expand down" buttons in the diff view could occasionally fail to appear.
- Fixed an issue where the agent could automatically merge a pull request while its checks were still running or failing.
- Fixed automation card titles always showing a pointer cursor on hover, even when the "Show pointer on hover" accessibility setting was disabled.
- Fixed automation runs sometimes staying stuck showing as running after they had already finished.
- Fixed code blocks breaking in the markdown editor when opening files with Windows-style (CRLF) line endings
- Fixed conversation rows briefly overlapping earlier messages when opening a session's history.
- Fixed conversation rows sometimes overlapping after resizing the workspace split pane.
- Fixed editing an MCP server with an argument containing spaces silently corrupting its argument list when saved without changes.
- Fixed existing sessions failing to reopen when an organization policy disables unattended tool approval; the session now resumes with prompts enabled instead of getting stuck.
- Fixed folders in the Files tree not being collapsible or re-expandable while a filter is applied.
- Fixed follow-up text unintentionally appearing bold after quoting a bolded reply in the composer.
- Fixed hidden overflow-menu and row-action buttons in settings and other lists incorrectly capturing taps on touchscreens.
- Fixed inline review comments and replies so text with angle brackets (like `Array<string>` or `<summary>`) displays exactly as typed instead of being misread as HTML.
- Fixed inline review comments sometimes moving to the wrong line or disappearing when the diff changed while a draft review was open.
- Fixed keyboard focus getting stuck when Tab or Shift+Tab was pressed while an image preview was open.
- Fixed misaligned branch labels in the session branch popover
- Fixed model-change notices showing a stale reasoning effort after switching to a model that doesn't support configurable reasoning.
- Fixed new right panel tabs (like Insights) sometimes appearing in the middle of the tab bar instead of after existing tabs
- Fixed pressing Page Up or Page Down while typing in the prompt box scrolling the conversation view instead of scrolling within the prompt.
- Fixed pull request activity not loading further pages after opening a pull request that was previously prefetched by hovering or focusing it.
- Fixed pull request checks incorrectly showing as passing when a workflow failed before creating any check runs.
- Fixed pull request checks incorrectly showing pending or in-progress workflows as having failed to create check runs.
- Fixed references (like pull request or file mentions) in your messages showing as raw markup instead of chips.
- Fixed session and workspace names showing raw reference markup instead of the slash command text when starting a session with a repository skill.
- Fixed session deletion sometimes failing with a git timeout error on large or slow worktrees, and made the error clearer when it still occurs.
- Fixed sessions failing to start when an organization's policy disallows Approve all mode; the app now falls back to Ask every time and shows a warning explaining why.
- Fixed skills that are only invokable by the user (not by the model) failing to run when selected from the composer's skill suggestions.
- Fixed the "Connect your repositories" onboarding step not submitting when the app window was narrower than 768px, which previously advanced to the next step without cloning repositories or saving the storage location.
- Fixed the agent repeatedly re-engaging on a pull request as if there were new comments to review when there weren't any.
- Fixed the app briefly freezing when expanding a large file diff in a tool call.
- Fixed the app freezing for minutes when a slow or throttled git host caused the new-session branch picker to block other git operations in the same project.
- Fixed the Changes file tree sometimes missing files that were added while the Changes tab wasn't active.
- Fixed the Changes panel sometimes going blank and staying blank for the rest of the session after a brief git error, even though your edits were still there.
- Fixed the chat area not spanning the full width of the pane when the full-height right panel layout is enabled and the review panel is closed.
- Fixed the chat transcript visibly jumping or collapsing back to the recent tail while older history was still loading in large sessions.
- Fixed the cloud automation edit dialog getting stuck on a loading spinner when the automation's details failed to load. It now shows the error and lets you retry.
- Fixed the context-window usage bar in the session title popover appearing as a tiny stub instead of a full-width bar
- Fixed the conversation shifting left when the timeline first appeared in the full-height right panel layout with the review panel closed.
- Fixed the conversation view briefly shifting up and down when returning to a previously viewed session.
- Fixed the diff view not immediately reflecting changes after saving edits in a file tab.
- Fixed the diff view showing no changes for tracked files when your git configuration changes how diff headers are formatted
- Fixed the diff view's "expand context" and "expand full file" controls sometimes showing the wrong or truncated lines when a committed diff's file had uncommitted changes on disk.
- Fixed the edit and remove buttons on an MCP server row in Settings staying visible after clicking its enable/disable switch, instead of hiding again once you moved the pointer away.
- Fixed the initial message of a new session briefly appearing below live agent activity while the session was starting.
- Fixed the markdown editor rewriting untouched table rows (adding extra escaping to backslashes and special characters) whenever any part of the document was edited.
- Fixed the merge drawer sometimes staying stuck in a checking state for a stacked pull request even after it was ready to merge.
- Fixed the merge when ready toggle sometimes reverting to an older state when rapidly enabled and disabled.
- Fixed the permission prompt sometimes denying a tool request or dismissing the prompt when confirming a candidate in an IME (such as Japanese, Chinese, or Korean input) while typing a denial reason.
- Fixed the plan reply box submitting the reply prematurely when pressing Enter to confirm an IME (Japanese, Chinese, Korean) input candidate.
- Fixed the Plan tab sometimes showing an empty state or staying open when a session had no plan or to-dos.
- Fixed the Plugins, Skills, MCP servers, and Themes tabs in Settings overflowing horizontally and hiding controls (like the Install button) at narrow window sizes or high zoom levels.
- Fixed the pull request tab incorrectly showing "No pull request description provided." when the description simply failed to load; it now shows a retry option instead
- Fixed the reasoning-effort gauge needle in the composer toolbar appearing detached from its pivot at higher zoom levels.
- Fixed the repository picker showing identical names for multiple checkouts of the same repository.
- Fixed the review panel feeling unresponsive or slow to open, especially the first time it's opened in a workspace.
- Fixed the spacing and styling of commentless review approvals in the pull request activity feed so they align with the surrounding timeline events.
- Fixed the timeline label for SQL queries so it shows the query's description instead of a generic, duplicated label.
- Fixed the What's new preview on the Home screen mangling identifiers with underscores (like function or error names) into unreadable, unsearchable text.
- Fixed unread session indicators not persisting after restarting the app.
- Grok models now show the xAI logo in the model picker instead of a generic icon, and are no longer mislabeled as a hidden model in Streamer Mode.
- Improved extension canvas behavior when session is stopped
- Improved performance when switching into sessions with multiple open tabs in the right panel, such as large diffs, terminals, or markdown files.
- In Balanced verbosity, tool calls now stay visible while running and only collapse into a summary once the agent's work settles, with a smoother transition and no more placeholder labels on file edit rows.
- Links to a Copilot session now work even when that session isn't set up on this device yet. You'll be asked whether to add its project, then taken straight into the session.
- Marking a draft pull request ready for review now transitions directly to the merge action, without briefly flashing back to "Ready for review".
- Merge stack rows now show the correct pull request status icon and badge (open, draft, merged, closed, or queued) instead of always looking open.
- New automations now default to the same local repository or worktree preference used for new sessions, instead of always defaulting to a new worktree.
- Opening a file with Go to File now reveals and selects it in the Files tree, expanding its parent folders.
- Pasted images are now forwarded to nested sessions created from the "Create nested session" dialog, instead of only being described in text.
- Pressing Enter at the end of inline code (like a file name in backticks) in the prompt composer now sends the message instead of inserting a newline.
- Pull request approvals and change requests without a comment now appear in the activity feed.
- Reduced CPU usage on Linux caused by the animated Invertocat on the Home page.
- Refined the full-height right panel layout: tabs now size to fit their label, and the close button no longer overlaps the tab text.
- Repository dropdowns no longer show a duplicate row when the same repository is checked out in more than one folder.
- Restored the microphone and dictation option in the new session dialog, and disabled the Create button until dictation finishes
- Restored the Started, Duration, and Output details inside expanded individual tool call results.
- Reworked the "View usage and plan…" action in the credits usage popover: dropped the misleading chevron (it doesn't drill into a submenu), aligned the label with the Settings destination it opens, and matched the row's chrome to the app's standard menu-item pill.
- Running shell command labels now shimmer consistently with other in-progress tool actions.
- Sessions that stall or lose connection while a tool is running are now detected and shown as interrupted, instead of appearing to work forever.
- The health check now reports the configured Storage location for repos instead of always showing the default directory.
- The health check page now shows a warning instead of a false green "OK" for the GitHub CLI or Git rows when their version could not be determined.
- The low-disk-space banner now refreshes when the app window regains focus and periodically while disk space is low, so it no longer stays stale after space is freed.
- The terminal for a new session now shows a "Setting up workspace..." state instead of a dead-end "Terminal unavailable" error while the workspace is still being created.
- Updated the Accessibility icon in the Settings sidebar to match the stroke weight of the other section icons.

### Removed

- Removed the option to disable custom text selection in diffs — precise cross-row selection and copying is now always on.

## v1.1.2

### Highlights

- GitHub Copilot now appears automatically as a read-only model provider in Model Providers settings when you have an active Copilot seat.
- Cloud automation triggers with a query field now use the same smart search filter input as issue triggers, with qualifier autocomplete and hints.
- The default model selection now matches what's actually available to your account instead of always defaulting to a fixed model.
- The Impeccable design skill got a major upgrade, adding native iOS and Android design guidance and a new doctor command for diagnosing setup issues.
- WSL remote environments now include GitHub pull request and issue workflow skills, plus more reliable remote session connections.

### Added

- GitHub Copilot now appears automatically as a read-only model provider in the Model Providers settings when you're signed in with an active Copilot seat.

### Changed

- Cloud automation triggers with a query field, like pull request opened/synchronized/merged, now use the same search filter input as issue triggers, with qualifier autocomplete, placeholders, and hint text.
- The default model selection now matches what's actually available to your account instead of always defaulting to a fixed model.
- Upgraded the Impeccable design skill to a new major version, adding native iOS and Android design guidance, a new doctor command for diagnosing setup issues, and refined design review workflows.
- WSL remote environments now include GitHub pull request and issue workflow skills, along with reliability improvements to remote session connections.

### Fixed

- Copying a selection from a chat response now preserves rich formatting, including tables, when pasting into apps like Slack, Teams, or Word.
- Custom agents defined only on a branch or worktree now appear correctly in the agent picker and /agent autocomplete for that session.
- Fixed a layout shift when opening an issue or pull request in My Work, where the assignees, reviewers, and labels controls would pop in and shift the toolbar after loading.
- Fixed a stuck "waiting for review" state on a session's plan when a parent session approved or rejected it.
- Fixed an empty progress bar appearing under the app's Dock icon on macOS while an agent turn is running.
- Fixed an issue where the app could fail to open (icon appeared but no window) or repeatedly show onboarding to already set up users.
- Fixed Copy (⌘C/Ctrl+C) sometimes clearing the clipboard instead of copying the selected text.
- Fixed janky window resizing when a chat session is open and scrolled into its history.
- Fixed the sidebar sometimes opening collapsed on startup and saved inbox sections not persisting between restarts.
- Fixed URLs typed in the composer getting broken by stray backslashes (e.g. before underscores) when sent or rendered.
- The reasoning effort you pick for a session now sticks, instead of reverting to Medium when you resume the session or restart the app.
- The selection popup in the chat transcript no longer flashes at the top-left corner when dismissed, and copying selected text now keeps it highlighted instead of clearing the selection.
- Timestamp reveal buttons on relative times (e.g. "3h ago") now announce "show timestamp" to screen readers instead of the generic "more info".
- Timestamps in the activity feed are now accessible disclosures that keep their visible relative time and reveal the exact date when activated.

## v1.1.1

### Highlights

- Added a toggle in the Files tab to show or hide hidden files (like .env) normally excluded by .gitignore.
- Large sessions now open much faster, with older messages loading in the background instead of freezing the app.
- Pull requests with many comments and reviews now load faster in the conversation and diff views.
- Press Shift+Tab in the message composer to cycle between Plan, Autopilot, and Interactive modes.
- Fixed agent merge not actually merging pull requests after being enabled.

### Added

- Added a toggle in the Files tab to show or hide hidden files (like .env) that are normally excluded by .gitignore.

### Changed

- Auto now appears as a switch at the top of the model picker with its own summary, and older model versions are grouped into a Previous models section so current models are easier to find.
- Large sessions now open much faster, with older messages loading in the background instead of freezing the app.
- Press Shift+Tab in the message composer to cycle between Plan, Autopilot, and Interactive modes.
- Pull requests with many comments and reviews now load faster in the conversation and diff views.

### Fixed

- Autopilot mode now stays selected after the agent finishes a task instead of automatically switching back to Interactive.
- Business, Enterprise, and GHES sign-in no longer gets blocked because of the Copilot CLI policy; access is now based on whether your organization has the Copilot app enabled.
- Comment and review thread timestamps can now be activated to reveal the exact date and time, with an accessible label that matches the visible relative time.
- Fixed a crash that could occur when copying text with ⌘C.
- Fixed a delay showing the added/removed line counts on the Changes tab when opening large pull requests.
- Fixed agent merge not actually merging pull requests after being enabled, and made a previous merge opt-in carry over to new pull requests.
- Fixed crashes when pasting text into the composer and when displaying reasoning text containing many inline code spans.
- Fixed keyboard and screen reader focus landing on the Settings dialog instead of the opened panel's heading when opening Settings directly to a specific panel.
- Fixed keyboard focus not returning to the usage gauge button after closing Settings opened from its "View plan & usage" link.
- Fixed the "Create from" dialog briefly showing a "no results" message while a pasted pull request or issue URL was still loading.
- Fixed the Created and Updated timestamps in the My Work table view so screen readers announce the visible relative time before the full date when opened.
- Fixed the diff toolbar overflowing in narrow panels by collapsing the update branch action, uncommitted label, and commit navigation controls gracefully as space shrinks.
- Fixed the keyboard focus indicator being invisible when tabbing to a collapsed comment in the Files changed view.
- Fixed the updated-at timestamp on My Work board cards so it correctly announces the relative time and reveals the exact date when activated, instead of only announcing the exact date.
- Page Up/Down, Home/End, and arrow keys now scroll the pull request and issue overview panes and the diff view.
- Screen readers now announce relative time labels (like session reset countdowns and timestamps) with full words instead of spelling out abbreviations.

## v1.1.0

### Highlights

- Session grid, side chats in the review panel, and automatic session renaming to the pull request title are now available to all users.
- Added `has:` and `no:` search qualifiers to the My Work filter, letting you filter issues and pull requests by label, assignee, milestone, project, type, sub-issue, or parent issue.
- Mathematical notation written in LaTeX now renders as formatted math in chat responses.
- Added a "Share as gist" action to the session panel to quickly upload a session's debug logs as a secret gist.
- Cloud automation dialogs now support additional trigger types and let you require the triggering actor to have write access to the repository.

### Added

- Added `has:` and `no:` search qualifiers to the My Work filter, letting you filter issues and pull requests by whether they have a label, assignee, milestone, project, type, sub-issue, or parent issue set.
- Added a "Share as gist" action to the session panel to quickly upload a session's debug logs as a secret gist.
- Added a low disk space warning banner in the sidebar to alert you when local sessions are likely to run out of disk space.
- Added Catppuccin Macchiato and Catppuccin Mocha theme options, and renamed the existing Catppuccin theme to Catppuccin Frappé.
- Agents can now edit a previously staged PR review comment instead of creating a duplicate when asked to revise wording in the pending review draft.
- Cloud automation dialogs now support additional trigger types and let you toggle whether an automation requires the triggering actor to have write access to the repository.
- Expanded tool call inputs like search patterns, shell commands, and arguments are now syntax highlighted for easier scanning.
- Expanded tool call rows in the timeline now show a metadata footer with when they started, how long they took, and the output size. Expanded reasoning rows show when they started.
- Mathematical notation written in LaTeX now renders as formatted math in chat responses.
- Model promotions can now spotlight a newly available model with a "Featured" badge and custom message, in addition to discount promotions.
- Session grid (view multiple sessions at once), side chats in the review panel, and automatic session renaming to the pull request title are now available to all users and can be turned off in Settings.
- Show an estimate of local disk space that will be reclaimed when deleting sessions
- The prompt composer toolbar now switches to compact icon-only buttons at narrow widths, so labels no longer clip or overflow in small windows or split panes.

### Changed

- Clicking a code pointer to a specific line range now highlights the referenced lines in the file viewer, and links using GitHub-style line anchors are now recognized.
- Improved diff rendering performance and inline hunk expansion in the session Changes view and remote change panel, matching the pull request Files tab.
- Improved scroll performance and accuracy in the pull request Files view when comment threads are expanded or collapsed. You can revert to the previous behavior in Settings.
- Navigating back to a recently viewed pull request's changed files now shows the diff instantly instead of reloading it.
- Refined the full-height right panel layout: tab icons now render at a crisper native size with more symmetric padding.
- The commit banner in the workspace diff view now appears immediately when you select a commit, showing a loading placeholder for the addition/deletion counts until they're ready.

### Fixed

- Bulk-archiving old sessions from the sidebar now also archives old quick chats, and no longer archives pinned sessions.
- Comment timestamps in the diff view are now properly announced by screen readers, with the exact date and time available on demand.
- Computer Use permission prerequisites now show the correct helper app name to grant permissions to.
- Dropping a file (such as an image) onto the sidebar no longer shows a confusing "Couldn't add this repository" error — only folder drops create new projects.
- Files without extensions, such as Makefile, Dockerfile, or scripts starting with a shebang like #!/usr/bin/env python, now get proper syntax highlighting instead of showing as plain text.
- Fixed a crash in the Excel canvas that could occur when reloading or replacing a workbook.
- Fixed a duplicate browser tab appearing when switching away from and back to a session with a running dev server.
- Fixed a permission prompt (such as one for enabling extension hooks) getting stuck after being answered, which could leave a session unresponsive.
- Fixed a rare crash on Windows that could occur while processing window events, including during app shutdown.
- Fixed a rare startup timing issue that could cause a new session to use a different model than your saved default.
- Fixed a red "Retry commits" error flashing in the Changes tab while a session's workspace was still being set up.
- Fixed a stray keyboard focus ring appearing on the commit navigation menu after a mouse click, and made the loading state consistent between the pull request and session commit toolbars.
- Fixed a visible scroll jump when reopening a conversation that was scrolled to the bottom
- Fixed an issue on macOS where memory usage could grow excessively while a chat response was streaming.
- Fixed an issue where choosing "Create PR + agent merge" could silently fail to turn on agent merge for the pull request.
- Fixed an issue where confirming "Edit and rewind" on an edited message could close the dialog without rewinding the conversation.
- Fixed an issue where pressing Enter to confirm an in-progress IME composition (e.g. Japanese input) in the free-form answer box could submit a half-typed answer instead of finishing the composition.
- Fixed an issue where reopening a session could unexpectedly trigger a permission prompt.
- Fixed an issue where resuming a session could show a blank or partial transcript instead of its full history.
- Fixed an issue where settings like sidebar folder colors, custom repo names, pinned/Quick-chat order, and sidebar collapsed state could reset and onboarding could reappear on launch.
- Fixed an issue where the app could fail to open, showing a dock icon but never displaying a window.
- Fixed autopilot sessions sometimes showing permission prompts instead of running without interruption.
- Fixed copying an image from chat to the clipboard, which previously did nothing.
- Fixed crashes when opening malformed links, using transcript selection menus, or opening microphone system settings from voice mode.
- Fixed extension and skill row content being hidden behind the hover background in high-contrast mode.
- Fixed keyboard focus landing in the wrong place when navigating to a Settings section via a deep link; focus now moves to the section heading.
- Fixed missing syntax highlighting for C#, Java, Kotlin, PHP, and other languages in the file view.
- Fixed pasting a screenshot or copied image into a pull request or issue comment, which was previously silently dropped.
- Fixed quick chats moving to the top of the sidebar's Last updated order just from opening them, without any real activity.
- Fixed resuming a session sometimes showing a duplicate permission prompt and taking longer when auto-approve was toggled.
- Fixed saved theme and accessibility settings being reset to defaults on app launch
- Fixed scrolling jank when viewing pull request review comments that contain a lot of code.
- Fixed sessions started by an automation getting stuck with no review panel, panel toggle, or Run / Open in / Create PR buttons until the app was restarted.
- Fixed sessions started from a merged pull request briefly showing a "Closed" status before correcting to "Merged".
- Fixed sessions with remote control incorrectly being blocked as requiring a Copilot subscription, and clarified the error shown when remote control isn't available.
- Fixed the "opened this issue/pull request" timestamp so it can be revealed by click as well as hover, and reads its full date correctly to screen readers
- Fixed the "Uncommitted" scope control in the diff toolbar not responding to clicks when there were no other scopes to switch to, and updated its label to match the file count style used elsewhere in the toolbar.
- Fixed the commits list and commit count showing empty or zero for a branch after its pull request was merged with a merge commit.
- Fixed the conversation view occasionally stopping auto-scroll to the bottom while the agent was still responding.
- Fixed the conversation view sometimes getting stuck partway up the transcript instead of staying pinned to the bottom while an agent's response was streaming.
- Fixed the Create PR options menu expanding too wide.
- Fixed the diff view briefly showing a misleading "Retry" button while a new session's workspace was still being set up.
- Fixed the diff view losing your scroll position when toggling the file tree sidebar while viewing wrapped lines.
- Fixed the diff view's scope control (Files/Commits/Uncommitted) to land on the correct view for sessions with only uncommitted changes, allow selecting an empty commits view, keep the scope menu reachable when there are no commits yet, and cleaned up spacing alignment in the toolbar.
- Fixed the dock/taskbar badge count to accurately reflect unread sessions and blockers without duplicate or stale counts.
- Fixed the expanded artifacts list growing beyond the viewport, which could push its close button off-screen; it now scrolls within a fixed height instead.
- Fixed the keyboard focus ring on dropdown menus in Settings, which incorrectly appeared near-black instead of the standard blue.
- Fixed the labels picker not showing labels past the first 100 on repositories with a large number of labels
- Fixed the model selector spuriously reopening on its own after it re-enabled once a new workspace's session became ready.
- Fixed the onboarding "setting up" screen not announcing its status to VoiceOver screen reader users.
- Fixed the prompt composer so blank lines added with Shift+Enter stay visible instead of collapsing.
- Fixed the side panel drifting out of place and the conversation losing its scroll position or reading spot when the app's zoom level was not 100%.
- Fixed the workflow run status control so keyboard and screen reader users can reveal the exact run time
- Fixed triple-click line selection in the canvas markdown source view so each source line is selected as its own block.
- Fixed wrapped diff lines sometimes getting clipped after the diff refreshed from an edit.
- Fixed your own commits showing initials instead of your avatar in the commit banner when committing with a verified email other than a GitHub noreply address.
- Home and End (and Shift+Home/Shift+End) now move or select to the start/end of the current line in the composer, instead of behaving inconsistently.
- MCP App consent prompts no longer interrupt sessions running in auto-approve-all (YOLO) mode — the app's tool and message capabilities are auto-approved without prompting, matching the extension-permission gate.
- Opening a session in VS Code now always opens in a new window instead of reusing an existing one.
- Option+Enter now inserts a newline in the prompt composer on macOS, matching Shift+Enter.
- Pasted HTML in chat messages now appears as plain text instead of being rendered as markup or disappearing.
- Pressing Enter to confirm an IME candidate (e.g. Chinese Pinyin) while answering an agent question no longer submits the unconverted text.
- Removed a non-functional "Create from" action from the sidebar for projects containing multiple repositories.
- Screen readers now announce the description text next to the Agent merge toggle.
- Screen readers now announce the onboarding steps prompting you to install the Copilot CLI or enable Copilot features when they appear.
- Sessions and forks created in a different project now stay nested under their parent session's project group in the sidebar, showing their own project name on hover.
- The "Last updated" time on the issue artifact tab can now be selected with keyboard or mouse to reveal the exact date, and is properly labeled for screen readers.
- The plan reset time in Settings > Account is now keyboard- and screen-reader-accessible, so activating it reveals the exact reset date.
- The quota warning banner's reset countdown is now keyboard- and screen-reader-accessible, so you can reveal the exact reset date without a mouse.
- Typing an exact issue or PR number after # in the composer now shows that number at the top of the suggestion list instead of below unrelated matches.

## v1.0.26

### Highlights

- New "New session" and "Open session" actions let you hand off an issue or pull request link to a new or existing session without leaving your current one.
- Added a project MCP settings section to view connection status, sign in via OAuth, refresh, and enable or disable MCP servers from a trusted repository.
- The pull request Changes tab now supports commit navigation to step through individual commits and diffs, plus a review progress indicator.
- Cloud automations now support scheduling daily and weekly runs at quarter-hour times, matching local automation scheduling.
- The /allow-all-tools and /yolo slash commands now accept on, off, and show arguments to set or check a session's tool approval mode.

### Added

- Added "New session" and "Open session" actions to the right-click menu on Copilot's "Issue created" pill and on any GitHub issue or pull request link inside a session, so you can hand a reference off to a new or existing session without leaving the current one.
- Added a project MCP settings section so you can view connection status, sign in via OAuth, refresh, and enable or disable MCP servers defined in a trusted repository.
- Added commit navigation to the pull request Changes tab, letting you step through individual commits and view their diffs, plus a review progress indicator showing how many files you've reviewed.
- Cloud automations now support scheduling daily and weekly runs at quarter-hour times (e.g. :15, :30, :45), matching local automation scheduling.
- External links can now open a new chat with a prompt, after you confirm the request.
- The /allow-all-tools and /yolo slash commands now accept on, off, and show arguments to set or check a session's tool approval mode.

### Changed

- Auto-resolved merge conflict replies now show the app attribution as a highlighted note instead of italicized text.
- Improved keyboard and screen reader accessibility in the My Work list view, including clearer row labels and an announced "new updates" notification.
- Improved the merge panel with clearer merge status, review, and check details, plus a new section showing uncommitted local and remote file changes with a quick way to view them.
- Markdown tables now support the same row, column, and alignment controls in every composer, and inserting a new column keeps header styling intact.
- Simplified the "No changes to compare" empty state in the changes panel to a cleaner, less cluttered view.

### Fixed

- Added accessible names to form fields that previously relied only on placeholder text, so screen readers can announce them correctly.
- Changing the model, reasoning effort, or context tier while a session is busy now waits to apply until the session is idle, instead of risking the change being lost or applied inconsistently.
- Command palette dialogs now announce their name and result count to screen readers
- Disabled switches in settings, and settings lists like keyboard shortcuts and skills, are now properly announced and reachable by screen readers.
- Fixed a brief empty flash when reopening the details panel in My Work for a previously viewed pull request or issue.
- Fixed a brief visual jump in the conversation view when opening a chat scrolled to the bottom.
- Fixed a crash on Windows that could occur when previewing certain local web content.
- Fixed a crash that could occur when dropping or pasting a file into the message composer while the selected text changed
- Fixed a crash that could occur when reloading or saving Excel files.
- Fixed a false "Couldn't copy the code automatically" message during device code sign-in.
- Fixed a race where late messages from a previous session could still be processed briefly after switching away from it.
- Fixed an intermittent brief scroll jump in the conversation transcript, most noticeable when switching between sessions.
- Fixed an issue where a newly created subsession could appear in the sidebar but never actually start its task.
- Fixed an issue where subscribed users could be incorrectly shown a "Copilot subscription required" error when starting a remote session.
- Fixed background agents in the composer pill showing an incorrect, ever-growing duration and lingering indefinitely after being abandoned.
- Fixed composer pills (Changes, Workflow, PR, Issue, Plan, Queued, Background, and overflow) appearing transparent instead of solid when hovered.
- Fixed embedded diffs for multiline pull request review comments so they show the correct GitHub line numbers and affected range instead of restarting at line 1.
- Fixed external links (like "Explore plans" and documentation links) not opening on some Linux distributions.
- Fixed messages sent from another session sometimes appearing as plain user messages instead of showing which session they came from.
- Fixed My Work repo selections and saved section filters getting dropped after a GitHub repo is renamed or transferred.
- Fixed pull request and issue views occasionally getting stuck showing stale data when real-time updates silently stopped arriving.
- Fixed sessions occasionally hanging forever during startup, mid-turn, or resume, and improved shutdown and git checkout speed on machines with many sessions or large repositories.
- Fixed sessions sometimes getting permanently stuck when resuming, and added a "Restart session" option to recover if resuming fails.
- Fixed Settings opening behind (and hidden from screen readers behind) the New Automation dialog when opened from within it.
- Fixed sign-in and canvas links not opening a browser on some Linux distributions.
- Fixed the "Last run" and "Next run" time details in the automation details popover so the exact timestamp is properly announced by screen readers and can be dismissed without closing the whole popover.
- Fixed the agent being unable to read from or write to a terminal you had opened yourself, which previously caused it to open a separate hidden terminal instead.
- Fixed the AI credits usage popup so it can be opened and used with the keyboard and works correctly with screen readers.
- Fixed the composer keeping a selection you added to a new side chat in place, along with anything typed while it loaded, instead of scattering the text around it.
- Fixed the copy button not copying text to the clipboard on some X11 Linux desktops
- Fixed the feedback textarea's screen reader label so it matches the visible "Report a bug or suggest a feature" heading.
- Fixed the keyboard copy shortcut not copying selected conversation text when the selection popup was open.
- Fixed the My Work detail panel toggle so it stays aligned with header actions, shows a tooltip when closed, and keeps its icon static when closing.
- Fixed the right panel and its toggle being unavailable for worktree sessions that already had a diff or pull request.
- Fixed the session preview popup lingering on screen after collapsing the sidebar.
- Fixed the Settings dialog appearing behind the workspace side drawer instead of on top of it.
- Fixed the system tray icon being invisible on dark panels on Linux.
- Fixed tools installed via the login shell profile (e.g. custom PATH entries) not being found by extensions on Linux.
- Hid the "Re-run" action for checks that GitHub doesn't allow re-running, preventing an error when clicked.
- In Streamer Mode, the usage gauge now shows a clear hidden-usage icon instead of a barely visible ring, and its hover popover correctly shows "Usage hidden" instead of a misleading plan name.
- Issue label, assignee, type, sub-issue, and close/reopen controls now respect your actual permissions instead of appearing editable when you don't have access.
- Made the reset time in the token usage quota popup accessible to screen readers, so activating it announces the full reset date instead of only revealing it on hover.
- Pasting a GitHub Gist URL into the composer now creates a proper gist reference instead of being incorrectly split into a repository reference.
- Screen readers now announce the currently active sidebar view (Home, My work, Automations, Extensions).
- Settings search no longer shows results for subsettings that are currently hidden, such as notification sound options, keep-awake grace period, or recent model history.
- Switching back to a chat session with an open file editor no longer shows a loading flash while the file reloads.
- The automation dialog now announces "Unsaved changes" to screen readers when you edit a field.

## v1.0.25

### Highlights

- Discounted model promotions are now highlighted on the Home screen and in the model picker.
- Web search tool calls now show the search query inline in the conversation.
- The Files tab filter now autofocuses and supports arrow keys and Enter to navigate and open matches.
- Running automations now show a live indicator in Recent runs, and you can filter runs by Running status.

### Added

- Show discounted model promotions on the Home screen and highlight them in the model picker.

### Changed

- Added a subtle outline around label color dots so overlapping colors are easier to distinguish.
- In the tool confirmation prompt, the custom feedback field now appears after all other options, matching the order used elsewhere.
- Keep the worktree icon visible and shimmer the status label while a worktree-backed session is being created
- The Files tab filter now autofocuses when opened and supports Arrow Up/Down to move between matches and Enter to open the highlighted file.
- Web search tool calls in the conversation now show the search query inline.

### Fixed

- Automations that are still running now appear in Recent runs with a running indicator, and you can filter runs by Running status.
- Enterprise Managed User accounts now see a direct link to open a new github/app issue instead of a broken in-app feedback form.
- Fixed empty state descriptions in workspace panels wrapping awkwardly on wide panels.
- Fixed find-in-conversation (⌘F) reporting "No results" for text that is visibly on screen but stored with markdown escape characters.
- Fixed folder rows in the Files tab shifting horizontally right after the file tree finished loading.
- Fixed issue and pull request detail views sometimes showing raw error page content instead of a clear message with a retry option when a request failed.
- Fixed pressing the up arrow key in the message composer incorrectly recalling prompt history when the cursor was on a list item that wasn't the first line.
- Fixed the keyboard focus ring being clipped on the first row of the Files tree.
- Fixed the permission prompt's "Always allow" rows wrapping their label onto two lines, and made the "won't ask again" detail also appear on hover, not just keyboard focus.
- Fixed the sidebar and right panel animation so text no longer reflows mid-slide when expanding or collapsing them.
- Fixed workflow timeline hover previews rendering behind the prompt composer during an active run.
- Grouped tool call summaries now shimmer while any tool call in the group is still running, instead of looking finished before the group actually completes.
- Review drafts and comments now show the correct account that will submit the review, instead of always showing your default account.
- Sidebar and review panel toggle icons now show active color feedback while pressed, matching other icon buttons.
- Smoothly animate the sidebar and right panel when expanding or collapsing them, without the conversation scroll position jumping.

## v1.0.24

### Highlights

- Added an "Install from URL…" button in the Extensions Canvas tab to install a canvas extension from a gist or GitHub folder URL without an active session.
- You can now enable or disable an automation directly from its context menu in the automations list.
- Added Error duration and Announcement duration settings under Accessibility to control how long notifications stay on screen.
- Issue details now appear instantly using cached data while the latest information loads in the background.
- The right panel's "+" add-tab button now opens a compact menu of tabs instead of the full command palette, with extensions grouped under an Extensions submenu.

### Added

- Added an "Install from URL…" button to the Extensions Canvas tab, so you can install a canvas extension from a gist or GitHub folder URL without needing an active session.
- Added an option to enable or disable an automation directly from its context menu in the automations list.
- Added Error duration and Announcement duration settings under Accessibility to control how long notifications stay on screen before automatically dismissing.

### Changed

- Issue details now appear instantly using cached data while the latest information loads in the background.
- Lightened the font weight of view titlebar titles for a less bold appearance.
- Reduced the size of the stop icon on the workspace run button to better match the icon sizing used elsewhere in the app.
- The folder tree sidebar in the Files tab now opens at its minimum width by default, giving more room to file content.
- The right panel's "+" add-tab button now opens a compact menu of tabs to add instead of the full command palette, with extensions grouped under an Extensions submenu.
- The Run and Open buttons in the workspace titlebar are now icon-only, freeing up space in the header.
- The selected file path in the Files tab now styles the directory prefix and filename the same way as the Changes tab, for a more consistent look.

### Fixed

- Fixed a stray console window appearing on Windows when using WSL-backed environments, which could unexpectedly terminate the session if closed.
- Fixed Account settings not offering a way to sign in to GitHub.com when the only signed-in account is a GitHub Enterprise Cloud account.
- Fixed an error that could appear when canceling a native file open or save dialog on Windows.
- Fixed an issue where deleting a session with a large workspace could fail and leave behind a corrupted, partially deleted directory.
- Fixed dependency information on an issue not updating when a linked blocking issue was closed or reopened
- Fixed Minimal verbosity mode leaving some completed tool calls and messages visible outside the collapsed summary.
- Fixed Shift+Enter in message composers so markdown shortcuts (lists, quotes, headings) keep working on new lines and line breaks are preserved in the sent message.
- Fixed the chat transcript showing through the composer's floating pills by fading it out behind them, and added a matching fade at the top of the transcript when scrolled down.
- Fixed the file count in the Changes tab being misaligned with the diff content it labels.
- Pressing Cmd/Ctrl+Enter to post a comment on an issue or pull request no longer also opens a session.
- The repository filter popup in My Work now widens to fit long org/repo names instead of truncating them.

## v1.0.23

### Highlights

- Added a Files tab to the right panel so you can browse and open files without leaving the diff or terminal.
- Added a low disk space warning in the sidebar with a breakdown of Copilot session storage and quick session management.
- Opening a workspace in VS Code or VS Code Insiders now also focuses the matching Copilot CLI chat session.
- Pull request file changes now load incrementally, showing file metadata and the sidebar sooner on large pull requests.
- Pull request pages now show the title, description, and key details first, loading comments and activity in the background.

### Added

- Added a Files tab to the right panel so you can browse and open files without switching away from the diff or terminal.
- Added a low disk space warning in the sidebar that shows a breakdown of Copilot session storage and a direct way to manage sessions when your disk is running low.
- Opening a workspace in VS Code or VS Code Insiders now also focuses the matching Copilot CLI chat session, not just the folder.

### Changed

- Improved screen reader support in the sessions sidebar, and added an "Interaction hints" preference under Accessibility settings to control whether keyboard shortcut hints are announced.
- Pull request file changes now load incrementally, so file metadata and the sidebar appear sooner while the rest of the diff continues loading on large pull requests.
- Pull request pages now show the title, description, and key details first, then load comments and activity in the background.

### Fixed

- Copy buttons now consistently announce "Copied to clipboard" for screen reader users and show a visible confirmation, with clearer accessible names.
- Fixed a crash in the formatting toolbar that could occur when text selection changed outside the message composer.
- Fixed a crash on the My Work tab when previously saved section view configuration contained malformed data.
- Fixed a crash that could occur when running a slash command or terminal command with malformed or unexpected data.
- Fixed an issue where a pull request review thread resolved outside the app could keep showing as unresolved in the conversation view.
- Fixed an issue where a pull request's conversation could appear stuck loading additional timeline events indefinitely.
- Fixed crashes that could occur when typing to focus the message box, using the voice mode keyboard shortcut, or selecting text to reveal the markdown formatting toolbar.
- Fixed duplicate slash command entries occasionally showing up in the composer's command menu.
- Fixed inconsistent capitalization of the "Go to repository" group heading in the command palette
- Fixed pasting a GitHub pull request or issue URL with extra suffixes (like /changes or a #discussion anchor) not matching the correct item when creating a session
- Fixed pull request review comment threads sometimes showing stale resolved/unresolved status in the conversation, files, and merge blocker views after resolving or unresolving a thread.
- Fixed the Agent Merge options popover sometimes appearing behind an open canvas instead of on top of it.
- Fixed the Extensions view's MCP tab sometimes spinning forever when the server list failed to load, and added a retry button if loading takes too long.
- Fixed the formatting toolbar in the Plan tab being clipped or hidden behind the tasks rail when selecting text.
- Fixed the response toolbar (copy / bookmark / fork) appearing repeatedly during multi-session coordination turns instead of only on the final response.
- Improved screen reader support for icons in the workspace popover, including token usage indicators and the QR code link.
- Pasting a GitHub branch URL into the command palette now starts a session on that branch instead of just adding the repository.
- Pressing Shift+Enter in the composer now inserts a line break instead of starting a new paragraph.
- Switching from Overview to Changes and back on a pull request no longer resets your scroll position on the Overview tab.
- The Background agents pill now only shows agents that are still running, removing finished ones instead of leaving stale entries behind.
- The QR code panel can now be opened with a click and operated via keyboard and screen readers, instead of requiring mouse hover.

### Removed

- Removed the find-in-page (Cmd+F) shortcut from the Home view; it remains available on other views.

## v1.0.22

### Highlights

- Add to panel now shows a "Relevant from session" group so you can quickly open issues and pull requests recently mentioned in the conversation.
- The full-screen pull request Changes view now displays each file in its own card with addition/deletion counts in the sidebar.
- Saved memories now appear in the conversation timeline, showing the fact that was remembered.
- The issue timeline now shows a reference card with status icon, title, and issue number for blocked/blocking relationships.

### Added

- Add to panel now shows a "Relevant from session" group with issues and pull requests recently mentioned in the conversation, so you can open them as panel tabs without hunting for the original link.

### Changed

- In the full-screen pull request Changes view, each file now appears in its own spaced, rounded card, and the files sidebar shows addition/deletion counts for each file.
- Saved memories now appear in the conversation timeline, showing the fact that was remembered.
- Settings search now finds specific controls within a section (not just whole sections) and reliably focuses the matching control when selected. Cmd+F while Settings is open now refocuses the settings search.
- Show a feedback icon (instead of a bug icon) on the Share feedback button in the sidebar.
- The issue timeline now shows a reference card (status icon, title, and issue number) when an issue is marked as blocked by, or blocking, another issue, instead of a bare action line.

### Fixed

- Fixed an issue where creating a session with an initial prompt could sometimes create an empty session with the prompt never delivered.
- Fixed browser preview tabs continuing to play audio and use resources after being closed
- Fixed crashes that could occur from unusual keyboard events and when resizing the right panel.
- Fixed expanding a message panel in a conversation sometimes scrolling the whole window instead of just the conversation.
- Fixed file drag-and-drop onto the composer, sidebar, and comments not working correctly when the app was zoomed in or out
- Fixed the environment picker in the new session composer showing every codespace under every project, even ones for a different repository.
- Fixed the run status tooltip in the automations runs table overlapping nearby content by showing it above the row instead of to the side.
- Fixed the storage location in Settings > General displaying mixed path separators on Windows; it now shows native Windows-style separators.
- Hidden HTML comments in markdown (e.g. in pull request descriptions and comments) are no longer shown as visible text, while comments inside code blocks are still displayed correctly.
- Long session durations in the Insights panel now show as hours and minutes (e.g. "2h 0m") instead of large minute counts.
- Sessions that are just resuming or loading history no longer show up under Working in the sidebar.

## v1.0.21

### Highlights

- Clarified that the "GitHub Enterprise" sign-in option is for GitHub Enterprise Cloud with data residency (*.ghe.com).
- Fixed a workspace's pull request status incorrectly showing as merged after the agent opened a new pull request for it.
- Fixed queuing a pull request for merge when it's waiting on a required review — auto-merge now enables automatically so it queues once requirements pass.

### Changed

- Clarified during sign-in and in account settings that the "GitHub Enterprise" option is for GitHub Enterprise Cloud with data residency (*.ghe.com).

### Fixed

- Fixed a workspace's pull request status incorrectly showing as merged after the agent opened a new pull request for that workspace.
- Fixed queuing a pull request for merge when it is waiting on a required review — the app now enables auto-merge so it queues automatically once requirements pass, instead of failing to queue.

## v1.0.20

### Highlights

- Added a /security-review slash command to start a security review of the current diffs.
- In local sessions, you can now edit a previous message to rewind the conversation and resend it as a new turn.
- Nested sessions in the sidebar now show connected hierarchy lines between parent and child rows for easier scanning.
- Simplified the loading state of the pull request checks panel to show a single animated header instead of duplicate loading indicators.

### Added

- Added a /security-review slash command to start a security review of the current diffs.
- In local sessions, you can now edit a previous message to rewind the conversation from that point and resend it as a new turn.

### Changed

- Nested sessions in the sidebar now show connected hierarchy lines between parent and child rows, making it easier to scan deeper session relationships.
- Simplified the loading state of the pull request checks panel to show a single animated header instead of a duplicate loading message and skeleton.

### Fixed

- Clicking the header of a session plan file in the diff view now opens the Plan tab instead of doing nothing.
- Collapsed project rows in the sidebar keep their project icon for working, paused, or completed sessions, only replacing it when a session needs input, is interrupted, or has failed.
- Collapsed repository groups in the sidebar now keep showing the repository icon when all sessions are completed or ready to merge, instead of looking like a single session.
- Fixed a spurious "Model changed to..." message appearing in the transcript when resuming a session with an unchanged model.
- Fixed agent merge getting stuck and not re-prompting after a required check finished running while another check was still failing.
- Fixed empty draft sessions sometimes remaining after leaving the multi-session grid view
- Fixed pull requests briefly jumping out of "Ready to merge" in the sidebar while a merge was in progress before landing in "Done".
- Fixed repository labels in the sidebar fading too early; hover and keyboard actions now only reserve space when revealed
- Fixed the auto-merge agent sending unnecessary follow-up replies triggered by its own previous comments on a pull request.
- Fixed the line-selection hint in the file header overlapping the toolbar buttons on narrow panels
- Fixed the project removal confirmation dialog remaining visible after deleting a project in Settings.
- Fixed the pull request author sometimes appearing as their own reviewer in the Reviewers panel.
- Improved screen reader support in the Health Check dialog: diagnostic rows now announce their labels and pass/warning/error status, and copy-path buttons have distinct, descriptive names.
- The Create PR action no longer appears for a workspace after a pull request has already been created for it.

## v1.0.19

### Highlights

- Added a rich text editor for the plan in the workspace Plan tab while Copilot waits for approval.
- Deep links that create a new session can now nest it under an existing session, so it appears as a child in the sidebar.
- You can now close an issue as a duplicate and select the canonical issue it duplicates.
- "Create nested session" now opens a dialog to describe the task, letting the parent session spawn the nested session(s) instead of starting from an empty draft.

### Added

- Added a rich text editor for the plan in the workspace Plan tab while Copilot waits for approval.
- Deep links that create a new session can now nest it under an existing session using a parent parameter, so it appears as a child in the sidebar.
- You can now close an issue as a duplicate and select the canonical issue it duplicates.

### Changed

- "Create nested session" now opens a dialog to describe the task, letting the parent session spawn the nested session(s) instead of starting from an empty draft.
- Clarified the subtitles in the Editor's Picks and Browse by Category sections of the extensions view.
- Issue numbers now appear inline next to the title in the sub-issue picker, and stay visible even when a row isn't highlighted.
- Refreshed the styling of nested-session message rows in the chat timeline for a calmer, more consistent look.

### Fixed

- Automation-related actions in the conversation timeline now show clear labels like "Listed automations" and "Saved automation" instead of generic "workflow" wording.
- Clicking a GitHub Actions check in the checks drawer now opens the Actions job page instead of an incorrect pull request checks link.
- Corrected "Healthcheck" to "Health check" in dialog and error messages for better readability and screen reader pronunciation.
- Fixed "New session" on project-scoped canvases in the Extensions Canvas tab so it starts the session directly instead of opening the generic canvas picker.
- Fixed "View logs" in the PR checks menu sometimes doing nothing for failing checks; it now opens the check's logs on GitHub, or is hidden if no link is available. Re-running a workflow run that is older than a month now shows a clear, calmer message instead of a raw GitHub API error.
- Fixed text selection in the file view so the line-range highlight no longer lingers across hovered rows and copy behaves correctly.
- Fixed the browser preview's Reload button sometimes clearing the address bar and failing to reload the page.
- Fixed the keyboard focus outline being clipped on the first and last rows of the workflow runs and skills lists.
- Fixed the pull request Reviewers list sometimes appearing empty when reviewers had already submitted a review or when a team was requested for review.
- Fixed the text caret not appearing when focusing an empty pull request or issue comment box
- Made date-group labels in the Recent runs list navigable as headings for screen readers.
- Terminal canvas commands no longer re-execute when a session is restored after restarting the app.
- The "Create PR" button no longer disappears for up to a minute after committing changes in a cloud-hosted workspace.

## v1.0.18

### Highlights

- Added a "Default agent" setting so new sessions automatically start with your chosen custom agent.
- Added a context-window usage graph to Session Insights, showing usage over time with zoom and pan synced to the tool timeline.
- Collaboration links can now open a session on a specific existing branch instead of always creating a new one.
- Pull requests and issues you're viewing now update in real time instead of waiting for the next periodic refresh.
- Draft pull requests now get conflict resolution, CI fixes, and review replies from the agent instead of being skipped entirely.

### Added

- Added a "Default agent" setting in Settings → Sessions so new sessions automatically start with your chosen custom agent.
- Added a "Mark as unread" / "Mark as read" action to the right-click menu for sessions and quick chats.
- Added a "Show in Finder/Explorer/Files" action to the repository context menu in the sidebar.
- Added a context-window usage graph to the Session Insights tab, showing how much of the context window has been used over time, with zoom and pan synced to the tool timeline.
- Added a Location column to the Manage sessions table showing each worktree's path, and replaced misleading dashes with loading skeletons while file and chat sizes are being calculated.
- Collaboration links can now open a session on a specific existing branch instead of always creating a new one.

### Changed

- Clicking a GitHub issue or pull request link in a Quick Chat now opens the built-in viewer in the chat panel instead of your system browser.
- Consolidated the panel maximize and full screen buttons into a single maximize control in the panel tab bar.
- Improved loading and scrolling performance for large pull request conversations, reducing blank gaps and scroll jumps.
- Polished the sign-in screen layout, shortening button labels and moving the GitHub Enterprise sign-in option to a subtler link.
- Pull requests and issues you're viewing now update in real time as changes happen, instead of waiting for the next periodic refresh.
- The quick open dialog (Cmd+K/Cmd+P) now opens and searches files more responsively.

### Fixed

- Draft pull requests now get conflict resolution, CI fixes, and review replies from the agent instead of being skipped entirely; merging is still withheld until the PR is marked ready for review.
- Fixed an issue where deleting a custom model provider left its model stuck in the model picker, even after restarting the app.
- Fixed an issue where renaming a session could be interrupted or reset if an automatic title update arrived while you were still typing.
- Fixed context menus (e.g. in the sidebar) sometimes closing immediately after right-clicking instead of staying open.
- Fixed crashes in the browser preview and extension canvas, and a rare crash when pruning old log files.
- Fixed inconsistent styling of attachment and reference chips (files, images, PR/issue links) so they now look and behave the same in the composer and in the conversation view.
- Fixed misaligned Path, Project, and Session ID values in the workspace info popover
- Fixed new chats sometimes being silently discarded when navigating away right after sending the first message or after only using the terminal, so the session and its messages are no longer lost.
- Fixed session and setup step file paths on Windows to display with native backslash separators instead of forward slashes.
- Fixed slow scrolling in the diff view when files are collapsed.
- Fixed the conversation scrolling or jumping around while Mermaid diagrams are loading or rendering.
- Fixed the conversation view sometimes jumping or showing blank content when scrolling to the bottom of a long chat
- Fixed the conversation view sometimes landing above the latest messages instead of at the bottom when returning to a session that received new output while you were away.
- Fixed the Create PR button and workspace safety checks not working correctly on WSL projects.
- Fixed the emoji suggestion picker in the comment composer being clipped when typing near the bottom of a constrained view, such as a pull request review comment.
- Long node and edge labels in Mermaid diagrams now wrap correctly instead of overflowing their shapes
- Made the Stop button in the run split button use a consistent subtle red styling across all color themes
- Screen readers now correctly associate labels with values (like Schedule, Next run, and Environment) in the automation details, session usage, and workspace/branch popovers, and the automation popover's dialog title now reads "Automation details" instead of "Workflow details".

## v1.0.17

### Highlights

- Added an optional sparse-checkout setting so new worktrees for very large repositories can include or exclude selected top-level directories.
- Added an Insights tab to the session panel showing a timeline of tool calls, sub-agent activity, and time spent per tool.
- Right-click a file, image, or reference chip in the prompt composer to open it, reveal it in your file manager, copy its path or link, or open it on GitHub.
- You can now leave multiple inline comments on a pull request diff and submit them together as a single review, plus react with emoji and reply within threads.
- Auto-merge, queueing, and ready-for-review actions now show their progress directly on the button you clicked, so the merge drawer no longer shifts during the action.

### Added

- Add an optional sparse-checkout setting in project settings so new worktrees for very large repositories can exclude or include only selected top-level directories.
- Added an Insights tab to the session panel showing a timeline of where a session spent its time, including tool calls, sub-agent activity, and a summary of time spent per tool.
- Right-click a file, image, or reference chip in the prompt composer to open it, reveal it in your file manager, copy its path or link, or open it on GitHub.
- You can now leave multiple inline comments on a pull request diff and submit them together as a single review, with the Review button showing how many comments are staged. You can also react to review comments with emoji and reply within threads.

### Changed

- Auto-merge, queueing, and ready-for-review actions in the merge drawer now show their progress directly on the button you clicked instead of a separate status message, so the drawer no longer shifts while the action is in progress.
- Restyled the "Show full diff"/"Show full file" expander as a full-width hover bar for easier reading.
- Simplified the feedback dialog to focus on reporting bugs or suggesting features, removing the topic and mood selectors.
- The Insights tab in the workspace panel is now closed by default and can be reopened from the "+" add-to-panel menu, instead of always appearing automatically.
- The Run menu now shows a Stop button while a script is running (instead of a disabled label) and lists recently run commands under a Recents group.
- Tightened wording of the prompt composer's placeholder text across modes for clarity and consistency.

### Fixed

- Clicking a GitHub reference like #123 now correctly opens an issue or pull request tab based on what it actually is, instead of sometimes guessing wrong.
- Enterprise Managed User and enterprise-only accounts now see a clear message explaining that a personal GitHub account is required to share feedback, instead of a confusing failed submission.
- Fixed a bug where editing a message you had sent to steer the assistant mid-response could blank out or corrupt the earlier part of that response.
- Fixed a visual jitter of the category icon on home screen suggestion cards when hovering in Safari
- Fixed adding a plugin marketplace failing on Windows with bundled git due to the credential helper sidecar not launching.
- Fixed custom skill directories configured in settings being ignored when running skills, causing them to fail
- Fixed image files (PNG, JPG, GIF, WebP, SVG) generated by the agent showing "This file can't be previewed" instead of rendering inline in the preview pane.
- Fixed installing plugins or adding a marketplace failing to clone private repositories.
- Fixed loading spinners appearing out of sync with each other.
- Fixed popover alignment for the reviewers, labels, and reaction pickers in the pull request view, and cleaned up the minimized comment header.
- Fixed resolved pull request review comments not showing their content and replies when expanded in the diff view.
- Fixed the app icon and tray unread badge showing a count that couldn't be cleared when a background automation finished running.
- Fixed the conversation view occasionally scrolling away from the bottom when sending a message or when content height changed during layout settling.
- Fixed the diff view stalling or scrolling erratically when viewing large pull requests.
- Fixed the keyboard focus ring being clipped on composer pill buttons (Changes, PR, Plan, etc.)
- Fixed the merge drawer disappearing abruptly instead of closing smoothly when actions like fixing unresolved comments or failing checks were triggered.
- Fixed the pull request activity view showing a "0 comments" heading and unusable filter/sort controls when there were no comments.
- Fixed the sidebar's "Last updated" sort so a session group moves to the top when one of its nested sessions is updated, not just the top-level session.
- On macOS, pressing Home or End in a text input no longer inserts a stray box glyph.
- Pushed commits now appear in the pull request conversation feed alongside comments.

## v1.0.16

### Highlights

- Selecting multiple projects when starting a new chat now starts a single orchestration chat across those repositories, with the sidebar grouping the spawned sessions together.
- Right-click a sidebar session to create a nested session or detach it.
- Mentioning a session with & in the composer now shows a removable pill, and pasted session IDs are automatically recognized the same way.
- When archiving or deleting a session with nested sessions, you're now prompted to also archive or delete them so they don't become orphaned.
- Added a copy button to the slash command and additional instructions sections of the system prompt detail dialog.

### Added

- Added a copy button to the slash command and additional instructions sections of the system prompt detail dialog.
- Mentioning a session with & in the composer now shows a removable pill, and pasted session IDs are automatically recognized and shown the same way.
- Right-click a sidebar session to create a nested session or detach the session.
- Selecting multiple projects when starting a new chat now starts a single orchestration chat across those repositories, and the sidebar groups the sessions it spawns together.
- When archiving or deleting a session that has nested sessions, you're now prompted to also archive or delete them, so they no longer become orphaned in the sidebar.

### Changed

- Refined the look of file attachment chips in the composer with rounded pill shapes and clearer, more consistent file type icons.
- The account chip in the sidebar now shows the account a project actually bills against, so opening a session switches it to the right account instead of showing your default.
- The agent merge status in the conversation now updates at minute-level granularity instead of ticking every second.
- Updated the theme search placeholder and label to say "palettes" instead of "themes".
- Updated v3 diff notices for files without textual differences to use a muted, padded treatment.

### Fixed

- Fixed a crash in the message composer that could occur when replacing its content.
- Fixed a crash that could occur in the message composer's formatting toolbar and when using select all with certain keyboard input.
- Fixed a crash that could occur when hovering table cells while editing a markdown table.
- Fixed a slight vertical misalignment between typed text and the placeholder in the message composer.
- Fixed connected Copilot Free accounts showing as "Copilot Pro" in Accounts settings.
- Fixed git operations failing on Linux AppImage builds after the app self-updated and restarted.
- Fixed inconsistent spacing between labels and inputs in project settings
- Fixed MCP server connection status getting stuck on "authenticating" for third-party OAuth servers even when the server was actually connected and its tools were working.
- Fixed screen readers announcing incomplete or missing information for the automation name and breadcrumb navigation in the automation details view.
- Fixed sessions using your own model (BYOK) getting silently switched to Auto when you hit a Copilot rate limit.
- Fixed tab strips that overflow now clip cleanly at the panel edge with a subtle fade, instead of cutting off scrolled tabs mid-label.
- Fixed the "Browse catalog" button in model provider settings not showing a tooltip on hover
- Fixed the Agent Merge status note so it no longer says "active" after Agent Merge has been turned off.
- Fixed the conversation view occasionally drifting away from the bottom as new messages arrived while scrolled to the end.
- Fixed the Hours and Day of week menu buttons in workflow scheduling so screen readers announce the full list of selected values, not just a summary count.
- Fixed the sidebar showing no projects when one project failed to load, so healthy projects now still appear even if another project has an error.
- Fixed third-party MCP servers requiring sign-in (like Slack) getting stuck on a failed status with no way to authenticate; they now show a Sign in button in MCP settings.
- Screen readers now announce the correct label and description for each control in the New automation dialog, and its field labels are clickable.
- Screen readers now announce when the composer mode changes via keyboard shortcut or slash command.

## v1.0.15

### Fixed

- Fixed the default branch reverting to the repository's default branch every time a project was reopened after being manually changed in Settings.

## v1.0.14

### Highlights

- Added an /init slash command to generate or improve a repository's Copilot instructions file.
- You can now type & in the composer to mention and reference another session by name.
- The home screen now shows prompt cards with suggested tasks that fill the composer when clicked.
- Added /model and /models slash commands to open the model picker or select a model by name or ID.
- AI credit usage warnings now appear above the chat composer with a next step when you run low or out.

### Added

- Added /clear and /reset slash commands to reset the current chat session transcript while staying in the same workspace or chat context.
- Added /model and /models slash commands to the prompt composer to open the model picker or select a model by name or ID.
- Added a /rename slash command to rename the current session or chat directly from the composer.
- Added a `/chronicle reindex` slash command to rebuild the Chronicle session index.
- Added a `/init` slash command to generate or improve a repository's Copilot instructions file.
- AI credit usage warnings now appear above the chat composer, with a plan-aware next step when you run low or run out.
- In the diff view, you can now open a file directly from its header, and right-click a file header to copy its file path or relative path, or open the file in a new tab or your browser.
- Session ID is now shown in the workspace and chat title popovers with a one-click copy button, making it easy to reference a session when working across multiple chats.
- The home screen now shows prompt cards below the composer with suggested tasks to try. Clicking a card fills the composer with the suggested prompt using a typewriter animation.
- You can now type & in the composer to mention and reference another session by name.

### Changed

- In repository settings, the trust actions (Accept, Revoke, Keep local, and Create config file) now show a spinner and become non-interactive while the request is in flight, so it's clear the action was registered.
- Refactored the repository configuration section of project settings into a reusable, presentational `RepositoryConfigFileSettings` component, with Storybook coverage now backed by the real component. No change to behavior.
- Shift+Tab in the chat composer now moves focus backward as expected for keyboard and screen-reader users, instead of cycling the session mode. Change modes from the mode menu or with ⌘/Ctrl+Shift+M (remappable in Settings → Keyboard Shortcuts).

### Fixed

- Agent merge check-in prompts no longer clutter the composer's prompt history.
- Closed pull requests that were previously drafts now show the closed icon in the sidebar instead of the draft icon.
- Fixed an error that could prevent bring-your-own-key models from working in project and workspace sessions.
- Fixed keyboard focus returning to the wrong place after closing the "Add from GitHub" repository picker during onboarding, so keyboard and screen-reader users can navigate correctly.
- Fixed lag when switching between chat sessions, especially very large conversations.
- Fixed pull request and issue lists, pull request details, and creating or updating pull requests/issues breaking after a repository was renamed or transferred on GitHub.
- Fixed the coding agent auto-merging a pull request before GitHub's own merge checks (e.g. required status checks) were satisfied.
- Fixed the composer's Changes pill not appearing on WSL workspaces when a session had uncommitted edits.
- Fixed the Impeccable design skill leaving behind stray cache files and git exclude entries in repos where no design issues were found.
- Fixed third-party MCP servers requiring OAuth getting stuck on an endless "authenticating" spinner instead of prompting to sign in.
- In project settings, the repository configuration file row is now hidden until a `.github/github-app.yml` config actually exists, instead of appearing before you've created one.
- Local automations now use your Settings and per-project instructions, matching interactive sessions.
- Widened the scrollbar thumb on Windows and Linux and fixed the dark theme hover color so the thumb is brighter on hover as expected.

## v1.0.13

### Highlights

- Chats can now be archived instead of only deleted, hiding them from the sidebar without losing history and letting you restore them later.
- A full-screen Present mode for canvas, diff, and file panels hides app chrome for a clean, distraction-free view.
- A new /compact slash command lets you manually compact a workspace or chat conversation on demand to reduce token usage.
- Selecting an HTML file in the Files panel now shows a globe button to open it directly in the integrated browser.
- You can now right-click an image in a pull request, issue, or comment to copy it, matching existing chat behavior.

### Added

- Added a "Show Copilot CLI Session" setting in Settings → Sessions that controls whether sessions created by the Copilot CLI appear in the sidebar and, if so, how far back to surface them. The setting defaults to Off, so CLI sessions are hidden until you opt in.
- Added a full-screen Present mode for canvas, diff, and file panels: an Enter full screen button in the panel tab bar hides the app chrome and window header for a clean, full-bleed view, and can be exited with the button, Esc, or the OS fullscreen toggle.
- Chats can now be archived instead of only deleted. Archive a chat from its sidebar context menu to hide it from the sidebar without losing its history, and restore it later from Manage sessions.
- New /compact slash command lets you manually compact a workspace or chat conversation to reduce token usage, with optional focus instructions. Compaction already happens automatically when a conversation grows large; this lets you trigger it on demand.
- Selecting an HTML file in the Files panel now shows a globe button in the header that opens the file in the integrated browser.
- Session spend now shows a separate "Agent merge" line when background agent merge activity contributed to the total, making it easier to see how your credits were used.
- You can now right-click an image in a pull request, issue, or comment to copy it, matching the existing behavior for images in chat.

### Changed

- Clicking an issue or pull request reference — in a conversation message or the prompt composer — now opens it in the in-app viewer instead of the browser when a workspace is active. Cmd/Ctrl-click still opens it in the browser.
- Copying an assistant response now pastes as formatted rich text (headings, bold, lists, tables, code) into apps like Teams, Outlook, and Word, instead of raw markdown.
- Improved rendering performance while assistant and reasoning messages are streaming in: completed parts of the message no longer get re-parsed on every update, making long streaming responses smoother.
- Pull requests in a merge queue now show a "Queued" status across all PR status surfaces, including badges, sidebar icons, tray menu labels, and the MyWork list, instead of appearing as open or merge-ready.
- Reworked the Add filter dropdown to show common filters first, with an "All filters" option to reveal the full grouped list and search across all filters.
- Screen readers now announce the number of matching results when filtering repositories and other item pickers.
- The branch name shown in the pull request view now includes a built-in copy button, merged into a single pill instead of a separate icon next to it.

### Fixed

- Automated agent check-in prompts no longer show up as ticks on the conversation timeline scrubber, and clicking the last tick now scrolls to its actual message instead of overshooting to a trailing automated exchange.
- Cloud automations now let you choose a model and reasoning effort, and remember your choice when you edit the automation later. Previously the model selection was ignored and reasoning effort couldn't be changed.
- Fixed a doubled border at the bottom of the merge summary card when a pull request is ready to merge
- Fixed an issue where messages sent while the agent was working could get stuck showing as pending, and could cause the earlier message to appear to disappear from the conversation.
- Fixed incorrect ARIA roles on segmented controls throughout the app so screen readers now correctly identify single-choice settings (theme mode, filter mode, plugin/skill/shortcut filters, etc.) as radio groups rather than tab controls, and added missing panel labels to the genuine tab controls (markdown editor, MCP settings).
- Fixed keyboard and screen-reader navigation order in the onboarding steps — on wide screens, the Continue/Finish button is now reached after the choices it applies to, matching the visual and expected reading order.
- Fixed screen readers announcing the Mode and Terminal theme options in Settings > Themes as tabs instead of radio buttons, and added missing group labels and descriptions.
- Fixed the sidebar session status spinner sometimes staying stuck on "working" after a session went idle.
- Hid the redundant scrollbar in the conversation view when the timeline is visible.
- In repository settings, the "Trusted" status label now appears to the left of the "Revoke" button, following the expected state-then-action order.
- Opening a new terminal from the add-tab menu or command palette now focuses the terminal immediately instead of leaving focus on the button you clicked.
- Screen readers now announce each control's name and description when navigating the Sessions settings panel.
- Screen readers now announce the empty-selection hint in the onboarding Repositories step when no repositories are selected.
- Screen readers now announce the field name and description when focusing the Mode and Font dropdowns in Settings > Themes.
- Screen readers now hear the sign-in code copy confirmation before the browser opens during device-code sign-in, so users are no longer dropped into the browser with no context of what happened.
- The attention badge dot on the Windows and Linux system tray icon is now amber instead of black, making it visible on dark taskbars.
- Toggling merge settings (like "Merge pull request") for a workspace with agent merge enabled now takes effect immediately instead of waiting up to 10 minutes for the next automatic check.

## v1.0.12

### Highlights

- Added an agent picker to the chat composer toolbar so you can select a custom agent before or during a session, including sessions opened from issues and pull requests.
- HTML files can now be opened in the integrated browser directly from the editor header, file tree, and inline chat references.
- Draft pull requests now open the full PR panel, giving access to agent-merge options and a "Ready for review" action.
- When creating GitHub issues, the agent now follows the repository's issue templates, preserving headings, sections, and comments.
- Fixed a bug where renaming a repository's default branch on the remote caused the diff view to show a large phantom diff of hundreds of files.

### Added

- Added an agent picker to the chat composer toolbar, letting you select a custom agent before or during a session. The selected agent is also applied to sessions spawned from issues, pull requests, and other entry points.
- HTML files can now be opened in the integrated browser directly from the file editor header, the file tree context menu, and inline file references in chat messages. File browser tabs also now show the file name instead of a blank label when opening local files. Build-step apps (for example Vite or React projects) that reference ES modules or server-root assets can't render from a local file, so the browser panel now shows a short "run a dev server" explanation instead of a blank page. Global agent discovery now degrades gracefully on CLIs that do not implement `agents.discover`.
- Right-clicking a chat image now shows a "Copy image" option that copies the image to your clipboard, available on both inline thumbnails and in the image viewer.

### Changed

- Draft pull requests now open the full PR panel, giving access to agent-merge options and a "Ready for review" action from the same place as other PR states.
- Quote in reply now appends quoted text to the end of your existing draft, preserves inline code and formatting, supports a keyboard shortcut (Cmd+Shift+'), and places the cursor on the line after the quote.
- The theme picker in Settings > Appearance is now fully keyboard and screen-reader accessible: arrow keys navigate between theme cards, Enter or Space applies a theme, Escape resets to the default GitHub theme, and selecting a theme announces its name to assistive technology.
- When creating GitHub issues, the agent now checks for and follows the repository's issue templates, preserving headings, sections, and HTML comments.

### Fixed

- Fixed a bug where renaming a repository's default branch (e.g. master → main) on the remote would cause the diff view to show a large phantom diff of hundreds of files even though the working tree was clean.
- Fixed keyboard focus loss on Windows after Alt+Tab — the chat composer now correctly regains focus when switching back to the app.
- Fixed panel scrollbars being unclickable on Windows because resize handles were overlapping them.
- In Project Settings, the "Open on GitHub" link for the config file is now hidden when the file has not yet been committed to the default branch. A "Reveal in file manager" button is shown instead so the file can still be found locally.
- Navigating to a Settings section via the in-dialog search or contextual buttons now moves keyboard focus to that section's heading, so keyboard and screen-reader users land directly on the destination content instead of the dialog container.
- On Windows, the tray now uses the main app icon so it keeps enough contrast in both light and dark taskbar modes.
- Opening a Markdown file in the editor canvas no longer silently rewrites its contents (e.g. escaping underscores or changing fenced-code indentation) when an external no-op file refresh occurs.

## v1.0.11

### Highlights

- Local automations now support custom CRON expressions, letting you schedule workflows at any cadence using a segmented expression editor with inline validation and a human-readable preview.
- Screen readers now announce agent activity in Sessions and Quick Chats — including replies, tool calls, and CLI commands — with new per-category announcement toggles in Settings > Accessibility.
- The Manage Sessions filter bar now supports "is not" exclusion on all four filters, and the State filter offers distinct values (Open, Draft, Merged, Closed, No pull request) instead of a two-bucket grouping.
- Fixed workflows failing to run when configured with a local or custom provider model (e.g. Ollama or Foundry) — scheduled and manual runs now correctly route to the selected model.
- Added a folder icon button next to the session path in the workspace dropdown to reveal the session folder in your native file manager.

### Added

- Added a folder icon button next to the session path in the workspace dropdown to reveal the session folder in the native file manager (Finder, Explorer, or Files).
- Local automations now support custom CRON expressions, letting you schedule a workflow at any cadence (e.g. "every 15 minutes on weekdays") using a segmented expression editor with inline validation and a human-readable preview.
- Screen readers now announce agent activity in Sessions and Quick Chats — including replies, tool calls, CLI commands, and a loading heartbeat — so non-sighted users get real-time feedback without leaving the prompt field. New per-category announcement toggles are available in Settings > Accessibility.

### Changed

- Plugin marketplace groups in Settings > Plugins are now collapsed by default, reducing visual clutter when opening the page.
- The "Open in" app list in session context menus is now collapsed into a single "Open in…" submenu, keeping the menus more compact when multiple apps are configured.
- The issue timeline now shows a reference card (status icon, title, and issue number) when a sub-issue or parent issue is added or removed, instead of a bare action line.
- The Manage Sessions filter bar now supports "is not" exclusion on all four filters (Status, State, Repository, Environment), and the State filter now offers distinct values — Open, Draft, Merged, Closed, and No pull request — instead of the previous two-bucket Open/Closed grouping.
- The prompt composer's borders, focus rings, and send button now consistently reflect the active mode color — neutral for interactive, blue for plan, green for autopilot, and orange for shell.

### Fixed

- Editing an automation's project now saves correctly even after the automation has run at least once.
- Fixed an issue where the fork button disappeared after a model change, skills reload, or agent switch notice appeared in the conversation.
- Fixed an issue where the scrollbar in the conversation timeline area was nearly impossible to grab when timeline markers were visible.
- Fixed an issue where typing an org name in the sidebar clone search could skip repos that belong to that org.
- Fixed missing Changes pill, command palette session actions, and side-panel toggle for existing sessions when the right panel started closed.
- Fixed the horizontal scrollbar in Manage sessions: it now scrolls to reveal all columns when they overflow, and disappears when all columns fit.
- Fixed workflows failing to run when configured with a local or custom provider model (e.g. Ollama, Foundry, or custom OpenAI-compatible). Scheduled and manual workflow runs now correctly route to the selected provider model instead of returning "model not available".
- Forking a session that had been idle for ~10 minutes no longer fails with a "not found" error.
- Page Up and Page Down now scroll the conversation transcript when focus is on the conversation area.
- Scrolling the slash-command and mention menus no longer dismisses the menu on Windows — dragging the scrollbar now scrolls as expected.
- The checks panel now shows a "Checks are starting" pending state instead of the neutral "No checks have run yet" message when GitHub has queued checks that haven't reported individual results yet, preventing the empty state from being misleadingly reassuring.

## v1.0.10

### Highlights

- Orchestrator sessions can now approve or redirect a child session's plan while it's paused in plan mode, instead of waiting for a human.
- "Share extension as gist" now appears in the command palette whenever a shareable extension is installed, and automatically opens the new gist in your browser.
- On macOS, the native menu bar now reflects your current keyboard shortcut bindings, and the View menu item has been renamed from "Open Search" to "Command Palette".
- On Windows, tools installed to the user-level PATH (such as winget or nuget) are now correctly found when running agent sessions or the integrated terminal.
- When a project is linked to the wrong GitHub account, the app now detects the correct account and prompts to re-authorize instead of silently failing.

### Added

- Orchestrator sessions can now approve or redirect a child session's plan while it's paused in plan mode, instead of the child waiting for a human. Plan-ready children notify their creator, the plan is surfaced via get_session, and the new respond_to_session_plan tool resolves it.

### Changed

- "Share extension as gist…" now appears in the command palette whenever a workspace session has a shareable extension installed, not only when an extension canvas is open. Sharing an extension now also opens the new gist in your browser so the result is obvious.
- Nested folders in workspace file trees now use a smaller indent step so deeply nested folder hierarchies are more compact and easier to read.
- Renamed "Quick Chat" / "Quick Chats" to "Chat" / "Chats" throughout the app (sidebar, tray menu, workflows, project picker, and menus).

### Fixed

- Automation run detail header no longer overlaps at narrow window widths — run status hides and action buttons compact to icon-only before the toolbar can crowd.
- Conversation scroll position is now correctly restored when switching between session tabs.
- Conversation scroll position is now preserved when switching back to a previously visited session.
- Fixed a crash that prevented the app from launching on macOS when a repository's configuration file contained a quoted YAML value with 16 or more consecutive spaces.
- Fixed a doubled border line appearing between adjacent file headers in the diff view when files are collapsed or when a sticky header slides into view.
- Fixed a wide empty gap in the GitHub authentication banner on wide windows — the message and action buttons now sit flush together instead of being separated by dead space.
- Fixed an issue on Windows where browser-based features could fail when the app was launched using Windows application compatibility settings.
- Fixed sidebar toggle button being unclickable when the sidebar is collapsed on the home view
- Fixed the spinner on the Merge when ready button freezing instead of animating in WebKit.
- On macOS, the native menu bar now reflects your current keyboard shortcut bindings — remapped shortcuts appear correctly in the menu. The View menu item has also been renamed from "Open Search" to "Command Palette", and the keyboard shortcuts settings search now shows only your active bindings.
- On Windows, tools installed to the user-level PATH (such as winget, nuget, or any per-user tool install) are now correctly found when running agent sessions or the integrated terminal.
- Onboarding now correctly shows badges for all selected GitHub repositories, including those found via search.
- Slash command and mention suggestion popovers in the chat input now span the full width of the composer.
- The Add files and Add folder dialogs now open in the active workspace directory instead of an arbitrary OS default location.
- The Plan pill no longer shows a shimmer animation or count when a background agent is running but no plan exists.
- The Quick chats sidebar section now shows a "No quick chats yet" message when empty, instead of a blank area.
- The search query no longer resets when selecting repositories in multi-select mode.
- Timeline navigation now smoothly animates when jumping to conversation history items that are offscreen, and clicking the expanded timeline lane correctly selects the hovered item.
- When a project is linked to the wrong GitHub account, the app now detects the correct account and prompts to re-authorize it, instead of silently failing with errors on repository actions, pull request creation, and pull request polling.

## v1.0.9

### Highlights

- Quick chats now support tool-approval commands (/yolo, /allow-all-tools, /reset-allowed-tools) and session forking, bringing them to feature parity with code sessions.
- The Settings → Usage & Plan page now shows your active Copilot plan name directly beneath the Plan heading, so you no longer need to visit GitHub.com to see which plan you are on.
- Sessions awaiting your input now display a question-mark icon in the sidebar instead of a small dot, making the needs-input state easier to recognize at a glance.
- Fixed orphaned git fsmonitor daemon processes accumulating after each app quit — daemons are now stopped on worktree removal and when the app exits.
- Fixed the Windows tray icon disappearing against the taskbar when using a dark system theme — the icon now uses a theme-appropriate asset and updates automatically.

### Added

- Quick chats now support tool-approval commands (/yolo, /allow-all-tools, /reset-allowed-tools) and session forking, bringing them to feature parity with code sessions.
- Searching or filtering in Settings (Themes, MCP servers, Skills, Experimental, and Plugins) now announces the number of matching results to screen readers.
- The Settings → Usage & Plan page now shows your active Copilot plan name (e.g. Copilot Max, Copilot Pro+, Copilot Business) directly beneath the Plan heading, so you no longer need to visit GitHub.com to see which plan you are on.

### Changed

- Folder rows in the Files and Changes trees now show only a chevron (no redundant folder icon), and changed-file status icons align with the folder gutter — matching VS Code's file-tree style.
- Improved the empty states in the automations view when search or filters return no results: the runs list now shows a title, description, and a "Clear filters" button consistent with the gallery section.
- Removed the inline Split down and Split right buttons from the tab bar. Splitting is still available via the tab right-click context menu, drag-and-drop to a pane edge, and keyboard shortcuts.
- Sessions awaiting your input now display a question-mark icon in the sidebar instead of a small dot, making the needs-input state easier to recognize at a glance.
- The model-change notice in the conversation now displays the long-context window as a dot-separated suffix (e.g. "Claude Opus 4.8 · 1M") and renders the reasoning effort label with proper spacing, matching the model picker's style.

### Fixed

- Clicking an attachment label in the overflow menu no longer accidentally removes the attachment — removal now requires clicking the explicit X button.
- Clicking an attachment row in the composer overflow menu now opens or previews the attachment, matching the behavior of clicking the visible attachment pill.
- Column resizing in table views (such as manage sessions) now works reliably when dragging.
- Fixed orphaned git fsmonitor daemon processes accumulating after each app quit. Daemons are now stopped on worktree removal and when the app exits.
- Fixed the repository visibility selector (Public/Private) in the Create new repository and Publish to GitHub dialogs to use correct radio-group semantics, so screen readers now properly announce the selected option and its description.
- Fixed the Windows tray icon disappearing against the taskbar when using a dark system theme. The tray icon now uses a theme-appropriate asset and updates automatically when the system theme changes.
- Keyboard focus now moves correctly when adding or removing environment variable and header rows in the MCP server settings editor.
- Screen readers now announce the keyboard shortcut when focusing the Search button in the sidebar (e.g. "Search, Command + K" on macOS, "Search, Ctrl + K" on Windows/Linux).
- The "Feeling lucky" button in the theme picker now announces the number of new themes and the name of the theme it applied to screen readers, replacing an inaccurate theme count.

## v1.0.8

### Highlights

- Sessions now automatically remember your last model, reasoning effort, and long-context state — no more configuring a default model in settings.
- Screen-reader users can navigate the chat transcript message-by-message using heading navigation, with each message announced as 'You said:' or 'Copilot said:'.
- The issue pill in the composer now shows a color-coded status icon (open, completed, not planned), matching pull request pill behavior.
- The Changes panel file list now always displays as a tree view, with a file count and diff stat shown in the toolbar.
- Closing a Terminal tab now prompts for confirmation before ending the session, with a 'Don't ask again' option for future closes.

### Changed

- Canvas tool calls in the conversation now show the canvas icon instead of a generic tools icon, making them easier to recognize at a glance.
- Closing a Terminal tab in the right panel now shows a confirmation dialog before ending the session. A "Don't ask again" checkbox lets you skip the prompt for future closes.
- Merged pull requests now display the merge icon instead of the pull request icon, making merged state easier to recognize at a glance.
- Screen-reader users can now navigate the chat transcript message-by-message using heading navigation — each message is announced as "You said:" or "Copilot said:" followed by a preview of the text.
- The Changes panel file list now always displays as a tree view (the flat/tree toggle has been removed), the toolbar shows a file count and diff stat, file header names use lighter typography, and a doubled border under the toolbar is fixed.
- The issue pill in the composer now shows a color-coded status icon (open, completed, not planned) matching the existing pull request pill behavior.

### Fixed

- Fixed microphone test playback in Settings → Voice playing only in the left ear on Linux when using multi-channel audio interfaces.
- Fixed the selected file scope label in the Files panel toolbar (e.g. "Committed") showing in muted text instead of the default color, making the active selection easier to read.
- In the Last updated sidebar view, session groups with recent child activity now correctly float to the top and land in the right date bucket (e.g. "Recent sessions") instead of staying pinned to the parent session's older timestamp.
- Opening the Changes tab with the mouse no longer leaves a stuck focus ring on the file list.
- The 'Created session' tool call row in conversations now shows the correct icon instead of a generic wrench.
- The main composer is now hidden while an "Ask Question" prompt is open, preventing accidental messages from being sent instead of answering the prompt.

### Removed

- Removed the "Default model" section from Sessions settings. New sessions now automatically start with the model, reasoning effort, and long-context state from your last selection in the session model picker.

## v1.0.7

### Highlights

- Added a "Quick chat" option to the home screen project picker, letting you start a chat session directly without selecting a repository.
- Automation runs now show token, context, and AI-credit usage in the run details popover, matching what chat sessions already display.
- The model picker now widens to fit long custom model names, and custom model providers show their own brand icons in the picker.
- macOS traffic light buttons are now native controls, restoring accessibility support and the green button long-press window management menu.
- Fixed agent-merge incorrectly declining to merge pull requests that the user has permission to merge.

### Added

- Added a "Quick chat" option to the home screen project picker, letting you start a chat session directly without selecting a repository.
- Automation runs now show token, context, and AI-credit usage in the run details popover, matching what chat sessions already display. Reopening a past run shows the spend from that run.

### Changed

- macOS traffic light buttons are now native controls, restoring accessibility support and the green button long-press window management menu.
- The model picker now widens to fit long custom model names, and custom model providers show their own brand icons (Ollama, Azure, Microsoft Foundry, Foundry Local) in the picker and the "Model changed" message. The "Custom" badge on custom models now flows inline with the model name.
- Updated the top-level fuzzy-matchable slash commands for the Impeccable design skill. The promoted shortcuts are now `/impeccable audit`, `/impeccable critique`, `/impeccable live`, `/impeccable polish`, and `/impeccable distill`.

### Fixed

- Closed issues now show the correct status indicator everywhere, including the inbox: purple for completed, and grey with a circle-slash icon for issues closed as not planned or duplicate (instead of red or a generic closed badge).
- Fixed a crash in the tray menu that could occur on startup when store data arrived while the menu was being built.
- Fixed agent-merge incorrectly declining to merge pull requests that the user has permission to merge.
- Fixed clipped border corners on settings textareas (e.g. the Instructions field) caused by the horizontal scrollbar gutter.
- Sidebar tooltips now dismiss immediately when the sidebar is collapsed, instead of remaining visible and floating disconnected from their triggers.

## v1.0.6

### Highlights

- Type @ in any comment or description composer to get autocomplete suggestions for mentionable users and org teams in the current repository.
- Manage sessions now supports pill-style filters, a bulk-select toolbar, and bulk archive or delete with a confirmation step.
- The Automations screen now has a unified search that filters both automation cards and runs simultaneously, with matched text highlighted.
- Opening a background agent's activity tab now scrolls to the latest output and shows a live progress indicator while the agent is working.
- Manually renamed sessions and workspaces are no longer overwritten by the agent's automatic rename.

### Added

- Images in the canvas editor markdown preview now render for all users.
- Type @ in any comment or description composer to get autocomplete suggestions for mentionable users and org teams in the current repository.

### Changed

- Composer status pills that don't fit on one row now collapse into a circular "…" button; clicking it opens a menu listing the overflowed items instead of wrapping onto a second line.
- Conversation image attachments now preserve their natural aspect ratio instead of being cropped to a square, and multiple images are displayed in a balanced grid layout.
- Conversation transcript polish: long ask-user questions can now be expanded and collapsed with a chevron disclosure (keyboard accessible), while short questions that already fit stay as a plain row; the timeline picker only selects when you click an actual tick (not surrounding whitespace) and only reveals near the bars; the native scrollbar is no longer hidden when the timeline picker is showing; Cmd+K in the terminal now clears the buffer instead of opening the command palette; and the New Window shortcut is hidden unless multi-window support is enabled.
- Manage sessions now uses pill-style filters to narrow the list, a bottom toolbar to select and bulk-archive or bulk-delete sessions, and a confirmation step for all bulk actions.
- Opening a background agent's activity tab now scrolls to the latest output and shows a live progress indicator while the agent is working.
- Renamed the sidebar "Group by" time option from "Updated" to "Last updated" for clarity.
- Routine agent actions (internal memory bookkeeping, read-only session/workspace lookups, and session/workspace renames) are no longer shown as individual rows in the conversation timeline, reducing clutter. Completed thinking and activity blocks now start collapsed by default.
- The "Manage sessions" view now shows two separate disk usage columns — "Files (Disk)" for the session's working files and "Chat (Disk)" for the chat history — instead of a single combined column. Both columns are sortable.
- The Automations screen now has a unified search input that filters both automation cards and runs simultaneously, with matched text highlighted. A filter icon inside the search bar provides access to Project, Status, and 'Runs of' filters. No-match states now show a proper empty state with a 'Clear filters' button.

### Fixed

- Action buttons in the home page "Up next" list are now visible when focused via keyboard, not only on mouse hover.
- Ctrl+Z (undo) and Ctrl+Shift+Z / Ctrl+Y (redo) now work in the chat composer on Linux, where WebKitGTK doesn't bind those keystrokes to native editing by default.
- Fixed a Windows resource leak where tray menu rebuilds could accumulate USER objects over time, potentially causing the app to malfunction after many session changes.
- Fixed an issue where the "This project's GitHub account was removed" banner could stay stuck even though the correct account was still connected.
- Fixed empty system sounds picker on Linux in notification settings
- Fixed image preview bounding box being wider than the image for wide (e.g. panoramic) images in conversations.
- Fixed the chat composer floating in the middle of the screen instead of staying pinned to the bottom when there are only a few messages.
- Fixed the in-app pull request view failing to load on GHES and GHE.com (data residency) hosts, where it previously showed a GraphQL schema error.
- Manually renamed sessions and workspaces are no longer overwritten by the agent's automatic rename.
- Running a script now focuses its terminal tab, so the command starts and streams output immediately instead of waiting until you click into the tab.
- Screen readers now correctly announce punctuation and arrow-key shortcuts in the command palette (e.g. "Command + Comma" for the Go to Settings shortcut), instead of silently dropping them.
- Slash command menu now filters more accurately and no longer surfaces unrelated commands when nothing matches the typed query. Keyboard shortcut glyphs in menus are now sized to match the surrounding text.
- The sidebar resize handle now shows a visible hover stripe when you drag to resize, making it easier to discover; Swift files now display syntax highlighting in the file viewer.
- The terminal now shows a clear, actionable error when your $SHELL points to a path that no longer exists, instead of a raw system error.
- When viewing a referenced pull request in the session panel, the Overview and Changes tabs are now shown so you can browse the PR diff.

## v1.0.5

### Added

- Model Providers configuration — connect your own API keys from OpenAI, Anthropic, Azure, and others — is now available to all users in Settings.

### Fixed

- Fixed a sidebar status flicker where merging a pull request briefly bounced between "Ready to merge" and "Done" before settling.

## v1.0.4

### Highlights

- Fixed a bug where backslashes (e.g. in Windows paths, LaTeX, or regex) were doubled on every save in the markdown editor, progressively corrupting files.
- Fixed multi-second freezes when opening the right-click context menu, command palette, and merge drawer while content was loading — open times now stay consistently fast.
- After an Autopilot task finishes, the session mode now automatically reverts to Interactive so your next prompt isn't silently run in Autopilot.
- The /impeccable design skill's subcommands are now discoverable and selectable directly in the slash-command palette.
- Fixed a frame-rate drop to ~5fps when typing in the composer while the agent streams a response.

### Added

- Added a `ghapp://automations/new` deep link that opens the new automation dialog with name, prompt, and trigger schedule pre-filled — the workflow is not created until the user clicks Create.
- Added an "Automatically check for updates" toggle in General settings. When turned off, the app no longer runs background update checks on launch or hourly; the manual "Check for updates" action still works.
- After the agent finishes an Autopilot task, the session mode now automatically reverts to Interactive so your next prompt is not silently run in Autopilot.
- The /impeccable design skill's subcommands (shape, craft, critique, polish, and more) are now discoverable and selectable directly in the slash-command palette.
- When the Impeccable design skill is enabled, the design hook now fires automatically after each file edit, giving the agent immediate design feedback to incorporate into its next step.

### Changed

- Internal: Desktop's Copilot CLI sessions can enable memory through typed copilot-sdk session configuration when the Session memory experiment is enabled.
- Renamed the "Recent sessions" menu item and view title to "Manage sessions" to better reflect that it supports search, bulk archive, and delete — not just a list of recent activity.
- Running a script now opens the run output as a regular tab instead of forcing a bottom split, so your current view stays undisturbed when the panel is already open.
- Settings tabs now preserve their state (search queries, expanded rows, and scroll position) when switching between sections, and switching back to a previously visited tab is instant.
- The Auto model row in the model picker now shows an info popover explaining that Auto selects the best model for your request and that usage through Auto is billed at a 10% discount.
- When the agent views multiple images in a single batch, they now collapse into a single "View N images" tool call that expands into a row of clickable thumbnails when clicked.

### Fixed

- Fixed a bug in the markdown editor canvas where backslashes (e.g. in Windows paths, LaTeX, or regex) were doubled on every save, progressively corrupting the file.
- Fixed a frame-rate drop (down to ~5fps) when typing in the composer while the agent is streaming a response, caused by an ungated per-row ResizeObserver in the conversation list.
- Fixed a remaining cause of multi-second freezes when opening the right-click context menu, command palette, and merge drawer while a diff, checks, or conversation was loading — open times now stay consistently fast.
- Fixed background agent duration showing an inflated time (e.g. "67h 8m") in the composer pill after resuming a session.
- Fixed image drag-and-drop onto the prompt composer being silently ignored on macOS Retina displays.
- Fixed the bulk selection toolbar in My Work wrapping the item count onto two lines when many items are selected.
- In multi-account setups, the avatar shown on ask_user prompt answers now correctly reflects the account linked to the session's repository instead of always showing the default account.
- Issue type indicators in the issue detail toolbar now show as hollow rings instead of filled circles, matching the style used elsewhere in the app and on GitHub.com.
- Keyboard users can now navigate the PR comment reaction picker using arrow keys, with Home/End to jump to the first or last emoji.
- Links in rendered markdown content now show a pointer cursor on hover, making them feel correctly interactive.
- Question and answer text in ask_user conversation rows is now selectable and copyable.
- The My Work detail panel now shows a proper empty state with a close button when no item is selected, so the panel is no longer a dead end.
- When an agent creates a sub-session via the `create_session` tool and specifies a custom agent in the kickoff parameters, the child session now correctly loads that agent instead of inheriting the parent session's agent.
- When multiple local clones of the same repository are open, the project picker now shows distinct labels (e.g. "work/webapp" and "personal/webapp") instead of identical names.

## v1.0.3

### Highlights

- Fixed a critical bug where an in-app update could silently wipe all workspaces and session history — the app now automatically recovers from a backup if the database is found empty or corrupt at startup.
- Daily scheduled workflows now support selecting multiple hours, so the same automation can run at several times per day without writing a custom cron expression.
- Settings now has a dedicated Sessions tab grouping session-related options — default model, custom instructions, auto-approve, agent merge attribution, remote access, and session lifecycle.
- The session info popover now shows a complete context window breakdown — system prompt, tools, MCP tools, messages, free space, and buffer — at any time, not just during an active turn.
- Fixed a progressive slowdown when opening the right-click context menu, command palette, and merge drawer after extended use — open times now stay consistently fast.

### Added

- Daily scheduled workflows now support selecting multiple hours, so the same automation can run at several times per day without writing a custom cron expression.
- Deep links now support opening a specific cloud automation or cloud automation run directly in the app (e.g. from a notification or the GitHub automations page).
- You can now customize project groups in the sidebar with a display name and color — right-click a project group and choose Customize to personalize it.

### Changed

- Bash command rows now show a live elapsed timer while a command is running, making it easy to tell how long a command has been going.
- Failed workflow run errors now show an inline copy button on hover, making it easy to copy exact error text without interfering with clicking the row.
- Merged pull requests now display the same pull request icon as open pull requests, distinguished by color, for a more consistent appearance everywhere they're shown.
- Pull request descriptions that fail to load now show a clear error with a Try again button instead of an empty description.
- Settings now has a dedicated "Sessions" tab grouping session-related options (default model, custom instructions, auto-approve, agent merge attribution, remote access, and session lifecycle) separately from general app settings.
- The send button in the prompt composer now changes color to match the active session mode — blue for Plan mode and green for Autopilot mode.
- The session info popover now shows a complete context window breakdown — system prompt, tools, MCP tools, messages, free space, and buffer — at any time, not just during an active turn.
- The Submit review and Cancel buttons in the PR review panel are now right-aligned, with Cancel to the left of Submit review, matching standard dialog conventions.

### Fixed

- Agent autocomplete now reflects newly installed or removed plugin-provided agents without requiring a restart.
- Changing reasoning effort without switching models now shows the correct notice (e.g. "Reasoning effort changed from Medium to High.") instead of incorrectly saying the model changed.
- Fixed a bug where an in-app update could silently wipe all workspaces and session history on the next launch. The app now automatically recovers from a backup if the database is found empty or corrupt at startup.
- Fixed an issue where the PR button always used "main" as the target branch even when a different base branch was selected, especially when clicking the button quickly before changes had loaded.
- Fixed conversation messages overlapping a long first prompt when scrolling through the chat history.
- Fixed file drag-and-drop missing the drop target on high-DPI displays.
- Fixed near-black hue colors in the Monochrome theme in light mode — colored elements now render as distinct, visible hues instead of collapsing to near-black.
- Fixed progressive slowdown when opening the right-click context menu, command palette, and merge drawer after extended app use — open times could grow from milliseconds to several seconds and now stay consistently fast.
- Fixed the breadcrumb in the pull request detail view being hidden behind macOS window controls when the sidebar is collapsed.
- In the sidebar's group-by-status view, a session tree now surfaces in its most urgent group, so a ready-to-merge or needs-input child session bubbles the whole tree up instead of being hidden under the root session's group.
- Issues that were transferred between repositories no longer get stuck on "Loading..." when opened, whether from the inbox or inside a session.
- Pull requests that have automatic merge enabled but with the 'Merge pull request' action turned off now correctly appear as ready to merge in the sidebar.
- The auto-merge button in the pull request merge drawer no longer flashes back to its previous state while the request is in flight — enabling or disabling auto-merge now immediately reflects the new state.
- Voice dictation no longer prevents the Linux app from launching on PipeWire or bare ALSA systems without PulseAudio client libraries installed.

## v1.0.2

### Highlights

- Session forking is now available to all users: fork a session from a completed agent response to explore an alternative approach, then merge the forked work back to the parent session.
- Pull request creation now automatically creates or reuses forks for public repositories when you don't have push access to the upstream.
- Start a Copilot session in any repository directly from an issue's context menu in My Work, not just the repository the issue was filed in.
- Weekly automations can now be scheduled to run on multiple days of the week.
- Remote sessions are easier to find: the sidebar's new-project menu includes a 'Resume remote session…' option, and the command palette groups remote sessions by repository.

### Added

- Added a "New session in repository..." option to the issue context menu in My work, letting you start a session in a different repository than the one the issue was filed in. The bulk Actions picker can also start individual sessions in a chosen repository.
- Pull request creation can now automatically create or reuse forks for public repositories when the current user cannot push to the upstream repository.
- Session forking is now available to all users: fork a session from a completed agent response to explore an alternative approach, then merge the forked work back to the parent session.
- Weekly automations can now be scheduled to run on multiple days of the week. Select multiple weekday checkboxes when creating or editing a weekly automation; the trigger displays a compact summary (e.g. "3 days selected") and the selected days are restored when you reopen the automation.

### Changed

- Clicking a GitHub issue link in chat or a canvas opens the issue in the app's side panel instead of the system browser. Right-click the link to open it in your default browser or copy it; in a canvas, Cmd/Ctrl-click also opens it in your browser.
- In the sidebar, sessions with an open pull request now appear above sessions that are still actively running.
- Remote sessions are now easier to find: the sidebar's new-project menu includes a 'Resume remote session…' option, and the command palette groups remote sessions by repository with pull-request or branch icons.
- Search and grep tool results are now grouped by file, showing each file path once as a header with a line-number gutter, making results easier to scan.
- Sessions whose PR is ready to merge now appear under a dedicated "Ready to merge" group in the grouped sidebar view, instead of being mixed into "Needs input".
- Settings sidebar navigation is now organized into logical groups, labels use consistent sentence case ("MCP servers", "Model providers"), and Model providers has a new icon.
- The composer now shows a dedicated Plan pill and a separate Background agents pill again, instead of a single combined Tasks pill.
- The default branch prefix now uses a dash separator (e.g. `username-my-feature`) instead of a slash (e.g. `username/my-feature`) for newly generated branch names.

### Fixed

- An error message now appears under the repository name input in the create repository dialog when the name contains disallowed characters, instead of the Create button silently staying disabled.
- Fixed a file-watcher leak that could accumulate while opening, archiving, and deleting workspaces over a long session, eventually exhausting the app's file watchers and causing it to stop detecting file changes until restart.
- Fixed an issue where editing the interval of a workspace-bound automation workflow (e.g., manual → hourly) would silently revert to the previous value after saving.
- Fixed an issue where the composer pills (Changes, PR, Plan, Tasks) would briefly stack vertically when closing an expanded panel.
- My Work list rows now stay highlighted while their context menu is open, making it clear which item the menu applies to.
- Opening the Automations view via a deep link on cold start no longer intermittently shows a blank screen.
- Repository name input no longer auto-capitalizes the first letter — the exact casing you type is now preserved.
- The add-tab (+) button in the right-panel tab bar now sits immediately after the last tab instead of floating at the far right edge of the bar.
- The changed-files count no longer resets to zero when a file-watcher error occurs; the last known file list is preserved until a successful update arrives.
- User, plugin, and remote agents are now shown in the /agent command when working inside a project, not just project-scoped agents.

## v1.0.1

### Highlights

- Added configurable branch prefix settings — set an app-wide default and a per-project override for the prefix used when generating worktree branches.
- External links can now open the app and pre-fill the plugin install form via deep links, letting plugin marketplace READMEs link directly into Settings → Plugins.
- Sketch is now available as a recommended MCP server in Settings, letting you connect Copilot to your Sketch designs.
- GitHub issue and pull request links now open in-app by default, showing them in right-panel tabs or the My Work detail view instead of the system browser.
- The "Default model" option has been removed from General Settings — your model, reasoning effort, and context tier selections in the composer are now automatically used for new sessions.

### Added

- Added configurable branch prefix settings — set an app-wide default and a per-project override for the prefix used when generating worktree branches.
- External links can now open the app and pre-fill the plugin install or add-marketplace form via deep links, letting plugin marketplace READMEs link directly into Settings → Plugins.
- Sketch is now available as a recommended MCP server in Settings, letting you connect Copilot to your Sketch designs.

### Changed

- GitHub issue and pull request links now open in-app by default across markdown and timeline cross-reference surfaces. In workspace sessions they open in right-panel issue/PR tabs, and in My Work they navigate to the corresponding detail view. Right-click on these links shows a consistent Open link and Copy link menu, where Open link and Cmd/Ctrl-click still open the system browser.
- In the composer Tasks panel, group headers ("To-dos" / "Background agents") are now hidden when only one group is present, reducing visual clutter.
- MCP settings now groups servers into categories — 'On this device', 'Plugins', and 'Built-in' — making it easier to see which servers come from plugins versus your own configuration.
- The "My work" filter bar now shows only your active filters instead of listing all available filters as placeholder pills. Adding a filter and then clearing its value keeps the picker open so you can choose a new value, and closing the picker with no value removes the pill. Filters showing "Any" now appear visually muted.
- The feature tip on new-session and quick-chat empty states is now stable for the duration of a session. The auto-rotating behavior and the "Show another tip" button have been removed.
- The sidebar's 'Filter sessions' dropdown (Sort by, Projects) has been replaced with a single toggle button to switch between grouped and flat session views.
- Updated slash command descriptions to use "session" instead of "workspace".
- When the agent asks you a question, your answer now shows your GitHub avatar and a curved connector linking the question to your response.

### Fixed

- Fixed an intermittent error ('Cannot rebase onto multiple branches') that occurred when running git rebase or git pull --rebase in a workspace while the app was open and polling for sync status in the background.
- Fixed the focus ring not appearing on the Keyboard Shortcuts settings heading when navigating to it via deep link on macOS.
- Keyboard focus ring now appears correctly when navigating the server-type selector in Settings → MCP Servers → Add server using arrow keys on macOS.
- Label color dots in the pull request and issue metadata toolbar now match the colors shown in the labels dropdown.
- macOS: pressing `Home` or `End` on an external keyboard no longer inserts an invalid `.notdef` box character (U+F729 / U+F72B) into the chat composer, home-screen prompt, or other text inputs.
- On Windows, the app no longer becomes unresponsive to NVDA and Windows Voice Access after the window loses focus or is covered by another window.
- On Windows, the Open dialog now shows the correct icon for PowerShell (Core / 7+) and correctly labels the legacy entry as "Windows PowerShell".
- Opening a dialog (such as Settings) now closes any open menu instead of leaving it visible on screen.
- Opening a non-text binary file (e.g. a font or other binary file) in the workspace file viewer now shows the "This file can't be previewed" placeholder instead of a "Failed to load workspace file." error banner.
- Restored the separate "Show another tip" button on the empty-state rotating tips, so the tip text is read as content instead of being hidden inside the button's accessible name.
- Right-clicking an item in My Work and choosing "New session" from the context menu now opens the session composer (where you can choose a model and write a prompt) instead of immediately starting an automatic review.
- Screen readers now announce the number of matching shortcuts (e.g. "3 shortcuts found" or "No shortcuts found") when filtering the keyboard shortcuts list in Settings → Accessibility.
- Text in extension canvases (editor preview, browser, terminal, and others) now renders with the same font smoothing as the rest of the app.
- The in-app terminal now correctly reports its terminal type as xterm-256color regardless of how the app was launched, fixing broken colors and missing capabilities in shells and TUI programs when the app was started from tmux, screen, or the macOS dock.
- Users on unlimited plans now see an infinity icon and a 'No usage limit' label in the prompt composer usage gauge instead of a blank space.
- Videos attached to a pull request or issue now play in the detail panel instead of showing a blank area.
- When editing an existing cloud automation, the "Run in the cloud" switch now correctly shows as enabled and disabled (read-only) instead of being hidden, and clicking the label text no longer accidentally toggles the switch.
- When opening the Keyboard Shortcuts settings section via the command palette, the section heading is now focused and scrolled into view.

### Removed

- The "Default model" option has been removed from General Settings. Your model, reasoning effort, and context tier selections in the composer are now automatically used when creating new sessions.

## v1.0.0

### Highlights

- The Recent sessions view now supports bulk actions — select multiple sessions and archive or delete them at once, with new sortable Branch and Created columns.
- The composer now shows a dedicated Tasks pill combining to-dos and background agents, plus a separate Plan pill that opens the plan document.
- In Local mode, the session composer now includes a branch picker so you can choose which branch to start a session on.
- Business, Enterprise, and GHES users whose organization had 'Editor preview features' disabled are no longer blocked from accessing the app during sign-in.
- Your local repository vs. new worktree preference for new sessions now carries across projects, defaulting to the type you last chose.

### Added

- Added an About dialog (accessible via the GitHub menu) that includes a License and Open Source Notices section listing third-party dependency licenses.
- Added an AI disclaimer — "GitHub Copilot uses AI. Check for mistakes." — at the bottom of the home view.
- In Local mode, the session composer now shows a branch picker so you can choose which branch to start a session on instead of always using the current branch.
- The Recent sessions view now supports bulk actions: select multiple sessions via checkboxes and archive or delete them at once. The view also gains sortable Branch and Created columns and a header actions menu with options to reset column widths or delete all archived sessions.

### Changed

- The composer now shows a dedicated Tasks pill that combines to-dos and background agents in one panel, plus a separate Plan pill that opens the plan document. The right-panel Plan tab is reserved for plan.md content and no longer appears for to-do-only sessions.

### Fixed

- Business, Enterprise, and GHES users whose organization had "Editor preview features" disabled are no longer blocked from accessing the app during sign-in.
- Enlarged the checkbox hit target in the My work and Recent sessions tables so the full cell area toggles selection, not just the small checkbox box.
- Fixed accessibility issues when customizing keyboard shortcuts in Settings: focus is now properly managed when entering capture mode, screen readers now announce shortcut recording state and results, and conflict resolution buttons are reachable by keyboard.
- The local repository vs. new worktree choice for new sessions now carries across projects — opening a project you haven't configured before defaults to the type you last chose, instead of always resetting to a new worktree.

## v0.2.34

### Highlights

- Added a Plugins tab in Settings to install, manage, and browse Copilot plugins from marketplaces, with enable/disable toggles, update, and uninstall.
- Pull request and issue detail views now show a metadata toolbar below the title with one-click editing for reviewers, assignees, and labels.
- You can now select and copy text from the diff view, with selections preserved as you scroll.
- New session screens display rotating feature tips covering slash commands, file references, modes, and more.
- Clicking a choice in an ask-user prompt now confirms it immediately, removing the need for a second Continue click.

### Added

- Added a Plugins tab in Settings to install, manage, and browse Copilot plugins from marketplaces, including enable/disable toggles, update, and uninstall.
- Added an "Open in default browser" option to the right-click context menu on links in chat messages.
- New session screens now display rotating feature tips — covering slash commands, file references, modes, and more — so you can discover what Copilot can do while you think about your first message.
- Pull request and issue detail views now show a metadata toolbar directly below the title with pill-shaped buttons for reviewers, assignees, and labels — each editable in one click.
- You can now select and copy text from the diff view, with selections preserved as you scroll through virtualized content.

### Changed

- Clicking a choice in an ask-user prompt now confirms it immediately, removing the need to click Continue as a second step.
- The rotating tip in the empty states is now more accessible: its shuffle control names the action in its accessible name ("Show another tip"), and a newly shuffled tip is announced to screen readers.
- You can now scroll the mouse wheel over the right-panel tab bar to reveal tabs that don't fit on screen, in addition to using the overflow menu.

### Fixed

- Fixed a horizontal scrollbar appearing in the Settings dialog at high browser zoom levels.
- In the keyboard shortcuts help dialog, screen readers now read each shortcut as a structured list that pairs the action with its keys, and announce punctuation keys such as comma, brackets, and backtick by name instead of skipping them.
- Long single-word pull request and issue titles (such as test method names) now wrap correctly instead of overflowing the container in both the full-screen and sidebar panel views.
- On Linux, middle-click paste no longer unexpectedly attaches a clipboard image to the message composer.
- Screen readers now announce the correct last-updated time for sidebar workspace rows instead of always saying '2 minutes ago'.
- Screen readers now announce which item is active in the Settings navigation panel, making it easier to orient within the Settings dialog without leaving the navigation list.
- Screen readers now correctly announce "Settings" (instead of "Projects") when the Settings dialog opens.
- The 'No GitHub repositories yet' empty-state heading in My Work is now a real heading, allowing screen-reader users to reach it via heading navigation.
- The Settings dialog page title is now properly announced as a heading by screen readers, improving navigation for assistive technology users.
- VoiceOver now announces Skills settings rows correctly — the disclosure reads only the skill name instead of including the action buttons' labels in the announcement.

## v0.2.33

### Highlights

- Added a /orchestrate composer command for coordinating multi-session and multi-repo work, letting the agent delegate tasks across child sessions.
- Added /context and /usage slash commands to view your session's token usage and AI credit spend, or your plan's usage and rate limits.
- The agent can now create cloud sessions on your behalf when using the create_session tool, in addition to local sessions.
- MCP App UI panels can no longer send chat messages or invoke tools without a user gesture, closing a security vulnerability where a server-authored panel could act automatically on load.
- Mermaid diagrams now render using the improved Beautiful Mermaid renderer by default, with automatic fallback for unsupported syntax.

### Added

- Added /context and /usage slash commands in the chat composer. /context opens the session usage summary (token count, context window, and AI credit spend); /usage opens your plan's usage and rate limits.
- Added a /orchestrate composer command for coordinating multi-session and multi-repo work, letting the agent delegate tasks across child sessions instead of working inline.
- File paths mentioned in assistant messages that point to generated artifacts are now rendered as clickable links that open the file in the right panel.
- The agent can now create cloud sessions on your behalf when using the create_session tool, in addition to local sessions.

### Changed

- Error toasts now show up to 4 lines of text, stay visible for 10 seconds, and include a "Copy error" button for messages with dynamic content so you can easily capture error details for bug reports.
- File paths mentioned in agent responses are now always clickable, opening the file directly in the editor.
- Images in conversations and pull requests now load lazily and use less memory.
- Improved accessibility of the Share feedback dialog: the topic menu now announces its current selection, the feedback textarea has a proper label, the submit button stays focusable and is announced as unavailable when empty, the mood picker uses correct radio button semantics with arrow-key navigation, and Tab no longer dismisses the dialog when focus is on the last control.
- Improved the command palette's session actions: added an "Open in panel..." item to open a terminal, browser, or other panel without leaving the keyboard; removed the now-redundant individual "Open terminal" and "Open browser" items; reordered thinking controls so "Set thinking effort" appears before the reasoning toggle; moved share and extension items to the bottom; and hid "Create PR" when the session has no changes. Also added a keyboard-shortcut tooltip to the right panel's "+" add-tab button.
- Mermaid diagrams now render using the improved Beautiful Mermaid renderer by default, with automatic fallback to the legacy renderer for unsupported syntax.
- The Azure DevOps popular MCP server preset now uses the hosted remote endpoint instead of a local npx command, so adding it no longer requires a local Node.js install.
- The find dialog (Cmd+F) is now unified across the conversation, diff view, and Home — one consistent experience with shared scope toggles wherever you search.

### Fixed

- Agent merge no longer silently enables on draft pull requests. Previously, a sticky per-project default could inherit onto a new draft PR and queue GitHub auto-merge without the user's knowledge.
- Binary and non-text files (e.g. .xlsx) now show a helpful empty state with "Show in Finder" and "Open file" actions instead of a raw error message. "Show in Finder/Explorer/File Manager" is also available in the file tree context menu and in the artifact editor toolbar.
- Copy, share, and bookmark actions now reliably appear on assistant responses in conversations that include tool use, task completions, or resumed historical sessions.
- Creating a session from a pull request no longer silently fails when the project's linked GitHub account is missing. The link is automatically restored if possible, and if not, an actionable error message is shown with the option to reassign the account in Project Settings.
- Dismissing the auto-cleanup prompt (via the X button, Escape, or swipe) now permanently suppresses it instead of allowing it to reappear on every app launch or every 6 hours.
- Fixed a bug where a new empty chat was created in the sidebar on every app launch.
- Fixed extra spacing on the Changes tab when no diff stats are present, so all workspace tabs now have consistent padding.
- Fixed the "GitHub authorization needed" banner flashing on and off during normal use.
- MCP App UI panels can no longer send chat messages or invoke tools on behalf of the user without a user gesture, closing a security vulnerability where a server-authored panel could do so automatically on load.
- Pasting rich content into the composer now imports supported formatting without inserting raw HTML markup. Cmd/Ctrl+Shift+V (paste as plain text) reliably inserts literal text without applying markdown formatting or link wrapping.
- Pending message bubbles now display a clearly visible dashed outline instead of a faint one.
- Pending user messages now show a "Pending" label on hover instead of a misleading timestamp.
- Quick chats are now automatically renamed by the agent based on the conversation content, matching the behavior of project sessions.
- Screen readers now announce correct item counts, keyboard shortcut names, and external-link affordances in app menus.
- Selecting a session from the Cmd-K palette now focuses the prompt composer on arrival, so you can start typing immediately without an extra click.
- The "Create from…" dialog now shows "Matching pull requests" and "Matching issues" instead of "Cached pull requests" and "Cached issues" when searching.
- The command palette now shows 'User extension' or 'Project extension' next to identically named extensions, making it easy to tell them apart when both scopes are installed.
- The sidebar toggle is now visible and usable while a workspace panel is maximized, so you can show or hide the sidebar without leaving panel focus mode.
- Toggle switches now maintain clear visual contrast across all themes, including custom and monochrome themes in both light and dark mode.
- Tooltips in the bottom pane of a split layout now display correctly instead of being hidden behind a browser preview pane.
- Voice mode mic test playback no longer hijacks the system play/pause media key.

### Removed

- Agent merge no longer remembers the last selection per project. This sticky default could enable agent merge on PRs the user never explicitly opted in for; agent merge is now always opt-in per PR.

## v0.2.32

### Added

- Export markdown content as a secret GitHub Gist from the workspace plan canvas, markdown file editor, and assistant reply actions.
- Free Copilot plan users now see an upgrade prompt in Account settings highlighting higher usage limits, premium models, and AI reviews.
- Use the /agent slash command in the prompt composer to select a custom agent for your session. The active agent is shown in the branch popover and persists across app restarts.

### Changed

- Creating a new session is now significantly faster — model data is preloaded in the background while the workspace is being set up, reducing cold-start time by ~900ms.
- Inline-code file paths in the markdown file viewer are now rendered as clickable pills that open the file directly, matching the behavior already present in chat messages and tool-call results. Newly created files also become clickable immediately without requiring a reload.
- The label filter picker in the work filter bar now renders GitHub emoji shortcodes (e.g. :bug:) as emoji glyphs instead of raw text.
- When a project's startup script fails, the error notification now shows a tail of the captured script output inline, along with a "View logs" action to see the full output and an "Edit script" action to jump directly to the project's script settings.

### Fixed

- Browser preview and extension canvas panels now correctly reflect the app zoom level instead of staying at a stale zoom when the zoom setting is changed.
- Centered dialogs no longer overflow off-screen or hide their footer and close button when the viewport is short or the user has zoomed in.
- Fixed a bug where toggling a state filter value off in the My work filter bar would have no effect when the view was saved with a legacy state qualifier (e.g. built-in views like Active), leaving the selection permanently stuck.
- On Linux, selecting a .desktop application from the "Open in..." custom app picker now correctly launches the app and displays its icon.
- Pressing ArrowDown from the newest prompt history entry now restores the saved draft and closes the history popover, instead of leaving the composer stuck at the most recent history item.
- Sleep prevention (keep awake) now works on Linux via systemd-logind D-Bus inhibit; the settings toggle is also visible on Linux.

## v0.2.31

### Added

- A new Background agents pill above the composer lists active background tasks; clicking a task opens its output in a side panel. In-chat subagent rows now also open task output in a side panel and show agent-type icons.
- Added a per-row actions menu to the pull request checks panel, letting you re-run failed checks, cancel pending checks, and open check logs without leaving the workspace.
- Agent merge now remembers your last choice per project. When you create a pull request, the agent-merge selection you last used in that project is reapplied automatically, so you don't have to re-enable it every time.
- GitHub Projects URLs pasted into the chat composer now render as styled reference pills (with the project name and icon), matching the existing behavior for Issues and Pull Requests.
- Quick chat now shows an empty state with a GitHub mark and rotating tips when no messages have been sent yet, helping users discover available commands and features.
- Right-clicking a GitHub-backed project in the sidebar now shows an "Open on GitHub" option that opens the repository in the browser.
- Right-clicking selected text in a conversation reply now shows a context menu with options to copy the selection or quote it as a follow-up in the composer.

### Changed

- Active tabs now use medium font weight instead of semibold, giving tab strips a lighter, more balanced appearance across the app.
- Git operations (such as status and diff) are now significantly faster when working with large repositories.
- The onboarding screen for users without access now directs them to explore Copilot subscription plans instead of joining a waitlist.

### Fixed

- Agent merge now starts its first check promptly after a pull request is created instead of waiting up to a minute.
- Clicking the scrollbar or padding in the slash command, skill mention, and file reference menus no longer closes the menu before you can scroll.
- Diff comments containing bare GitHub URLs no longer render clipped or invisible after their link metadata loads.
- Fix the Linux clipboard via the native backend: images now paste when the webview doesn't expose them, and copy buttons work on wlroots Wayland compositors (such as Hyprland).
- Fixed a 2–3 second UI freeze on macOS when enabling voice dictation for the first time and the microphone permission prompt appeared.
- Fixed a security issue where agent-generated links using dangerous URL schemes (javascript:, data:, vbscript:) could execute code in the app.
- Fixed git operations failing with "terminal prompts disabled" when working in repositories with non-GitHub remotes (Azure DevOps, GitLab, Bitbucket, etc.)
- Fixed high GPU usage and fan spin-up on macOS while the app is idle, particularly noticeable on high-refresh-rate (120 Hz ProMotion) displays.
- Fixed intermittent server errors when performing pull request actions (such as queuing, toggling auto-merge, and adding reactions) by automatically retrying transient failures.
- Fixed the merge panel incorrectly showing "Merge blocked" when a pull request is in the merge queue; it now correctly shows "Queued to merge".
- Fixed the Update branch button in the merge drawer incorrectly triggering the conflict-resolution agent flow when the branch was simply behind the base branch with no merge conflicts.
- Links and avatars in the inbox, pull request view, and prompt URL chips now correctly point to the right host when connected to a GitHub Enterprise Cloud Data Residency instance.
- Mention, issue, and commit autolinks in pull request and comment bodies now resolve to the correct host when connected to a GitHub Enterprise Cloud Data Residency instance.
- On macOS and Linux, the app now restricts the local database file (which may contain an auth token) to owner-only permissions (0600), and repairs existing installations on the next launch.
- Opening Settings is now faster.
- Opening the command palette (⌘K) is now faster and feels instant: it no longer triggers redundant network subscriptions on every open (which could cause multi-second delays for users with many pull requests), renders its overlay through a dedicated portal to avoid expensive whole-window style recalculation, and appears immediately instead of animating in.
- Project attachment pills in the composer now show the correct project icon and project name instead of the GitHub owner avatar and a user-like label.
- Screen readers now announce the actual key combination when focusing a keyboard shortcut chip in Settings › Accessibility › Keyboard shortcuts, instead of only reading the command name.
- The app now attempts to bring itself to the foreground when opened via a deep link from the browser, including when the app window is on a different macOS Space.
- The auto-merge agent no longer blocks on or attempts to fix optional (non-required) CI checks; only checks required by branch protection are considered when determining whether a PR is mergeable.

## v0.2.30

### Added

- Added a "Remote sessions" setting in General settings that lets you choose the default remote behavior for new sessions: Off, Export (transcript only), or Remote control.
- Added a new "Agent merge reply attribution" toggle in Settings > General (on by default). When enabled, agent merge appends a short attribution line to the replies it posts when resolving pull request review threads, indicating the reply was made automatically by the GitHub Copilot app.
- Quick Chat now includes an integrated terminal in its right panel, so you can run commands without leaving the chat.
- You can now paste or drag-and-drop images directly into GitHub comment boxes (issues, pull requests, reviews, and the create issue dialog) — the image uploads automatically and the hosted link is inserted into the comment.

### Changed

- Agent questions now appear as a card above the composer instead of replacing it. Clicking a choice or pressing its number key highlights it; pressing Enter or clicking Continue confirms. Pressing Escape or sending a normal message dismisses the prompt.
- Anthropic model names now display in full (e.g. "Claude Opus 4.8", "Claude Sonnet 4.6") in the model picker and model-change messages, matching how GPT and Gemini models are already shown.
- Clicking Run now opens the run-script terminal in a bottom split of the right panel instead of taking over the main tab group, so the diff or files surface stays visible above the run output.
- The command palette placeholder now mentions sessions, making it easier to discover that you can search for active sessions from the same entry point.
- The pull request inbox now loads initial results faster; diff stats and check status badges appear shortly after in a follow-up update.

### Fixed

- (Windows/Linux) Deep-links now route to the focused app instance when multiple instances are running, and closing one instance no longer breaks deep-link handling in others.
- API errors (billing misconfiguration, bad credentials, server errors, connection failures) now display as readable messages in the conversation instead of raw JSON or HTTP response text.
- Canvas tabs (extension, editor, and browser canvases) no longer reappear after restarting a session when the user had previously closed them.
- Closing a terminal canvas now persists across session switches — it no longer reappears when reselecting a session.
- Enabling remote control now shows a clear error when the session is unavailable (e.g. blocked by enterprise policy) instead of a false success notification with non-functional actions.
- Fixed a bug in the Rich view editor where saving a markdown file containing snake_case identifiers in tables caused backslashes to double on every save, ballooning the file size and freezing the session.
- Fixed a false "Copilot CLI failed to start" error that could appear on busy machines even when the CLI was healthy.
- Fixed a performance issue where opening multiple workspaces could pin a CPU core at 100% and cause the app to drop to near-zero frames per second.
- Fixed an error when opening an installed extension canvas from the "+" menu that caused a "Failed to open canvas" error for extensions with longer names.
- Fixed an error where USB microphones reporting 24-bit or 32-bit audio formats (such as the Jabra Link 380 on Windows) failed with "Unsupported microphone sample format" in Voice mode.
- Fixed an issue on macOS and Linux where Git Credential Manager would repeatedly display a "GitHub Sign in" dialog during background git operations, causing a loop of prompts that could not be permanently dismissed.
- Fixed an issue where clicking "Re-run" in the pull request Checks panel would open duplicate browser tabs instead of re-running the check.
- Fixed an issue where reopening a pull request with an already-provisioned workspace would stall the UI indefinitely on "Preparing project..."
- Fixed an issue where the GitHub re-authentication banner would appear repeatedly during transient GitHub API outages, even when the account token was still valid.
- Fixed deep-link callbacks on Linux opening a new instance instead of routing to the running one.
- Fixed Linux updates so deb and rpm installs show release-page guidance instead of failing to self-update, while AppImage installs can self-update again.
- Fixed markdown rendering: footnotes now appear as smaller muted text with a dividing line, task-list checkboxes stay vertically centered at all text sizes, and GitHub issue/PR reference links wrap correctly inside task lists.
- Fixed unreadable word-level diff highlights in the GitHub Light High Contrast theme, where changed words appeared as dark text on a dark background.
- Inbox search results now respect the requested sort order instead of always being sorted by most recently updated.
- Model provider icons in the model picker now correctly reflect the active light/dark theme tone, including on first paint.
- Pasting multiline text inside a blockquote now keeps all lines within the quote instead of only the first line escaping into unquoted text.
- Project pickers in the automation dialog and new-session view now label each entry by its unique project name, so multiple worktrees or folders of the same repository are distinguishable.
- Sessions are now correctly renamed by the agent when the first-prompt auto-generated name contained punctuation or mixed casing that differed from its stored form.
- Switching to a model that does not support reasoning effort (such as Auto or MAI Code 1 Flash) no longer causes session creation to fail when a reasoning effort was previously configured.
- Unsaved filter refinements in the My work inbox are now preserved when navigating away and back within the app.

## v0.2.29

### Changed

- Bare GitHub PR and issue URLs in markdown now render as compact references (owner/repo#123, or #123 for same-repo links); in list items, they also include a state-aware icon and title to match github.com rich reference behavior.
- Clicking a linked issue from the pull request body or the issue system-prompt card now opens the issue directly in the right panel instead of navigating to an external browser tab or displaying generic system prompt.

### Fixed

- Fixed automations failing to run after switching to a model that does not support reasoning.
- Fixed terminal failing to launch on Windows when PowerShell 7 was installed from the Microsoft Store.
- Fixed the timeline picker's collapsed hover area so it no longer accidentally intercepts mouse events on nearby controls in narrow viewports
- Restoring an archived session no longer fails when the session's local git branch has been deleted (e.g. after a pull request is merged and its branch auto-deleted).
- The "working" activity indicator (sidebar Working badge and the in-conversation loading row) now keeps animating when the OS has Reduce Motion enabled, instead of freezing into a static shape that looked stuck.

## v0.2.28

### Added

- Press Cmd+F (Ctrl+F on Windows/Linux) inside a conversation to search for text, with match-case and match-whole-word toggles, navigation between matches, and a configurable dialog corner in General settings.
- Quick chats now show token usage, context window, and AI credit spend in the chat title menu, matching the detail already available in regular sessions.
- When starting a session from an issue, a new "New session in repository..." option in the start menu lets you pick which of your project repositories the session opens in.

### Changed

- Comments in the pull request and merge drawers now render their content progressively as you scroll, reducing load time when opening pull requests with many comments.
- Issue pills above the composer now show the entity type in the label (for example 'Issue #1234'), matching the existing pattern used for pull request pills ('PR #6483').
- Pasting a GitHub URL (e.g. github.com/org/repo/pull/123) into the "Add GitHub repository" search now automatically extracts the repository and searches for it instead of treating the full URL as a query.
- Scheduled session automations now show a badge in the sidebar and display the next scheduled run time in the hover preview.
- The banner shown during an in-progress merge, rebase, cherry-pick, or revert now reads "Resolving …" instead of "… paused", more accurately reflecting that the operation is actively being handled by the agent.
- The conversation timeline is now always shown by default — no setting required. Timeline navigation and bookmarks are available whenever there is enough conversation history.
- The deep link URL for the Inbox view has changed from `ghapp://inbox` to `ghapp://mywork`.

### Fixed

- Collapsing a session in the sidebar now correctly hides all of its descendants, even when they belong to different repository groups.
- Fixed a soft-lock during onboarding where the "Sign in to GitHub" button never appeared for users with the system Reduce Motion accessibility setting enabled, or when the headline text was empty.
- Fixed blank terminal tab and scripts not executing when running commands on Windows with Command Prompt (cmd.exe) as the default shell.
- Fixed the Plan pill in the composer being taller and misaligned compared to other pills.
- Unlimited plans no longer show incorrect exhausted-quota indicators, and session AI-credit spend is now shown consistently in the usage gauge and workspace info popover.

## v0.2.27

### Fixed

- Fixed task-list checkboxes overflowing outside the card boundary in the pull request drawer, and enabled interactive checkbox toggling in that view.
- The "Read documentation" link on the home screen now opens the GitHub Copilot app-specific getting started guide instead of the generic Copilot documentation page.

## v0.2.26

### Added

- Added support for toggling task list checkboxes (`- [ ]` / `- [x]`) directly in the embedded pull request and issue descriptions. Changes are saved back to GitHub.
- F6 and Shift+F6 now cycle keyboard focus through major regions of the app, making it faster for keyboard and screen-reader users to navigate between the sidebar, conversation area, composer, and other landmarks.

### Changed

- Reduced worktree session startup time by roughly half, from ~6 seconds to ~3.5 seconds.
- The token usage section in the workspace branch popover now shows cached tokens and reasoning tokens in addition to input and output token counts.

### Fixed

- Conversation no longer replays a long catch-up scroll when returning to a session after display sleep, App Nap, or extended window occlusion.
- Fixed @mentions, EMU usernames, and commit SHA links not rendering correctly in pull request descriptions containing raw HTML (e.g. <details> blocks).
- Fixed an issue where delegated sessions using `notify_on_idle: "always"` would send a flood of repeated desktop notifications with no new content.
- Fixed an issue where deleting a worktree session could force-delete the local branch even when it contained local commits that were never pushed, causing data loss.
- Fixed an issue where the model picker would revert to the session's previous model when switching back to an existing session, discarding any model selection the user made.
- Fixed inline images in private-repository issues, pull requests, and comments failing to load with an HTTP 404 error once the page had been open for a few minutes. These images now refresh their short-lived signed URLs on demand.
- Fixed several keyboard navigation issues in the sidebar chat list: Tab now correctly exits the list instead of getting trapped, activating "Show more" moves focus to the first newly revealed item, and pressing Space no longer accidentally activates a chat row while typing a search.
- Fixed the end-of-response actions toolbar (copy, share, bookmark, fork) appearing on an assistant message while the response was still in progress. The toolbar now stays hidden across the whole in-flight response and only surfaces once the turn genuinely ends.
- Removed spurious "No comments yet." placeholder from the pull request conversation area and review draft panel when there are no comments.
- Settings dropdowns now immediately reflect the chosen archive and delete windows after accepting the auto-cleanup prompt, instead of showing "Disabled" until the next app restart.
- Show a loading spinner in the diff view when file changes are still loading, preventing a blank white area with no visual feedback.
- The branch sync indicator now correctly shows when a workspace branch is both diverged from its upstream and behind the PR base, instead of silently dropping the behind-base count and showing a misleading status.

## v0.2.25

### Fixed

- The app now restores your last viewed page after a reload (such as waking your Mac from sleep), instead of returning you to the home screen.

## v0.2.24

### Fixed

- In worktree sessions, the agent now correctly anchors file paths to the worktree's own checkout instead of the project's main checkout, preventing edits from silently landing on the wrong branch.

## v0.2.23

### Fixed

- Fixed automatic sync incorrectly resetting local branch checkouts, which could silently discard local commits or move the branch behind its expected position.
- Fixed canvas panels disappearing while a modal overlay (such as the command palette or settings dialog) was open; the canvas now stays visible beneath the overlay.

## v0.2.22

### Fixed

- Fixed slash commands (e.g. /chronicle) being incorrectly displayed as incoming cross-session messages instead of normal user messages.
- Fixed the app becoming slow and unresponsive when opening a pull request or workspace with a very large diff.

## v0.2.21

### Added

- Added a long context toggle in the model picker for models that support extended context windows, with the active tier shown in the model picker button.
- Added support for a `gh://session/new` deep link that opens the app and starts a new session for a given repository, pull request, or branch — with optional prompt and mode query parameters.
- Several experiments are now on for all users: canvases, MCP apps, the inbox tray menu, the channels view, cli sessions, browser-agent tools, the workspace uncommitted scope, the invertocat minigame, and editing files by selecting lines. Cloud workflows are also always on, and cloud sessions remain user-toggleable but default on for everyone. Voice dictation is now opt-in for everyone from Settings → Experimental.
- The agent can now read back the rendered output from a terminal after running a command, enabling it to see and act on command results in the terminal.

### Changed

- Copilot Pro, Pro+, and Max subscribers are now taken directly to the repository selection step after sign-in, bypassing the waitlist.
- The copy button next to PR and issue references is now always visible instead of only appearing on hover.
- The remove-project and delete-session dialogs now accurately explain that session worktrees are force-deleted, that uncommitted work is snapshotted to a recovery ref, and that recovering that work is a manual git step.

### Fixed

- Automation run timeline now displays older runs above newer runs, matching the order used in the session timeline picker.
- Command Palette now shows "Go to My work" (with the correct icon) instead of the outdated "Go to Inbox" label.
- External links clicked inside the browser preview now show a confirmation dialog offering to open the URL in your default browser, instead of being silently blocked.
- Fixed a bug where clicking "Update branch" after a local branch diverged from its upstream remote would send Copilot to merge or rebase the wrong target branch instead of the correct remote tracking branch.
- Fixed a spurious scrollbar appearing in the inline diff comment textarea on macOS when "Always show scrollbars" is enabled.
- Fixed app sluggishness (slow typing, slow session switching) when multiple concurrent sessions are streaming responses at the same time.
- Fixed images embedded in issue timelines failing to load due to an HTTP 400 error on signed attachment URLs.
- Fixed the !cmd shell shortcut when triggered from the home screen or an empty/new session — it now correctly bootstraps a workspace and opens a terminal tab in the session worktree directory instead of failing or running in the wrong location.
- Pasting a pull request URL into the quick-open palette (cmd-k) now opens the session that created that PR instead of offering to start a duplicate. Sessions are also now findable by the PR title or URL even when the session name differs.
- Quota usage percentages now display as whole numbers, consistent with the Copilot CLI.
- Removed the floating "No comments or activity yet." text that appeared visually in the pull request and issue detail view when there was no activity.
- Restored the hidden octocat minigame on the home screen, which had stopped appearing after a recent update.
- Restored the message composer during active automation runs, allowing users to respond to prompts and permission requests without first opening the session separately.
- Searching for "high contrast" in Settings now surfaces the Mode section where the High Contrast option lives.
- The model picker and session info popover now correctly show the context window size when long context is enabled.
- Uncommitted and untracked files are now preserved in a recoverable git ref before archiving or deleting a session, preventing silent data loss when removing worktrees.

## v0.2.20

### Added

- Added a long context toggle in the model picker for models that support extended context windows, with the active tier shown in the model picker button.
- Added support for a `gh://session/new` deep link that opens the app and starts a new session for a given repository, pull request, or branch — with optional prompt and mode query parameters.
- Several experiments are now on for all users: canvases, MCP apps, the inbox tray menu, the channels view, cli sessions, browser-agent tools, the workspace uncommitted scope, the invertocat minigame, and editing files by selecting lines. Cloud workflows are also always on, and cloud sessions remain user-toggleable but default on for everyone. Voice dictation is now opt-in for everyone from Settings → Experimental.
- The agent can now read back the rendered output from a terminal after running a command, enabling it to see and act on command results in the terminal.

### Changed

- Copilot Pro, Pro+, and Max subscribers are now taken directly to the repository selection step after sign-in, bypassing the waitlist.
- The copy button next to PR and issue references is now always visible instead of only appearing on hover.
- The remove-project and delete-session dialogs now accurately explain that session worktrees are force-deleted, that uncommitted work is snapshotted to a recovery ref, and that recovering that work is a manual git step.

### Fixed

- Automation run timeline now displays older runs above newer runs, matching the order used in the session timeline picker.
- Command Palette now shows "Go to My work" (with the correct icon) instead of the outdated "Go to Inbox" label.
- External links clicked inside the browser preview now show a confirmation dialog offering to open the URL in your default browser, instead of being silently blocked.
- Fixed a bug where clicking "Update branch" after a local branch diverged from its upstream remote would send Copilot to merge or rebase the wrong target branch instead of the correct remote tracking branch.
- Fixed a spurious scrollbar appearing in the inline diff comment textarea on macOS when "Always show scrollbars" is enabled.
- Fixed app sluggishness (slow typing, slow session switching) when multiple concurrent sessions are streaming responses at the same time.
- Fixed the !cmd shell shortcut when triggered from the home screen or an empty/new session — it now correctly bootstraps a workspace and opens a terminal tab in the session worktree directory instead of failing or running in the wrong location.
- Pasting a pull request URL into the quick-open palette (cmd-k) now opens the session that created that PR instead of offering to start a duplicate. Sessions are also now findable by the PR title or URL even when the session name differs.
- Quota usage percentages now display as whole numbers, consistent with the Copilot CLI.
- Removed the floating "No comments or activity yet." text that appeared visually in the pull request and issue detail view when there was no activity.
- Searching for "high contrast" in Settings now surfaces the Mode section where the High Contrast option lives.
- The model picker and session info popover now correctly show the context window size when long context is enabled.
- Uncommitted and untracked files are now preserved in a recoverable git ref before archiving or deleting a session, preventing silent data loss when removing worktrees.

## v0.2.19

### Fixed

- Extension permission dialogs no longer disappear when the agent finishes a turn, preventing the extension from becoming permanently blocked waiting for approval.
- Fixed an issue where the extension-permission dialog could appear on session start even when "auto-approve all tools" was enabled.
- Fixed the session hover card appearing in the wrong position (top-left corner) when hovering over a pinned workspace in the sidebar.

## v0.2.18

### Changed

- The files panel toolbar no longer shows redundant insertion/deletion counts when the active scope's stats match the Changes tab total (e.g. the "All changes" scope, or "Committed" with a clean working tree).

### Fixed

- Cross-session messages and workspace kickoffs now show the clean message text across all clients instead of the verbose internal wrapper, while the desktop still shows the sender attribution banner.
- Fixed an issue where leaving an active streaming session with the display asleep caused the entire session to replay character-by-character on wake, with heavy repainting and blocked session switching.
- Spell-check squiggles no longer appear in the freeform answer text box when responding to agent prompts.
- The README toggle in the new repository dialog now shows a visible label and description, making the option clearer for sighted users.
- When Git is not installed, the error shown during repository cloning now clearly states that Git is required and prompts you to install it, instead of showing a confusing system-level error message.

## v0.2.17

### Added

- Extensions can now be installed from a GitHub repository folder URL (e.g. `https://github.com/{owner}/{repo}/tree/{ref}/{path}`), in addition to gist URLs.
- The agent can now edit GitHub Actions workflow files (`.github/workflows/`) directly using its OAuth token, without requiring separate local Git credentials or the `gh` CLI.

### Changed

- Workflow tool calls (such as renaming sessions, running SQL queries, storing memory, and navigating) are now visible in the conversation timeline instead of being hidden, so you can see more of what the agent is doing.

### Fixed

- Clicking the plan.md filename link in a Create/Edit tool-call card now opens the Plan tab instead of doing nothing.
- Decision prompts (questions, plans, permission requests) no longer steal focus when they appear, preventing accidental option selection or dismissal while typing.
- Fixed a floating "Loading conversation…" label that was incorrectly visible while pull request comments were loading; the text is now hidden visually but still announced to screen readers.
- Model picker tooltip now correctly shows context window size and pricing details when connected to a cloud session.

## v0.2.16

### Added

- Sessions created by another session are now shown nested under their parent session in the sidebar.

### Changed

- Automation runs no longer flicker as placeholder sessions in the sidebar. Starting a run now immediately shows a 'Preparing automation' progress state. The 'Open session' button is promoted to a primary action in the run view. The Automations sidebar item now shows green/red counts of succeeded and failed runs instead of a single status dot.
- The pull request detail view in My Work now displays branch labels with an arrow instead of verbose merge text, and the split-pane view now shows the PR title, status badge, and labels in a compact inline row.

### Fixed

- "Always allow for this project" permission approvals now persist correctly across sessions when using git worktrees — the approval dialog no longer re-prompts on every new worktree-backed session.
- Fixed EGL_BAD_PARAMETER crashes on Wayland systems (Arch, Fedora 42) when launching the Linux AppImage
- Fixed the "Last commit" diff scope incorrectly showing an empty "No changes to compare" state and a nonsense branch label when the tip commit had changes.
- The context window size shown in the workspace header now displays the correct default tier value instead of the maximum long-context window. AI credit usage is also preserved when resuming a previous session.

## v0.2.15

### Changed

- Branch (in-place) workspace sessions now create pull requests in-place by default instead of redirecting the agent to spawn a parallel worktree session. Picking a branch workspace is treated as the signal that work belongs in the local clone, and repo-specific guidance in AGENTS.md / CLAUDE.md takes precedence over the app's general advice. The `create_pull_request` soft gate that previously refused on branch workspaces without `allow_in_place: true` has been removed.

### Fixed

- Reduced UI lag in the system tray menu during workspace switching and streaming

## v0.2.14

### Added

- Added a copy button to the markdown editor toolbar so you can copy the full document contents to your clipboard without manually selecting all the text.
- The app now prompts you to review and trust a repository's `.github/github-app.yml` configuration file before applying any of its customizations (scripts, system-prompt injections, or automation settings). The conversation input is blocked until you approve or dismiss, and you can review or revoke trust at any time from the project settings.
- The rubber-duck agent is now enabled by default for all users, providing constructive feedback on code and designs via the /rubber-duck slash command.

### Changed

- Exporting a reply as a secret gist no longer shows a success toast — the browser opens the gist automatically and the URL is copied to your clipboard.
- Improved the MCP Servers settings page with a unified Add server button, a searchable popular servers grid with text highlighting, and a better empty state with actionable guidance.
- Reordered settings for easier access — Scripts now appears higher in Project Settings, and Default model now appears higher in General Settings.
- The Status filter in the filter bar now supports multi-select, letting you view open and closed items at the same time.

### Fixed

- Expanded sidebar project groups with no sessions now show a 'No sessions yet' label instead of appearing blank.
- Fixed spurious "git-lfs is not installed" errors when creating worktree sessions for repositories that use Git LFS, even with git-lfs installed and working in your terminal.
- Fixed the keyboard shortcuts dialog so the "Current view" tab (previously "Contextual") only shows shortcuts specific to the active view, hides the tab selector entirely when no view-specific shortcuts exist, and scrolls to the top when switching tabs
- Loading spinners now rotate around their own center instead of an offset point.
- On macOS, the bash tool in agent sessions now correctly inherits your login shell's PATH, so tools installed via Homebrew, fnm, nvm, and similar managers no longer report "command not found".
- Slash commands (such as /chronicle) now show their short command text in the conversation timeline instead of the full verbose system prompt.
- The Changes toolbar no longer shows a branch sync button for folder workspaces that have no local git context.

## v0.2.13

### Added

- Added experimental Voice dictation that lets you capture speech locally and insert transcripts into the composer using a configurable shortcut, with support for push-to-talk or toggle mode, microphone device selection, and local transcription model management.

### Changed

- In workspace sessions, Cmd+T (Ctrl+T on Windows/Linux) now opens the add-tab palette for the right panel instead of creating a new chat session.
- Inline review threads the agent skipped (e.g. when several comments arrive at once and the agent collapses them into a single reply) now show an "Unanswered" badge instead of the alarming "Error" badge. The "Error" label is reserved for true failures where a reply was produced but didn't stick. The inline review prompt also now explicitly tells the agent that each thread in a batch needs its own reply_to_comment call.
- Skill invocations (e.g. /e2e-test-author, /design-foundations) now appear as a labeled card pill in the conversation instead of showing the raw prompt text.
- The branch sync indicator now shows 'Behind origin/<base> (N↓) · Update branch' when your branch is behind its PR base, making it easier to distinguish this case from being diverged from your own remote.
- The macOS Help menu now has working links to Documentation, What's New, Automations, MCP Servers, and Skills resources, and menu items have been reorganized and relabeled for clarity.
- Workspaces now silently auto-sync to their server branch when it's safe to do so. PR review workspaces fast-forward when the local tree is clean and there are no unpushed commits; author workspaces fast-forward or, when there are clean unpushed commits and `merge-tree` predicts no conflicts, auto-merge upstream into the local branch. Anything riskier (dirty tree, predicted conflicts) keeps today's manual "Sync" / "Resolve conflicts" affordance.

### Fixed

- Clicking a session or action in the system tray menu now reliably brings the app to the foreground on macOS.
- Filter queries using GitHub's comma-list shorthand (e.g. `repo:a/b,c/d`, `label:bug,docs`) now parse into separate filter pill values instead of a single literal value with embedded commas.
- Fixed crash when editing certain MCP servers in Settings and corrected server type badge display
- Help menu items (Keyboard Shortcuts, Share Feedback, Run Health Check, Show Home Tips Again, Credits, Manage Copilot Subscription) are now correctly disabled and grayed out during onboarding instead of appearing active but doing nothing when clicked.
- Pasting a full GitHub URL (e.g. an issue or PR link) into the Add GitHub Repository field now correctly resolves to the repository instead of returning no results.
- Pasting a GitHub repository URL into the quick-open dialog now correctly finds and shows the matching repository.
- Selecting multiple values in a filter pill (e.g. Author, Assignee) now correctly matches any of the selected values instead of silently returning no results.
- The session list now only includes sessions that were directly created by the CLI.

## v0.2.12

### Added

- Added a Comments filter pill to My work for filtering by total comment count. Pick an operator (greater than, at least, less than, at most, exactly, or between) and enter a number.
- Added a copy-to-clipboard button to the pasted text preview dialog, and made the text selectable so content can be copied via standard text selection.
- Added a hidden minigame to the home screen — find the secret platform to start an infinite jumping adventure with power-ups, hazards, and a persistent high score.
- Added a native system tray menu with live session status, PR checks and review info, badge notifications for sessions needing attention, quick actions to create sessions and chats, and a Settings toggle to show or hide the tray icon.
- Added a terminal font picker in Settings that lists your installed fonts, previews each in its own typeface, and applies your selection to the embedded terminal.
- Right-clicking a pull request or issue reference in a conversation now shows a context menu with a "Copy link" option to quickly copy the GitHub URL.

### Changed

- Error screens now show a plain text recovery UI instead of an illustration.
- Project color picker in the repository context menu now displays as a compact 4x2 grid of color tiles, making it faster to scan and select. Orange has been added as a new color option.

### Fixed

- Avatar fallback initials no longer overflow for multi-word names — they are now capped at two letters.
- Fixed a spurious "Error" badge appearing on inline review comment threads after the agent successfully replied to a review comment.
- PR and issue badges now correctly respect the 'Use a pointer cursor over buttons and links' accessibility setting instead of always showing a pointer cursor.

## v0.2.11

### Added

- Added a Conversation timeline toggle in Settings > General, letting you enable a timeline scrubber and bookmark controls for quickly navigating long conversations.
- Added Toolbox in Foundry to the popular MCP servers list in Settings, making it easy to connect a Microsoft Foundry-hosted toolbox endpoint without manual configuration.

### Changed

- Account usage in Settings now shows AI credits terminology, contextual Manage budget and Upgrade plan links, and updated overage copy for users on usage-based billing plans.
- The copy button next to the PR or issue number now copies the full GitHub URL instead of just the bare number.
- Users on usage-based billing plans now see AI credit quota labels, accurate quota error messages, and session AI-credit spend in the composer gauge and sidebar.

### Fixed

- Emoji reactions and the approve/request-changes badge are now shown on PR review summary comments in the pull request view.
- Fixed filter pills (Author, Assignees, etc.) appearing to return no results when typing — items were rendered but hidden behind an invisible block.
- Fixed scroll position drifting off the viewport in the pull request diff view when inline review threads grow taller (e.g., when a new reply is added to a review thread).
- Pasting a closed or merged pull request URL into the workspace creation dialog now correctly finds and shows the pull request.

## v0.2.10

### Changed

- Merging a pull request now updates the UI immediately with a pulsing "Finalizing merge…" indicator, rather than waiting for the full server round-trip to complete.
- Model picker now groups models by capability tier (Versatile, Powerful, Lightweight), shows recently used models, and adds an Unavailable section for policy-gated models. Anthropic model labels no longer include the redundant "Claude" prefix.

### Fixed

- Fixed the diff view jumping or shifting when the agent edits files while you are scrolling through changes.
- Slash-command menu on the home screen no longer appears behind the logo, making its options readable.

## v0.2.9

### Added

- Branch-mode scheduled workflows now bind to a dedicated branch workspace pinned at first run, with a workflow icon in the sidebar for workflow-owned workspaces. Project-less workflows run as general chat sessions, and the sidebar filter menu gains a "Hide workflow sessions" toggle.
- New /chronicle slash commands let you view session history, generate standup summaries, search past activity, and get workflow improvement tips directly from the chat input.
- Session automations (scheduled wake-ups and recurring prompts) are now supported in workspace sessions, in addition to general chat sessions.

### Changed

- Multiple workspace package scripts can now run at the same time. The Scripts menu shows running scripts first with per-script stop and log controls, and a Stop all option separates active scripts from idle ones.

### Fixed

- Clicking the find button in the markdown file toolbar now opens the find overlay and focuses the search input, matching the behavior of the Command-F keyboard shortcut.
- Fixed a bug where expanding a full file in the diff view after a prior partial expansion could leave some rows displaying stale line numbers and text from other lines.
- Fixed an issue where browser previews could become unresponsive after being hidden or minimized in the background.
- Fixed an issue where the agent could get stuck in a loop replying to the same inline review comment multiple times instead of moving on.
- Spellcheck is now disabled in comment fields and search inputs, removing false-positive red underlines on code, file paths, and identifiers.
- Syntax highlighting now works correctly for .mjs, .cjs, .mts, and .cts files in the file view.
- Terminal processes (dev servers, scripts) are now properly stopped when a workspace is deleted or archived, preventing orphaned background processes from continuing to run.
- The model selected in the draft composer is now consistently used when starting a new session, including from the command palette and other workspace creation paths.
- When automatic feedback submission fails, the feedback form now offers a prefilled GitHub issue URL as a fallback instead of timing out silently.

## v0.2.8

### Added

- Scheduled workflows now bind to a dedicated workspace (worktree by default). Successive runs reuse the same workspace, and the workflow creation/edit dialog includes a workspace type selector matching the regular session flow.
- Workspace files panel now offers a three-scope dropdown: "All" (working tree vs base), "Branch" (HEAD vs base), and "Uncommitted" (working tree vs HEAD). "All" is the new smart default for git-backed workspaces. Empty states for each scope offer a one-click switch when another scope has changes.

### Changed

- Improved keyboard and screen-reader accessibility on the onboarding theme step: focus now returns to the color-family filter button when its menu closes, and selecting themes via search or the "Feeling lucky" button announces results to screen readers.
- Renamed the "Branch" file scope option to "Committed" in the workspace Files panel dropdown, so it pairs clearly with "Uncommitted".
- The Settings "Add account" flow now uses the device-code authentication experience, matching the sign-in flow for both GitHub.com and GitHub Enterprise Server accounts.

### Fixed

- Browser tabs opened by the agent now correctly appear as shared in the UI.
- Chat sessions now show their title in the back/forward navigation history menu instead of raw URLs or duplicate "Chat" entries.
- Fixed a bug where the model picker displayed one model (e.g. Claude Opus 4.6) but sessions were started with a different model when no model had been explicitly selected or after using "Reset to recommended".
- Fixed a false "Session appears to have been interrupted" banner appearing on app restart for sessions that had ended cleanly.
- Fixed a keychain timeout error on macOS when interacting with the Keychain Allow/Always Allow prompt during sign-in. The timeout has been raised from 5s to 30s to accommodate user interaction with the dialog.
- Fixed a regression syncing the model picker between home and pending sessions.
- Fixed an infinite session recreation loop on startup that could silently replace conversation history with empty sessions when resuming sessions failed.
- Fixed an issue where session resume could fail due to a CLI ping response deserialization mismatch.
- Fixed an issue where the My Work filter preview would re-run aggressively while the autocomplete dropdown was open, causing the list to refilter underneath it.
- Fixed an issue where typing `- ` in the message editor would immediately convert to a list, preventing users from creating task-list items with `- [ ]`.
- Fixed branch label truncation in the workspace branch popover so both the session branch and parent branch shrink proportionally when space is limited, preventing the session branch from being crushed to a sliver.
- Fixed browser preview misalignment in the chat canvas area after the panel finishes animating open
- Fixed diff not refreshing after file edits in branch workspaces on the default branch.
- Fixed emoji shortcode picker not opening when typing a bare `:` in the live markdown editor
- Fixed GHE/Proxima user avatars expiring and falling back to initials by refreshing the stored avatar URL on every connection.
- Fixed incorrect inline review thread statuses where threads could be mislabeled as Error or Answered and status badges could disappear after a page reload.
- Fixed markdown canvas briefly showing a loading spinner when unrelated UI updates occurred (e.g., typing in the composer, browser tab edits).
- Fixed misalignment of the "3. Suggest changes" number in the exit plan prompt.
- Fixed Mona logo anchoring on the home screen when using the rich text composer.
- Fixed Session Rename not triggering reliably
- Fixed silent workspace creation failures on large repositories where git initialization could exceed the previous timeout, causing kickoff prompts to be dropped with no error feedback
- Fixed the canvas markdown editor flashing a loading spinner multiple times during chat session startup.
- Fixed the floating markdown toolbar link button sometimes appearing to do nothing when clicked
- Fixed the integrated browser preview remaining overlaid on the app UI after archiving a session that had it open.
- Git operations no longer override `core.sshCommand`, fixing broken SSH authentication for users with custom SSH setups such as SSH certificate wrappers, 1Password SSH agent, and similar tools.
- Improved keyboard and screen reader accessibility for toggle switches in Settings, including proper focus indicators and correct announcement behavior.
- Improved screen reader navigation across the app shell with proper landmarks and heading hierarchy: the sidebar, main content area, view headers, and key panels now expose semantic landmark elements with accessible names, and each view declares an <h1> so assistive technology users can orient themselves and jump between sections.
- Improved screen reader support on the onboarding theme, repositories, enterprise URL, and authorize steps: each step now exposes its title as a visually-hidden heading that receives focus on mount, so assistive technology announces the new step on navigation.
- On macOS, Ctrl+A in the rich composer now correctly moves the caret to the start of the line instead of selecting all text.
- Recent pull requests and issues now populate immediately when opening the "Create from…" dialog on a GitHub-backed repository, instead of appearing empty until a search query is typed.
- Screen readers now announce onboarding setup progress messages as they appear during the final setup step.
- The "Create From" dialog no longer surfaces archived sessions as existing workspaces, and selecting a branch always creates a new workspace instead of navigating to an existing one.
- The /agent-merge slash command now correctly enables the agent-merge loop, preventing work from stalling on wait states like pending CI or awaiting review.
- Traffic lights no longer dim when focus moves to the browser preview on macOS

## v0.2.7

### Added

- Added a "Pause all sessions" command palette action that suspends every running session at once, enabling clean restarts without triggering interrupted-session banners when resuming.
- Added keyboard shortcuts for adding comments on plan text, with support for rebinding via the command palette.
- Added OAuth Client ID field to the remote MCP server configuration form, and added Slack as a popular MCP server preset.
- Canvas markdown editor now shows a floating formatting toolbar when text is selected, making inline formatting actions available right where you're working.
- Emoji shortcode picker in the message composer: type `:` to search and insert GitHub emoji shortcodes (e.g. `:rocket:` → 🚀). Shortcodes are rendered as emoji while editing and preserved as `:shortcode:` in the exported markdown.
- Git is bundled with the app under a staff-only experiment, paving the way for users to no longer need git installed on their system.
- Health check view now shows a Database section with schema version, latest supported version, and database file path (with copy button)
- Rich Markdown editors now support table editing with row and column insertion, deletion, and column alignment controls.
- Sidebar workspace hover previews now show when a PR has auto-merge or agent merge enabled.

### Changed

- GitHub Enterprise Server onboarding now uses the device-code authentication flow, matching the GitHub.com experience.
- Improved markdown list editing in the rich composer: nested lists now render correctly, indent/outdent actions are available via toolbar buttons and Tab/Shift+Tab (or Cmd/Ctrl+[/]) when the cursor is in a list item, and raw markdown editing mode uses a monospace font.
- Plan review now shows a single unified toolbar when selecting text, combining the comment action and formatting options in one place.
- The artifact file picker now starts collapsed by default when opening a markdown editor from the chat canvas panel, keeping the editor focused on the new document.

### Fixed

- Anchor navigation in the integrated browser now works correctly without disrupting the current page view.
- Cross-session messages (send_session_message / send_chat_message) are now reliably delivered even when the target workspace session is not currently active, instead of silently failing while reporting success.
- File tree folders can now be manually collapsed even when they contain the currently selected file
- Fixed a Linux-only bug where temporary files created during PR comment replies would appear in the repository root and show up in diffs.
- Fixed an issue where clicking "New session" on a pull request or issue could create duplicate workspaces in the sidebar.
- Fixed an issue where creating a new session for a repository that was still cloning would silently create the session in a different, already-cloned repository instead.
- Fixed an issue where navigating away while a merge or review drawer was open would leave the backdrop stuck over the app.
- Fixed an issue where plan canvas comments would disappear the first time a user attached one during exit-plan review.
- Fixed an issue where the model could repeatedly call the session rename tool instead of continuing with the user's task.
- Fixed browser preview layout on Linux where the preview appeared as the bottom half of the window instead of in the right panel.
- Fixed the inline review reply loop and duplicate agent replies that could occur when multiple comments were posted on the same thread in quick succession.
- Improved canvas markdown editor performance during window resize.
- Improved error guidance when app update signature verification fails — users now see a clear message with a link to download and reinstall the latest release.
- Inline review comments from agent reviews no longer get permanently stuck showing an "Investigating" badge.
- PR review comments can now be added to deleted lines (shown in red) in the diff view, not just added or context lines.
- Restored undo/redo (Cmd+Z / Ctrl+Z) functionality in the composer, and fixed an issue where focus could be unexpectedly pulled back into the composer textarea.
- Screen readers now announce the Welcome page heading immediately when the onboarding step appears.
- Status updates during the app authorization flow (code copied, browser opened, waiting for authorization, timeout hint) are now announced to screen readers.

## v0.2.6

### Added

- Added a "Share as secret gist" button to the assistant message hover toolbar, allowing you to save a reply as a secret gist with one click. On success, the gist URL is copied to your clipboard and opened in the browser.
- Multi-select and bulk actions on the My work table — select multiple PRs or issues and act on them all at once via the command palette
- Repository clone deep links (`gh://clone/owner/repo` and `gh://github.com/owner/repo`) now open Quick Open prefilled with the repository URL, routing you into the existing clone/add repository flow.
- Visual Studio installations are now detected and available in the "Open in" IDE list on Windows.

### Changed

- In branch (in-place) workspaces, the agent now routes PR creation to a new worktree-backed session by default instead of opening a PR directly from the local clone. Users can still create a PR from the current session by explicitly asking (e.g. "open the PR from this branch").
- Moved the file folder picker button and tree to the left side of the file view, next to the file path.
- The agent-merge feature now re-checks CI and pull request status every 10 minutes by default, down from 30 minutes, so the agent responds more promptly after CI finishes.
- The command palette now animates smoothly on open, scaling and fading in instead of appearing abruptly.
- The folder tree is now the permanent file navigation experience for workspace files. The experimental settings toggle to disable it has been removed.
- Updated onboarding discovery cards to better clarify that sessions run in their own worktree and that pull requests are created manually when you're ready.

### Fixed

- Added `read:org` scope to OAuth token requests, fixing `gh pr edit` and other org-scoped operations hanging for ~3 minutes before timing out
- Arrow keys now move the cursor correctly when renaming a file inline, instead of being intercepted by tree navigation.
- Bold and italic toolbar formatting in the Markdown editor now visually appears in the editor surface as expected.
- Chart canvases now update live when the agent edits the backing artifact, instead of showing stale content.
- Clicking an artifact pill in group view now navigates to the correct session before opening the artifact.
- Comments and replies on diff lines no longer interrupt the agent mid-task — they are now queued and delivered after the current agent turn completes.
- File viewer (Cmd-P) now refreshes automatically when the underlying file is updated by a tool or other change, instead of showing stale content.
- Fixed a bug where the agent's reply-to-review-comment tool could send duplicate replies to the same review thread in a loop.
- Fixed an issue where editing a saved workflow prompt that starts with a slash command would immediately show the slash suggestions popup, obscuring the edit form.
- Fixed an issue where formatting in the markdown editor could trigger an unnecessary loading spinner during autosave
- Fixed an issue where the diff view would get stuck in an outdated state when a comment composer was opened but abandoned without entering any content
- Fixed broken images in pull request bodies and comments that appeared as broken placeholders in the app.
- Fixed file sort order in the changed-files sidebar to match github.com when directory names share a prefix.
- Fixed markdown editors in the right panel flickering back to a loading state when the agent modified files.
- Fixed Share Feedback from the macOS Help menu not working when the sidebar was collapsed.
- Fixed the agent `create_session` tool failing to create sessions in folder-backed projects. It now creates a folder workspace instead of attempting a git worktree against a non-git directory.
- Forking a pinned session now keeps the fork pinned in the sidebar automatically.
- Markdown images in the PR view now render at their intrinsic size and scale down proportionally when the panel is narrower than the image.
- Merge assistance now correctly handles stacked PRs whose base branch has been auto-retargeted by GitHub, avoiding stale base branch data during merges.
- Pasting a PR URL into Cmd-K for a repository not yet connected to the app now correctly opens that PR after the repository is cloned, instead of falling back to a generic draft session.
- PR check run rows now open the GitHub PR checks page for that run, instead of the provider's external details URL
- Queued messages panel no longer expands wider than the composer when messages contain long content
- Reduced flickering and blank states when switching between Repository and Artifacts in the file-tab folder picker.
- Reduced UI lag when switching between sessions with multiple sessions open
- Session references in markdown now correctly resolve and navigate to the referenced session, including when the session is known through workspace state.
- The file tree filter now stays visible while scrolling through long file lists, so you no longer need to scroll back to the top to filter the tree.
- Windows installers now clean up legacy installs, removing stale shortcuts and registry entries that could cause the old app to launch unexpectedly.
- Workflow prompts now support multi-line input using the Enter key.
- Workflow sessions are now correctly scoped to their project's account, preventing GitHub Enterprise repositories from inheriting the wrong host (github.com) when running project workflows.

## v0.2.5

### Added

- Workflow schedules now support quarter-hour start times (e.g. 12:15 AM), giving more flexibility when configuring daily and weekly automations.

### Changed

- Composer status pills are now hidden while prompt or widget takeover surfaces are active, keeping the focus on the current decision. Pending-decision row numbers also stay aligned when choices wrap to multiple lines.
- Improved accessibility across onboarding, including better keyboard navigation, focus rings, and screen reader support for theme selection, as well as clearer repository-selection semantics.

### Fixed

- App auto-update now retries failed authenticated requests anonymously, fixing update failures for users whose GitHub token is blocked by SAML/SSO enforcement.
- Fixed an issue where workflow creation could get stuck on clean installs due to the model picker showing a default model that wasn't recognized by the workflow dialog.
- Fixed focus ring rendering issues on home composer buttons — including clipping, z-order, WebKit ghost outlines, and pixel misalignments.
- Fixed sidebar navigation snapping back to the active chat when clicking Workflows or other sidebar items while the quick chat composer was focused.
- Fixed the composer send button visibly shifting position when switching between sessions.
- Follow-up messages submitted in the composer while a session is starting are now queued and shown immediately, instead of being blocked until the session is ready.
- In-place (non-worktree) sessions now stay on the current branch by default. The agent will no longer create new branches, switch branches, or commit without being explicitly asked to do so.
- Long branch names in the home screen branch picker no longer overflow their container.
- Nested lists in the markdown editor now render with correct indentation.
- Nested markdown lists now render with correct indentation.
- Restored bottom spacing and muted backdrop on the draft session composer so the project and branch pickers are visually grouped with the composer card.
- Restored live git clone progress updates (e.g. "Receiving objects: 42%") in the workspace cloning indicator
- Session creation no longer fails when a stale git lock file is present — the lock file is now automatically removed and the operation retried.
- The My Work inbox filter panel now remembers whether it was open when navigating away and back.

## v0.2.4

### Added

- Queued follow-up messages are now available by default during active sessions, allowing users to queue prompts while a response is in progress.
- Skills now appear as slash commands in the Quick chat composer, matching the behavior already available in Home and draft workspaces.

### Changed

- Consecutive tool calls are now grouped into a single collapsible panel with a natural-language summary (e.g. "Edited foo.ts and 3 other tool calls"), reducing visual noise in the conversation timeline. The panel shows a live spinner while tools are running, auto-opens during active work, and auto-closes when complete.
- PR number labels now display as "PR #123" instead of bare "#123" in the workspace PR tab and composer PR pill, avoiding potential confusion with issue references.

### Fixed

- Fixed blurry app icon on Windows at all DPI scales
- Fixed fullscreen toggle appearing on the wrong side in split panel layouts
- Restored spinner animation for in-progress todos in the Plan tab
- Fixed sidebar navigation snapping back to the active quick chat when clicking another section (e.g. Workflows) while the chat composer was focused
- Quick chats with unsent composer drafts are no longer discarded when navigating away from the chats view, so typed text isn't lost when switching to another sidebar section

## v0.2.3

### Added

- Right-click context menu (New session / View session, Quick chat, Copy link) is now available in the My Work inbox list view, matching the existing context menu in the table view.
- Session automations are now available as an opt-in experiment in Experimental settings, letting you repeat prompts on a schedule.
- Skills now appear in the slash command picker on the Home screen and in draft workspaces, so you can invoke `/skill-name` before starting a session.

### Changed

- Adding a GitHub repository now opens the command palette repo picker instead of the older dialog.
- The feedback form now shows a notice that submissions will be posted as public GitHub issues, and the submit button is labeled "Share feedback".
- The folder view is now available by default when viewing individual files, and the Changes panel no longer shows an "All files" scope.

### Fixed

- Bot account names (e.g. `github-actions[bot]`) are now displayed without the `[bot]` suffix in issue/PR rows, author cells, assignee avatars, search cards, and other UI surfaces.
- Draft sessions no longer show incorrect setup or worktree state before a prompt is submitted. A loading indicator is shown while a repo is cloning, and the project picker is now available in the draft composer footer.
- Feedback drafts are now preserved when accidentally dismissing the feedback popover (e.g. outside click, Escape, or sidebar collapse), so you no longer lose what you've typed.
- Fixed an issue where the find-in-file search window could render outside the app window when opened near the right edge of the screen.
- Fixed worktree creation timing out with "Timed out fetching the base branch" on large repositories by streaming fetch progress with an idle timeout instead of a fixed wall-clock limit.
- Recent sessions header now shows correctly in the sidebar when no sessions exist yet
- Skill files and MCP configs are now correctly rediscovered when resuming a session, fixing a bug where they were silently lost on resume.
- The Changes pill label in the composer now stays visible at medium session widths, making the diff entry point easier to find.

## v0.2.2

### Added

- Added a context menu to folder tree file rows with options to open the file in a new tab and copy its absolute path.
- Added a folder tree for navigating workspace files, with stable toolbar controls when switching files, search support for markdown files, and automatic reveal of the active file when the tree opens.
- Added column visibility controls to the My Work table view, letting you show or hide individual columns from a new Columns submenu. Reset options for column widths, order, and visibility are now grouped under a Reset submenu.
- Agents can now share and interact with the integrated browser preview — navigating pages, reading content, taking screenshots, and performing clicks and input — when the browser agent tools experiment is enabled.
- Canvas and browser tabs in the chat panel can now be split side by side
- The folder tree view for file navigation is now available as an opt-in experiment in Settings for all users.
- The slash command palette now shows argument autocomplete — enum-argument commands (like `/remote`, `/collect-debug-logs`, `/skills`) keep the palette open with allowed values after you type a space, while freeform-argument commands show a ghost-text hint describing what to type.

### Changed

- Added subtle vertical dividers between right panel tabs for easier visual distinction.
- Clicking an author or assignee avatar in the My Work inbox now opens that user's GitHub profile in your browser.
- Improved accessibility of the repository connection onboarding flow for screen reader and voice control users.
- Polished My work views and table interactions: the new view button now shows a 'New view' tooltip, the reset button is renamed from 'Clear' to 'Reset', deleting a custom view now shows a confirmation dialog with a 'Don't ask again' option, right-clicking an avatar in the inbox table now correctly opens the row context menu, and a separator was added above 'Copy link' in the row context menu.
- Queued follow-up prompts now use a consistent icon across both the submit button (when holding Cmd/Ctrl) and the queued-message pill.
- Redesigned the home screen as a discovery surface — surfaces inbox previews and contextual feature prompts to help you understand what to do next.
- Refined the My work inbox: restyled the filter editor as an inset card, added a split Save menu with "Save to this view" and "Save as new view" options, renamed "Reset to default" to "Clear", added right-click context menus on inbox tabs (Edit, Duplicate, Delete) and on table rows with a new "Quick chat" option to start a chat about the selected pull request or issue.
- Renamed the "View inbox" button to "View all" in the Up next section of the home screen.
- Revamped the default inbox sections: replaced "Needs my attention" with "Active" (issues and PRs assigned to you, plus PRs you authored) and "Review requests" (PRs where you or a team you're on is requested as a reviewer), and fixed the "Done" section so it no longer shows closed-unmerged pull requests.
- Reworked the My work filter editor with two distinct modes: a quick-filter mode (funnel toggle) for query-only edits with an inline Undo button and save/revert menu, and an edit mode for renaming a view and resetting it to its defaults.
- Right-panel tab close button now appears in the leading icon slot instead of as a right-side overlay, providing a more consistent interaction target.
- Sidebar badges and state pills for ready-to-merge and completed workspaces now use green success styling.
- Submitting a prompt on the home page without selecting a project now starts a quick chat instead of silently doing nothing.
- The "new updates" banner in the My work inbox is now displayed as a full-width strip flush against the filter bar, making it easier to spot when new items are available.
- The My Work inbox now remembers your last active tab and returns you to it on next load.

### Fixed

- Arrow keys now move the cursor correctly inside the new workspace search input instead of switching between source tabs.
- Browser preview pages no longer have unexpected DOM mutations (color-scheme attributes, injected style tags, or matchMedia overrides) applied by the app.
- Command palette "Set thinking effort" action now works correctly when no active session has started yet
- Discarding a draft session now shows a dedicated confirmation dialog with appropriate copy, instead of the generic delete dialog.
- Discovery cards on the home page are now automatically dismissed for items completed during onboarding, so already-configured features no longer appear as suggestions after setup.
- File attachment icons in chat messages now match the size used in attachment chips
- Fixed a crash that could occur when loading pull request checks for PRs with large check result pages
- Fixed a crash that could occur when loading pull request details with deeply nested check contexts.
- Fixed a crash that could occur when refreshing PR details with a large number of status checks.
- Fixed a gap between the sidebar and content area when using zoom levels above 1x.
- Fixed an error that could appear in the document navigator when opening files in ephemeral markdown canvases.
- Fixed an issue where adding an empty GitHub repository could cause the first feature branch pushed by a session to become the repo's default branch.
- Fixed an issue where attaching files to a chat could stop working after a draft session was converted into an active session.
- Fixed the add-tab menu alignment so it opens anchored to the trigger button edge instead of centering beneath it.
- Home screen discovery cards now correctly show actionable onboarding cards first, with tip cards as fallback, regardless of onboarding completion status.
- MCP tool calls now display with the correct server label and icon (e.g. "GitHub · Search code") instead of a raw slug like "Github Mcp Server · Search Code".
- Pull requests no longer appear as ready to merge when GitHub's merge requirements are not yet satisfied.
- Selecting a file in the Changes panel's All files tree now keeps the selected row highlighted while its content is displayed.
- Split controls now appear in a pane whenever any tab in that pane can be split, instead of being hidden when the active tab is pinned or otherwise unsplittable.

## v0.2.1

### Added

- Added `/skills reload` slash command in the composer palette to reload skills mid-session, with an inline transcript notice showing the updated skill count.
- Added a hover-to-reveal copy button to inbox item links
- Added an onboarding step for Business, Enterprise, and GHES users that detects when required Copilot preview features are not enabled and guides them to enable the necessary settings.
- Live progress is now shown while cloning a GitHub repository, with per-stage status (receiving objects, resolving deltas) and percentages streamed from git.
- Section editor qualifiers now support comma-separated multi-values (e.g. `repo:a,b,c`, `label:bug,docs`). Typing a comma after a value reopens the autocomplete with already-selected options filtered out.

### Changed

- My Work inbox filter tabs can now be reordered by dragging, and the "All" tab appears first by default.
- The "Archive sessions" button in the sidebar now shows the number of sessions that will be archived (e.g. "Archive 5 sessions" or "Archive 1 session").

### Fixed

- Browser preview theming now uses native OS appearance (macOS webview appearance, isolated Windows WebView2 profiles) instead of injecting scripts into the previewed page, preventing hydration mismatches in frameworks like Next.js. The theme toggle is hidden on Linux where native external theming is unsupported.
- Browser previews now retain their page state (URL, title, favicon) when switching panels or navigating away from a session.
- Fixed a bug where adding a new GitHub repository would briefly show the new workspace then redirect to the home page, hiding clone progress and any error dialogs.
- Fixed an issue on Windows where the app would become unresponsive to screen readers (NVDA) and voice control software after losing window focus.
- Fixed an issue on Windows where the browser preview could appear duplicated due to the native WebView2 surface being out of sync with the React placeholder.
- Fixed sidebar header controls overlapping main content at non-default zoom levels
- Fixed theme toggle not applying correctly in browser preview on Windows
- Fixed update error messages in Settings > General appearing as a second status line below the app version subtitle instead of replacing it
- Git error toasts for failed push, pull, and commit operations now show the actual git error message instead of the raw command arguments.
- Improved alignment and visual consistency across the Settings dialog: switch rows are now vertically centered; the account removal confirmation no longer shows a nested card or double border; MCP server action button spacing is consistent with the rest of the UI.
- Merge and auto-merge availability now correctly reflects GitHub's actual merge permissions, fixing cases where the merge button appeared disabled when it should have been enabled.

## v0.2.0

### Added

- Technical Preview for the GitHub app
