import React, { Component } from 'react';
import '../../node_modules/bootstrap/dist/css/bootstrap.min.css'

class StatePractice extends Component {

    constructor(){
        super()
        this.state ={
            name:'Nazmul Hdua',
            age: 24,
            profession:'Programmer'
        }
    }

    changeState(name, age, profession){

        this.setState({name:name, age:age, profession:profession})
    }



    render() {
        return (
            <div className='jumbotron text-center'>
                <h1>Name: {this.state.name}</h1>
                <h1>Age: {this.state.age}</h1>
                <h1>Profession: {this.state.profession}</h1>
                <button className='btn btn-warning btn-lg' onClick={()=>this.changeState('Bilal Hossain', 25, 'Frontend Developer')}>Change Data</button>
            </div>
        );
    }
}

export default StatePractice;