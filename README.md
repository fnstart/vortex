# Vortex Website Rework - Example
- By @fnstart (blacksmith)


Get User Profile - Headers: None
- `https://playvortex.io/api/users/avatar-pictures?ids={id}`
- `https://playvortex.io/api/users/avatar-pictures?ids={id},{id}`

User Data - Headers: Cookie
- `https://playvortex.io/api/users/{id}`

Friends List - Headers: Cookie
- `https://playvortex.io/api/friends/{id}`
return { id: number, username: string, online_status: "in_game" | "offline" | "online" }[]

Games List - Headers: None
- `https://playvortex.io/api/games`
return {
    id: number,
    name: string
    description: string,
    creator_id": number,
    creator_name: string,
    thumbnail_version: string
}[]

Game Stats - Headers: Cookie
- `https://playvortex.io/api/game-stats`
return { [string]: { active: number, visits: number } }

Game Picture - Headers: None
- `https://playvortex.io/assets/thumbnails/{id}.png`
return image

Catalog Thumbnails - Headers: None
- `https://playvortex.io/api/catalog/thumbnails?ids={id}`
- `https://playvortex.io/api/catalog/thumbnails?ids={id},{id}`
return { [string]: "data:image/..." } 

Catalog Init - Headers: Cookie
- `https://playvortex.io/api/catalog/init`
return {
    items:  { id: number, name: string, type: "shirt" | "pant" | "face" }[],
    shirt_id: number,
    pant_id: number,
    body_type: "male" | "female",
    body_colors: string[],
    face_id: number
}

Catalog Asset - Headers: None
- `https://playvortex.io/api/clothing/image/{id}`
return image

Glp - Headers: None
- `https://playvortex.io/assets/male.glb`
- `https://playvortex.io/assets/female.glb`
return glp

Me - Headers: Cookie
- `https://playvortex.io/me`
return {
    id: number,
    username: string
}
