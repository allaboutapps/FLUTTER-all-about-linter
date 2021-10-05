# all_about_linter

## Install

Add `all_about_linter` as dependency to your `pubspec.yaml`
```yaml
dependencies:
  all_about_linter:
   git:
     url: https://git.allaboutapps.at/scm/flutter/all-about-linter.git
```

Create a `analysis_options.yaml` file in the root of your project and import the `all_about_linter` rules:

```yaml
# single quotes
include: package:all_about_linter/analysis_options.yaml
# double quotes
include: package:all_about_linter/analysis_options_double.yaml
```

## Line length

Most of the projects at allaboutapps use the same number of characters in a singe line.
Please specify the number of chars on the top of your `analysis_options.yaml` file and also change the settings of your editor and the dart formatter.

```yaml
# 120
include: package:all_about_linter/analysis_options_double.yaml
```

## Enable/Disable rules

`all_about_linter` is customizable, you can add or remove rules, depending on your needs. 
To do so adjust your `analysis_options.yaml`.

```yaml
include: package:all_about_linter/analysis_options.yaml

linter:
  rules:
    # ------ Disable individual rules ----- #
    #                 ---                   #
    # Turn off what you don't like.         #
    # ------------------------------------- #

    # Use parameter order as in json response
    always_put_required_named_parameters_first: false
    
    # Util classes are awesome!
    avoid_classes_with_only_static_members: false


    # ------ Enable individual rules ------ #
    #                 ---                   #
    # These rules here are good but too     #
    # opinionated to enable them by default #
    # ------------------------------------- #

    # Make constructors the first thing in every class
    sort_constructors_first: true

    # The new tabs vs. spaces. Choose wisely
    prefer_single_quotes: true
    prefer_double_quotes: true

    # Good packages document everything
    public_member_api_docs: true
    
    # Blindly follow the Flutter code style, which prefers types everywhere
    always_specify_types: true
  
    # Back to the 80s
    lines_longer_than_80_chars: true
```