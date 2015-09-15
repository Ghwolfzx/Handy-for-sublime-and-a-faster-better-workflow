Type the word -> press tab. 

The numbers you see in ${} are the locations where the next tab will jump right to 
if you press it again and again depending on the highest number.

##Routes: 
================================
	Named route
	type 'nroute' 
		output:
		Route::${1}('${2}', ['as' => '${3}', 'uses' => '${4}Controller@${5}']);

================================
	Pivot Scheme Builder
	type 'nrg' 
		output:
		Route::group(['middleware' => '${1}', 'as' => '${2}'], function () {

			${3}

		});