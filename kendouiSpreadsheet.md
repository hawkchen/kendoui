# Quick Evaluation Report

# Rendering massive cells
* only render a limit number of cells according to visible ranges (columns x rows)
check $('.k-spreadsheet-cell').size()
* can render more than 10 million cells (10c x 1,000,000r)
* scrolling down to 1000000 row is smooth and doesn't have blank page
* editing a cell doesn't have any delay
* inserting and deleting rows/columns work instantly
* render non-blank cells with <div>
* blank cell doesn't have a corresponding <div>, only grid lines
* render grid lines with a group of independent <div> (not with cells)


# Performance problem
* selecting the whole column (100,000 cells) takes more than 10 sec, the more cells you select, the more time it takes
* selecting 1 millions cells crashes a browser tab for out-of-memory, stop responding
