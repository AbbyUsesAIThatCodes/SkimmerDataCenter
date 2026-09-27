# Skimmer Data Center: Non-Binding Concept Notes

Recorded September 27, 2026.

> Status: exploratory concept record. These notes preserve the brainstorming discussion, not an approved specification, roadmap, release scope, deadline, or instruction to begin implementation. Merging this document records the ideas; it does not commit to building every suggestion.

## Purpose and Naming

Help students enter, select, copy, paste, visualize, and interpret data from their classroom skimmer trials. Spreadsheet skills are an explicit learning objective: many students may be using a spreadsheet successfully for the first time.

Names discussed were **Skimmer Test Lab**, **Skimmer Data Center**, and **Skimmer Sheets**. The repository is SkimmerDataCenter, and **Skimmer Data Center** is the current working display name. It allows room for data entry, charts, comparison, and interpretation.

The companion **[Mean Machine](https://github.com/AbbyUsesAIThatCodes/MeanMachine)** project teaches arithmetic mean through equal sharing in a factory. The teacher proposed separate games to keep development focused and make eventual integration into Fulcrum and possibly Learning Compass easier. No integration contract or technology choice has been made.

## Proposed Student Journey

Students first enter their measurements in the class Google Sheet. They then select appropriate ranges, copy them, and paste them into a rows-and-columns spreadsheet element inside this application. The pasted measurements produce a box-and-whisker plot.

The interface should guide students through progressively wider datasets:

| Stage | Intended Data | Candidate Investigation |
| --- | --- | --- |
| Your Skimmer | The student's or team's own trial results | How did our skimmer perform across its flights? |
| Your Class | The student's class results | Where do our results sit within our class? |
| All Classes | The combined participating classes' results | What changes when we include more data? |

The exact meaning of individual versus team data needs confirmation. Each stage should identify the dataset being analyzed. Successive pastes should not accidentally append overlapping data and count the student's flights multiple times.

Whether plots remain side by side, appear one at a time, or can be revisited is open for the roadmap.

## Teach the Spreadsheet Operation Explicitly

A candidate repeated sequence is:

1. Open the correct Google Sheet and tab.
2. Enter or locate the intended measurements.
3. Select the requested range.
4. Copy the selection.
5. Click the starting cell in the application's grid.
6. Paste the copied rows and columns.
7. Check the imported measurements and their count.
8. Read the plot and respond to an interpretation prompt.

Teach rows, columns, cells, a selected range, and a destination cell in the context of this task. Do not assume students already understand selecting a range or copying several cells.

The teacher suggested screenshots of the actual Google Sheet, and using that sheet as a source for illustrated guidance. A possible interface places an annotated source screenshot beside the destination grid, with the relevant range highlighted.

The specific Google Sheet, tab names, layout, ranges, and screenshots have not been supplied or verified in this planning conversation. Those must be inspected before writing exact copy-and-paste instructions. Avoid inventing cell addresses or presenting an unrelated template as the classroom sheet.

## Candidate Import Behavior

These ideas need a concrete data format and scope decision later:

- Preserve pasted rows and columns in a visible grid so students can check the transfer.
- Show a preview and a clear count, such as **Found 18 Flight Distances**.
- Distinguish measurement cells from labels, student identifiers, dates, and summary calculations. Do not treat every numeric cell in a pasted rectangle as a flight.
- Handle expected headers and blank cells helpfully, with understandable feedback for unexpected values.
- Keep a recorded zero as a real value; a blank cell is not automatically zero.
- Keep units explicit and consistent.
- Explain a rejected or ignored value instead of silently changing the data.
- Support an understandable way to correct or replace an import.

Copy and paste is the proposed learning interaction. A live Google connection, account login, or automatic synchronization has not been requested or selected.

## Statistical Meaning and Plot Decisions

A box-and-whisker plot foregrounds the median, quartiles, and spread. It does not, by itself, display the arithmetic mean. A separately labeled mean value and possibly a distinct mean marker were suggested to connect this application to Mean Machine without confusing mean and median.

The roadmap must choose and document the quartile and whisker conventions. Different conventions can produce different results, especially for small datasets. Decide how to explain and handle very small samples, repeated values, outliers, and datasets with no spread.

Choose what each observation represents: an individual flight or an already-calculated student/team mean. Preserve that meaning across the three stages. Pooling flights and averaging group means are not interchangeable when groups have different numbers of trials.

Raw measurements should remain inspectable. Any optional visual model of redistribution should use clearly separate copies and leave recorded trial results intact.

## Other Ideas Preserved for Discussion

Earlier brainstorming included:

- Comparing skimmer designs by mean distance rather than relying only on the longest flight.
- Predicting how one changed result affects the mean.
- Finding a missing third flight distance that would reach a target mean.
- Showing movable copies of distance bars to connect trial data with equal sharing.
- Entering actual classroom race results after practicing with a small example dataset.

These are optional extensions, not first-release commitments. Spreadsheet guidance and the three-stage paste-and-plot journey are the teacher's later, more specific direction.

## Accompanying Worksheet

The worksheet should follow the application's stages and record students' reasoning as well as their charts.

Possible entries include:

- Identify the dataset and units.
- Record how many measurements were imported.
- Check that the selected source cells match the intended dataset.
- Record or calculate relevant statistics.
- Label or interpret a box-and-whisker plot.
- Compare the student's/team's results with the class and combined data.
- Explain mean versus median and describe what the spread suggests.
- Answer an independent interpretation question.

The earlier suggestion of a double-sided worksheet remains a possibility. Exact length, screenshots, plotting scaffolds, teacher key, and calculation expectations should be decided after the source sheet and first application scope are settled.

## Development Boundaries and Open Questions

- Which Google Sheet is the reference, and how are its tabs, columns, units, and class groups organized?
- What is the smallest useful paste-and-plot experience for spreadsheet beginners?
- Are the source data recorded per student, per team, or per skimmer?
- Will students copy a contiguous range, several ranges, or use a combined-data tab for all classes?
- How should keyboard shortcuts and touch/device differences be taught?
- What grid interactions are needed initially: pasting only, editing cells, selecting columns, or more?
- Which statistics, plot conventions, and comparison views should be taught first?
- How should import feedback help students find an incorrect selection?
- What are the intended browser/device targets, technology, hosting, and versioning approach?
- What should remain independent before discussing Fulcrum or Learning Compass integration?

The earlier suggestion was to start Mean Machine first while settling the sheet layout for this project. That is a sequencing idea, not a deadline or a prerequisite imposed on this repository.

## Handoff

In a new conversation, read these notes and the current repository, identify and inspect the actual classroom Google Sheet or supplied screenshots, and agree on a concrete roadmap for Skimmer Data Center. Then turn agreed scope into concrete issues and implement focused PRs.

No implementation issues, release dates, technical commitments, live integrations, or working charts are established by this document.
