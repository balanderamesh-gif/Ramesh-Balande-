# Junior Advocate — Online Platform Audit & Quality-Control Plan
**Project owner / author:** Adv. Ramesh S. Balande  
**Languages:** Marathi first, with English terminology and bilingual summaries  
**Review date:** 26 October 2026  
**Status:** Planning / pre-publication. This document is not a legal opinion and does not certify any individual legal proposition.

## 1. Audit of the current website starter

The current `index.html` is a polished one-page landing page and an acceptable visual prototype. It is **not yet a complete legal-information platform**.

### Findings to resolve before public launch
- Topic cards mostly point to page anchors; there are no dedicated, searchable article pages yet.
- There is no search across legal topics, statutes, judgments, or updates.
- Content has no structured metadata for author, reviewer, jurisdiction, source links, last legal verification date, or next review date.
- There is no editorial approval state to prevent draft or unverified legal content from being published.
- The bilingual toggle swaps only elements carrying `data-mr`; new content must be checked for full translation, accessible labels, and correct language metadata.
- There is no documented daily update workflow, change log, correction policy, or version history for legal articles.
- The public site needs clear privacy, terms of use, disclaimer, contact/correction channel, accessibility checks, and an explanation that educational content is not a substitute for advice on a specific case.
- No production search, content-management interface, database, scheduled official-source monitoring, video library, or user account/membership system is present in the current single HTML file.
- Do not label the site “daily updated” unless a dated, auditable update process actually runs. A scheduled check is not the same as automatic publication.
- Any claim that content is “error-free” or guaranteed accurate must be avoided. The defensible promise is a documented, multi-step verification and correction process.

## 2. Publication policy: legal accuracy before speed

Every legal article, video script, downloadable draft, and update must pass these gates:

1. **Issue definition:** identify the jurisdiction, court, legal issue, relevant dates, and facts assumed.
2. **Primary source:** read the official Act / Rules / Gazette notification / court order or judgment. Use secondary sources only as discovery aids.
3. **Commencement and amendments:** verify the commencement notification, amendment history, rules, state-specific notifications, and transitional provisions where relevant.
4. **Case verification:** check exact case title, court, bench, decision date, neutral/report citation, relevant paragraphs, subsequent history, and whether the decision has been stayed, reversed, distinguished, or overruled.
5. **Application check:** explain what the authority actually decides and what it does not decide; distinguish binding ratio from observations and facts.
6. **Independent review:** a qualified legal reviewer checks the draft before publication. AI-generated summaries are never the sole verification source.
7. **Editorial sign-off:** only a human editor with permission may move an item from Draft to Verified / Approved.
8. **Versioning:** save publication date, verification date, reviewer, source URLs, and a revision log.
9. **Correction process:** if an error is reported, mark the affected item for review promptly; unpublish or add a visible correction notice if material; preserve the correction history.
10. **Periodic re-check:** review fast-changing procedural material more often and all material after relevant amendments or controlling judgments.

### Required status labels
- **Draft — Not for reliance**
- **Source located — Not yet legally verified**
- **Under legal review**
- **Verified for publication** (include verification date and reviewer)
- **Needs re-check / Update pending**
- **Superseded / Archived**

Never display “Verified” without a named responsible reviewer and a dated record. Never fabricate a citation or paraphrase a judgment without checking the original.

## 3. Required article schema

Each article or resource should contain:

- Unique article ID and stable URL slug
- Marathi title and English title
- Topic / tags (e.g. Criminal Procedure, Bail, Evidence, Civil Procedure)
- Jurisdiction and court level
- Audience and assumed facts
- Short answer / overview
- Applicable statute, section, rule, and exact relevant text or a carefully limited summary
- Commencement / transitional note, if relevant
- Procedure in numbered steps
- Documents and evidence checklist
- Practical risks and common mistakes
- Verified cases: full title, court, date, citation / neutral citation, paragraph numbers, holding, and subsequent-treatment note
- Official source links
- Author, legal reviewer, verification date, publication date, next review trigger/date
- Version number and change log
- Disclaimer and correction/report-an-error link

## 4. Source hierarchy

Use sources in this order, depending on the question:

1. Gazette of India / relevant State Gazette and official notifications.
2. India Code for central Acts and available amendment materials.
3. Official Supreme Court of India judgment/order pages and Supreme Court Reports search.
4. Official Bombay High Court orders/judgments and unified search.
5. Official Maharashtra Government / department / GR portals for Maharashtra-specific rules, GRs, revenue and municipal matters.
6. Official court rules, practice directions, e-Courts and relevant tribunal portals.
7. Reputable law reports and secondary commentary as discovery or cross-check tools, not as a replacement for the primary source.

A search-result snippet alone is not sufficient verification. Open and read the source document and relevant paragraphs.

## 5. Initial official source directory

- Ministry of Home Affairs — New Criminal Laws: https://www.mha.gov.in/en/commoncontent/new-criminal-laws
- India Code — BNSS, 2023: https://www.indiacode.nic.in/indiacode/handle/123456789/20099?view_type=browse
- India Code — BSA, 2023: https://www.indiacode.nic.in/indiacode/handle/123456789/20063?col=123456789%2F1362&view_type=search
- Bombay High Court — Unified Orders/Judgments Search: https://bombayhighcourt.gov.in/bhc/front/unified-search
- Supreme Court of India: https://www.sci.gov.in/
- Supreme Court Reports search: https://scr.sci.gov.in/scrsearch/
- Bureau of Police Research & Development — New Criminal Laws resources: https://bprd.nic.in/page/new_criminal_laws

For every article, select the specific primary source relevant to the proposition; this directory is not proof that every cited proposition has been verified.

## 6. Special rule for BNS / BNSS / BSA

The three new criminal laws generally came into force on 1 July 2024, subject to the exact commencement notification and its stated exception. Do not mechanically replace IPC/CrPC/Indian Evidence Act references with BNS/BNSS/BSA numbers. For every real case, assess the relevant date, applicable transitional provision, the offence/proceeding context, and the exact statutory text. Record the rule used and its official source.

## 7. Online platform architecture

### Phase 1 — Safe public website
- Responsive Marathi / English interface
- Landing page, topic directory, article pages, source directory, latest verified updates
- Search and filters by subject, statute, court, year, and verification status
- Article metadata, source links, version history, disclaimer, privacy and terms pages
- Report-an-error form and contact route
- SEO metadata, sitemap, accessible navigation, mobile testing
- No public self-publication of AI-generated legal text

### Phase 2 — Editorial CMS
- Secure login and role-based permissions: Author, Legal Reviewer, Editor, Administrator
- Draft → source-check → legal review → editorial approval → publish workflow
- Required fields that block publication if source/citation/reviewer/date is missing
- Audit log and version rollback
- Backups, secret management, rate limiting, spam protection and dependency updates

### Phase 3 — Verified update workflow
- Scheduled checks of official source pages and court feeds where technically permitted
- Human review of each detected change
- A dated update card showing what changed, source, relevance, reviewer, and verification date
- “No verified material update found” when appropriate
- Never auto-publish scraped or AI-generated legal conclusions without human approval

### Phase 4 — Video, e-book, and app
- Every video is linked to its source-checked article
- Script and subtitle versions share the article's version number
- Visible correction workflow for already published videos
- E-book / PDF generated only from approved content
- App uses the same approved content source and displays “last verified” dates
- Membership or paid content is added only after privacy, payment, consumer, tax, and applicable professional-conduct review

## 8. Security, privacy, and professional conduct

- Do not collect identifiable client facts, case papers, phone numbers, or confidential documents unless necessary and protected.
- Never upload client-confidential documents to public repositories or public AI tools.
- Use HTTPS, least-privilege access, secure authentication, backups, and secrets outside source code.
- Do not publish client-identifying case details without a lawful basis and appropriate safeguards.
- Review the applicable Bar Council rules and professional-conduct restrictions before adding advertisements, testimonials, lead generation, paid consultation, or promotional claims.
- Have a qualified reviewer check privacy notices, terms, disclaimers, and any data collection before launch.

## 9. Launch checklist

- [ ] All article claims trace to an opened primary source.
- [ ] Every citation and relevant paragraph checked against the original.
- [ ] Commencement, amendments, transitional rules, and Maharashtra-specific rules checked where applicable.
- [ ] Reviewer and verification date recorded.
- [ ] No unsupported claim, fabricated citation, or guarantee of outcome.
- [ ] Marathi and English versions reviewed for legal meaning, not merely literal translation.
- [ ] Links, search, mobile layout, keyboard navigation, and screen-reader labels tested.
- [ ] Privacy, terms, disclaimer, corrections, and contact pages published.
- [ ] Backup and rollback tested.
- [ ] Final human approval recorded before release.

## 10. Current verified starting points (26 October 2026)

- India Code lists the BNSS as Act 46 of 2023 and gives its enforcement date as 1 July 2024.
- The Ministry of Home Affairs maintains an official New Criminal Laws page for BNS, BNSS and BSA.
- The Bombay High Court provides an official unified search for orders and judgments.
- The Supreme Court of India provides official judgments, orders, and updates.

These are source-directory facts only; they do not verify any individual section, case-law proposition, or draft in the book.

## 11. Immediate next work items

1. Build article templates and metadata before adding substantive legal content.
2. Convert the master index into topic pages with no unsupported case citations.
3. Draft the first chapters in Marathi-first bilingual format, with a source note for each legal proposition.
4. Test the approval workflow using one low-risk educational article.
5. Add official-source links and a visible update/correction log.
6. Publish only after legal review and deployment checks.

**Release rule:** If a legal proposition cannot be verified from a suitable source, omit it or label it clearly as pending verification. Accuracy takes priority over publishing frequency.
