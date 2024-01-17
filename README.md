# My-Portfolio

# Introduction
## Andres Arevalo Vitela
*Passionate Problem Solver | Transforming Challenges into Solutions.*
### Greetings! I am Andres Arevalo Vitela, a recent graduate in Computer Science from the University of California, Riverside. Aspiring to commence my career as a software developer, I am enthusiastic about delving into industry-level code. Possessing a self-driven and passionate approach to problem-solving, I tenaciously address challenges until resolution. Backed by a demonstrated technical acumen, I am confident in my ability to contribute significantly as a valuable asset to any software development team.
# Projects
## Create a section to showcase your projects. For each project:

## Money Social
    Planned and developed a budgeting app in JavaScript using React-Native with a team of 5.
    Used MongoDB and GraphQL to manage the back-end.
*Home Screen*
![money social home](https://github.com/aa2510759/My-Portfolio/assets/28612170/1813ec83-40ee-423e-bd1e-00c6e5b65da9)
<br/>
<br/>
*Profile Screen*
![graphics](https://github.com/aa2510759/My-Portfolio/assets/28612170/ad65e272-f17d-4def-a1cd-a60a697e4724)
<br/>
<br/>
*Group Screen*
![groups](https://github.com/aa2510759/My-Portfolio/assets/28612170/4bd60415-6191-4ea4-b75d-089d2575c27c)
<br/>

code snippet from App.js using graphQL to authenticate the user
`function App() {
  useEffect(() => {
    const syncUser = async () => {
      // get Auth user
      const authUser = await Auth.currentAuthenticatedUser({
        bypassCache: true,
      });

      // query the database using Auth user id (sub)
      const userData = await API.graphql(
        graphqlOperation(queries.getUser, { id: authUser.attributes.sub })
      );

      if (userData.data.getUser) {
        console.log("User already exists in DB");
        console.log(userData)
        return;
      }
      // if there is no users in db, create one
      const newUser = {
        id: authUser.attributes.sub,
        name: authUser.attributes.name,
        imageUri: '',
        bio: "Hey, I am using MoneySocial"
      };

      await API.graphql(
        graphqlOperation(mutations.createUser, { input: newUser })
      );
    };

    syncUser();
  }, []);

  return (
  <StackNavigator />
  );
};`

[Money Social Repo](https://github.com/lojason71/cs180-project/tree/main/moneysocial)



## AI Puzzle Solver

## Melody Player

# Skills

## List your technical skills. Categorize them based on languages, frameworks, databases, and tools. Use icons or badges for a visually appealing layout.
# Education
## Mention your educational background. Include your degree, major, university, and graduation date.
# Contact Information.
## Provide ways for people to contact you. You can include your email address or link to your LinkedIn profile.
