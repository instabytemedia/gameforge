# Entity Relationship Diagram - GameForge

> **Auto-generated** from your idea analysis
> **Entities:** 2

---

## Visual Diagram

```mermaid
erDiagram
    profiles {
        uuid id PK
        text username UK
        text display_name
        text avatar_url
        timestamptz created_at
        timestamptz updated_at
    }

    games {
        uuid id PK
        uuid user_id FK
        uuid id
        timestamptz created_at
        timestamptz updated_at
        uuid user_id FK
        text title
        text description
        timestamptz created_at
        timestamptz updated_at
    }

    users {
        uuid id PK
        uuid user_id FK
        uuid id
        timestamptz created_at
        timestamptz updated_at
        uuid user_id FK
        text username UK
        text email UK
        timestamptz created_at
        timestamptz updated_at
    }

    %% Relationships
    profiles ||--o{ games : owns
    profiles ||--o{ users : owns
    games ||--o{ users : "A user can create many games"
    users ||--o{ games : "A user can create many games"
```

---

## Entity Details

### Game
> A user-created board game

**Fields:**
  - `id`: uuid (required) - Primary key
  - `created_at`: datetime (required) - Creation timestamp
  - `updated_at`: datetime (required) - Last update timestamp
  - `user_id`: uuid (required) - Owner user ID
  - `title`: string (required, indexed)
  - `description`: text

**Relationships:**
  - one_to_many → **User**: A user can create many games

### User
> A registered user

**Fields:**
  - `id`: uuid (required) - Primary key
  - `created_at`: datetime (required) - Creation timestamp
  - `updated_at`: datetime (required) - Last update timestamp
  - `user_id`: uuid (required) - Owner user ID
  - `username`: string (required, unique, indexed)
  - `email`: string (required, unique, indexed)

**Relationships:**
  - one_to_many → **Game**: A user can create many games

---

## Notes

- All entities have standard fields: `id`, `user_id`, `created_at`, `updated_at`
- `PK` = Primary Key, `FK` = Foreign Key, `UK` = Unique Key
- Copy the Mermaid code block to visualize in any Mermaid-compatible tool
- Relationships: `||--o{` = one-to-many, `||--||` = one-to-one, `}o--o{` = many-to-many
