H2 PRIME STYLE GUIDE — wiring cleanup, 25 Oct 2026

Five files. Drop them into your style guide folder beside the other
h2p-section-*.html files and h2p-shared.css. All links are bare filenames,
so everything resolves as long as the folder stays flat.

WHAT WAS BROKEN
  The amendment and the build record existed but nothing pointed at them.
  13A mentioned the amendment only in its footer; Section 14 ignored it
  entirely; the cover listed neither. The build record had no style guide
  chrome at all — no shared stylesheet, no nav, no footer, no way back.

THE CHAIN NOW
  9 → 13A → 13A Amendment → 14 → Notification Center build record
  Every one of the five documents links to every other, in both the top
  nav and the footer. Verified programmatically, not by eye.

FILES
  h2p-cover.html
      New "Companion documents" block with cards for the amendment and the
      build record, two new rows in the status table, version → v1.2, and
      direct links in the footer.

  h2p-section-13a-figma-variables.html
      Amendment promoted into the top nav (it was footer-only). Footer now
      also points forward to the build record as the first consumer of
      these variables.

  h2p-section-13a-amendment-2026-10-25.html
      Build record added to nav and footer.

  h2p-section-14-overlay-surface-system.html
      Amendment and build record added to the nav. Footer restructured to
      match the house pattern — it was the only section with links on the
      right-hand side. Divider element corrected from <span> to <div>.

  h2p-notification-center-figma-build-2026-10-25.html
      Rebuilt on h2p-shared.css. Now has the standard nav, doc-header with
      kicker/title/lead/meta, a table of contents, lettered sections A–F,
      house tables and callouts, and a page footer. Content unchanged except
      for the additions below; every class it uses is either in the shared
      sheet or defined in its own <style> block (verified).

      Added in this pass:
        · the full /notifications page and its dark counterpart
        · "Why the page is a table and the drawer is not"
        · the Soft Badge defect with measurements, and the 92-instance fix
        · ADR 14-1 trace rule and ADR 14-2 peek, in the rules-applied table
        · library components used on the full page

NOTE ON THE PROJECT COPY
  In the claude.ai project, the cover and 13A sit at the root while the
  amendment, Section 14 and the build record sit under claude/ — new files
  written by Claude get namespaced there. The links are written for a flat
  folder, so they resolve locally but not in the project's file view. If you
  want them to resolve there too, upload these three to the project root:
    h2p-section-13a-amendment-2026-10-25.html
    h2p-section-14-overlay-surface-system.html
    h2p-notification-center-figma-build-2026-10-25.html
