Problem: Complex Queries
========================

Have you ever seen a query like this in an application?

```ruby
class User < ActiveRecord::Base
  ...
  scope :in_trial, -> joins(:subscription).where("subscriptions.trial_end_date > ?", Time.zone.now)
  ...
end
```

Or, what about this one?

```ruby
class Listing < ActiveRecord::Base
  ...
  def self.with_more_than_three_photos_and_a_comment
    joins("LEFT JOIN photos ON photos.listing_id = listings.id").
    joins("LEFT JOIN comments ON comments.commentable_id = listings.id").
    group("listings.id").
    having("count(photos.id) > 3")
    having("count(comments.id) > 0")
  end
  ...
end
```

These are what we like to call complex queries. You have to read a bunch of SQL
in your model. Even more so, do you use that query all the time? Probably not.

Solution
========

Instead of keeping these queries in your model, create a separate object for
them.

```ruby
class UsersInTrialQuery

end
```

```ruby
class ListingsWithMoreThanThreePhotosQuery

end

class ListingsWithCommentsQuery

end
```

For further reading: 
- [7 Patterns to Refactor Fat ActiveRecord Models](http://blog.codeclimate.com/blog/2012/10/17/7-ways-to-decompose-fat-activerecord-models/)
See `4. Extract Query Objects`.

