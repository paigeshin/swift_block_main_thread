# swift_block_main_thread

```swift
 // block main thread
    DispatchQueue.global().async {
        sleep(1)
        DispatchQueue.main.sync {
            CFRunLoopStop(CFRunLoopGetCurrent())
        }
    }
    CFRunLoopRun()
```
