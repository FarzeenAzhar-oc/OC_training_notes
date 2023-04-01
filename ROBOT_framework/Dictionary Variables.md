#command 
- key value pair
- Assign `&{search_text}  abc=books  bcd=travel`
- Access `${search_text.abc}`
- Utility is in defining a different test enviroment
- You can use a combination of dictionary and scalar varaibles to make the codes more reusable
- You can define the scalar variable in command line 
	- `robot -d results -v var_name:value robotFile`