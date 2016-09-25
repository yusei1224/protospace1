# Table

* prototypes
* users
* images
* comments
* likes



## prototypes

### column

* name :string
* concept :text
* catch_copy :text
* likes_num :integer
* comment_num :integer
* user_id :integer


### association

* has_many :images
* has_many :comments
* has_many :likes
* belongs_to :user



## users

### column

* name :string
* works :text
* profile :text
* avatar :text
* email :string
* password :string
* member :string

### association

* has_many :prototypes
* has_many :comments
* has_many :likes


## images

### column

* prototype_id :integer
* proto_image :text
* status :integer-enum%i(main sub)

### association

* belongs_to :prototype


## comments

### column

* comment :text
* user_id :integer
* prototype_id :integer

### associtation

* belongs_to :prototype
* belongs_to :user


## likes

### column

* user_id :integer
* prototype_id :integer

### association

* belongs_to :prototype
* belongs_to :user


