# Hyperledger-study-14

하이퍼레져 앱 만들기 실습 14일차 - props 사용

출처 : https://www.opentutorials.org/module/4058/24737

참고자료 : https://reactjs.org/docs/components-and-props.html

1. 13일차 예제 앱을 이어서 사용

2. Component의 내용을 Props로 변경

        class App extends Component {
          render() {
            return (
              <div className="App">
               <Subject title="WEB" sub="world wide web"></Subject>
               <Nav></Nav>
               <ART title="HTML" desc="HTML is HyperText Markup Language."></ART>
              </div>
            );
          }  
        }

3. Subject의 객체 내용 변경

        class Subject extends Component {
          render() {
            return(
              <header>
                <h1>{this.props.title}</h1>
                {this.props.sub}
              </header>
            );
          }
        }

4. ART의 객체 내용 변경

        class ART extends Component {
          render(){
            return(
              <article>
                <h2>{this.props.title}</h2>
                {this.props.desc}
              </article>
            );
          }
        }

결론 : 위와 같이 내용들을 Props로 정리하면 같은 개체의 속성을 안의 내용만 변경하여 사용가능함.
