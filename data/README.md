# Build Personal Blog with Laradock - Laravel
###### What is this Personal Blog about?
The repo will create a sample project with laradock and laravel for learning.
It will build a personal blog website: allow manage post, show author profile and contact form

### Blog features
- Manage blog categories
- Manage blog post
- Manage author information
- Manage contact message
- Config header block information
- Config footer block information


### Database tables
1. blog_category
- category_id: int (11) primary auto increment
- name: varchar (200)
- url_key: varchar (200)
- short_description: varchar (255)
- description: text
- created_at: datetime or current_timestamp
- modified_at: datetime or current_timestamp
- parent_id: int(11) default 0
- is_active: smallint(4) 1 or 0, default 1

2. blog_post
- post_id: int (11) primary auto increment
- post_title: varchar (200)
- url_key: varchar (200)
- short_description: varchar (255)
- description: text
- created_at: datetime or current_timestamp
- modified_at: datetime or current_timestamp
- category_id: int(11) default 0
- is_active: smallint(4) 1 or 0, default 1
- author_id: int(11)
- author_name: varchar(200)
- post_tags: varchar(255)
- meta_keywords: varchar(255)
- meta_description: varchar(255)

3. author
- user_id: int(11) primary
- author_name: varchar(200) 
- author_email: varchar(200)
- author_socials: varchar(200)
- author_description: varchar(255)
- is_active: smallint(4) 1 or 0, default 1

4. contact_message
- message_id: int(11) pprimary auto increment
- subject: varchar(255)
- message: text
- from_email: varchar(255)
- from_name: varchar(200)
- from_phone: varchar(50)
- created_at: datetime or current_timestamp