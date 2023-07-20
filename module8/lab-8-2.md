User collection:

{
  _id: ObjectId,
  username: String,
  email: String,
  password: String,
  created_at: Date
}


Post collection:

{
  _id: ObjectId,
  user_id: ObjectId (references User collection),
  title: String,
  description: String,
  image_url: String,
  created_at: Date
}


Like collection:

{
  _id: ObjectId,
  user_id: ObjectId (references User collection),
  post_id: ObjectId (references Post collection),
  created_at: Date
}


Comment collection:

{
  _id: ObjectId,
  user_id: ObjectId (references User collection),
  post_id: ObjectId (references Post collection),
  comment_text: String,
  created_at: Date
}


