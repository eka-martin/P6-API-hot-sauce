# P6-API-hot-sauce
#ROUTES

-------------------------------------------
##La route POST pour créer un compte
-------------------------------------------
http://localhost:3000/api/auth/signup
Body-->Raw (JSON)

{
"email" : "xxxxxxxx", 
"password" : "xxxxxxxx" (mot de passe fort)
}

-------------------------------------------
##La route POST pour se logger
-------------------------------------------
http://localhost:3000/api/auth/login

{
"email" : "xxxxxxxx", 
"password" : "xxxxxxxx" 
}

-------------------------------------------
##La route POST pour créer une sauce
-------------------------------------------
http://localhost:3000/api/sauces/

Params-->KEY: userId VALUE: _id de l'user
Authorization: Bearer Token TOKEN: xxxxxxxx
Body-->form-data-->
KEY: sauce
VALUE:
{
    userId: "xxxxxx",
    name: "xxxxxx",
    manufacturer: "xxxxxx",
    description: "xxxxxx",
    mainPepper: "xxxxxx",
    heat: "xxxxxx",
    likes: 0,
    dislikes: 0,
    usersLiked: [],
    usersDisliked: [],
}
KEY: image
file et selectionner l'image

-------------------------------------------
##La route GET pour afficher tous les sauces d'un user
-------------------------------------------
http://localhost:3000/api/sauces/
Authorization: Bearer Token TOKEN: xxxxxxxx
Body-->raw
{
"userId" : "xxxxxxx"
}

-------------------------------------------
##La route GET pour afficher une sauce
-------------------------------------------
http://localhost:3000/api/sauces/:id
Params-->KEY: userId VALUE: _id de l'user
Authorization: Bearer Token TOKEN: xxxxxxxx
Body-->none

-------------------------------------------
##La route PUT pour modifier une sauce qui était selectionner par son _id
-------------------------------------------
http://localhost:3000/api/sauces/:id
Params-->KEY: userId VALUE: _id de l'user
Authorization: Bearer Token TOKEN: xxxxxxxx
Body-->form-data-->
KEY: sauce
VALUE:
{
    userId: "xxxxxx",
    name: "xxxxxx",
    manufacturer: "xxxxxx",
    description: "xxxxxx",
    mainPepper: "xxxxxx",
    heat: "xxxxxx",
    }
KEY: image
file et selectionner l'image

-------------------------------------------
##La route DELETE pour modifier une sauce qui était selectionner par son _id
-------------------------------------------
http://localhost:3000/api/sauces/:id
Params-->KEY: userId VALUE: _id de l'user
