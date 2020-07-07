GENERATING THE RESULTS

1 - Install ProVerif 2.00. Please refer to the guidelines provided in the tool's official manual:

      https://prosecco.gforge.inria.fr/personal/bblanche/proverif/manual.pdf

    For Windows users, be sure to perform the steps described in the manual for installing Graphviz and GTK+2.24.
    These two allow ProVerif to generate graphical representations of the traces that it might find.

2 - After installing ProVerif in a folder of your choice, select the protocols that you want to run the formal verification.
    Move their folders to a directory of your choice inside the installation folder of ProVerif.

3 - In a terminal window (e.g., cmd on windows), move to the ProVerif's installation directory, for example:

      cd [YOURPATH]\proverif2.00

    In my case, I decided to separate the protocols in a subfolder on the root, called 'protocols-wsn'.
    Inside it, each protocol has its folder containing a .pv file describing the protocol's model and a .css file for formatting purposes.
    Running the formal verification would look something like this for each protocol:

      proverif -html ./protocols-wsn/tpbc ./protocols-wsn/tpbc/tinypbc.pv

      proverif -html ./protocols-wsn/najmussaqib ./protocols-wsn/najmussaqib/najmussaqib.pv

      proverif -html ./protocols-wsn/herrerahu ./protocols-wsn/herrerahu/herrerahu.pv

4 - After ProVerif finishes executing, several files will be generated in the specified folder.
    In order to visualize the results, open the index.html using any internet browser.
