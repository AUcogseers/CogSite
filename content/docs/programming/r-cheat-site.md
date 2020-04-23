---
weight: 1
title: "R cheat site"
---

# The ultimate R cheat site

Please contribute additional tasks and solutions.

## Transforming data frames

| Task                 | Package | Function(s)                                                                   | Tutorial |
| :------------------- | :------ | :---------------------------------------------------------------------------- | :------- |
| Wide-to-long         | `tidyr` | `gather()`, `pivot_longer()`                                                  |          |
| Long-to-wide         | `tidyr` | `spread()`, `pivot_wider()`                                                   |          |
| Summarize columns    | `dplyr` | `summarize()`, `count()`                                                      |          |
| Order data frame     | `base`  | `order()`                                                                     |          |
|                      | `dplyr` | `arrange()`                                                                   |          |
| Summarize data frame | `skimr` | `skim()`                                                                      |          |
|                      | `base`  | `str()`                                                                       |          |
| Merge data frames    | `dplyr` | `bind_cols()`, `bind_rows()`, `left_join()`, `right_join()` + other *_join()s |          |
| Select rows          | `base`  | `df[..., ]`                                                                   |          |
|                      | `dplyr` | `filter()`                                                                    |          |
| Select columns       | `base`  | `df[, ...]`                                                                   |          |
|                      | `dplyr` | `select()`                                                                    |          |

## Model functions

| Task                    | Package        | Function(s)         | Tutorial |
| :---------------------- | :------------- | :------------------ | :------- |
| Linear mixed effects    | `lme4`         | `lmer()`, `glmer()` |          |
|                         | `nlme`         | TODO                |          |
| Bayesian modeling       | `brms`         | `brm()`             |          |
| Support-vector machines | `e1071`        | `svm()`             |          |
|                         | `parsnip`      | TODO                |          |
| Naïve Bayes             | `e1071`        | `naiveBayes()`      |          |
|                         | `parsnip`      | TODO                |          |
| Random Forest           | `randomForest` | `randomForest()`    |          |
|                         | `parsnip`      | TODO                |          |
| Neural network          | `keras`        | TODO                |          |
|                         | `tensorflow`   | TODO                |          |
|                         | `nnet`         | TODO                |          |
| GAMLSS                  | `gamlss`       | `gamlss()`          |          |
| LQM(M)                  | `lqmm`         | `lqm()`, `lqmm()`   |          |

## Model evaluation

| Task                    | Package               | Function(s)                                                                                       | Tutorial                                                                                                  |
| :---------------------- | :-------------------- | :------------------------------------------------------------------------------------------------ | :-------------------------------------------------------------------------------------------------------- |
| Evaluate predictions    | `cvms`                | `evaluate()` - regression and classification. Also: ID-level evaluation.                          | [ID evaluation](http://ludvigolsen.dk/cvms/id_evaluations/)                                               |
|                         | `yardstick`           | TODO                                                                                              |                                                                                                           |
| Create confusion matrix | `cvms`                | `evaluate()` or `confusion_matrix()` - see also `plot_confusion_matrix()`                         | [Create confusion matrix](http://ludvigolsen.dk/cvms/create_confusion_matrix/)                            |
|                         | `caret`               | `confusionMatrix()`                                                                               |                                                                                                           |
|                         | `yardstick`           | `conf_mat()`                                                                                      |                                                                                                           |
| Cross-validation        | `cvms` + `groupdata2` | `cross_validate()` for `lm()`/`lmer()`/`glm()`/`glmer()` or `cross_validate_fn()` for most others | [Cross-validate custum model functions](http://ludvigolsen.dk/cvms/cross_validate_custom_model_function/) |
|                         | `caret`               | `trainControl`? TODO                                                                              |                                                                                                           |
|                         | `tidymodels`          | TODO                                                                                              |                                                                                                           |

## Plotting with `ggplot2`

| Task                  | Package     | Function(s)                                     | Tutorial                                                                       |
| :-------------------- | :---------- | :---------------------------------------------- | :----------------------------------------------------------------------------- |
| Combine ggplots       | `patchwork` | TODO (`+/` etc)                                 |                                                                                |
| Add images            | `ggimage`   | `geom_image()`, `geom_bgimage()`, `geom_icon()` |                                                                                |
| Add pokemons          | `ggimage`   | `geom_pokemon()`                                |                                                                                |
| Plot confusion matrix | `cvms`      | `plot_confusion_matrix()`                       | [Create confusion matrix](http://ludvigolsen.dk/cvms/create_confusion_matrix/) |


