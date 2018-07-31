# Volatile Landmarks

## Summary
[summary]: #summary

Add a new category of landmarks that is volatile, i.e. can be overwritten by a new observation with the same ID.

## Motivation
[motivation]: #motivation

Currently, landmarks are assumed to be fixed points in the environments that have an unique ID assigned to it.

In real-world applications, it can happen that landmark IDs occur twice.
With the current implementation, this leads to very destructive results if the landmark is weighted high.

*add example image / video with landmark sampler*

## Approach
[approach]: #approach

Add a `volatile` flag to landmark entries.

If it is set, the landmark will be trimmed once a new landmark observation with the same ID enters the pose graph.

## Discussion Points
[discussion]: #discussion

* how to trim landmarks?
