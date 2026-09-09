# PROJECT TITLE
An interactive sound installation in which three participants manipulate suspended public-transport handrails to produce independent real-time sound.

## Short Description
An interactive sound installation in which three participants manipulate suspended public-transport handrails to produce independent real-time sound.

## Concept / Intent
This project explores how individual bodily actions can coexist within a temporary shared space without requiring collaboration.

The installation consists of three suspended public-transport handrails. Each participant can independently grip and pull one handle, producing an individual sound response. One, two or three people can interact with the work at the same time.

Public-transport handrails are used as a familiar spatial reference to a shared public environment rather than as a literal reconstruction of a bus. The project developed from an earlier interest in how environmental forces are registered through the body, and gradually shifted towards how multiple bodies, objects and sounds can become perceptible to one another within a shared system.


## Technology Used
### Hardware
- Bela board
- 3 resistive stretch sensors / stretch-based sensing elements
- Voltage-divider circuits
- 3 public-transport handrails
- Soldered prototyping board
- Speakers
- Wooden wall-mounted structure
- Mechanical limiters
- Heat-shrink tubing and wiring

### Software
- Pure Data
- Bela IDE

Each handrail is connected to a separate analogue input on Bela:

- Handle 1 → `adc~ 3`
- Handle 2 → `adc~ 4`
- Handle 3 → `adc~ 5`

In Pure Data, each sensor signal is smoothed, mapped and compared with an individually calibrated threshold. Each channel controls its own sine-wave oscillator before the three voices are mixed to the stereo audio output.

Basic signal flow:

Participant  
↓  
Grip / pull  
↓  
Stretch sensor  
↓  
Voltage divider  
↓  
Bela analogue input  
↓  
Pure Data  
↓  
Signal smoothing + threshold / frequency mapping  
↓  
Oscillator  
↓  
Audio output


## How to Run / Install
1. Connect the three sensor circuits to Bela analogue inputs 3, 4 and 5.
2. Connect Bela audio output to the speakers.
3. Power the Bela board.
4. Open the Bela IDE.
5. Upload/open the project containing the final Pure Data patch.
6. Run the Bela project.
7. Pull each handle individually and confirm that all three channels respond correctly.
8. Before exhibition, check the sensor thresholds and recalibrate if necessary.

Current approximate thresholds used in the final patch:

- Handle 1: `0.437`
- Handle 2: `0.395`
- Handle 3: `0.430`

These values are specific to the physical sensors used in the final installation and may need to be adjusted if the sensors or mounting tension change.

## Requirements
- Bela board
- Three analogue stretch-sensor circuits
- Stereo speaker / audio output system
- 5V power supply for Bela

- Bela
- Pure Data

The final installation is designed to run as a standalone Bela system after the project has been uploaded.

## Screenshots / Media
![alt text](<Installation -Final.png>)

## Credits / Acknowledgements
Byrne, D. (2008) Playing the Building [interactive sound installation]. Battery Maritime Building, New York: Creative Time. Available at: https://creativetime.org/projects/playing-the-building/ (Accessed: 9 September 2026).

Goffman, E. (1963) Behavior in public places : notes on the social organization of gatherings. New York: Free Press.

Hall, E.T. (1969) The hidden dimension. Garden City, N.Y: Doubleday.

Ingold, T. (2016) Lines A Brief History. 1st edition. London: Routledge

LaBelle, B. (2010) Acoustic Territories: Sound Culture and Everyday Life. New York: Continuum.

Li, Z. Rocking Pipe Organ. UAL Graduate Showcase. https://ualshowcase.arts.ac.uk/project/714864/cover

Martinez Avila, J., Hazzard, A., Greenhalgh, C., Benford, S. and McPherson, A. (2023) ‘The Stretchy Strap: supporting encumbered interaction with guitars’, Journal of New Music Research, 52(1), pp. 19–40. doi:10.1080/09298215.2023.2274832.



## License
MIT License.
This project is created for artistic and educational purposes. 

## Contact / Links
 https://vimeo.com/1225209958?share=copy&fl=sv&fe=ci