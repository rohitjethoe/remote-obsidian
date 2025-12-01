---
tags:
  - CSE1105
title: "Self-Study: Getting Started with OpenJFX"
---
## Table of Contents
****

## Setup OpenJFX
****
- Download the [JavaFX SDK](https://openjfx.io/)
- Unzip the downloaded SDK `.zip` somewhere (e.g. `/path/to/javafx-sdk`)
- Make sure this extracted path contains a `lib` 
- Add VM Arguments to your *Run Configs* for the `client.Main`
	- `-module-path="/path/to-/javafx-sdk-1.2.3/lib" -add-modules=javafx.controls,javafx.fxml,javafx.web`
- Download the [SceneBuilder](https://gluonhq.com/products/scene-builder/) tool
## Create Scene with Button and Counter
****
**Open Template Project**
-  Import the Template Project into your IDE (or download `.zip` from Brightspace)

**Create Basic Scene**
- Open SceneBuilder & create basic scene that contains only `Pane`, `Button` and  `Label`
