# My-Portfolio
## Andres Arevalo Vitela
*Passionate Problem Solver | Transforming Challenges into Solutions.*
### Greetings! I am Andres Arevalo Vitela, a recent graduate in Computer Science from the University of California, Riverside. Aspiring to commence my career as a software developer, I am enthusiastic about delving into industry-level code. Possessing a self-driven and passionate approach to problem-solving, I tenaciously address challenges until resolution. Backed by a demonstrated technical acumen, I am confident in my ability to contribute significantly as a valuable asset to any software development team.
# Projects
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

code snippet from App.js using graphQL to authenticate the user: 
    
    function App() {
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
    };

[Money Social Repo](https://github.com/lojason71/cs180-project/tree/main/moneysocial)

<br/>

## AI Puzzle Solver
        Developed an AI that solves an 8 puzzle. I utilized several efficient graph algorithms including A*search.
        Was written in C++. 
        
### An 8 puzzle is a sliding puzzle where you must slide the pieces of a puzzle in such a way that they are ordered like so:
        1  2  3
        4  5  6 
        7  8  0

*inital state with menu options*
![inital state](https://github.com/aa2510759/My-Portfolio/assets/28612170/d7ca0d44-6f30-4d11-8424-7e4fcb4820da)

*Runnning with Uniform Cost Search*
![ucs ](https://github.com/aa2510759/My-Portfolio/assets/28612170/9ab76cca-33bf-4ca9-ad3f-58ce83787925)


*Running with Astar Search with a euclidian heuristic*
![astar ](https://github.com/aa2510759/My-Portfolio/assets/28612170/a0cfee3f-aa01-49c1-b374-410d3368b3a2)



### This is a snippet of the function that implements A* Search

            Node* astarH(deque<Node*>& d){
            	int astar = 2147483647;
            	Node* temp = nullptr;
            	int popIndex = 0;
            	for (int i = 0; i < d.size(); i++){
            		int curr = d.at(i)->misplaced + d.at(i)->depth;
            		if (curr < astar){
            			astar = curr;
            			temp = d.at(i);
            			popIndex = i;
            			//cout << "the new min distance is: " << distance << endl;
            		}
            	}
            	d.erase(d.begin() + popIndex);
            	return temp;
            }
[AI puzzle solver repo](https://github.com/aa2510759/cs170/blob/main/main.cpp)

## Melody Player

### I developed a melody player with an LCD UI that was written in C. I implemented embedded programming principles such as a state machines to handle continuious user input.
![video screen shot](https://github.com/aa2510759/My-Portfolio/assets/28612170/5a1811f0-de63-41ec-a70e-eabdbe067025)
<br/>
[Melody player video demo](https://www.youtube.com/watch?v=A4fi2tVMfPc)
<br/>
<br/>
*snippet of code:*

            int TickFct_LCDOutput(int state) {
      switch (state) {
        case 0:
          state = first_screen;
          break;
        case first_screen:
          LCDWriteLines("Song 1  Song 2", "Song 3  Start");
          pos1();
          lcd.blink();
          state = first_screen_wait;
          break;
        case second_screen1:
          LCDWriteLines("Playing Song 1", "Pause    Play");
          pos5();
          lcd.blink();
          state = second_screen_wait;
          break;
        case second_screen2:
          LCDWriteLines("Playing Song 2", "Pause    Play");
          pos5();
          lcd.blink();
          state = second_screen_wait;
          break;
        case second_screen3:
          LCDWriteLines("Playing Song 3", "Pause    Play");
          pos5();
          lcd.blink();
          state = second_screen_wait;
          break;
          case first_screen_wait: //idle
[Melody player repo](https://github.com/aa2510759/embedded_systems)
<brk/>
# Skills

### Languages
            C/C++, HTML5, CSS, JavaScript, Python
### Frameworks
    ![React-icon svg](https://github.com/aa2510759/My-Portfolio/assets/28612170/5e2477a6-4baf-4bf4-9f3d-26cbc71d7af3)

# Education
    University of California,  Riverside 
    2020-2023 
    B.S. in Computer Science
<brk/>

    Norco College                                
    2015-2020    
    A.S. in Computer Science

# Contact Information.
    Email: andres.arevalo.vitela@gmail.com
    Phone: +1(951)220-1876
Linkedin: [https://www.linkedin.com/in/andres-arevalo-vitela-0070a1206](https://www.linkedin.com/in/andres-arevalo-vitela-0070a1206)


