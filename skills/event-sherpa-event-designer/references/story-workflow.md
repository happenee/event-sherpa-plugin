# The Story workflow, steps 2 to 10

Read this once the person has asked for an Event Story or picked it as the
next step. Step 1 (reading the core) is in SKILL.md. Every path below is
relative to the skill's folder, the one that holds SKILL.md.

2. Lead the conversation from those instructions. Declare `mode: text` and
   `artifact: markdown` to yourself the way the run header describes, follow
   the state machine of S4 without writing its `STATE:`, `ARCHETYPE:` and
   `MODULES:` lines at all, the way S4 prescribes for this shape: here a
   person reads the reply, nothing parses it, and ChatGPT shows an HTML
   comment as text. The step you are in binds you all the same. The fact ids
   the cards carry under the json shapes (`f-01`) stay in your own ledger
   here and are not printed on the cards, for the same reason. S4
   defines that shape and this file only picks it: the artefact turn is the
   Markdown story without section 9 and the status line, and without the
   render specification's section 10, which exists only in an `A+B` run, and the json block
   and that section come to a person who asks for them, „pošli Story JSON" or
   "send the Story JSON" in either language, each in a reply of its own: that
   reply is the state STORY again.

   Before you send the story, check four things against the specification,
   because a turn drifts where a runner would have caught it: a candidate
   read from the brief stays as the working assumption, never dropped and
   never marked confirmed; in the story every line under „Kde vám Happenee
   pomůže“ reads „název · proč“; a branch detail's heading is the same
   words as its card; and no `STATE:`, `ARCHETYPE:` or `MODULES:` line
   stands anywhere in the reply. The legend sentences, the counters and the
   sentence about missing product screenshots are left out (see "No web
   page parts").
3. Before a turn that is about to ask a question, read
   `instructions/questions.cs.md` or `instructions/questions.en.md` once. It
   is the question bank S4's CLARIFY state draws from. A brief that already
   answers everything the three cards need skips this file entirely: nothing
   in the conversation asks for it.
4. Once you have settled the archetype, in your own ledger and not on any
   written line, read its article from `knowledge/archetypes/`, for example
   `knowledge/archetypes/conference.cs.md` or
   `knowledge/archetypes/hybrid.en.md`. Read a second one only when the match
   changes.
5. Before you write the story, settle the modules the story is going to recommend,
   from the closed list of fourteen `module_slug` values the core carries, in
   your own ledger: under `artifact: markdown` no `MODULES:` line is written,
   the list only decides which articles step 7 reads.
6. Once the person has asked for the story and before you write it,
   read `instructions/story.cs.md` or `instructions/story.en.md` once: the
   full text of the always-loaded articles, one line on each knowledge base
   article that loads on demand and the render specification arrive there.
   The wire schema does not: the Markdown story does not need it, and step 10
   reads it for the reply that carries the JSON.
7. Then read the module articles. First the articles
   `config/archetype_ondemand.json` lists for the archetype you settled on,
   in its order, so that the engagement functions article (03.24) a
   conference, a hybrid or an internal event needs is read before any module
   spends the budget. Then look each name from your module list up
   in `config/kb_module_map.json`, where a module answers
   to its `web_slugs`, to its `tag`, to any of its `capability_keys` and to an
   alias, and one name may match two modules, as `event-app` does. Its
   `articles` are the numbers to read, so `02.10` in Czech is
   `knowledge/ondemand/kb.cs.02.10.md`. The modules then take turns in the
   order you named them: every module's first article before any module's
   second, each article once however many modules pulled it in, and at most
   120 000 B of article text in the whole conversation. An article that would
   cross that is skipped and you carry on with the next module, so one module
   of long articles does not spend the budget on its own. What you did not
   read stays what its line in that list says, a title and one sentence;
   do not cite it and do not put its id in `source_refs[]`.
   Leave what you did not read out of the story: an article number or a
   sentence about what was loaded tells the reader nothing (render
   specification, section 9). If the person asks what the story rests on,
   name the topics, never the numbers.
8. Before you write the Markdown story, read `schema/labels.cs.json` or
   `schema/labels.en.json`: the render specification prints seven
   vocabularies through that file, and a status printed from memory is a
   defect. The goals section (render specification, section 1b) always ends,
   while `success_criteria[]` has a record, with the block headed `Jak
   poznáte, že se jednotlivé cíle splnily` or `How you will know each goal
   was met`, that heading and no other: one bullet per record with the goal,
   its measure, the evidence and when, the working-assumption label where it
   is one, and to whom the result is shown.
9. `INSUFFICIENT` is reachable on the first turn, before you have read
   `instructions/story.cs.md` or `instructions/story.en.md`. The core
   describes a runner that answers such a turn in two steps, prose first and
   the object once the extension has arrived; that split is the runner's own
   mechanic and does not apply here, because you can read a file yourself.
   Read the story file now, in the same turn, and deliver the `INSUFFICIENT`
   turn at once, in the declared shape. This turn remains readable and does not save a plan that is still incomplete.
10. Read `schema/event_story.wire.json` before building the Story document,
    then follow Saved role plans to store and verify the exact document used
    for the readable Story and to handle requests for its JSON.
