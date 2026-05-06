---
title: "Feature #10: Full report in a txt file"
description: "Define and implement a function called `stat_report` to write in a text file the result of:"
Milestone: 2
Issue: 10
---

## Feature description

Define and implement a function called `stat_report` to write in a text file the result of:

- max_pixel
- min_pixel
- max_component R
- max_component G
- max_component B
- min_component R
- min_component G
- min_component B

Parameters|value
-|-
name | stat_report
Command | `-c stat_report`
Input  | an image 
output | a text file

## Usage

```bash
freud.exe -f ./images/input/image.jpeg -c stat_report
```
## Output

A text file is created at the root of the project.
Skip a line between each function result.

## Describe tips for implementing feature

Use the function `read_image_data` from `estia-image` and functions implemented previously.
