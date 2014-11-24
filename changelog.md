# Changelog for [`process` package](http://hackage.haskell.org/package/process)

## 1.2.0.1  *TBA*

  * Add support for `base-4.8.0.0`

  * Expose documentation for `System.Process.Internals`

## 1.2.0.0  *Dec 2013*

  * Update to Cabal 1.10 format
  * Remove NHC specific code
  * Add support for `base-4.7.0.0`
  * Improve `showCommandForUser` to reduce redundant quoting
  * New functions `callProcess`, `callCommand`, `spawnProcess` and `spawnCommand`
  * Implement WCE handling according to http://www.cons.org/cracauer/sigint.html
  * New `delegate_ctlc` field in `CreateProcess` for WCE handling
  * Use `ExitFailure (-signum)` on Unix when a proc is terminated due to
    a signal.
  * Deprecate `module System.Cmd`
  * On non-Windows, the child thread now comunicates any errors back
    to the parent thread via pipes.
  * Fix deadlocks in `readProcess` and `readProcessWithExitCode`