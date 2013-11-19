TableViewAutolayoutEstimatedHeightDemo
======================================

Trying to demonstrate in an minimal project a bug I think I'm suffering with on iOS related to Autolayout and Estimated cell heights.

This issue was showing itself on iOS 7.0.4 with the project built with Xcode 5.02.

Basically getting Autolayout errors when the estimated height of the cell is too large.  Run the app in debug mode and if you hit the "Add cell" button a few times you should see an error like the one below.

```
2013-11-19 21:01:04.004 TableViewAutolayoutEstimatedHeightDemo[355:60b] Unable to simultaneously satisfy constraints.
	Probably at least one of the constraints in the following list is one you don't want. Try this: (1) look at each constraint and try to figure out which you don't expect; (2) find the code that added the unwanted constraint or constraints and fix it. (Note: If you're seeing NSAutoresizingMaskLayoutConstraints that you don't understand, refer to the documentation for the UIView property translatesAutoresizingMaskIntoConstraints) 
(
    "<_UIScrollViewAutomaticContentSizeConstraint:0x17ea5500 UITableView:0x18894000.contentHeight{id: 28} == -32.000000>"
)

Will attempt to recover by breaking constraint 
<_UIScrollViewAutomaticContentSizeConstraint:0x17ea5500 UITableView:0x18894000.contentHeight{id: 28} == -32.000000>

Break on objc_exception_throw to catch this in the debugger.
The methods in the UIConstraintBasedLayoutDebugging category on UIView listed in <UIKit/UIView.h> may also be helpful.
```
