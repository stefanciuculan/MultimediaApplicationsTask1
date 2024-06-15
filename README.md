# Requirements
Sure, here is the translation of the requirements into English:

---

### On the client side:

1. **Define and run a graphical interface with 3 buttons, located at the top of the window (in a row) [1 point]:**
   - The first button reads a CSV file from the disk. The CSV file must be previously created, either manually or obtained from an online source (in which case the source must be specified). It should contain at least 3 columns, the first column being a description of the record, and the other columns containing numerical data that can be correlated (there is a relationship between them). [1 point]
   - An example of such a file could be "The evolution of the Gross Domestic Product of Eastern European countries from 2010 to 2020."

   - The second button generates a graph with the data from the previously read CSV file (if the first button has not been pressed, then a message should be displayed, and the CSV file should be read at this point) and displays it in the application, in the area below the buttons. [1 point]
   - Attention: the generated graph must make sense for your data, and there can be multiple such graphs. Keeping the example above, a figure can be generated with the horizontal axis representing the years and the vertical axis representing the GDP values, creating a graph for each country represented in the file. Another possible variation is summing the GDPs of a year for all recorded countries and plotting the relationship of this sum relative to the years.

   - The third button generates a DOCX file based on the initial CSV file. It will contain a title, an explanatory paragraph referring to the CSV file, along with the entered data in tabular form and the generated image. If the first two buttons have not been pressed, this will be signaled, and the CSV file will be read, and the graph will be generated. The resulting DOCX document will be sent to the server. [2 points]
   - For transmitting documents or information whose size is not known beforehand, a mechanism can be used to send and receive a fixed number of bytes (buffer size) as long as there are data to be sent.

### On the server side:

2. **Read the contents of the DOCX file received from the client [1 point]:**
   - Create and write a PDF file containing all the information from the DOCX, except for the table (with the data from the initial CSV). [2 points]
   - Based on the table data, generate a representative XML file, whose structure should be relevant to the table's information. [2 points]
   - Attention: there is not just one possible configuration, but it must make sense in the context of the respective data.

   - The corresponding client files (CSV, generated DOCX), and server files (received DOCX, XML) will be kept in separate directories (named `client_files` and `server_files` respectively).

---
