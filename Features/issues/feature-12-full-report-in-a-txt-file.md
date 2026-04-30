# Feature #12: Full report in a txt file

- State: open
- Milestone: Milestone 2: Statistics
- Labels: export, statistics
- Assignees: None
- Created: 2022-06-02T13:04:13Z
- Updated: 2022-06-02T13:05:48Z
- URL: https://github.com/Estia-1a/projetGenieInfo_template/issues/12

## Description

**Feature description**
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

**Usage**
```bash
freud.exe -f ./images/input/image.jpeg -c stat_report
```
**Output**
A text file is created at the root of the project.
Skip a line between each function result.

**Describe tips for implementing feature**
Use the function `read_image_data` from `estia-image` and functions implemented previously.
