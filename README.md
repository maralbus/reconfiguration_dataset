# Reconfiguration Dataset

## Fileformat

The reconfiguration dataset is extended from the description of the ".ALB" file format ".ALB" by Armin Scholl, Christian Becker (FSU Jena), Nils Boysen, and Malte Fliedner (University of Hamburg).
It extends the data by adding `<investment costs>, <task types>, <line depot>, <processing costs>`, and `<saving costs>` for the reconfiguration.

Each block of information is preceded by a `<keyword>`-tag. Tags and descriptions are listed below:

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

The data is structured based on the equipment alternatives `r={5, 10, 15, 20}` and named `instance_n=20_${instance number}_r=${equipment}.alb`.

For further information, we refer to the paper [Resource reconfiguration and optimization in brownfield constrained Robotic Assembly Line Balancing Problems](https://www.sciencedirect.com/science/article/pii/S0278612523000018).


## License

This work is licensed under a [Creative Commons Attribution 4.0 International](https://creativecommons.org/licenses/by/4.0/) license.

```yaml
SPDX-License-Identifier: CC-BY-4.0
```

## Reference

```bibtex
@article{ALBUS2023132,
    title = {Resource reconfiguration and optimization in brownfield constrained Robotic Assembly Line Balancing Problems},
    journal = {Journal of Manufacturing Systems},
    volume = {67},
    pages = {132-142},
    year = {2023},
    issn = {0278-6125},
    doi = {https://doi.org/10.1016/j.jmsy.2023.01.001},
    url = {https://www.sciencedirect.com/science/article/pii/S0278612523000018},
    author = {Marcel Albus and Marco F. Huber},
    keywords = {Reconfiguration, Assembly line balancing, Production},
}
```