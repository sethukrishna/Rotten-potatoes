# Rotten-potatoes

    1  git clone https://bitbucket.org/santony/movies_app.git
    2  cd movies_app/
    6  bundle
   12  rake db:migrate
   13  rails s -b $IP -p $PORT
   
   
 Navigate to layouts and add a <p> tag with your name
 
 then 
 
for row number:
  - @movies.each_with_index do |movie, index|
      %tr
        %td= index

For that pink one:
<style> tr:hover {background-color: pink;}</style>

for sorting title:
@movies = @movies.order('title')

for button 
= button_to 'Edit info', edit_movie_path(@movie), :method => :get

for cancel
  = button_to 'Cancel', movies_path, :method => :get
  
for description:


in index
%td= movie.description


in new
= label :movie, :description, 'Description'
  = text_field :movie, :description
  
in edit
= label :movie, :description, 'Description'
  = text_field :movie, :description
  
  
in controller
def movie_params
    params.require(:movie).permit(:rating, :release_date, :title, :description)
  end






        
        
 
