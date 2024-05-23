One of the things that Go encourages you to do, is to handle errors.

I like to do that from the very beginning of my programm and that's why every `main` function of my projects actually only calls the `run` function which returns an error in case something goes wrong and in the main function with can handle the error and Exit our program.

```go
func Run(ctx context.Context, w io.Writer, args []string) error {
    ctx, cancel := signal.NotifyContext(ctx, os.Interrupt)
    defer cancel()

    // Some Run logic here
}

func main() {
    ctx := context.Background()
    if err := Run(ctx, os.Stdout, os.Args); err != nil {
        fmt.Fprintf(os.Stderr, "%s\n", err)
        os.Exit(1)
    }
}
```