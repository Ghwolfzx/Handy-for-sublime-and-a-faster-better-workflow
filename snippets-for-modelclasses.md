Type the word -> press tab. 

The numbers you see in ${} are the locations where the next tab will jump right to 
if you press it again and again depending on the highest number.

##for Model classes: 
================================
	Model Boilerplate
	type 'bomo' 

	output:
		//variables

		    protected $table = '${1}s';

		    protected $fillable = [${2}];

		    protected $hidden = [];

		    protected $with = [${3}];

		// relations

		    // one ${1} on one

		    // one ${1} to many

		    // many ${1}s to one

		    // many trough

		    // many to many

		    // polymorphic

		    // many to many polymorphic 

		// functions

		// getters

		// setters

================================
================================
	One to one
	type 'one-one' 
	    output:
	    public function ${1}()
	    {
	    	return $this->belongsToOne( ${1/(^|\.\s)([a-z])/\1\u\2/g}::class );
	    }
================================
	One to Many
	type 'one-many' 
		output:
		public function ${1}s()
		{
			return $this->hasMany( ${1/(^|\.\s)([a-z])/\1\u\2/g}::class );
		}
================================
	Many to One
	type 'many-one' 
		output:
		public function ${1}()
		{
			return $this->belongsTo( ${1/(^|\.\s)([a-z])/\1\u\2/g}::class );
		}
================================
	Many Through
	type 'many-through' 
		output:
		public function ${1}()
		{
			return $this->hasManyThrough( ${1/(^|\.\s)([a-z])/\1\u\2/g}::class , ${2}::class );
		}
================================
	Many to Many
	type 'many-many' 
		output:
		public function ${1}s()
		{
			return $this->belongsToMany( ${1/(^|\.\s)([a-z])/\1\u\2/g}::class );
		}
================================
	Polymorphic
	type 'poly' 
		output:
		public function ${1}s()
		{
			return $this->morphMany( ${1/(^|\.\s)([a-z])/\1\u\2/g}::class , '${2}ble' );
		}
================================
	Many To Many Polymorphic
	type 'poly-many' 
		output:
	    public function ${1}s()
	    {
	        return $this->morphToMany( ${1/(^|\.\s)([a-z])/\1\u\2/g}::class , '${2}ble');
	    }
================================
	If this is the class to morph to
	type 'morphclass' 
		output:
	    public function ${1}ble()
	    {
	        return $this->morphTo();
	    }
================================
	If this is the class to morph to with Many
	type 'morphmanylass' 
		output:
	    public function ${1}s()
	    {
	        return $this->morphedByMany( ${1/(.*?)(\..+)/\u$1/}::class , '${3}ble' );
	    }
================================
================================
	type 'getAtt' 
		output:
	    public function get${1/(.*?)(\..+)/\u$1/}Attribute(${2})
	    {
	        return $this->attributes['${1}'] = ${3};
	    }
================================
	type 'setAtt' 
		output:
	    public function set${1/(.*?)(\..+)/\u$1/}Attribute(${2})
	    {
	        return $this->attributes['${1}'] = ${3};
	    }
================================
