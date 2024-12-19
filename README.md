# React useEffect setInterval Memory Leak

This repository demonstrates a common error in React applications involving the `useEffect` hook and `setInterval`. The improper usage of `setInterval` without a cleanup function leads to a memory leak. 

## Problem

The `setInterval` function, when used inside the `useEffect` hook without proper cleanup, continues to run even after the component unmounts. This results in multiple intervals being created, causing a memory leak and potentially performance issues. 

## Solution

The solution involves using the return value of `useEffect` to add a cleanup function. This function clears the interval when the component unmounts or when the dependency array changes, preventing the memory leak.