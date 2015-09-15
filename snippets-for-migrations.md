Type the word -> press tab. 

The numbers you see in ${} are the locations where the next tab will jump right to 
if you press it again and again depending on the highest number.

##Migrations: 
================================
	Data Scheme Builder
	select the two functions up and down and replace with 
	typing 'scheme' 
		output:
		public function up()
		{
			Schema::create( '${1}' , function (Blueprint \$table)
			{
				\$table->increments('id');
				\$table->${2};
			});
		}

		public function down()
		{
			Schema::drop( '${1}' );
		}
================================
	Pivot Scheme Builder
	select the two functions up and down and replace with 
	typing 'pivotscheme' 
		output:
		public function up()
	    {
	        Schema::create( '${1}_${2}' , function (Blueprint \$table)
	        {
	            \$table->integer('${1}_id')->unsigned();
	            \$table->integer('${2}_id')->unsigned();

	            \$table->foreign('${1}_id')
	            ->references('id')
	            ->on('${1}s')
	            ->onDelete('cascade');

	            \$table->foreign('${2}_id')
	            ->references('id')
	            ->on('${2}s')
	            ->onDelete('cascade');

	            \$table->primary([ '${1}_id' , '${2}_id' ]);
	        });
	    }
	    
	    public function down()
	    {
	        Schema::drop( '${1}_${2}' );
	    }