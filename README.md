# AoH0a

# Import Anvil dependencies
import anvil.server
import anvil.http

# Import Anvil design components
from anvil import *
import anvil.tables as tables
import anvil.tables.query as q
from anvil.tables import app_tables

# Create the app object
anvil.server.connect("<YOUR ANVIL APP KEY>")
app = anvil.server.get_app()

# Define the form class
class Form1(Form1Template):
  
  # Define the event handler for the 'calculate' button
  def calculate_button_click(self, **event_args):
    # Get the values of the two input fields
    num1 = self.number_1.text
    num2 = self.number_2.text
    
    # Perform addition, subtraction, multiplication, and division
    add = float(num1) + float(num2)
    sub = float(num1) - float(num2)
    mul = float(num1) * float(num2)
    div = float(num1) / float(num2)
    
    # Output the results to the labels on the form
    self.addition_label.text = "Addition: " + str(add)
    self.subtraction_label.text = "Subtraction: " + str(sub)
    self.multiplication_label.text = "Multiplication: " + str(mul)
    self.division_label.text = "Division: " + str(div)

# Start the app
if __name__ == '__main__':
  app.run()
