// App.js
import React, { Component } from 'react';

class App extends Component {
  constructor(props) {
    super(props);
    this.state = {
      person: {
        fullName: 'Say Joel',
        bio: 'Software Engineer',
        imgSrc: 'Developper.jpeg',
        profession: 'Developer'
      },
      showProfile: false
    };
  }
  

    

  toggleProfile = () => {
    this.setState({ showProfile: !this.state.showProfile });
  }

  render() {
    return (
      <div style={{borderStyle : 'solid' , width:'117px'}}>
        <button onClick={this.toggleProfile}>Toggle Profile</button>

        {this.state.showProfile && (
          <div>
            <h2 >{this.state.person.fullName}</h2>
            <img src={this.state.person.imgSrc} alt={this.state.person.fullName} />
            <p>{this.state.person.bio}</p>
            <p>Profession: {this.state.person.profession}</p>
          </div>
        )}
        
        <p>Time since mount: {this.state.mountTime}</p>
      </div>
    );
  }

 
}


export default App;
