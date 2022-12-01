# Reconfiguration Dataset

## Fileformat ALB

The reconfiguration dataset is extended from the description of the ".ALB" file format ".ALB" by Armin Scholl, Christian Becker (FSU Jena) and Nils Boysen, Malte Fliedner (University of Hamburg).
It extends the data by adding `<investment costs>, <task types>, <line depot>, <processing costs>` and `<saving costs>` for the reconfiguration.

Each block of information is preceded by a `<keyword>`-tag, tags and descriptions are listed below:

| Tag                      | Description                                                                                                                                   |
| :----------------------- | :-------------------------------------------------------------------------------------------------------------------------------------------- |
| `<number of tasks>`      | Number of tasks in the instance, `n`                                                                                                          |
| `<number of equipment>`  | Number of equipment in the instance, `r`                                                                                                      |
| `<cycle time>`           | Cycle time in `s`                                                                                                                             |
| `<investment costs>`     | Investment costs per equipment `j`, e.g. `E1, 1000$`                                                                                          |
| `<task times>`           | Task times as `n x r`, starting with the task index. Next comes task time `t_ij` for every equipment `j`, e.g. `t1, t_1E1, t_1E2, t_1E3, ...` |
| `<precedence relations>` | Precedence relations as `predecessor, successor`.                                                                                             |
| `<task types>`           | Task type, where `{separation = 1, handling = 2, joining = 3}`. First the task number `i`, then the task type, e.g. `t1, separation`.         |
| `<line depot>`           | Number of available equipment `j`, e.g. `E1, 0 available`, `E2, 1 available`.                                                                 |
| `<processing costs>`     | Processing costs per equipment `j`, e.g. `E1, 1000$`.                                                                                         |
| `<saving costs>`         | Saving costs per equipment `j`, e.g. `E1, 1000$`.                                                                                             |
| `<end>`                  | End of file tag.                                                                                                                              |

For further information we refer to: 