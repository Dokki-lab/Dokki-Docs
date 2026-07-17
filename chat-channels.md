---
title: "Chat Channels"
canonical: "https://dokki.one/pub/docs/chat-channels"
source_url: "https://dokki.one/pub/docs/chat-channels"
updated_at: "2026-07-12T15:12:29.651+00:00"
generated_by: Dokki
---

# Chat Channels

Chat Channels let you talk to your built-in Dokki Agent from a supported messaging app without opening Dokki first. The connection belongs to your Dokki account and uses the workspace you select when

Canonical source: [https://dokki.one/pub/docs/chat-channels](https://dokki.one/pub/docs/chat-channels)

Chat Channels let you talk to your built-in Dokki Agent from a supported messaging app without opening Dokki first. The connection belongs to your Dokki account and uses the workspace you select when you connect it.

Dokki currently supports **Weixin** private chat. More chat providers may appear here over time, but only providers shown in your Connections screen are available to use.

## Connect Weixin

1. Open **Connections** in Dokki.
1. Select the **Chat channels** tab.
1. Make sure the workspace shown in Dokki is the one you want the Agent to use.
1. Click **Connect Weixin**.
1. Scan the QR code with Weixin and confirm on your phone.
1. If Weixin shows a pairing code, enter it in Dokki and click **Confirm**.

When the connection succeeds, the Chat channels page shows the connected Weixin account. You can then open the corresponding private conversation in Weixin and send a message.

A QR code expires after a short time. If it expires or the confirmation times out, start the connection again to generate a new code.

## What you are chatting with

The Weixin conversation uses your built-in **Dokki Agent**. It does not select or create one of the custom agents shown on the Agents page.

The Agent:

- Acts as your Dokki user, not as another workspace member.
- Uses the workspace selected when the connection was created.
- Can use only the resources and tools your Dokki account is allowed to access.
- Uses the same **Dokki Agent conversation** in the App and across every private IM channel connected to this workspace.
- Cannot be invoked from Weixin groups or channels.

Messages from the App and connected private IM channels share one conversation history for your Dokki account in the selected workspace. When that conversation is open in Dokki, new IM messages and Agent replies appear automatically. Different workspaces keep separate conversations so permissions and resource context never cross workspace boundaries.

## Send messages

Send a normal private message in Weixin. It is added to the same Dokki Agent conversation shown in the App, Dokki queues the request, and the Agent's final text reply is returned to Weixin. Messages from other supported private IM channels connected to the same workspace use this conversation too.

Current message support:

- **Text**: supported.
- **Voice messages with Weixin transcription**: the transcription can be sent to the Agent as text.
- **Files**: Dokki can show the file name, but it does not currently download or analyze the file contents.
- **Images and video**: binary transfer and analysis are not currently supported.

Long-running requests may take longer than a normal chat reply because the Agent can search the selected workspace and use Dokki tools before responding. Sending the same upstream message again does not intentionally create a second Agent run.

## Usage and errors

The chat uses the same Dokki plan and usage limits as your account. If the current usage limit has been reached, the Agent returns a message explaining that it cannot process the request.

If a reply does not arrive:

- Check **Connections → Chat channels** for the connection status or a recent error.
- Confirm that your Dokki account still has access to the selected workspace.
- Wait briefly and try again if the service is recovering from a temporary connection problem.
- Disconnect and reconnect Weixin if the saved login is no longer valid.
- Contact your Dokki administrator if the channel repeatedly shows an error.

## Disconnect or reconnect

Open **Connections → Chat channels** and click **Disconnect** to stop the Weixin connection. New Weixin messages will no longer reach Dokki.

To use Weixin again, start a new QR connection. Reconnecting refreshes the channel credentials without discarding the existing Dokki Agent conversation for that workspace. Choosing a different workspace switches to that workspace's separate Dokki Agent conversation.

## Privacy and security

Dokki stores the minimum provider identifiers and delivery context needed to receive and return a private message. Provider credentials and reply tokens are encrypted or kept in server-only fields and are not exposed to other workspace members.

Chat Channels do not import unrelated Weixin conversations, group messages, or channel history. Only messages sent through the connected private Agent conversation enter the Dokki processing flow.

Chat Channels are different from **Connected Apps** and **MCP Connections**:

- Use **Chat Channels** when you want to talk to your Dokki Agent from a messaging app.
- Use **Connected Apps** when Copilot or an agent should act in another service such as GitHub, Slack, or Gmail.
- Use **MCP Connections** when an external AI client needs controlled access to Dokki.



---

Published from Dokki.
