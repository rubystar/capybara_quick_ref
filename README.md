capybara_quick_ref
==================
#### Visiting pages
```ruby
  visit "/posts"
```
#### Current path
```ruby
  current_path.should == "/login"
```
#### Buttons and Links
```ruby
  click_link("Ads")    # Name or id of the link
  click_button("Save") # Name or id of the button
  click_on("some")     # Either link or button
```
#### Form elements
```ruby
  fill_in("Name", :with => "DHH")           # Name or id of the field  # Text field
  select("Male", :from => "gender_id")      # Normal Select, Use id of the field
  select2_select("Male", "gender_id_input") # Select2 select, _input is necessory
  select2_ajax("publisher name", :from => "#publisher_id") #id of the field
  check('A Checkbox')                       # Checkbox, use id or name
  choose('Male')                            # Name or id of the Radio Button
```
#### Auto complete
```ruby
fill_in_autocomplete("#advertiser_id", "adver")
choose_autocomplete("advertiser")
```
#### Page expectations
```ruby
  expect(page).to have_content("Awesome Post")                 # expecting text  
  expect(page).to have_link("Edit Post")                       # expecting link
  expect(page).to have_css(".acitve")                          # expecting css
  expect(page).to have_select('Company', :options => ['RMM'])  # expecting select field with options
  expect(page).to have_field('name', with: "siva")             # expecting text field with some value
```

####Check alert messages
```ruby
  page.driver.alert_messages.should == ["Alert Message."]
```
#### Other
```ruby
find("#sites_more_actions").trigger(:mouseover)
```

...test..
