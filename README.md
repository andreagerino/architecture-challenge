# System architecture

In our system we process a high number of documents in a streaming data pipeline.
We would like to design a data validation solution to integrate in our pipeline.

## The solution should:

- Support reading data from Parquet files
- Output validated documents in the JSON data format
- Be easily shared across different actors in the pipeline

## Other considerations:

- The solution will be used by approx 10 different services
- Performance is important in order to support low latency real-time streaming

## Questions

1. How would you design such a solution? Please specify at least two different approaches
2. What would be the pros and cons of each solution?
3. How would you handle updating the solution when schema changes?

# Coding challenge

Now that you have defined the solution, can you implement a quick proof of concept?

The proof of concept should:

- Use TypeScript and Rust
- Read data from a parquet file using Rust ([file](https://github.com/andreagerino/architecture-challenge/blob/main/trips.parquet?raw=true))
- Validate the data in Node according to a type definition ([file](https://raw.githubusercontent.com/andreagerino/architecture-challenge/main/trip.ts))
- Output parsed data to the console in JSON format
