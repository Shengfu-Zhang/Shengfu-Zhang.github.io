Part 2 of 2: If the same defect can appear twice in review, it deserves a rule.

That is the operating principle I keep coming back to when teams ask how to use coding agents without letting quality drift.

Once AI makes code cheap, the scarce resource becomes trust. And trust does not scale through reviewer heroics. It scales through better infrastructure.

For me, that infrastructure has three layers.

First, deterministic enforcement: build rules that catch repeated structural mistakes before a reviewer sees them.

Second, dynamic steering: shared SOPs and steering files that reduce variance across engineers while the pattern is still too judgment-heavy to lint.

Third, measurement: revision rounds, iteration depth, harness catch rate, and post-merge defects. Those are the signals that tell you whether autonomy is actually being earned.

The part I find most under-discussed is testing the harness itself. Teams test app code, but they rarely test the system that generates and validates the code. If a lint rule stops firing or a steering change quietly regresses, the cost shows up later as review churn.

The goal is not “less review because AI is good now.” The goal is lighter review only when the signals are strong enough to carry that weight.

Which signal would give you the most confidence to reduce review depth on a real production change?

[Blog link in comments]
