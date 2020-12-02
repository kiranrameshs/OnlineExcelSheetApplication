

#### Spreadsheet Application like Google/Excel Sheet using Javascript, RxJS, and SCSS

  - Add/Delete Rows and Columns 
  - Select multiple rows or columns and display their sum in a cell by using a formula. 
  - The formula should be of the format "=SUM(START_CELL:END_CELL)"
  - Formula can also be of the format =A1+A2 
  - Handle algebraic operations (+, -, *, /) using BODMAS rule
  - Export sheet as a CSV
  - Import CSV as a sheet
  - Formula Bar to display the formula and the current value of the selected cell 

#### Approach!
  - Use an Array of n*m to handle the table contents
  - Use Objects with attributes such as display Value, formula and observables
  - Link these objs to the array so as to access the objs using array access methods
  - Add/Update/Delete operations first updates the array. Table is just a visualizing tool representing array data
  - Add ID attribute to the cells just as Excel sheet representing their Column and Row header  
  - ID is of the format A1...A10, B1...B10 where A, B are column headers and digits are row header values
  - ID is used to get the cell values from the view to the array after processing the input
  - Use RxJS, observables to manage the formula and update the result when there is an update to cells involved in the formula
  

#### Installation
1. Clone the repository `git clone
2. Navigate to project directory.
3. Run `npm install`.
4. Install Chrome/Firefox to view the running application
5. Install visual StudioCode/ IntelliJ to view to source Code.



#### Run
1. npm run sass (builds the CSS file from the SCSS using node-sass in the dist folder as main.css)
2. Open the index.html file in the browser (through VS code extensions/manually)


#### Test Cases
The formula should be of the format "=SUM(START_CELL:END_CELL)". Example "=SUM(A1:A10)"
Cells involved in the folmula can be of the below types and to be handled:
  - NaN
  - Empty Cell
  - Number
  - !ERR
  - Group SUM
  - Algebraic OP
  - boundary check

 Other cases:
  - Divisible by 0
  - Cross reference
  - Cross row/column SUm computation = !ERR
  - Starts or end with spl char
