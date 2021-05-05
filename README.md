# cardlisting
import React, { Component } from "react";
import './cardlisting.css';

export default class CardListing extends React.Component {
    constructor(props){
        super(props);
        this.state = {
            color: "black"
          };
        }
        changeColor = () => {
            this.setState({color: "blue"});
          }
    render(){
        const card1 = {
            name: 'Sonakshi Darak',
            designation: 'Front-End Developer Intern',
            title:'Queen',
            birth:'Born on 10th oct 2000',
          };
          const card2 = {
            name: 'Jay',
            designation: 'Intern',
            title:'Prince',
            birth:'Born on 29th Feb 1999',
          };
          const card3 = {
            name: 'Aayushi',
            designation: 'Developer',
            title:'Princess',
            birth:'Born on 18th Oct 2000',
          };
          const card4 = {
            name: 'Saakshi',
            designation: 'Graphic Designer',
            title:'Queen',
            birth:'Born on 31st Dec 1998',
          };
          const card5 = {
            name: 'Anmol',
            designation: 'UI Developer',
            title:'King',
            birth:'Born on 16th Nov 1999',
          };
          const card6 = {
            name: 'Sejal',
            designation: 'Content-Writer',
            title:'Princess',
            birth:'Born on 20th March 2001',
          };
          const card7 = {
            name: 'Aditi',
            designation: 'App Developer',
            title:'Princess',
            birth:'Born on 8th April 2000',
          };
          const card8 = {
            name: 'Hrithik',
            designation: 'Management',
            title:'Prince',
            birth:'Born on 15th March 2000',
          };
        return(
            <div>
                <button
                type="button"
                onClick={this.changeColor}
                style={{position:"relative",width:"100px", height:"50px",left:"90%"}}>
                    Change Color
                    </button>
            <div class="row" style={{color:(this.state.color)}}>
                <div class="column">
                    <Card card={card1} />
                    </div>
                <div class="column">
                    <Card card={card2} />
                    </div>
                <div class="column">
                    <Card card={card3} />
                    </div>
                <div class="column">
                    <Card card={card4} />
                    </div>
                </div>
            <div class="row" style={{color:(this.state.color)}}>
                <div class="column">
                    <Card card={card5} />
                    </div>
                <div class="column">
                    <Card card={card6} />
                    </div>
                <div class="column">
                    <Card card={card7} />
                    </div>
                <div class="column">
                    <Card card={card8} />
                    </div>
                </div>
</div>
        );
        
    }
}
const Card = ({ card }) =>
<div class="card">
<div class="profile">
<img src='../images/Avatar.jpg' style={{width: "75px", height: "75px",borderRadius:"50%", display:"flex",flexDirection:"column"}}></img>
<h4>{card.name}</h4>
<text>{card.designation}</text>
</div>
<div class="mydiv">
<hr />
<text>{card.title}</text>
<hr />
<text>{card.birth}</text>
</div>
</div>
