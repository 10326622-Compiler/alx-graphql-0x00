# GraphQL Episode Queries

This directory contains GraphQL queries to retrieve episode information from the Rick and Morty API using episode IDs.

## Endpoint

```
https://rickandmortyapi.com/graphql
```

## Query Structure

Each query uses the `episode(id: ID!)` field to fetch specific episode details including:
- `id` - The unique identifier of the episode
- `name` - The name of the episode
- `air_date` - The air date of the episode
- `episode` - The episode code (e.g., S01E01)

## Files

- `episode-id-1.graphql` - Query for episode with ID 1
- `episode-id-1-output.json` - Output for episode ID 1
- `episode-id-2.graphql` - Query for episode with ID 2
- `episode-id-2-output.json` - Output for episode ID 2
- `episode-id-3.graphql` - Query for episode with ID 3
- `episode-id-3-output.json` - Output for episode ID 3
- `episode-id-4.graphql` - Query for episode with ID 4
- `episode-id-4-output.json` - Output for episode ID 4

## Episode Information

- **Episode 1**: "Pilot" - The first episode of the series
- **Episode 2**: "Lawnmower Dog" - The second episode
- **Episode 3**: "Anatomy Park" - The third episode
- **Episode 4**: "M. Night Shaym-Aliens!" - The fourth episode

## How to Execute

You can execute these queries using:

1. **GraphQL Playground**: Visit https://rickandmortyapi.com/graphql and paste the query
2. **cURL**: 
   ```bash
   curl -X POST https://rickandmortyapi.com/graphql \
     -H "Content-Type: application/json" \
     -d '{"query":"your_query_here"}'
   ```
3. **GraphQL Client Libraries**: Use libraries like Apollo Client, urql, or graphql-request in your application

## Example Usage in Code

```typescript
import { useQuery, gql } from '@apollo/client';

const GET_EPISODE = gql`
  query {
    episode(id: 1) {
      id
      name
      air_date
      episode
    }
  }
`;

function EpisodeComponent() {
  const { loading, error, data } = useQuery(GET_EPISODE);
  
  if (loading) return <p>Loading...</p>;
  if (error) return <p>Error: {error.message}</p>;
  
  return (
    <div>
      <h2>{data.episode.name}</h2>
      <p>Episode: {data.episode.episode}</p>
      <p>Air Date: {data.episode.air_date}</p>
    </div>
  );
}
```

## Learning Objectives

- Understand how to query single items by ID in GraphQL
- Learn to work with episode data from the Rick and Morty API
- Practice selecting specific fields from a GraphQL schema
- Understand the structure of episode data