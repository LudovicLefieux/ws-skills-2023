# TypeScript

> ❌ A travailler

> ✔️ Auto validation par l'étudiant

## 🎓 J'ai compris et je peux expliquer

- l'intéret de TypeScript dans l'IDE ✔️
  - Typescript indique directement dans l'IDE si une erreur de typage a été commise contrairement à Javascript. Cela permet de détecter et de corriger une erreur plus rapidement.
- les types de bases ✔️
  - ```javascript
    string
    number
    boolean
    null
    undefined
    any
    never
    array
    object
    void
    ```
- comment et pourquoi étendre une interface ✔️
  - Une interface permet de définir la structure que doit respecter un objet. Une interface se définit comme suit :
  ```javascript
  interface IWilder {
    id: number;
    name: string;
    city: string;
  }
  
  const Ludovic: IWilder = {
    id: 1,
    name: Ludovic,
    city: Strasbourg
  }
  ```
- les classes et les decorators ✔️
  - Une classe permet de créer des instances d'objets possédant les mêmes propriétés
  - Un décorateur permet d'ajouter des fonctionnalités aux propriétés d'une classe

## 💻 J'utilise

### Un exemple personnel commenté ✔️
Un exemple de composant React en Typescript tiré du projet WildBook
```javascript
import axios from "axios";
import blank_profile from "./../assets/blank_profile.png";
import styles from "./../styles/Wilder.module.css";

import Skill, { ISkillProps } from "./Skill";

export interface IWilderProps {
  id: number;
  name: string;
  city: string;
  skills: ISkillProps[];
}

const handleDelete = (id: number) => {
  console.log(id);
  axios.delete(`http://localhost:5000/api/wilder/${id}`);
};

const Wilder = ({ id, name, city, skills }: IWilderProps) => (
  <article className={styles.card}>
    <img src={blank_profile} className={styles.profilePicture} alt="profile" />
    <button onClick={() => handleDelete(id)}>Delete</button>
    <h3>{name}</h3>
    {city ? <strong>{city}</strong> : null}
    <p className={styles.description}>
      Lorem ipsum dolor sit amet, consectetur adipiscing elit. Etiam convallis
      molestie velit ut mattis. Nulla sit amet lacus purus. Phasellus sit amet
      dignissim odio. Nullam vitae imperdiet nibh.
    </p>
    <h4>Wild Skills</h4>
    <ul className={styles.skills}>
      {skills
        ? skills.map((skill) => (
            <Skill title={skill.title} votes={skill.votes} />
          ))
        : null}
    </ul>
  </article>
);

export default Wilder;
```

### Utilisation dans un projet ❌

[lien github](...)

Description :

### Utilisation en production si applicable❌

[lien du projet](...)

Description :

### Utilisation en environement professionnel ❌

Description :

## 🌐 J'utilise des ressources

### Titre

- [Typescript](https://www.typescriptlang.org/docs/)
- La documentation officielle de Typescript

## 🚧 Je franchis les obstacles

### Point de blocage ❌

Description:

Plan d'action : (à valider par le formateur)

- action 1 ❌
- action 2 ❌
- ...

Résolution :

## 📽️ J'en fais la démonstration

- J'ai ecrit un [tutoriel](...) ❌
- J'ai fait une [présentation](...) ❌
