# Titre de la compétence

> ❌ A travailler

> ✔️ Auto validation par l'étudiant

## 🎓 J'ai compris et je peux expliquer

- l'état (_state_) pour contrôler l'affichage d'un composant ✔️
  - le `state` permet de définir des états pour un composant. Il se définit comme suit :
  - `const [name, setName] = useState("");`
- les composants enfants et les _props_ qu'on leur passe ✔️
  - Un composant peut contenir d'autres composants et leur passer des données via les "props". Un composant auquel on passe des props se définit comme suit :
  - `<Component prop={prop} />`
- le déclenchement d'instructions en fonction des actions de l'utilisateur ✔️
  - Il s'agit de l'écoute d'évènement auquel on va passer une fonction à exécuter lorsque cet évènement est déclenché comme `onClick()` ou `onChange()` par exemple.
- le déclenchement d'instructions en fonction de l'étape du cycle de vie du composant ou du changement de valeur de ses props ✔️
  - `useEffect` permet de déclencher des instructions au montage ou au démontage d'un composant.
- l'usage d'un reducer (_useReducer_) pour gérer un état composé dans un composant ❌
- l'état stocké dans un composant avec un _context provider_ et accessible dans ses descendants via `useContext` ❌

## 💻 J'utilise

### Un exemple personnel commenté ✔️
Un exemple de composant du projet WildBook :
```javascript
import axios from 'axios';
import blank_profile from '../assets/blank_profile.png';
import Skill from './Skill';
import styles from '../styles/Wilder.module.css';

const handleDelete = (id) => {
    axios.delete(`http://localhost:5000/api/wilder/${id}`);
}

const Wilder = ({ id, name, city, skills }) => (
    <article className={styles.card}>
        <img src={ blank_profile } className={styles.profilePicture} alt="profile" />
        <h3>{ name }</h3>
        { city ? <strong>{ city }</strong> : null }
        <p className={styles.description}>
            Lorem ipsum dolor sit amet, consectetur adipiscing elit. Etiam convallis molestie velit ut mattis. Nulla sit amet lacus purus. Phasellus sit amet dignissim odio. Nullam vitae imperdiet nibh.
        </p>
        <h4>Wild Skills</h4>
        <ul className={styles.skills}>
            {skills ? skills.map(skill => <Skill name={ skill.name } votes={ skill.votes }/>) : null}
        </ul>
        <button onClick={() => handleDelete(id)}>Delete</button>
    </article>
);

export default Wilder;
```

### Utilisation dans un projet ✔️

[WildBook](https://github.com/LudovicLefieux/js_wildbook)

Description : Un projet de la Wild Code School permettant de répertorier des étudiants. Ce projet a permis de pratiquer le Javascript en back comme en front.

### Utilisation en production si applicable❌

[lien du projet](...)

Description :

### Utilisation en environement professionnel ❌

Description :

## 🌐 J'utilise des ressources

### Titre

- [React](https://react.dev/reference/react)
- Documentation officielle de React.

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
