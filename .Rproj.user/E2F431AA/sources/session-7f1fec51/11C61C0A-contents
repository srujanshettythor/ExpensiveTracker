library(shiny)

# Define UI for application that calculates monthly expenses and plots them over time
shinyUI(fluidPage(
  
  # Application title
  titlePanel("Monthly Expense Calculator"),
  
  # Sidebar with input fields for different expense categories
  sidebarLayout(
    sidebarPanel(
      selectInput("month", "Select Month:", 
                  choices = month.name, selected = month.name[1]),
      numericInput("rent", "Rent:", value = 0, min = 0, step = 0.01),
      numericInput("utilities", "Utilities:", value = 0, min = 0, step = 0.01),
      numericInput("groceries", "Groceries:", value = 0, min = 0, step = 0.01),
      numericInput("transportation", "Transportation:", value = 0, min = 0, step = 0.01),
      numericInput("entertainment", "Entertainment:", value = 0, min = 0, step = 0.01),
      numericInput("miscellaneous", "Miscellaneous:", value = 0, min = 0, step = 0.01),
      
      # Action buttons to calculate total and to reset data
      actionButton("calculate", "Calculate Total"),
      actionButton("reset", "Reset Data")
    ),
    
    # Show a table of the expenses and the total
    mainPanel(
      tableOutput("expenseTable"),
      h3("Total Monthly Expenses:"),
      textOutput("totalExpenses"),
      h3("Expense Breakdown by Month:"),
      tableOutput("breakdownTable"),
      h3("Total Expenses Over Time:"),
      plotOutput("expensePlot")
    )
  )
))
