# View Demo

Demonstration of views in ServiceNow

Things to do:
- Create a View Rule that forces Child Demo form to only use the Default View
- Add a Related List of Child Demo records to the Alpha Demo view
- Test what happens when the Child Demo view is set to Default view and navigate via the Parent field on the form to the Parent Demo record that has a mandatory field in the Default view
- Create a view named Alpha Demo for the Child Demo form and see that it uses the same view as Parent Demo
- Change the View Rule for Child Demo to an invalid View (eg "Alpha Demo") and see which view loads. Then try editing the form layout and answering yes to create the view and get stuck in an infinite loop that creates Form Section records with view set to "null"
- Investigate how the form view is captured in an update set as a single update set record even though there are multiple records associated with the form section
- Add a form section to the Alpha Demo view for Child Demo, then delete the main Form Section to see how the form behaves
