# Go HTTP Handler Resource Leak: Forgetting to close request body

This repository demonstrates a common error in Go's HTTP handlers: forgetting to close the request body using `defer r.Body.Close()`.  This can lead to resource exhaustion, especially when handling large requests.

The `bug.go` file shows the problematic code, while `bugSolution.go` provides the corrected version.  Always remember to properly close resources to prevent leaks and ensure your application's stability and efficiency.