# Tailwind Purge: Unused CSS in Production Build

This repository demonstrates a common issue with Tailwind CSS's `purge` feature where unused CSS classes are still included in the production build, leading to larger file sizes.  The `bug.js` file shows the incorrect configuration, while `bugSolution.js` provides the solution.

## Problem

The `purge` option in the Tailwind configuration wasn't correctly configured to include all sources of CSS classes, leading to unused styles in the final CSS output.

## Solution

The `content` array in the purge options must correctly list all files and directories containing CSS classes.  This includes HTML files using classes directly and JavaScript/React files that dynamically add classes. The updated configuration in `bugSolution.js` comprehensively lists possible source files.