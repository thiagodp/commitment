# English

> Simple rules for commit messages.

## Message rules

1. **Title must be up to 72 characters long**
   - It facilitates to see the log, *i.e.*, `git log --oneline`
   - There are tools that truncate messages
   - If you can, keep it under 50 characters
2. **Title must start with a uppercase letter**
3. **Title must start with a verb in third person singular**
4. **Title must not use passive voice**
5. **Title must not end with a period (full stop)**
6. **Title must be separated from the message body by an empty line**
7. **Body is optional**
8. - Usually the title is enough to express the change
9. **Body must explain *what* and *why*, but not *how***
   - It must focus in the perceived contribution

### Examples without a body

- `Add option to export to PDF`
- `Refactor class Foo`
- `Remove foo.json and bar.xml`
- `Closes #123`
- `Document component Acme`
- `Approve merge #456`
- `Approve merge #456 from some-user/some-branch`
- `Update version to 1.2.1`
- `Fix #123 about watchamacallit`

### Examples with a body

```
Undo "Add option to export to PDF"

Revert commit c83d7a9ac83d7a9ac83d7a9ac83d7a9ac83d7a9a
```

```
Release version 1.3.0

What's new:
- New watchamacallit, see #125
- Improve performance of thingamajig
- Fix #123 about thingamabob
- Fix #124 about doodad
```

## Content rules

1. **Always group a set of changes or files by a *single* task**
   - Atomic commits are easier to undo
   - It facilitates to track changes from the commit messages

2. **Separate fixes from changes**
   - It facilitates to apply a fix to other branches
   - It makes commits easier to undo

3. **Never commit if it does not compile**
   - Verify before committing

4. **Integrate every day**
   - It avoids to accumulate work to do
   - Use `fetch` to get updates
   - Always `merge` with stable branches

5. **Set aside some time to integrate**
   - It helps to comply with Rule 4
   - It makes it easier to organize your work

6. **Do not integrate when you are in the middle of a task**
   - It facilitates to merge branches

7. **Always update before sending your work**
    - Use `fetch` and `merge` (or `pull`) before `push`ing


### Additional recommendations

1. **Separate branches for changes and fixes**
   - It help with rules 1 and 2

2. **Organize yourself to do one thing at a time**
   - Rules 1, 2, and 5 require organization. Try to plan your work beforehand.

3. **Submit incomplete work to personal remote branches**
   - At the end of the day, whether you could not to finish a certain task, submit your work to a remote branch. Thus, you lower the risk to lose your work if your computer gets broken, make your work accessible to other team members, and do not interfere with other people's work.

4. **Submit incomplete work to the stash when merging**
   - Use `stash` appropriately to not lose your work or to facilitate its integration to the merged content.

5. **Use tools to detect problems before commiting**
   - Use pre-commit or pre-push hooks.
   - Use linters to detect problems or potencial failures.
   - Verify if your code compiles correctly.
   - Verify if your code pass the automated tests.


[Back](readme.md)