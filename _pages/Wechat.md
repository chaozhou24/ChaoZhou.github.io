---
title: "Wechat Moments"
permalink: /Wechat.html
---

<div class="dc-page">
  <div class="dc-shell">

    <!-- Server rail -->
    <aside class="dc-serverbar">
      <button class="server-btn active" type="button" aria-label="Main server" data-room="public">
        <span>CZ</span>
      </button>
      <button class="server-btn" type="button" aria-label="Research server" data-room="research">
        <span>R</span>
      </button>
      <button class="server-btn" type="button" aria-label="Life server" data-room="life">
        <span>L</span>
      </button>

      <div class="server-sep"></div>

      <button class="server-btn add-btn" type="button" aria-label="More">
        <span>+</span>
      </button>
    </aside>

    <!-- Sidebar -->
    <aside class="dc-sidebar">
      <div class="dc-brand">
        <div class="dc-brand-text">
          <strong>Chao Zhou Hub</strong>
          <span>Academic community space</span>
        </div>
      </div>

      <div class="dc-search-wrap">
        <label class="visually-hidden" for="channel-search">Search channels</label>
        <input id="channel-search" type="text" placeholder="Search channels" />
      </div>

      <div class="channel-section">
        <button class="section-toggle" type="button" data-section="community" aria-expanded="true">
          <span class="section-caret">▾</span>
          <span>COMMUNITY</span>
        </button>
        <div class="section-body" data-section-body="community">
          <div class="dc-channel-list">
            <button class="dc-channel active" type="button" data-room="public" aria-current="true">
              <div class="dc-channel-main">
                <span class="hash hash-mark">#</span>
                <div class="channel-meta">
                  <strong>public-feed</strong>
                  <small>Open posts and public interaction</small>
                </div>
              </div>
              <span class="channel-badge" id="badge-public" style="visibility:hidden;"></span>
            </button>
          </div>
        </div>
      </div>

      <div class="channel-section">
        <button class="section-toggle" type="button" data-section="academic" aria-expanded="true">
          <span class="section-caret">▾</span>
          <span>ACADEMIC</span>
        </button>
        <div class="section-body" data-section-body="academic">
          <div class="dc-channel-list">
            <button class="dc-channel" type="button" data-room="research">
              <div class="dc-channel-main">
                <span class="hash hash-mark">#</span>
                <div class="channel-meta">
                  <strong>research-board</strong>
                  <small>Papers, methods, experiments</small>
                </div>
              </div>
              <span class="channel-badge" id="badge-research" style="visibility:hidden;"></span>
            </button>
          </div>
        </div>
      </div>

      <div class="channel-section">
        <button class="section-toggle" type="button" data-section="social" aria-expanded="true">
          <span class="section-caret">▾</span>
          <span>SOCIAL</span>
        </button>
        <div class="section-body" data-section-body="social">
          <div class="dc-channel-list">
            <button class="dc-channel" type="button" data-room="life">
              <div class="dc-channel-main">
                <span class="hash hash-mark">#</span>
                <div class="channel-meta">
                  <strong>life-board</strong>
                  <small>Habits, balance, daily thoughts</small>
                </div>
              </div>
              <span class="channel-badge" id="badge-life" style="visibility:hidden;"></span>
            </button>
          </div>
        </div>
      </div>

      <div class="dc-sidebar-footer">
        <div class="dc-profile-card">
          <div class="profile-avatar">CZ</div>
          <div class="profile-meta">
            <strong>Chao Zhou</strong>
            <span>Online</span>
          </div>
        </div>
        <button id="clear-current-room" type="button">Clear Current Channel</button>
      </div>
    </aside>

    <!-- Main -->
    <section class="dc-main">
      <header class="dc-topbar">
        <div class="dc-topbar-left">
          <span class="topbar-hash hash-mark">#</span>
          <div>
            <h2 id="room-title">public-feed</h2>
            <p id="room-desc">A board for public posts, thoughts, questions, and open interaction.</p>
          </div>
        </div>

        <div class="dc-topbar-right">
          <button id="theme-toggle" class="top-icon-btn active" type="button" aria-label="Toggle theme" title="Toggle theme">
            <span id="theme-icon">🌙</span>
          </button>
          <div class="dc-status-pill">
            <span class="status-dot"></span>
            <span id="chat-status">3 channels · 0 posts</span>
          </div>
        </div>
      </header>

      <div class="dc-feed-panel">
        <div class="dc-room-intro">
          <div class="intro-icon hash-mark">#</div>
          <div>
            <h3 id="intro-heading">Welcome to #public-feed</h3>
            <p id="intro-text">Share a post, start a discussion, and leave comments under a specific topic. This area feels more like a community board than a chat room.</p>
          </div>
        </div>

        <section class="forum-composer-card">
          <div class="forum-composer-top">
            <div class="dc-role-switch" role="group" aria-label="Switch poster role">
              <button id="role-visitor" class="dc-role-btn active" type="button" data-role="visitor">Visitor</button>
              <button id="role-author" class="dc-role-btn" type="button" data-role="author">Author</button>
            </div>

            <div class="forum-compose-hint">
              Posting in <strong id="compose-room-label">public-feed</strong>
            </div>
          </div>

          <div class="forum-compose-grid">
            <input id="post-title" type="text" maxlength="90" placeholder="Post title (optional but recommended)" />
            <textarea id="post-text" maxlength="1200" placeholder="Write something thoughtful... share a question, an update, an idea, or a reflection."></textarea>
          </div>

          <div class="forum-composer-bottom">
            <div class="dc-prompts" aria-label="Quick prompts">
              <button type="button" data-fill-title="Looking for advice on research direction" data-fill-text="I am currently exploring several possible research topics. I would love to hear how others narrow down a good direction and judge whether a topic is worth pursuing long term.">Research direction</button>
              <button type="button" data-fill-title="A paper worth discussing" data-fill-text="I recently read a paper that I found interesting. I want to share the core idea, what I think is useful, and a few questions that might be worth discussing together.">Share a paper</button>
              <button type="button" data-fill-title="How do you balance work and life?" data-fill-text="I am curious how people maintain consistent research productivity while also keeping healthy routines, exercise, and enough rest.">Work-life balance</button>
            </div>

            <div class="forum-compose-actions">
              <span id="composer-count" class="composer-count">0 / 1200</span>
              <button id="submit-post" class="publish-btn" type="button">Publish Post</button>
            </div>
          </div>
        </section>

        <section class="forum-feed-wrap">
          <div class="forum-feed-head">
            <div>
              <h3>Community Feed</h3>
              <p id="feed-summary">Posts are displayed in a clean thread style. Click “Comment” to discuss a specific post.</p>
            </div>
          </div>

          <div id="forum-feed" class="forum-feed" aria-live="polite"></div>
        </section>

        <div class="dc-discussion">
          <div class="dc-discussion-title">Archive Discussion</div>
          <p>This section still supports long-form public discussion through GitHub Discussions. The post feed above is the visual forum layer; the section below can remain as a persistent archive.</p>

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
      </div>
    </section>
  </div>
</div>

<style>
  :root {
    --dc-shadow: 0 18px 40px rgba(0, 0, 0, 0.35);
    --dc-radius-lg: 22px;
    --dc-radius-md: 16px;
    --dc-radius-sm: 10px;
    --dc-transition: .18s ease;
  }

  body.theme-dark,
  :root {
    --dc-serverbar: #111214;
    --dc-sidebar: #1e1f22;
    --dc-sidebar-2: #18191c;
    --dc-main: #313338;
    --dc-main-2: #2b2d31;
    --dc-card: #232428;
    --dc-card-soft: #383a40;
    --dc-card-hover: rgba(255,255,255,0.06);
    --dc-border: rgba(255,255,255,0.06);
    --dc-border-strong: rgba(255,255,255,0.10);
    --dc-text: #f2f3f5;
    --dc-text-soft: #b5bac1;
    --dc-text-faint: #8e9297;
    --dc-accent: #5865f2;
    --dc-accent-2: #4752c4;
    --dc-green: #23a559;
    --dc-author: #f0b232;
    --dc-visitor: #4ea1ff;
    --dc-red: #ed4245;
    --dc-input: #1e1f22;
    --dc-reply-bg: #2c2f36;
    --dc-hover-toolbar: #1b1d21;
    --dc-post-shadow: 0 14px 30px rgba(0,0,0,0.16);
  }

  body.theme-light {
    --dc-serverbar: #edf1f7;
    --dc-sidebar: #f8fbff;
    --dc-sidebar-2: #f0f4fa;
    --dc-main: #ffffff;
    --dc-main-2: #f7f9fd;
    --dc-card: #ffffff;
    --dc-card-soft: #eef3fb;
    --dc-card-hover: rgba(15,23,42,0.04);
    --dc-border: rgba(15,23,42,0.08);
    --dc-border-strong: rgba(15,23,42,0.12);
    --dc-text: #172033;
    --dc-text-soft: #526077;
    --dc-text-faint: #7e8aa0;
    --dc-accent: #4f61ff;
    --dc-accent-2: #4250d6;
    --dc-green: #16a34a;
    --dc-author: #eab308;
    --dc-visitor: #3b82f6;
    --dc-red: #ef4444;
    --dc-input: #f5f8fd;
    --dc-reply-bg: #eef3fb;
    --dc-hover-toolbar: #ffffff;
    --dc-post-shadow: 0 12px 28px rgba(15,23,42,0.08);
  }

  .visually-hidden {
    position: absolute;
    width: 1px;
    height: 1px;
    overflow: hidden;
    clip: rect(0 0 0 0);
    white-space: nowrap;
  }

  .dc-page {
    max-width: 1560px;
    margin: 24px auto;
    padding: 0 16px;
  }

  .dc-shell {
    display: grid;
    grid-template-columns: 72px 270px minmax(0, 1fr);
    min-height: 940px;
    border-radius: var(--dc-radius-lg);
    overflow: hidden;
    background: var(--dc-main);
    box-shadow: var(--dc-shadow);
    border: 1px solid var(--dc-border);
  }

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
    background: var(--dc-card);
    color: var(--dc-text-soft);
    cursor: pointer;
    font-weight: 800;
    transition: all var(--dc-transition);
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
    background: currentColor;
    color: #fff;
  }

  .add-btn {
    color: #57f287;
    background: rgba(35,165,89,0.12);
  }

  .add-btn:hover {
    background: #23a559;
    color: #fff;
  }

  .server-sep {
    width: 34px;
    height: 2px;
    border-radius: 999px;
    background: var(--dc-border-strong);
    margin: 2px 0;
  }

  .dc-sidebar {
    background: var(--dc-sidebar);
    display: flex;
    flex-direction: column;
    padding: 14px 12px;
    border-right: 1px solid var(--dc-border);
  }

  .dc-brand {
    padding: 10px 10px 14px;
    margin-bottom: 8px;
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

  .dc-search-wrap {
    padding: 0 8px 12px;
  }

  .dc-search-wrap input {
    width: 100%;
    box-sizing: border-box;
    border: 1px solid var(--dc-border);
    background: var(--dc-card);
    color: var(--dc-text);
    border-radius: 12px;
    padding: 10px 12px;
    outline: none;
    font-size: 14px;
    transition: border-color var(--dc-transition), box-shadow var(--dc-transition);
  }

  .dc-search-wrap input::placeholder {
    color: var(--dc-text-faint);
  }

  .dc-search-wrap input:focus {
    border-color: rgba(88,101,242,0.6);
    box-shadow: 0 0 0 3px rgba(88,101,242,0.18);
  }

  .channel-section {
    margin-bottom: 8px;
  }

  .section-toggle {
    width: 100%;
    border: 0;
    background: transparent;
    color: var(--dc-text-faint);
    padding: 8px 10px;
    display: flex;
    align-items: center;
    gap: 8px;
    font-size: 11px;
    font-weight: 800;
    letter-spacing: 0.08em;
    cursor: pointer;
    text-align: left;
    border-radius: 8px;
    transition: background var(--dc-transition), color var(--dc-transition);
  }

  .section-toggle:hover {
    background: var(--dc-card-hover);
    color: var(--dc-text-soft);
  }

  .section-caret {
    display: inline-block;
    transition: transform var(--dc-transition);
    font-size: 12px;
  }

  .section-toggle[aria-expanded="false"] .section-caret {
    transform: rotate(-90deg);
  }

  .section-body[hidden] {
    display: none;
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
    border-radius: 12px;
    text-align: left;
    display: flex;
    justify-content: space-between;
    align-items: center;
    gap: 10px;
    padding: 10px 10px;
    cursor: pointer;
    transition: background var(--dc-transition), color var(--dc-transition), transform var(--dc-transition);
  }

  .dc-channel:hover {
    background: var(--dc-card-hover);
    color: var(--dc-text);
    transform: translateX(2px);
  }

  .dc-channel.active {
    background: var(--dc-card-hover);
    color: var(--dc-text);
    box-shadow: inset 0 0 0 1px var(--dc-border);
  }

  .dc-channel.hidden-by-search {
    display: none;
  }

  .dc-channel-main {
    display: flex;
    gap: 10px;
    align-items: flex-start;
    min-width: 0;
  }

  .hash-mark {
    font-family: "Arial Black", "Segoe UI Black", "Helvetica Neue", Arial, sans-serif;
    font-weight: 900 !important;
    letter-spacing: -0.03em;
    text-shadow: 0 0 0.01px currentColor, 0 0 0.01px currentColor;
    -webkit-font-smoothing: antialiased;
    text-rendering: geometricPrecision;
  }

  .hash {
    color: var(--dc-text-faint);
    font-size: 22px;
    line-height: 1;
    margin-top: -1px;
    flex: none;
    display: inline-block;
  }

  .dc-channel.active .hash {
    color: var(--dc-accent);
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
    background: var(--dc-red);
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
    border: 1px solid var(--dc-border);
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
    border: 1px solid var(--dc-border);
    background: var(--dc-sidebar-2);
    color: var(--dc-text-soft);
    border-radius: 10px;
    padding: 11px 12px;
    cursor: pointer;
    font-weight: 700;
    transition: background var(--dc-transition), color var(--dc-transition), transform var(--dc-transition);
  }

  .dc-sidebar-footer button:hover {
    background: var(--dc-card-hover);
    color: var(--dc-text);
    transform: translateY(-1px);
  }

  .dc-main {
    display: flex;
    flex-direction: column;
    background: var(--dc-main);
    min-width: 0;
  }

  .dc-topbar {
    min-height: 72px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    gap: 12px;
    padding: 0 22px;
    background: var(--dc-main);
    border-bottom: 1px solid var(--dc-border);
  }

  .dc-topbar-left {
    display: flex;
    align-items: center;
    gap: 12px;
    min-width: 0;
  }

  .topbar-hash {
    color: var(--dc-text-faint);
    font-size: 30px;
    line-height: 1;
    flex: none;
    display: inline-block;
    margin-top: -1px;
  }

  .dc-topbar h2 {
    margin: 0;
    color: var(--dc-text);
    font-size: 19px;
    line-height: 1.15;
  }

  .dc-topbar p {
    margin: 3px 0 0;
    color: var(--dc-text-soft);
    font-size: 13px;
    line-height: 1.4;
    max-width: 640px;
  }

  .dc-topbar-right {
    display: flex;
    align-items: center;
    gap: 10px;
    flex: none;
  }

  .top-icon-btn {
    width: 40px;
    height: 40px;
    border: 1px solid var(--dc-border);
    border-radius: 12px;
    background: var(--dc-card);
    color: var(--dc-text-soft);
    cursor: pointer;
    transition: all var(--dc-transition);
    font-size: 16px;
  }

  .top-icon-btn:hover,
  .top-icon-btn.active {
    background: var(--dc-accent);
    color: #fff;
  }

  .dc-status-pill {
    display: inline-flex;
    align-items: center;
    gap: 8px;
    padding: 8px 14px;
    border-radius: 999px;
    background: var(--dc-card);
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

  .dc-feed-panel {
    display: flex;
    flex-direction: column;
    min-width: 0;
  }

  .dc-room-intro {
    display: grid;
    grid-template-columns: 70px minmax(0, 1fr);
    gap: 18px;
    align-items: center;
    padding: 26px 34px 18px;
    border-bottom: 1px solid var(--dc-border);
  }

  .intro-icon {
    width: 62px;
    height: 62px;
    border-radius: 18px;
    display: grid;
    place-items: center;
    background: var(--dc-card);
    color: var(--dc-accent);
    font-size: 36px;
    flex: none;
    box-shadow: inset 0 1px 0 rgba(255,255,255,0.03);
  }

  .dc-room-intro h3 {
    margin: 0;
    color: var(--dc-text);
    font-size: 26px;
    line-height: 1.16;
    letter-spacing: -0.02em;
  }

  .dc-room-intro p {
    margin: 8px 0 0;
    color: var(--dc-text-soft);
    font-size: 15px;
    line-height: 1.65;
    max-width: 860px;
  }

  .forum-composer-card {
    margin: 24px 28px 18px;
    padding: 20px;
    border: 1px solid var(--dc-border);
    border-radius: 22px;
    background: linear-gradient(180deg, var(--dc-main-2), var(--dc-card));
    box-shadow: var(--dc-post-shadow);
  }

  .forum-composer-top {
    display: flex;
    justify-content: space-between;
    align-items: center;
    gap: 14px;
    flex-wrap: wrap;
    margin-bottom: 16px;
  }

  .forum-compose-hint {
    color: var(--dc-text-soft);
    font-size: 14px;
    font-weight: 600;
  }

  .forum-compose-hint strong {
    color: var(--dc-accent);
  }

  .dc-role-switch {
    display: inline-flex;
    background: var(--dc-card);
    border: 1px solid var(--dc-border);
    border-radius: 999px;
    padding: 4px;
    gap: 4px;
  }

  .dc-role-btn {
    border: 0;
    border-radius: 999px;
    padding: 8px 14px;
    background: transparent;
    color: var(--dc-text-soft);
    cursor: pointer;
    font-size: 13px;
    font-weight: 700;
    transition: background var(--dc-transition), color var(--dc-transition), transform var(--dc-transition);
  }

  .dc-role-btn.active {
    background: var(--dc-accent);
    color: #fff;
  }

  .dc-role-btn:hover {
    transform: translateY(-1px);
  }

  .forum-compose-grid {
    display: grid;
    gap: 12px;
  }

  .forum-compose-grid input,
  .forum-compose-grid textarea {
    width: 100%;
    box-sizing: border-box;
    border: 1px solid var(--dc-border);
    background: var(--dc-input);
    color: var(--dc-text);
    border-radius: 16px;
    outline: none;
    transition: border-color var(--dc-transition), box-shadow var(--dc-transition), transform var(--dc-transition);
  }

  .forum-compose-grid input {
    padding: 14px 16px;
    font-size: 15px;
    font-weight: 700;
  }

  .forum-compose-grid textarea {
    min-height: 140px;
    resize: vertical;
    padding: 16px;
    font-size: 15px;
    line-height: 1.7;
    font-family: inherit;
  }

  .forum-compose-grid input::placeholder,
  .forum-compose-grid textarea::placeholder {
    color: var(--dc-text-faint);
  }

  .forum-compose-grid input:focus,
  .forum-compose-grid textarea:focus {
    border-color: rgba(88,101,242,0.6);
    box-shadow: 0 0 0 3px rgba(88,101,242,0.16);
  }

  .forum-composer-bottom {
    margin-top: 14px;
    display: flex;
    justify-content: space-between;
    gap: 14px;
    align-items: flex-end;
    flex-wrap: wrap;
  }

  .dc-prompts {
    display: flex;
    gap: 8px;
    flex-wrap: wrap;
  }

  .dc-prompts button {
    border: 1px solid var(--dc-border);
    background: var(--dc-card);
    color: var(--dc-text-soft);
    border-radius: 999px;
    font-size: 13px;
    font-weight: 600;
    padding: 8px 12px;
    cursor: pointer;
    transition: background var(--dc-transition), color var(--dc-transition), transform var(--dc-transition);
  }

  .dc-prompts button:hover {
    background: var(--dc-card-hover);
    color: var(--dc-text);
    transform: translateY(-1px);
  }

  .forum-compose-actions {
    display: flex;
    align-items: center;
    gap: 12px;
  }

  .composer-count {
    color: var(--dc-text-faint);
    font-size: 12px;
    font-weight: 700;
  }

  .publish-btn {
    border: 0;
    border-radius: 14px;
    padding: 12px 18px;
    background: linear-gradient(180deg, var(--dc-accent), var(--dc-accent-2));
    color: #fff;
    font-weight: 800;
    cursor: pointer;
    transition: transform var(--dc-transition), box-shadow var(--dc-transition);
    box-shadow: 0 10px 20px rgba(88,101,242,0.24);
  }

  .publish-btn:hover {
    transform: translateY(-1px);
    box-shadow: 0 14px 24px rgba(88,101,242,0.28);
  }

  .forum-feed-wrap {
    padding: 2px 28px 28px;
  }

  .forum-feed-head {
    padding: 8px 0 16px;
    border-bottom: 1px solid var(--dc-border);
    margin-bottom: 18px;
  }

  .forum-feed-head h3 {
    margin: 0;
    color: var(--dc-text);
    font-size: 19px;
  }

  .forum-feed-head p {
    margin: 6px 0 0;
    color: var(--dc-text-soft);
    font-size: 14px;
    line-height: 1.6;
  }

  .forum-feed {
    display: flex;
    flex-direction: column;
    gap: 18px;
  }

  .forum-empty {
    padding: 34px 24px;
    border: 1px dashed var(--dc-border-strong);
    border-radius: 20px;
    background: var(--dc-main-2);
    color: var(--dc-text-soft);
    text-align: center;
  }

  .forum-post {
    position: relative;
    background: var(--dc-card);
    border: 1px solid var(--dc-border);
    border-radius: 22px;
    padding: 20px 20px 16px;
    box-shadow: var(--dc-post-shadow);
    transition: transform var(--dc-transition), border-color var(--dc-transition), box-shadow var(--dc-transition);
  }

  .forum-post:hover {
    transform: translateY(-2px);
    border-color: var(--dc-border-strong);
  }

  .forum-post-head {
    display: flex;
    justify-content: space-between;
    gap: 16px;
    align-items: flex-start;
    margin-bottom: 14px;
  }

  .forum-post-author {
    display: flex;
    align-items: center;
    gap: 12px;
    min-width: 0;
  }

  .post-avatar {
    width: 48px;
    height: 48px;
    border-radius: 16px;
    display: grid;
    place-items: center;
    font-size: 13px;
    font-weight: 800;
    flex: none;
    box-shadow: 0 10px 20px rgba(0,0,0,0.16);
  }

  .post-avatar.author {
    background: linear-gradient(135deg, var(--dc-author), #f7c75d);
    color: #3a2400;
  }

  .post-avatar.visitor {
    background: linear-gradient(135deg, var(--dc-visitor), #79bcff);
    color: #082542;
  }

  .post-author-meta {
    min-width: 0;
  }

  .post-author-meta strong {
    display: block;
    color: var(--dc-text);
    font-size: 15px;
    line-height: 1.2;
  }

  .post-submeta {
    display: flex;
    gap: 8px;
    flex-wrap: wrap;
    align-items: center;
    margin-top: 4px;
  }

  .post-time {
    color: var(--dc-text-faint);
    font-size: 12px;
    font-weight: 600;
  }

  .post-role-tag {
    border-radius: 999px;
    padding: 4px 8px;
    font-size: 11px;
    font-weight: 800;
    letter-spacing: 0.03em;
  }

  .post-role-tag.author {
    background: rgba(240, 178, 50, 0.14);
    color: var(--dc-author);
  }

  .post-role-tag.visitor {
    background: rgba(78, 161, 255, 0.14);
    color: var(--dc-visitor);
  }

  .post-actions-top {
    display: inline-flex;
    align-items: center;
    gap: 8px;
    flex-wrap: wrap;
    justify-content: flex-end;
  }

  .room-chip {
    padding: 6px 10px;
    border-radius: 999px;
    background: var(--dc-main-2);
    border: 1px solid var(--dc-border);
    color: var(--dc-text-soft);
    font-size: 12px;
    font-weight: 700;
  }

  .post-title {
    margin: 0 0 12px;
    color: var(--dc-text);
    font-size: 22px;
    line-height: 1.25;
    letter-spacing: -0.02em;
  }

  .post-content {
    color: var(--dc-text-soft);
    font-size: 15px;
    line-height: 1.85;
    white-space: pre-wrap;
    word-break: break-word;
  }

  .post-footer {
    margin-top: 18px;
    display: flex;
    justify-content: space-between;
    gap: 12px;
    flex-wrap: wrap;
    align-items: center;
    padding-top: 14px;
    border-top: 1px solid var(--dc-border);
  }

  .post-stat {
    color: var(--dc-text-faint);
    font-size: 13px;
    font-weight: 700;
  }

  .post-action-row {
    display: flex;
    gap: 10px;
    flex-wrap: wrap;
  }

  .post-btn {
    border: 1px solid var(--dc-border);
    background: var(--dc-main-2);
    color: var(--dc-text-soft);
    border-radius: 12px;
    padding: 9px 13px;
    font-size: 13px;
    font-weight: 700;
    cursor: pointer;
    transition: background var(--dc-transition), color var(--dc-transition), transform var(--dc-transition);
  }

  .post-btn:hover {
    background: var(--dc-card-hover);
    color: var(--dc-text);
    transform: translateY(-1px);
  }

  .post-btn.primary {
    background: rgba(88,101,242,0.12);
    color: var(--dc-accent);
    border-color: rgba(88,101,242,0.2);
  }

  .post-btn.primary:hover {
    background: var(--dc-accent);
    color: #fff;
  }

  .comment-area {
    margin-top: 16px;
    border-top: 1px solid var(--dc-border);
    padding-top: 16px;
  }

  .comment-list {
    display: flex;
    flex-direction: column;
    gap: 12px;
    margin-bottom: 14px;
  }

  .comment-item {
    display: flex;
    gap: 10px;
    align-items: flex-start;
    background: var(--dc-main-2);
    border: 1px solid var(--dc-border);
    border-radius: 16px;
    padding: 12px;
  }

  .comment-avatar {
    width: 34px;
    height: 34px;
    border-radius: 12px;
    display: grid;
    place-items: center;
    font-size: 11px;
    font-weight: 800;
    flex: none;
  }

  .comment-avatar.author {
    background: linear-gradient(135deg, var(--dc-author), #f7c75d);
    color: #3a2400;
  }

  .comment-avatar.visitor {
    background: linear-gradient(135deg, var(--dc-visitor), #79bcff);
    color: #082542;
  }

  .comment-body {
    min-width: 0;
    flex: 1;
  }

  .comment-meta {
    display: flex;
    gap: 8px;
    flex-wrap: wrap;
    align-items: center;
    margin-bottom: 4px;
  }

  .comment-meta strong {
    color: var(--dc-text);
    font-size: 13px;
  }

  .comment-meta span {
    color: var(--dc-text-faint);
    font-size: 12px;
  }

  .comment-text {
    color: var(--dc-text-soft);
    font-size: 14px;
    line-height: 1.7;
    white-space: pre-wrap;
    word-break: break-word;
  }

  .comment-form {
    display: grid;
    gap: 10px;
  }

  .comment-form textarea {
    width: 100%;
    box-sizing: border-box;
    min-height: 88px;
    resize: vertical;
    border: 1px solid var(--dc-border);
    background: var(--dc-input);
    color: var(--dc-text);
    border-radius: 14px;
    padding: 12px 14px;
    outline: none;
    font-size: 14px;
    line-height: 1.7;
    font-family: inherit;
  }

  .comment-form textarea::placeholder {
    color: var(--dc-text-faint);
  }

  .comment-form textarea:focus {
    border-color: rgba(88,101,242,0.6);
    box-shadow: 0 0 0 3px rgba(88,101,242,0.14);
  }

  .comment-form-row {
    display: flex;
    justify-content: space-between;
    gap: 12px;
    align-items: center;
    flex-wrap: wrap;
  }

  .comment-note {
    color: var(--dc-text-faint);
    font-size: 12px;
    font-weight: 600;
  }

  .comment-submit {
    border: 0;
    border-radius: 12px;
    padding: 10px 14px;
    background: linear-gradient(180deg, var(--dc-accent), var(--dc-accent-2));
    color: #fff;
    font-weight: 800;
    cursor: pointer;
    transition: transform var(--dc-transition), box-shadow var(--dc-transition);
    box-shadow: 0 10px 20px rgba(88,101,242,0.20);
  }

  .comment-submit:hover {
    transform: translateY(-1px);
  }

  .dc-discussion {
    background: var(--dc-main-2);
    border-top: 1px solid var(--dc-border);
    padding: 22px 28px 30px;
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
      grid-template-columns: 72px 1fr;
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

    .forum-composer-card,
    .forum-feed-wrap,
    .dc-discussion {
      padding-left: 18px;
      padding-right: 18px;
    }

    .forum-composer-card {
      margin-left: 18px;
      margin-right: 18px;
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
      grid-template-columns: 56px minmax(0, 1fr);
      padding: 18px 16px 12px;
    }

    .dc-room-intro h3 {
      font-size: 20px;
    }

    .forum-composer-card {
      margin: 14px 12px;
      padding: 16px;
      border-radius: 18px;
    }

    .forum-feed-wrap {
      padding: 2px 12px 18px;
    }

    .forum-post {
      padding: 16px 14px 14px;
      border-radius: 18px;
    }

    .forum-post-head {
      flex-direction: column;
      align-items: stretch;
    }

    .post-title {
      font-size: 19px;
    }

    .dc-discussion {
      padding: 16px 14px 22px;
    }

    .forum-composer-bottom,
    .comment-form-row {
      align-items: stretch;
    }

    .forum-compose-actions {
      width: 100%;
      justify-content: space-between;
    }
  }
</style>

<script>
  (function () {
    const rooms = {
      public: {
        title: 'public-feed',
        desc: 'A board for public posts, thoughts, questions, and open interaction.',
        introHeading: 'Welcome to #public-feed',
        introText: 'Share a post, start a discussion, and leave comments under a specific topic. This area feels more like a community board than a chat room.'
      },
      research: {
        title: 'research-board',
        desc: 'Focused posts on papers, methods, experiments, and reproducibility.',
        introHeading: 'Welcome to #research-board',
        introText: 'Post ideas, discuss technical details, compare methods, and leave targeted comments under each research topic.'
      },
      life: {
        title: 'life-board',
        desc: 'A relaxed board for routines, health, balance, habits, and daily reflection.',
        introHeading: 'Welcome to #life-board',
        introText: 'Use this space for slower discussions about life, motivation, habits, exercise, and maintaining long-term balance.'
      }
    };

    const storageKey = 'forum-style-room-posts-v2';
    const unreadKey = 'forum-style-room-unread-v2';
    const themeKey = 'forum-style-theme-v2';

    const roomTitle = document.getElementById('room-title');
    const roomDesc = document.getElementById('room-desc');
    const introHeading = document.getElementById('intro-heading');
    const introText = document.getElementById('intro-text');
    const statusText = document.getElementById('chat-status');
    const feedSummary = document.getElementById('feed-summary');
    const composeRoomLabel = document.getElementById('compose-room-label');
    const forumFeed = document.getElementById('forum-feed');
    const postTitleInput = document.getElementById('post-title');
    const postTextInput = document.getElementById('post-text');
    const submitPostBtn = document.getElementById('submit-post');
    const composerCount = document.getElementById('composer-count');
    const clearBtn = document.getElementById('clear-current-room');
    const channelSearch = document.getElementById('channel-search');
    const themeToggleBtn = document.getElementById('theme-toggle');
    const themeIcon = document.getElementById('theme-icon');

    const roleButtons = Array.from(document.querySelectorAll('.dc-role-btn'));
    const promptButtons = Array.from(document.querySelectorAll('.dc-prompts button'));
    const channelButtons = Array.from(document.querySelectorAll('.dc-channel'));
    const serverButtons = Array.from(document.querySelectorAll('.server-btn[data-room]'));
    const sectionToggles = Array.from(document.querySelectorAll('.section-toggle'));

    const badges = {
      public: document.getElementById('badge-public'),
      research: document.getElementById('badge-research'),
      life: document.getElementById('badge-life')
    };

    if (!forumFeed || !postTextInput || !submitPostBtn) return;

    function uid(prefix) {
      return prefix + '-' + Date.now() + '-' + Math.random().toString(36).slice(2, 8);
    }

    function formatTime(timestamp) {
      const date = new Date(timestamp);
      return date.toLocaleString('en-US', {
        month: 'short',
        day: 'numeric',
        hour: '2-digit',
        minute: '2-digit',
        hour12: false
      });
    }

    function seedPosts() {
      return {
        public: [
          {
            id: uid('post'),
            title: 'Welcome to the new community board',
            text: 'This page is now designed as a post-and-comment space instead of a chat room. Feel free to share ideas, questions, or updates in a more structured way.',
            role: 'author',
            sender: 'Author',
            time: Date.now() - 1000 * 60 * 90,
            comments: [
              {
                id: uid('comment'),
                role: 'visitor',
                sender: 'Visitor',
                text: 'This structure feels much cleaner for discussion. It is easier to focus on one topic at a time.',
                time: Date.now() - 1000 * 60 * 70
              }
            ]
          },
          {
            id: uid('post'),
            title: 'What kind of topics should this page encourage?',
            text: 'I am thinking this board can be used for academic exchange, project sharing, and also some daily reflections. What balance would feel the most natural?',
            role: 'visitor',
            sender: 'Visitor',
            time: Date.now() - 1000 * 60 * 35,
            comments: []
          }
        ],
        research: [
          {
            id: uid('post'),
            title: 'How should we evaluate a new research direction?',
            text: 'When exploring a new direction, I usually look at novelty, feasibility, and whether it can lead to a coherent long-term story. I would be interested in hearing other criteria as well.',
            role: 'author',
            sender: 'Author',
            time: Date.now() - 1000 * 60 * 120,
            comments: [
              {
                id: uid('comment'),
                role: 'visitor',
                sender: 'Visitor',
                text: 'I also care a lot about whether the problem setting is realistic and whether there is a clear baseline to compare against.',
                time: Date.now() - 1000 * 60 * 80
              }
            ]
          }
        ],
        life: [
          {
            id: uid('post'),
            title: 'How do you reset after intense work?',
            text: 'After long research sessions, I find that a short walk, stretching, or just leaving the screen for a while helps a lot. I am curious what routines work best for others.',
            role: 'visitor',
            sender: 'Visitor',
            time: Date.now() - 1000 * 60 * 55,
            comments: [
              {
                id: uid('comment'),
                role: 'author',
                sender: 'Author',
                text: 'A simple rule I like is to separate deep work and recovery on purpose, instead of waiting until I feel exhausted.',
                time: Date.now() - 1000 * 60 * 40
              }
            ]
          }
        ]
      };
    }

    function loadPosts() {
      try {
        const raw = localStorage.getItem(storageKey);
        if (!raw) return seedPosts();
        const parsed = JSON.parse(raw);
        return {
          public: Array.isArray(parsed.public) ? parsed.public : [],
          research: Array.isArray(parsed.research) ? parsed.research : [],
          life: Array.isArray(parsed.life) ? parsed.life : []
        };
      } catch (e) {
        return seedPosts();
      }
    }

    function savePosts() {
      try {
        localStorage.setItem(storageKey, JSON.stringify(posts));
      } catch (e) {}
    }

    function loadUnread() {
      try {
        const raw = localStorage.getItem(unreadKey);
        if (!raw) {
          return {
            public: 0,
            research: posts.research.length,
            life: posts.life.length
          };
        }
        const parsed = JSON.parse(raw);
        return {
          public: Number.isFinite(parsed.public) ? parsed.public : 0,
          research: Number.isFinite(parsed.research) ? parsed.research : 0,
          life: Number.isFinite(parsed.life) ? parsed.life : 0
        };
      } catch (e) {
        return {
          public: 0,
          research: posts.research.length,
          life: posts.life.length
        };
      }
    }

    function saveUnread() {
      try {
        localStorage.setItem(unreadKey, JSON.stringify(unread));
      } catch (e) {}
    }

    let currentRoom = 'public';
    let currentRole = 'visitor';
    let posts = loadPosts();
    let unread = loadUnread();
    let expandedPosts = new Set();

    function initTheme() {
      let savedTheme = null;
      try {
        savedTheme = localStorage.getItem(themeKey);
      } catch (e) {}

      const prefersDark = window.matchMedia && window.matchMedia('(prefers-color-scheme: dark)').matches;
      const theme = savedTheme || (prefersDark ? 'dark' : 'light');
      applyTheme(theme);
    }

    function applyTheme(theme) {
      document.body.classList.remove('theme-dark', 'theme-light');
      document.body.classList.add(theme === 'light' ? 'theme-light' : 'theme-dark');

      if (themeIcon) {
        themeIcon.textContent = theme === 'light' ? '☀️' : '🌙';
      }

      try {
        localStorage.setItem(themeKey, theme);
      } catch (e) {}

      const giscusFrame = document.querySelector('iframe.giscus-frame');
      if (giscusFrame && giscusFrame.contentWindow) {
        giscusFrame.contentWindow.postMessage(
          {
            giscus: {
              setConfig: {
                theme: theme === 'light' ? 'light' : 'dark'
              }
            }
          },
          'https://giscus.app'
        );
      }
    }

    function bindSectionToggles() {
      sectionToggles.forEach(function (btn) {
        btn.addEventListener('click', function () {
          const section = btn.getAttribute('data-section');
          const body = document.querySelector('[data-section-body="' + section + '"]');
          const expanded = btn.getAttribute('aria-expanded') === 'true';
          btn.setAttribute('aria-expanded', expanded ? 'false' : 'true');
          if (body) body.hidden = expanded;
        });
      });
    }

    function updateComposerCount() {
      const len = (postTextInput.value || '').length;
      composerCount.textContent = len + ' / 1200';
    }

    function updateBadges() {
      Object.keys(badges).forEach(function (key) {
        if (!badges[key]) return;
        const count = Number.isFinite(unread[key]) ? unread[key] : 0;
        if (key === currentRoom || count <= 0) {
          badges[key].textContent = '';
          badges[key].style.visibility = 'hidden';
        } else {
          badges[key].textContent = count;
          badges[key].style.visibility = 'visible';
        }
      });
    }

    function getRoomLabel(roomId) {
      return rooms[roomId] ? rooms[roomId].title : roomId;
    }

    function switchRole(role) {
      currentRole = role;
      roleButtons.forEach(function (btn) {
        btn.classList.toggle('active', btn.getAttribute('data-role') === role);
      });
    }

    function switchRoom(roomId) {
      if (!rooms[roomId]) return;
      currentRoom = roomId;
      unread[currentRoom] = 0;
      saveUnread();

      channelButtons.forEach(function (btn) {
        const active = btn.getAttribute('data-room') === roomId;
        btn.classList.toggle('active', active);
        btn.setAttribute('aria-current', active ? 'true' : 'false');
      });

      serverButtons.forEach(function (btn) {
        btn.classList.toggle('active', btn.getAttribute('data-room') === roomId);
      });

      renderRoom();
      updateBadges();
    }

    function createCommentItem(comment) {
      const item = document.createElement('div');
      item.className = 'comment-item';

      const avatar = document.createElement('div');
      avatar.className = 'comment-avatar ' + comment.role;
      avatar.textContent = comment.role === 'author' ? 'AU' : 'VS';

      const body = document.createElement('div');
      body.className = 'comment-body';

      const meta = document.createElement('div');
      meta.className = 'comment-meta';

      const name = document.createElement('strong');
      name.textContent = comment.sender;

      const time = document.createElement('span');
      time.textContent = formatTime(comment.time);

      const text = document.createElement('div');
      text.className = 'comment-text';
      text.textContent = comment.text;

      meta.appendChild(name);
      meta.appendChild(time);
      body.appendChild(meta);
      body.appendChild(text);

      item.appendChild(avatar);
      item.appendChild(body);

      return item;
    }

    function createPostCard(post) {
      const card = document.createElement('article');
      card.className = 'forum-post';

      const head = document.createElement('div');
      head.className = 'forum-post-head';

      const authorWrap = document.createElement('div');
      authorWrap.className = 'forum-post-author';

      const avatar = document.createElement('div');
      avatar.className = 'post-avatar ' + post.role;
      avatar.textContent = post.role === 'author' ? 'AU' : 'VS';

      const authorMeta = document.createElement('div');
      authorMeta.className = 'post-author-meta';

      const name = document.createElement('strong');
      name.textContent = post.sender;

      const subMeta = document.createElement('div');
      subMeta.className = 'post-submeta';

      const time = document.createElement('span');
      time.className = 'post-time';
      time.textContent = formatTime(post.time);

      const roleTag = document.createElement('span');
      roleTag.className = 'post-role-tag ' + post.role;
      roleTag.textContent = post.role === 'author' ? 'AUTHOR' : 'VISITOR';

      subMeta.appendChild(time);
      subMeta.appendChild(roleTag);

      authorMeta.appendChild(name);
      authorMeta.appendChild(subMeta);

      authorWrap.appendChild(avatar);
      authorWrap.appendChild(authorMeta);

      const rightActions = document.createElement('div');
      rightActions.className = 'post-actions-top';

      const roomChip = document.createElement('span');
      roomChip.className = 'room-chip';
      roomChip.textContent = getRoomLabel(currentRoom);

      rightActions.appendChild(roomChip);

      head.appendChild(authorWrap);
      head.appendChild(rightActions);

      card.appendChild(head);

      if (post.title && post.title.trim()) {
        const title = document.createElement('h4');
        title.className = 'post-title';
        title.textContent = post.title;
        card.appendChild(title);
      }

      const content = document.createElement('div');
      content.className = 'post-content';
      content.textContent = post.text;
      card.appendChild(content);

      const footer = document.createElement('div');
      footer.className = 'post-footer';

      const stat = document.createElement('div');
      stat.className = 'post-stat';
      stat.textContent = (post.comments ? post.comments.length : 0) + ' comment' + ((post.comments && post.comments.length === 1) ? '' : 's');

      const actionRow = document.createElement('div');
      actionRow.className = 'post-action-row';

      const toggleBtn = document.createElement('button');
      toggleBtn.className = 'post-btn primary';
      toggleBtn.type = 'button';
      toggleBtn.textContent = expandedPosts.has(post.id) ? 'Hide Comments' : 'Comment';
      toggleBtn.addEventListener('click', function () {
        if (expandedPosts.has(post.id)) {
          expandedPosts.delete(post.id);
        } else {
          expandedPosts.add(post.id);
        }
        renderFeed();
      });

      const quoteBtn = document.createElement('button');
      quoteBtn.className = 'post-btn';
      quoteBtn.type = 'button';
      quoteBtn.textContent = 'Use as Draft';
      quoteBtn.addEventListener('click', function () {
        postTitleInput.value = 'Re: ' + (post.title || 'Discussion');
        postTextInput.value = '> ' + post.text.split('\n').join('\n> ') + '\n\n';
        updateComposerCount();
        postTextInput.focus();
      });

      actionRow.appendChild(toggleBtn);
      actionRow.appendChild(quoteBtn);

      footer.appendChild(stat);
      footer.appendChild(actionRow);

      card.appendChild(footer);

      if (expandedPosts.has(post.id)) {
        const commentArea = document.createElement('div');
        commentArea.className = 'comment-area';

        const commentList = document.createElement('div');
        commentList.className = 'comment-list';

        if (Array.isArray(post.comments) && post.comments.length) {
          post.comments.forEach(function (comment) {
            commentList.appendChild(createCommentItem(comment));
          });
        }

        const form = document.createElement('div');
        form.className = 'comment-form';

        const textarea = document.createElement('textarea');
        textarea.placeholder = 'Write a focused comment on this post...';

        const row = document.createElement('div');
        row.className = 'comment-form-row';

        const note = document.createElement('div');
        note.className = 'comment-note';
        note.textContent = 'Commenting as ' + (currentRole === 'author' ? 'Author' : 'Visitor');

        const submit = document.createElement('button');
        submit.className = 'comment-submit';
        submit.type = 'button';
        submit.textContent = 'Publish Comment';

        submit.addEventListener('click', function () {
          const value = textarea.value.trim();
          if (!value) return;

          const targetRoom = posts[currentRoom];
          const targetPost = targetRoom.find(function (item) { return item.id === post.id; });
          if (!targetPost) return;

          targetPost.comments = Array.isArray(targetPost.comments) ? targetPost.comments : [];
          targetPost.comments.push({
            id: uid('comment'),
            role: currentRole,
            sender: currentRole === 'author' ? 'Author' : 'Visitor',
            text: value,
            time: Date.now()
          });

          savePosts();
          expandedPosts.add(post.id);
          renderFeed();
        });

        row.appendChild(note);
        row.appendChild(submit);

        form.appendChild(textarea);
        form.appendChild(row);

        commentArea.appendChild(commentList);
        commentArea.appendChild(form);
        card.appendChild(commentArea);
      }

      return card;
    }

    function renderFeed() {
      const roomPosts = Array.isArray(posts[currentRoom]) ? posts[currentRoom].slice() : [];
      roomPosts.sort(function (a, b) {
        return b.time - a.time;
      });

      forumFeed.innerHTML = '';

      if (!roomPosts.length) {
        const empty = document.createElement('div');
        empty.className = 'forum-empty';
        empty.innerHTML = '<strong>No posts yet.</strong><br/>Be the first to publish something in this channel.';
        forumFeed.appendChild(empty);
      } else {
        roomPosts.forEach(function (post) {
          forumFeed.appendChild(createPostCard(post));
        });
      }

      const totalPosts = roomPosts.length;
      const totalComments = roomPosts.reduce(function (sum, post) {
        return sum + (Array.isArray(post.comments) ? post.comments.length : 0);
      }, 0);

      feedSummary.textContent = totalPosts + ' posts · ' + totalComments + ' comments in this channel.';
      statusText.textContent = Object.keys(rooms).length + ' channels · ' + totalPosts + ' posts';
    }

    function renderRoom() {
      const meta = rooms[currentRoom];
      roomTitle.textContent = meta.title;
      roomDesc.textContent = meta.desc;
      introHeading.textContent = 'Welcome to #' + meta.title;
      introText.textContent = meta.introText;
      composeRoomLabel.textContent = meta.title;
      renderFeed();
    }

    function publishPost() {
      const title = postTitleInput.value.trim();
      const text = postTextInput.value.trim();

      if (!text) return;

      const newPost = {
        id: uid('post'),
        title: title,
        text: text,
        role: currentRole,
        sender: currentRole === 'author' ? 'Author' : 'Visitor',
        time: Date.now(),
        comments: []
      };

      posts[currentRoom] = Array.isArray(posts[currentRoom]) ? posts[currentRoom] : [];
      posts[currentRoom].push(newPost);
      savePosts();

      postTitleInput.value = '';
      postTextInput.value = '';
      updateComposerCount();
      expandedPosts = new Set([newPost.id]);
      renderRoom();
    }

    bindSectionToggles();
    initTheme();
    updateComposerCount();

    roleButtons.forEach(function (btn) {
      btn.addEventListener('click', function () {
        switchRole(btn.getAttribute('data-role'));
      });
    });

    channelButtons.forEach(function (btn) {
      btn.addEventListener('click', function () {
        switchRoom(btn.getAttribute('data-room'));
      });
    });

    serverButtons.forEach(function (btn) {
      btn.addEventListener('click', function () {
        switchRoom(btn.getAttribute('data-room'));
      });
    });

    promptButtons.forEach(function (btn) {
      btn.addEventListener('click', function () {
        postTitleInput.value = btn.getAttribute('data-fill-title') || '';
        postTextInput.value = btn.getAttribute('data-fill-text') || '';
        updateComposerCount();
        postTextInput.focus();
      });
    });

    if (submitPostBtn) {
      submitPostBtn.addEventListener('click', publishPost);
    }

    if (postTextInput) {
      postTextInput.addEventListener('input', updateComposerCount);
    }

    if (clearBtn) {
      clearBtn.addEventListener('click', function () {
        posts[currentRoom] = [];
        unread[currentRoom] = 0;
        savePosts();
        saveUnread();
        renderRoom();
        updateBadges();
      });
    }

    if (channelSearch) {
      channelSearch.addEventListener('input', function () {
        const keyword = channelSearch.value.trim().toLowerCase();
        channelButtons.forEach(function (btn) {
          const text = btn.textContent.toLowerCase();
          const matched = !keyword || text.indexOf(keyword) !== -1;
          btn.classList.toggle('hidden-by-search', !matched);
        });
      });
    }

    if (themeToggleBtn) {
      themeToggleBtn.addEventListener('click', function () {
        const isLight = document.body.classList.contains('theme-light');
        applyTheme(isLight ? 'dark' : 'light');
      });
    }

    updateBadges();
    renderRoom();
  })();
</script>
