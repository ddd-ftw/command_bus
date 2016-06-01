# Wet::CommandBus

> Command Pattern - decoupling what is done from who does it.


Usage:

```ruby
require 'wet/command_bus'

command_bus = Wet::CommandBus.new
register    = command_bus.method(:register)

{ FooCommand => FooService.new(event_store: event_store).method(:foo),
  BarCommand => BarService.new,
}.map(&:register)


command_bus.(FooCommand.new)

```

Now think how that makes your system simpler and use it or forget and move on.

## Convenience alias

```ruby
require 'wet/command_bus/alias'
```

From now on you can use top-level `::CommandBus`.

## About

<img src="http://arkency.com/images/arkency.png" alt="Arkency" width="20%" align="left" />

Command Bus is funded and maintained by Arkency. Check out our other [open-source projects](https://github.com/arkency).

You can also [hire us](http://arkency.com) or [read our blog](http://blog.arkency.com).
