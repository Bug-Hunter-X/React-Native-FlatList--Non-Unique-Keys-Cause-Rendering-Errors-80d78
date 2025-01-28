# React Native FlatList: Non-Unique Keys Bug

This repository demonstrates a common bug in React Native's `FlatList` component: using non-unique keys for list items. This can lead to incorrect rendering, performance issues, and unpredictable behavior when updating the list.

## The Problem

When you don't provide unique `key` props for each item in your `FlatList` data, React Native struggles to track and update items efficiently. This often results in items not appearing correctly or the list not updating smoothly when data changes.

## The Solution

The solution is simple: ensure each item in your data array has a unique key.  This key should ideally be a stable, unique identifier for the item (such as a database ID). If you don't have a stable ID you can use the item's index as a last resort, but this is less efficient.

## How to Reproduce

1. Clone this repository.
2. Run `npm install`.
3. Run the app.  Observe the buggy rendering in `BuggyFlatList.js`.
4. Switch to `FixedFlatList.js` to see the corrected version.

## Files

- `BuggyFlatList.js`: Demonstrates the bug with non-unique keys.
- `FixedFlatList.js`: Shows the corrected implementation with unique keys.