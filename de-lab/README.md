# DE lab exams

One folder per unit of the Data Engineering Lab course. The portal's **⟳ Sync DE exams** button
(managers, Mock exams) reads this folder from GitHub and keeps one exam per unit.

```
<unit>/exam.json             the exam: id, name, domains (the unit's lessons)
<unit>/questions/<set>.json  question banks (certification-exams question-bank schema 1.0 / 1.1)
```

- A unit shows up for members once its `questions/` has at least one usable question.
- Question ids: `<set>-001`, `<set>-002` … (the bank's `source` is `<set>`); `exam_id` is the unit's id.
- `domain` is the lesson's number in `exam.json` (`3`, or `2.1` for a sub-lesson); `domain_name` /
  `subdomain_name` carry their names.
- Edit or add questions, push, then Sync: new and changed questions reach members; a question
  removed from a file leaves the exam (old reviews keep it).
