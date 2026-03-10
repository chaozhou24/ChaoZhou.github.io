---
title: "Wechat Moments"
permalink: /Wechat.html
---

<div class="dc-page">
  <div class="dc-shell">

    <!-- Far-left server rail -->
    <aside class="dc-serverbar">
      <button class="server-btn active" type="button" aria-label="Main server">
        <span>CZ</span>
      </button>
      <button class="server-btn" type="button" aria-label="Research server">
        <span>R</span>
      </button>
      <button class="server-btn" type="button" aria-label="Life server">
        <span>L</span>
      </button>

      <div class="server-sep"></div>

      <button class="server-btn add-btn" type="button" aria-label="More">
        <span>+</span>
      </button>
    </aside>

    <!-- Channel sidebar -->
    <aside class="dc-sidebar">
      <div class="dc-brand">
        <div class="dc-brand-text">
          <strong>Chao Zhou Hub</strong>
          <span>Academic community space</span>
        </div>
      </div>

      <div class="dc-nav-title">TEXT CHANNELS</div>

      <div id="chat-list" class="dc-channel-list">
        <button class="dc-channel active" type="button" data-room="public" aria-current="true">
          <div class="dc-channel-main">
            <span class="hash">#</span>
            <div class="channel-meta">
              <strong>public-chat</strong>
              <small>Open discussion for everyone</small>
            </div>
          </div>
          <span class="channel-badge" id="badge-public">2</span>
        </button>

        <button class="dc-channel" type="button" data-room="research">
          <div class="dc-channel-main">
            <span class="hash">#</span>
            <div class="channel-meta">
              <strong>research-room</strong>
              <small>Papers, methods, experiments</small>
            </div>
          </div>
          <span class="channel-badge" id="badge-research">5</span>
        </button>

        <button class="dc-channel" type="button" data-room="life">
          <div class="dc-channel-main">
            <span class="hash">#</span>
            <div class="channel-meta">
              <strong>life-corner</strong>
              <small>Habits, balance, well-being</small>
            </div>
          </div>
          <span class="channel-badge" id="badge-life">1</span>
        </button>
      </div>

      <div class="dc-sidebar-footer">
        <div class="dc-profile-card">
          <div class="profile-avatar">CZ</div>
          <div class="profile-meta">
            <strong>Chao Zhou</strong>
            <span>Online</span>
          </div>
        </div>
        <button id="clear-current-chat" type="button">Clear Current Channel</button>
      </div>
    </aside>

    <!-- Main panel -->
    <section class="dc-main">
      <header class="dc-topbar">
        <div class="dc-topbar-left">
          <span class="topbar-hash">#</span>
          <div>
            <h2 id="room-title">public-chat</h2>
            <p id="room-desc">A place for open conversation, quick questions, and casual interaction.</p>
          </div>
        </div>

        <div class="dc-topbar-right">
          <div class="dc-status-pill">
            <span class="status-dot"></span>
            <span id="chat-status">Community active</span>
          </div>
        </div>
      </header>

      <div class="dc-room-intro">
        <div class="intro-icon">#</div>
        <div>
          <h3 id="intro-heading">Welcome to #public-chat</h3>
          <p id="intro-text">This is the beginning of the channel. Start a conversation, share ideas, or switch to a more focused room.</p>
        </div>
      </div>

      <div id="quick-chat" class="dc-chat" aria-live="polite"></div>

      <div id="typing-row" class="dc-typing" hidden>
        <span></span><span></span><span></span>
        <em id="typing-text">Someone is typing...</em>
      </div>

      <div class="dc-toolbar">
        <div class="dc-role-switch" role="group" aria-label="Switch sender role">
          <button id="role-visitor" class="dc-role-btn active" type="button" data-role="visitor">Visitor</button>
          <button id="role-author" class="dc-role-btn" type="button" data-role="author">Author</button>
        </div>

        <div class="dc-prompts" aria-label="Quick prompts">
          <button type="button" data-prompt="@Author I’d like to ask about choosing a research direction.">@Author question</button>
          <button type="button" data-prompt="I want to share a paper I recently found interesting:">Share a paper</button>
          <button type="button" data-prompt="How do you keep a healthy balance between research and daily life?">Work-life balance</button>
        </div>
      </div>

      <form id="chat-form" class="dc-input-wrap" autocomplete="off">
        <div class="dc-input-shell">
          <input
            id="chat-text"
            type="text"
            maxlength="280"
            placeholder="Message this channel"
            aria-label="Type a chat message"
          />
          <button type="submit">Send</button>
        </div>
      </form>

      <div class="dc-discussion">
        <div class="dc-discussion-title">Long-form Discussion</div>
        <p>Use the quick chat above for fast interaction. For deeper and persistent discussion, leave your thoughts below.</p>

        <script src="https://giscus.app/client.js"
                data-repo="chaozhou24/chaozhou24.github.io"
                data-repo-id="R_kgDORD_nug"
                data-category="General"
                data-category-id="DIC_kwDORD_nus4C4BcA"
                data-mapping="pathname"
                data-strict="0"
                data-reactions-enabled="1"
                data-emit-metadata="0"
                data-input-position="bottom"
                data-theme="dark"
                data-lang="en"
                crossorigin="anonymous"
                async>
        </script>
      </div>
    </section>
  </div>
</div>

<style>
  :root {
    --dc-bg: #1e1f22;
    --dc-serverbar: #111214;
    --dc-sidebar: #1e1f22;
    --dc-sidebar-2: #18191c;
    --dc-main: #313338;
    --dc-main-2: #2b2d31;
    --dc-card: #232428;
    --dc-border: rgba(255,255,255,0.06);
    --dc-text: #f2f3f5;
    --dc-text-soft: #b5bac1;
    --dc-text-faint: #8e9297;
    --dc-accent: #5865f2;
    --dc-accent-2: #4752c4;
    --dc-green: #23a559;
    --dc-bubble: #383a40;
    --dc-input: #1e1f22;
    --dc-author: #f0b232;
    --dc-visitor: #4ea1ff;
    --dc-shadow: 0 18px 40px rgba(0,0,0,0.35);
  }

  .dc-page {
    max-width: 1380px;
    margin: 24px auto;
    padding: 0 16px;
  }

  .dc-shell {
    display: grid;
    grid-template-columns: 76px 300px 1fr;
    min-height: 900px;
    border-radius: 22px;
    overflow: hidden;
    background: var(--dc-main);
    box-shadow: var(--dc-shadow);
    border: 1px solid rgba(255,255,255,0.05);
  }

  /* server bar */
  .dc-serverbar {
    background: var(--dc-serverbar);
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 12px;
    padding: 14px 0;
    border-right: 1px solid var(--dc-border);
  }

  .server-btn {
    width: 48px;
    height: 48px;
    border: 0;
    border-radius: 16px;
    background: #232428;
    color: var(--dc-text-soft);
    cursor: pointer;
    font-weight: 800;
    transition: all .18s ease;
    position: relative;
  }

  .server-btn span {
    display: grid;
    place-items: center;
    width: 100%;
    height: 100%;
  }

  .server-btn:hover {
    border-radius: 14px;
    background: var(--dc-accent);
    color: #fff;
    transform: translateY(-1px);
  }

  .server-btn.active {
    background: linear-gradient(135deg, var(--dc-accent), #7983ff);
    color: #fff;
    border-radius: 14px;
    box-shadow: 0 10px 20px rgba(88,101,242,0.28);
  }

  .server-btn.active::before {
    content: "";
    position: absolute;
    left: -12px;
    top: 50%;
    transform: translateY(-50%);
    width: 4px;
    height: 22px;
    border-radius: 999px;
    background: #fff;
  }

  .add-btn {
    color: #57f287;
    background: #1a2b20;
  }

  .add-btn:hover {
    background: #23a559;
    color: #fff;
  }

  .server-sep {
    width: 34px;
    height: 2px;
    border-radius: 999px;
    background: rgba(255,255,255,0.08);
    margin: 2px 0;
  }

  /* sidebar */
  .dc-sidebar {
    background:
      linear-gradient(180deg, rgba(255,255,255,0.02), rgba(255,255,255,0)),
      var(--dc-sidebar);
    display: flex;
    flex-direction: column;
    padding: 14px 12px;
    border-right: 1px solid var(--dc-border);
  }

  .dc-brand {
    padding: 10px 10px 14px;
    margin-bottom: 10px;
    border-bottom: 1px solid var(--dc-border);
  }

  .dc-brand-text strong {
    display: block;
    color: var(--dc-text);
    font-size: 15px;
    line-height: 1.2;
  }

  .dc-brand-text span {
    display: block;
    color: var(--dc-text-faint);
    font-size: 12px;
    margin-top: 4px;
  }

  .dc-nav-title {
    color: var(--dc-text-faint);
    font-size: 11px;
    font-weight: 800;
    letter-spacing: 0.08em;
    padding: 4px 10px 10px;
  }

  .dc-channel-list {
    display: flex;
    flex-direction: column;
    gap: 6px;
  }

  .dc-channel {
    border: 0;
    background: transparent;
    color: var(--dc-text-soft);
    border-radius: 10px;
    text-align: left;
    display: flex;
    justify-content: space-between;
    align-items: center;
    gap: 10px;
    padding: 10px 10px;
    cursor: pointer;
    transition: background .18s ease, color .18s ease, transform .18s ease;
  }

  .dc-channel:hover {
    background: rgba(255,255,255,0.06);
    color: var(--dc-text);
    transform: translateX(2px);
  }

  .dc-channel.active {
    background: rgba(255,255,255,0.09);
    color: var(--dc-text);
  }

  .dc-channel-main {
    display: flex;
    gap: 10px;
    align-items: flex-start;
    min-width: 0;
  }

  .hash {
    color: var(--dc-text-faint);
    font-weight: 800;
    font-size: 20px;
    line-height: 1;
    margin-top: 1px;
    flex: none;
  }

  .dc-channel.active .hash {
    color: #d9dcff;
  }

  .channel-meta {
    min-width: 0;
  }

  .channel-meta strong {
    display: block;
    font-size: 15px;
    font-weight: 700;
    line-height: 1.25;
    color: inherit;
  }

  .channel-meta small {
    display: block;
    color: var(--dc-text-faint);
    margin-top: 3px;
    line-height: 1.35;
  }

  .channel-badge {
    min-width: 20px;
    height: 20px;
    padding: 0 6px;
    border-radius: 999px;
    background: #ed4245;
    color: #fff;
    font-size: 11px;
    font-weight: 800;
    display: inline-flex;
    align-items: center;
    justify-content: center;
    flex: none;
    box-shadow: 0 6px 14px rgba(237, 66, 69, 0.25);
  }

  .dc-channel.active .channel-badge {
    background: var(--dc-accent);
    box-shadow: 0 6px 14px rgba(88,101,242,0.28);
  }

  .dc-sidebar-footer {
    margin-top: auto;
    padding-top: 16px;
    display: flex;
    flex-direction: column;
    gap: 10px;
  }

  .dc-profile-card {
    display: flex;
    align-items: center;
    gap: 10px;
    background: var(--dc-sidebar-2);
    border: 1px solid rgba(255,255,255,0.05);
    border-radius: 12px;
    padding: 10px;
  }

  .profile-avatar {
    width: 38px;
    height: 38px;
    border-radius: 50%;
    display: grid;
    place-items: center;
    background: linear-gradient(135deg, var(--dc-accent), #7c84ff);
    color: #fff;
    font-weight: 800;
    flex: none;
  }

  .profile-meta strong {
    display: block;
    color: var(--dc-text);
    font-size: 14px;
    line-height: 1.2;
  }

  .profile-meta span {
    display: block;
    color: #57f287;
    font-size: 12px;
    margin-top: 2px;
  }

  .dc-sidebar-footer button {
    width: 100%;
    border: 1px solid rgba(255,255,255,0.08);
    background: var(--dc-sidebar-2);
    color: var(--dc-text-soft);
    border-radius: 10px;
    padding: 11px 12px;
    cursor: pointer;
    font-weight: 700;
    transition: background .18s ease, color .18s ease, transform .18s ease;
  }

  .dc-sidebar-footer button:hover {
    background: #24262b;
    color: var(--dc-text);
    transform: translateY(-1px);
  }

  /* main */
  .dc-main {
    display: flex;
    flex-direction: column;
    background: var(--dc-main);
  }

  .dc-topbar {
    height: 72px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    gap: 12px;
    padding: 0 20px;
    background: rgba(49, 51, 56, 0.96);
    border-bottom: 1px solid var(--dc-border);
    box-shadow: 0 1px 0 rgba(255,255,255,0.02);
  }

  .dc-topbar-left {
    display: flex;
    align-items: center;
    gap: 12px;
    min-width: 0;
  }

  .topbar-hash {
    color: var(--dc-text-faint);
    font-size: 28px;
    font-weight: 800;
    flex: none;
  }

  .dc-topbar h2 {
    margin: 0;
    color: var(--dc-text);
    font-size: 20px;
    line-height: 1.2;
  }

  .dc-topbar p {
    margin: 3px 0 0;
    color: var(--dc-text-soft);
    font-size: 13px;
    line-height: 1.4;
  }

  .dc-status-pill {
    display: inline-flex;
    align-items: center;
    gap: 8px;
    padding: 8px 12px;
    border-radius: 999px;
    background: #232428;
    border: 1px solid var(--dc-border);
    color: var(--dc-text-soft);
    font-size: 13px;
    font-weight: 700;
    white-space: nowrap;
  }

  .status-dot {
    width: 9px;
    height: 9px;
    border-radius: 50%;
    background: var(--dc-green);
    box-shadow: 0 0 0 0 rgba(35, 165, 89, 0.6);
    animation: dcPulse 1.8s infinite;
  }

  @keyframes dcPulse {
    0% { box-shadow: 0 0 0 0 rgba(35, 165, 89, 0.6); }
    70% { box-shadow: 0 0 0 8px rgba(35, 165, 89, 0); }
    100% { box-shadow: 0 0 0 0 rgba(35, 165, 89, 0); }
  }

  .dc-room-intro {
    display: flex;
    gap: 16px;
    align-items: center;
    padding: 22px 22px 12px;
    border-bottom: 1px solid rgba(255,255,255,0.03);
  }

  .intro-icon {
    width: 56px;
    height: 56px;
    border-radius: 18px;
    display: grid;
    place-items: center;
    background: #232428;
    color: #c9cdfb;
    font-size: 28px;
    font-weight: 800;
    flex: none;
  }

  .dc-room-intro h3 {
    margin: 0;
    color: var(--dc-text);
    font-size: 24px;
    line-height: 1.2;
    letter-spacing: -0.02em;
  }

  .dc-room-intro p {
    margin: 6px 0 0;
    color: var(--dc-text-soft);
    font-size: 14px;
    line-height: 1.55;
    max-width: 760px;
  }

  .dc-chat {
    flex: 1;
    min-height: 320px;
    max-height: 500px;
    overflow-y: auto;
    padding: 12px 0 8px;
    background: linear-gradient(180deg, rgba(255,255,255,0.01), rgba(255,255,255,0));
  }

  .dc-chat::-webkit-scrollbar {
    width: 10px;
  }

  .dc-chat::-webkit-scrollbar-thumb {
    background: #1a1b1e;
    border-radius: 999px;
  }

  .date-separator {
    display: flex;
    align-items: center;
    gap: 12px;
    padding: 12px 22px 6px;
  }

  .date-separator::before,
  .date-separator::after {
    content: "";
    flex: 1;
    height: 1px;
    background: rgba(255,255,255,0.08);
  }

  .date-separator span {
    color: var(--dc-text-faint);
    font-size: 12px;
    font-weight: 700;
    letter-spacing: 0.02em;
    white-space: nowrap;
  }

  .msg-row {
    display: flex;
    gap: 14px;
    align-items: flex-start;
    padding: 10px 22px;
    transition: background .16s ease;
  }

  .msg-row:hover {
    background: rgba(255,255,255,0.025);
  }

  .msg-row.outgoing {
    flex-direction: row-reverse;
  }

  .msg-avatar {
    width: 42px;
    height: 42px;
    border-radius: 50%;
    display: grid;
    place-items: center;
    font-weight: 800;
    font-size: 13px;
    color: white;
    flex: none;
    box-shadow: 0 8px 18px rgba(0,0,0,0.24);
  }

  .msg-row.author .msg-avatar {
    background: linear-gradient(135deg, var(--dc-author), #f7c75d);
    color: #3a2400;
  }

  .msg-row.visitor .msg-avatar {
    background: linear-gradient(135deg, var(--dc-visitor), #79bcff);
    color: #082542;
  }

  .msg-body {
    max-width: min(78%, 760px);
    min-width: 0;
  }

  .msg-row.outgoing .msg-body {
    text-align: right;
  }

  .msg-meta {
    display: flex;
    align-items: baseline;
    gap: 8px;
    margin-bottom: 4px;
  }

  .msg-row.outgoing .msg-meta {
    justify-content: flex-end;
  }

  .msg-name {
    color: var(--dc-text);
    font-weight: 800;
    font-size: 15px;
  }

  .msg-time {
    color: var(--dc-text-faint);
    font-size: 12px;
  }

  .bubble {
    display: inline-block;
    max-width: 100%;
    background: var(--dc-bubble);
    color: var(--dc-text);
    border-radius: 16px;
    padding: 11px 14px;
    line-height: 1.65;
    border: 1px solid rgba(255,255,255,0.03);
    box-shadow: 0 8px 18px rgba(0,0,0,0.12);
    word-break: break-word;
    transform: translateY(6px);
    opacity: 0;
    animation: msgIn .18s ease forwards;
  }

  .msg-row.outgoing .bubble {
    background: linear-gradient(180deg, var(--dc-accent), var(--dc-accent-2));
    color: #fff;
  }

  @keyframes msgIn {
    to {
      transform: translateY(0);
      opacity: 1;
    }
  }

  .dc-typing {
    display: inline-flex;
    align-items: center;
    gap: 5px;
    margin: 2px 22px 12px;
    color: var(--dc-text-faint);
    font-size: 13px;
  }

  .dc-typing span {
    width: 6px;
    height: 6px;
    border-radius: 50%;
    background: #9ca3af;
    animation: blink 1.1s infinite ease-in-out;
  }

  .dc-typing span:nth-child(2) { animation-delay: .15s; }
  .dc-typing span:nth-child(3) { animation-delay: .3s; }

  @keyframes blink {
    0%, 80%, 100% { opacity: .25; transform: translateY(0); }
    40% { opacity: 1; transform: translateY(-2px); }
  }

  .dc-toolbar {
    display: flex;
    justify-content: space-between;
    gap: 12px;
    align-items: center;
    padding: 14px 18px 10px;
    border-top: 1px solid rgba(255,255,255,0.04);
  }

  .dc-role-switch {
    display: inline-flex;
    background: #232428;
    border: 1px solid var(--dc-border);
    border-radius: 999px;
    padding: 4px;
    gap: 4px;
  }

  .dc-role-btn {
    border: 0;
    border-radius: 999px;
    padding: 7px 12px;
    background: transparent;
    color: var(--dc-text-soft);
    cursor: pointer;
    font-size: 13px;
    font-weight: 700;
    transition: background .18s ease, color .18s ease, transform .18s ease;
  }

  .dc-role-btn.active {
    background: var(--dc-accent);
    color: #fff;
  }

  .dc-role-btn:hover {
    transform: translateY(-1px);
  }

  .dc-prompts {
    display: flex;
    gap: 8px;
    flex-wrap: wrap;
  }

  .dc-prompts button {
    border: 1px solid rgba(255,255,255,0.06);
    background: #232428;
    color: var(--dc-text-soft);
    border-radius: 999px;
    font-size: 13px;
    font-weight: 600;
    padding: 7px 12px;
    cursor: pointer;
    transition: background .16s ease, color .16s ease, transform .16s ease;
  }

  .dc-prompts button:hover {
    background: #2b2d31;
    color: var(--dc-text);
    transform: translateY(-1px);
  }

  .dc-input-wrap {
    padding: 0 18px 18px;
  }

  .dc-input-shell {
    display: flex;
    gap: 10px;
    align-items: center;
    background: var(--dc-input);
    border: 1px solid rgba(255,255,255,0.06);
    border-radius: 16px;
    padding: 10px;
  }

  .dc-input-shell input {
    flex: 1;
    border: 0;
    outline: none;
    background: transparent;
    color: var(--dc-text);
    font-size: 15px;
    padding: 8px 10px;
  }

  .dc-input-shell input::placeholder {
    color: var(--dc-text-faint);
  }

  .dc-input-shell button {
    border: 0;
    border-radius: 12px;
    padding: 10px 16px;
    background: linear-gradient(180deg, var(--dc-accent), var(--dc-accent-2));
    color: #fff;
    font-weight: 800;
    cursor: pointer;
    transition: transform .16s ease, box-shadow .16s ease;
    box-shadow: 0 10px 20px rgba(88,101,242,0.24);
  }

  .dc-input-shell button:hover {
    transform: translateY(-1px);
    box-shadow: 0 14px 24px rgba(88,101,242,0.28);
  }

  .dc-discussion {
    background: #2b2d31;
    border-top: 1px solid rgba(255,255,255,0.05);
    padding: 18px 20px 26px;
  }

  .dc-discussion-title {
    color: var(--dc-text);
    font-size: 16px;
    font-weight: 800;
    margin-bottom: 6px;
  }

  .dc-discussion p {
    margin: 0 0 14px;
    color: var(--dc-text-soft);
    font-size: 14px;
    line-height: 1.6;
  }

  @media (max-width: 1180px) {
    .dc-shell {
      grid-template-columns: 76px 1fr;
    }

    .dc-sidebar {
      display: none;
    }
  }

  @media (max-width: 1024px) {
    .dc-topbar {
      height: auto;
      padding: 16px 18px;
      flex-direction: column;
      align-items: flex-start;
    }

    .dc-toolbar {
      flex-direction: column;
      align-items: flex-start;
    }

    .dc-chat {
      max-height: 420px;
    }
  }

  @media (max-width: 680px) {
    .dc-page {
      margin: 14px auto;
      padding: 0 8px;
    }

    .dc-shell {
      grid-template-columns: 1fr;
      border-radius: 16px;
      min-height: auto;
    }

    .dc-serverbar {
      flex-direction: row;
      justify-content: center;
      padding: 10px;
      gap: 10px;
      border-right: 0;
      border-bottom: 1px solid var(--dc-border);
    }

    .server-btn.active::before {
      display: none;
    }

    .server-sep {
      width: 2px;
      height: 26px;
    }

    .dc-room-intro {
      padding: 18px 16px 10px;
    }

    .dc-room-intro h3 {
      font-size: 20px;
    }

    .msg-row {
      padding: 10px 16px;
    }

    .msg-body {
      max-width: 86%;
    }

    .dc-input-wrap {
      padding: 0 12px 14px;
    }

    .dc-discussion {
      padding: 16px 14px 22px;
    }
  }
</style>

<script>
  (function () {
    const rooms = {
      public: {
        title: 'public-chat',
        desc: 'A place for open conversation, quick questions, and casual interaction.',
        introHeading: 'Welcome to #public-chat',
        introText: 'This is the beginning of the channel. Start a conversation, share ideas, or switch to a more focused room.',
        welcome: 'Welcome to the public channel. Everyone is free to join, ask, and share.',
        badge: 2
      },
      research: {
        title: 'research-room',
        desc: 'Focused discussion on papers, methods, experiments, and reproducibility.',
        introHeading: 'Welcome to #research-room',
        introText: 'Use this channel to discuss research ideas, technical methods, paper feedback, and experiment design.',
        welcome: 'Welcome to the research room. Sharing your problem setting and what you have tried usually leads to better discussion.',
        badge: 5
      },
      life: {
        title: 'life-corner',
        desc: 'A relaxed space for productivity, habits, health, and daily balance.',
        introHeading: 'Welcome to #life-corner',
        introText: 'This channel is for routines, motivation, exercise, balance, and everyday thoughts beyond research.',
        welcome: 'Welcome to the life corner. Slow down a bit and talk about daily life too.',
        badge: 1
      }
    };

    const storageKey = 'discord-style-room-history-v2';
    const quickChat = document.getElementById('quick-chat');
    const chatList = document.getElementById('chat-list');
    const form = document.getElementById('chat-form');
    const input = document.getElementById('chat-text');
    const typingRow = document.getElementById('typing-row');
    const typingText = document.getElementById('typing-text');
    const clearBtn = document.getElementById('clear-current-chat');
    const roomTitle = document.getElementById('room-title');
    const roomDesc = document.getElementById('room-desc');
    const introHeading = document.getElementById('intro-heading');
    const introText = document.getElementById('intro-text');
    const statusText = document.getElementById('chat-status');
    const roleButtons = Array.from(document.querySelectorAll('.dc-role-btn'));
    const promptButtons = Array.from(document.querySelectorAll('.dc-prompts button'));
    const badges = {
      public: document.getElementById('badge-public'),
      research: document.getElementById('badge-research'),
      life: document.getElementById('badge-life')
    };

    if (!quickChat || !chatList || !form || !input) return;

    let currentRoom = 'public';
    let currentRole = 'visitor';
    let history = loadHistory();

    function nowText() {
      const now = new Date();
      return now.toLocaleTimeString('en-US', {
        hour: '2-digit',
        minute: '2-digit',
        hour12: false
      });
    }

    function todayLabel() {
      const now = new Date();
      return now.toLocaleDateString('en-US', {
        weekday: 'long',
        month: 'short',
        day: 'numeric'
      });
    }

    function loadHistory() {
      try {
        const raw = localStorage.getItem(storageKey);
        const parsed = raw ? JSON.parse(raw) : {};
        return {
          public: Array.isArray(parsed.public) ? parsed.public : [],
          research: Array.isArray(parsed.research) ? parsed.research : [],
          life: Array.isArray(parsed.life) ? parsed.life : []
        };
      } catch (e) {
        return { public: [], research: [], life: [] };
      }
    }

    function saveHistory() {
      try {
        localStorage.setItem(storageKey, JSON.stringify(history));
      } catch (e) {
        // ignore storage errors
      }
    }

    function createDateSeparator(text) {
      const row = document.createElement('div');
      row.className = 'date-separator';

      const label = document.createElement('span');
      label.textContent = text;

      row.appendChild(label);
      return row;
    }

    function createMsg(msg) {
      const row = document.createElement('div');
      row.className = `msg-row ${msg.direction} ${msg.role}`;

      const avatar = document.createElement('span');
      avatar.className = 'msg-avatar';
      avatar.textContent = msg.role === 'author' ? 'AU' : 'VS';

      const body = document.createElement('div');
      body.className = 'msg-body';

      const meta = document.createElement('div');
      meta.className = 'msg-meta';

      const name = document.createElement('span');
      name.className = 'msg-name';
      name.textContent = msg.sender;

      const time = document.createElement('span');
      time.className = 'msg-time';
      time.textContent = msg.time;

      const bubble = document.createElement('div');
      bubble.className = 'bubble';
      bubble.textContent = msg.text;

      meta.appendChild(name);
      meta.appendChild(time);
      body.appendChild(meta);
      body.appendChild(bubble);

      row.appendChild(avatar);
      row.appendChild(body);

      return row;
    }

    function appendMessage(msg, shouldSave) {
      if (!quickChat.querySelector('.date-separator')) {
        quickChat.appendChild(createDateSeparator(`Today · ${todayLabel()}`));
      }

      quickChat.appendChild(createMsg(msg));
      quickChat.scrollTop = quickChat.scrollHeight;

      if (shouldSave) {
        history[currentRoom].push(msg);
        history[currentRoom] = history[currentRoom].slice(-120);
        saveHistory();
        updateBadges(currentRoom, 0);
      }
    }

    function renderRoom() {
      const meta = rooms[currentRoom];
      roomTitle.textContent = meta.title;
      roomDesc.textContent = meta.desc;
      introHeading.textContent = meta.introHeading;
      introText.textContent = meta.introText;
      statusText.textContent = `${Object.keys(rooms).length} channels available`;
      quickChat.innerHTML = '';
      quickChat.appendChild(createDateSeparator(`Today · ${todayLabel()}`));

      if (!history[currentRoom].length) {
        quickChat.appendChild(createMsg({
          text: meta.welcome,
          direction: 'incoming',
          role: 'author',
          sender: 'Author',
          time: nowText()
        }));
      } else {
        history[currentRoom].forEach(function (msg) {
          quickChat.appendChild(createMsg(msg));
        });
      }

      quickChat.scrollTop = quickChat.scrollHeight;
      updateBadges(currentRoom, 0);
    }

    function switchRoom(roomId) {
      if (!rooms[roomId]) return;
      currentRoom = roomId;

      Array.from(chatList.querySelectorAll('.dc-channel')).forEach(function (btn) {
        const isActive = btn.getAttribute('data-room') === roomId;
        btn.classList.toggle('active', isActive);
        btn.setAttribute('aria-current', isActive ? 'true' : 'false');
      });

      renderRoom();
    }

    function switchRole(role) {
      currentRole = role;
      roleButtons.forEach(function (btn) {
        const active = btn.getAttribute('data-role') === role;
        btn.classList.toggle('active', active);
      });
    }

    function updateBadges(activeRoom, resetValue) {
      Object.keys(badges).forEach(function (key) {
        if (!badges[key]) return;

        if (key === activeRoom) {
          badges[key].textContent = resetValue;
          badges[key].style.visibility = resetValue > 0 ? 'visible' : 'hidden';
        } else {
          const count = rooms[key].badge;
          badges[key].textContent = count;
          badges[key].style.visibility = count > 0 ? 'visible' : 'hidden';
        }
      });
    }

    chatList.addEventListener('click', function (e) {
      const target = e.target.closest('.dc-channel');
      if (!target) return;
      switchRoom(target.getAttribute('data-room'));
    });

    roleButtons.forEach(function (btn) {
      btn.addEventListener('click', function () {
        switchRole(btn.getAttribute('data-role'));
      });
    });

    promptButtons.forEach(function (btn) {
      btn.addEventListener('click', function () {
        input.value = btn.getAttribute('data-prompt') || '';
        input.focus();
      });
    });

    input.addEventListener('input', function () {
      const typing = input.value.trim().length > 0;
      typingRow.hidden = !typing;
      typingText.textContent = currentRole === 'author' ? 'Author is typing...' : 'Visitor is typing...';
    });

    form.addEventListener('submit', function (e) {
      e.preventDefault();
      const value = input.value.trim();
      if (!value) return;

      const isAuthor = currentRole === 'author';

      appendMessage({
        text: value,
        direction: isAuthor ? 'incoming' : 'outgoing',
        role: currentRole,
        sender: isAuthor ? 'Author' : 'Visitor',
        time: nowText()
      }, true);

      input.value = '';
      typingRow.hidden = true;
    });

    if (clearBtn) {
      clearBtn.addEventListener('click', function () {
        history[currentRoom] = [];
        saveHistory();
        renderRoom();
      });
    }

    updateBadges(currentRoom, 0);
    renderRoom();
  })();
</script>
