# Reduce Operator

## Overview

Apply a function to each item emitted by an Observable, sequentially, and emit the final value.

![](http://reactivex.io/documentation/operators/images/reduce.png)

## Example

```go
observable := rxgo.Just([]interface{}{1, 2, 3}).
	Reduce(func(_ context.Context, acc interface{}, elem interface{}) (interface{}, error) {
		if acc == nil {
			return elem, nil
		}
		return acc.(int) + elem.(int), nil
	})
```

Output:

```
6
```

## Options

### WithBufferedChannel

[Detail](options.md#withbufferedchannel)

### WithContext

[Detail](options.md#withcontext)

### WithObservationStrategy

[Detail](options.md#withobservationstrategy)

### WithErrorStrategy

[Detail](options.md#witherrorstrategy)

### WithPool

https://github.com/ReactiveX/RxGo/wiki/Options#withpool

### WithCPUPool

https://github.com/ReactiveX/RxGo/wiki/Options#withcpupool