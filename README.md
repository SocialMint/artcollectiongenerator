# Social Mint NFT Art Generator

## Introduction

Social Mint NFT Art Generator is a free application used to generate NFT art collections from an input of base image layers. Complete with configurable layer rarity and metadata generation. Ready to upload and mint to the Ethereum, and Biannce blockchains!

## Downloads

[Windows English](https://github.com/socialmint/artcollectiongenerator/releases/download/v1.0.0/social-mint-English.exe)

[Windows Spanish](https://github.com/socialmint/artcollectiongenerator/releases/download/v1.0.2/social-mint-Spanish.exe)

[Mac English](https://github.com/socialmint/artcollectiongenerator/releases/download/v1.0.3/MAC.Social.Mint.English.dmg)

[Mac Spanish](https://github.com/socialmint/artcollectiongenerator/releases/download/v1.0.4/MAC.Social.Mint.Spanish.dmg)

[LINUX English](https://github.com/socialmint/artcollectiongenerator/releases/download/v.1.0.5/LINUX.Social.Mint.English.AppImage)

[LINUX Spanish](https://github.com/socialmint/artcollectiongenerator/releases/download/v1.0.4/LINUX.Social.Mint.Spanish.AppImage)

## Usage Quick Start

1. Run the Nft Art Generator executable
2. LOGIN IN by submitting Name and Email address
3. Click the "Load Input Folder" Button
4. Select the folder which contains your NFT image layer folders (Output images are saved in a folder at the same level e.g. if input folder is in Desktop, the output folder will also be placed there)
5. Adjust the layer ordering by dragging the layers to position
6. Adjust the individual layer percentage probabilities
7. Adjust the rarity folder percentage probabilities - **must add up to 100**
8. Test that image creation is as expected by clicking the "Random" button
9. Set the number of Nfts to generate
10. Select the blockchain to generate metadata for
11. **Optional** - Set "Art Base Name" NFT Image prefix (This only sets the image metadata name)
12. Click Generate
13. ???
14. Profit

## How to video guide
[![Video guide](https://img.youtube.com/vi/mXuUX2EQlJQ/0.jpg)](https://www.youtube.com/watch?v=mXuUX2EQlJQ)

## Concepts
### Layer
Image artwork is composed of many layers stacked on each other. Layers can have a percentage probability assigned.

### Rarity Folder
Layers contain a common, fixed number of rarity folders. Each rarity folder defines a configurable "probability bucket" in which layer items can be placed.

### Item
An item is an individual piece of artwork which belongs to a layer, items layered on top of other items make up the image.

### Image creation process
Each image goes through the following process in order to be created:

For each layer, a random roll is made to determine selection.

For each _selected_ layer, another random roll is made to select which rarity folder is selected.

Each rarity folder has a random image selected from it, if no images exist, nothing is selected for the layer.

If the end image has already been generated, repeat the whole process until a unique image is generated.
Metadata is created for this created image.


## Requirements
The application assumes these to be true in order for it to function correctly.

### Folder Structure
The input folder should be structured as follows:

Input Folder > Layers > Rarity Folders > Items

Rarity Folders need to be the same across all the layers

#### Example Folder Structure

```
📦Input Folder
┣ 📂Accessory
┃ ┣ 📂common
┃ ┣ 📂legendary
┃ ┗ 📂rare
┃ ┗ 📂super_rare
📂Background
┃ ┣ 📂common
┃ ┣ 📂legendary
┃ ┗ 📂rare
┃ ┗ 📂super_rare
📂Eyes
┃ ┣ 📂common
┃ ┣ 📂legendary
┃ ┗ 📂rare
┃ ┗ 📂super_rare
📂Face
┃ ┣ 📂common
┃ ┣ 📂legendary
┃ ┗ 📂rare
┃ ┗ 📂super_rare
📂Hands
┃ ┣ 📂common
┃ ┣ 📂legendary
┃ ┗ 📂rare
┃ ┗ 📂super_rare
📂Mouth
┃ ┣ 📂common
┃ ┣ 📂legendary
┃ ┗ 📂rare
┃ ┗ 📂super_rare

###  Layer Names
Individual words in a layers name must be separated by an underscore in order for the matching metadata to be generated correctly.
###  Item Names
Individual words in an items name must be separated by an underscore in order for the matching metadata to be generated correctly.
###  Image Dimensions
Images need to have the same width and height, so that the position of the image item is correct relative to the other layered image items.

##  FAQ's
Ask away

## For Developers

### Introduction

### Getting Started

Clone this repository locally:

> git clone https://github.com/SocialMint/artcollectiongenerator.git

Install dependencies with npm (used by Electron renderer process):
> cd NFT-Art-Generator/
> 
> npm install

There is an issue with yarn and node_modules when the application is built by the packager. Please use npm as dependencies manager.

If you want to generate Angular components with Angular-cli , you MUST install @angular/cli in npm global context. Please follow Angular-cli documentation if you had installed a previous version of angular-cli.

> npm install -g @angular/cli

Install NodeJS dependencies with npm (used by Electron main process):

> cd app/
> 
> npm install

### Creating a build
To create the build/executable, install the above dependencies, then navigate to the main directory and run:

> npm run electron:build


