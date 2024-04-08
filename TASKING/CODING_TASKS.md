
### Example: Refactor & Improve a project

Take different separate steps, in order for user to wrap their head about what is about to be improved
Eacht stage should generate a report that the user can evaluate before executing, and a report after.

- User specifies simple goals to adhere to
- Agents scan and discuss what the end goal is, and make a plan.
- The Agents split up the roadmap to the plan in seperate stages

For example:
1 Write missing tests for uncovered code.
2 Fix bugs, but don't create or delete any new files or functions
3 Refactor existing functions that can be refactored without creating or deleting files.
4 Refactor the splittable or mergable files (make sure the previous step does not superfluously refactors too many things that are going to be changed in this step)
5 Retest all previously tested code, and all new code.
6 Doublecheck for uncovered code