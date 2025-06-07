# U-Shapez2-Components

The project is a component library for [Shapez2](https://store.steampowered.com/app/2162800/2/ 'Steam').

This component library **is not** designed to minimize the number of platforms, the number of buildings, and the footprint. Because the blind pursuit of small size will lead to confusion and asymmetry of wiring, and it is not conducive to intuitive display of its working mode and content, which is not what I want to see.

Admittedly, without extreme compression, the number of platforms used in games would increase. So I think the balance between perfect wiring and extreme compression is my ultimate goal.

## Naming Notations

Each component has a name like 'U-Do-Something'

They start with U, words are hyphenated, and the first letter of each word is always capitalized

I attempted to make the naming of the components follow the rule of first describing the category and then the details.

Such as:

+ `U-Half-Destoryer` rename to `U-Destoryer-Half`
+ `U-Diagonal-Cutter` rename to `U-Cutter-Diagonal`

For the plantform version, the name is prefixed with 'UA-'. They always include foundations in the blueprint

We are trying to orient each component towards the north and label them with their names. If there are any differences, please kindly inform us in time.

## Design Criterions

1. If the pipeline can be stacked vertically without side effects, then stack it (in most scenarios, it will take up the 1x1 space).

     - U-Rotator
     - U-Pin Pusher
     - ...

2. If criterion 1 cannot be met, then the 3x4 pipeline is spread out horizontally for processing (it also usually takes up a maximum of 1x3 space).

     - U-Stacker
     - U-Diagonal-Cutter
     - ...

3. If the component has more than one output(3x12 pipeline), then place the two outputs on opposite sides of the input.

     - U-Cutter
     - U-Diagonal-Cutter
     - ...

4. The main input and output are generally located on the long side.

     - U-Stacker
     - U-Painter

5. If there is more than one main input, arrange them on ends of the input side.

     - U-Mosaic

6. The auxiliary material input is generally located on the side next to the main input side.

     - U-Stacker
     - U-Painter

7. If there are more than one auxiliary input, place the second auxiliary input next to the main input near the first auxiliary input.

     - U-Crystal-Generator

8. Shape and Fluid miners are usually in groups of 3, that is, there are 3 Shape(Fluid) miners and 9 Shape(Fluid) Miner extensions. They each output the product to 3 layers.

     - U-Shape-Miner
     - U-Fluid-Miner

9. Each component does not contain platforms, which allows you to combine components freely in use (for example, 2 1x3 components on a 2x3 platform).

10. Each component's input does not contain catcher, and its output does not contain launcher. Instead, we put the 3x4 fluid and shape catcher and launcher separately.

     - U-In-Fluid
     - U-In-Shape
     - U-Out-Fluid
     - U-Out-Shape
     - U-Connector-Shape

## License

The project is under the [MulanPSL-2.0](./LICENSE).
