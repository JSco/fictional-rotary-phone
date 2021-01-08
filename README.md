# View Demo

Demonstration of views in ServiceNow

Things demo:
- Create a View Rule that forces Child Demo form to only use the Default View
- Add a Related List of Child Demo records to the Alpha Demo view
- Test what happens when the Child Demo view is set to Default view and navigate via the Parent field on the form to the Parent Demo record that has a mandatory field in the Default view
- Create a view named Alpha Demo for the Child Demo form and see that it uses the same view as Parent Demo
- Change the View Rule for Child Demo to an invalid View (eg "Alpha Demo") and see which view loads. Then try editing the form layout and answering yes to create the view and get stuck in an infinite loop that creates Form Section records with view set to "null"
  - Go to Form Sections and look for form sections that have been created for the Child Demo table that have view *null*
- Add a form section to the Alpha Demo view for Child Demo
- Review how the form view is captured in an update set as a single update set record even though there are multiple records associated with the form section
  - Review how multiple form sections are captured as multiple records in an update set
- Review how List Views work
  - The List View will show the most recent view selected from the Form View. If that view does not exist, then the Default View will be displayed, but the View label will show the view name from the Form View instead.
- Views created in a Scope will belong to that Scope, but when in another Scoped Application and you use the same View name as a view in another Scoped Application, what happens? Is a new view created in that Scope? What happens to the view if the original Scoped Application is removed?
