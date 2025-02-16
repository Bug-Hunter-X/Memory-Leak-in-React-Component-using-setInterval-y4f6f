# React setInterval Memory Leak
This repository demonstrates a common React bug: a memory leak caused by the improper use of `setInterval` within the `useEffect` hook.  The provided `bug.js` file shows the flawed code. The solution, `bugSolution.js`, demonstrates how to correctly use `setInterval` to avoid memory leaks.

## Bug Description
The original code uses `setInterval` to update a counter every second. However, it fails to clear the interval when the component unmounts. This leads to the interval continuing to run indefinitely, even after the component is no longer needed, resulting in a memory leak and potential performance issues.

## Solution
The solution provides a corrected version using `clearInterval`.  This ensures that the interval is correctly stopped when the component unmounts, preventing the memory leak.