# Activity

Activity is dependant on [QOR Admin](https://github.com/kisrobot/admin). It provides [QOR Admin](https://github.com/kisrobot/admin) with an activity tracking feature for any Resource.

Applying Activity to a Resource will add `Comment` and `Track` data/state changes within the [QOR Admin](https://github.com/kisrobot/admin) interface.

[![GoDoc](https://godoc.org/github.com/kisrobot/activity?status.svg)](https://godoc.org/github.com/kisrobot/activity)

## Usage

```go
import "github.com/kisrobot/admin"

func main() {
  Admin := admin.New(&qor.Config{DB: db})
  order := Admin.AddResource(&models.Order{})

  // Register Activity for Order resource
  activity.Register(order)
}
```

The above code snippet will add an activity tracking feature to the Order resource in a hypothetical project, which would look a bit like the screenshot below in [QOR Admin](https://github.com/kisrobot/admin):

## License

Released under the [MIT License](http://opensource.org/licenses/MIT).
