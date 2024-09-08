---
layout: post
<<<<<<< HEAD
title: The Encyclopedia Agatha
subtitle: Technical Details
categories: Rust
=======
title:The Encyclopedia Agatha
subtitle: Technical Details
categories: Rust 
>>>>>>> 56bff036ada51b9cfff7eb96d28a439d3b23e883
---

# Features

_Checking off all the boxes quantitatively defines the end result as a completed
proof of concept. The Project officially graduates to a budding Minimum
Viable Product._

## Proof of concept

- [ ] A user can download The Encyclopedia `Agatha` from GitHub
- [ ] The user creates a new `Volume` in The Encyclopedia `Agatha`
- [ ] The user can write a `Message`in the`Volume` by typing in the UI with their keyboard
- [ ] The tool generates ... seeded by the `Message`:
  - [ ] `phenotype-(date-machine-time).jpg` (400x400) (Favicon)
  - [ ] `plasmid(date-machine-time)-visualization.jpg` (looks like [Minecraft circles](https://donatstudios.com/PixelCircleGenerator))
- [ ] Color according to `plasmid(date-machine-time)-visualization.jpg` ...
- [ ] Spawn `eBug-blank-template`
- [ ] Apply the `Phenotype` to the `eBug-blank-template`
- [ ] Remove `Background` from `eBug-blank-template`
- [ ] Generate the `PlasmidVisualization` based on the `Message`
  - [ ] Choose a color pallet
  - [ ] Pull pre-defined gene names from a pool :.: it's simple
  - [ ] Define simple coloring rule
  - [ ] Put each pixel of the circle in a 2D buffer
  - [ ] Write each pixel (R, G, B, Alpha) according to pixel coordinate
  - [ ] Put each pixel of a rectangle area holding the `eBug` into a fixed size 2D buffer
  - [ ] Write each pixel (R, G, B, Alpha) according to pixel coordinates
- [ ] Spawn an `eBugPortrait-template`
- [ ] Appy the modified `eBug-blank-template` to the `eBugPortrait-template`
  - [ ] Center the `eBug-blank-template` in the `viewport` of the `eBugPortrait-template`
  - [ ] Center the `PlasmidVisualization` in the `viewport` of the `eBugPortrait-template`
- [ ] Generate `eBugPortrait-(date-machine-time).jpg` (400x400)
- [ ] Generate an HTML page
- [ ] Add the completed `eBugPortrait-(data-machine-time).jpg` to the html page as a copy-pasteable image
- [ ] Add the completed `eBug-blank-tempate.jpg` to the html page as a copy-pasteable image
- [ ] Add the `PlasmidVisualization.jpg` to the html page as a copy-pasteable image

## Minimum Viable Product

_Checking off all the boxes quantitatively defines the end result as a completed
Minimum Viable Product. The project officially graduates to the Stretch Goal Phase._

- [ ] Measure application speed
- [ ] Optimize the coloring algorithm
- [ ] Define simple rules for gene naming
- [ ] A user visits a website hosting the web tool
- [ ] The user can create multiple `Volume`s per account (Melvor style)
  - [ ] Generate the `Plasmid` using (PlasCAD)[https://github.com/David-OConnor/plascad]
- [ ] The user can save their `Volume` as a `.txt` file to their machine
- [ ] The tool generates `.ico` files of the images
- [ ] User authentication

## Stretch

_["Everything's coming up Millhouse!"](https://elliotsmaker.space/2024-09-08-agatha/)_

- [ ] Officially supported "Professor Oak Challenge" game mode
- [ ] Solo Campaign
