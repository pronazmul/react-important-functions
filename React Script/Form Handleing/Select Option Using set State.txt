import React, { Component } from 'react';
import '../../node_modules/bootstrap/dist/css/bootstrap.min.css'

class SelectOption extends Component {

    constructor(){
        super()
        this.state = {
            selected:'',
            auto:'Dhaka',
            city1:'Mymensingh',
            city2: 'Sylet',
            city3: 'Khulna',
            city4: 'Barishal',
            city5: 'Chittagong',
            city6: 'Rajshahi',
            city7: 'Rangpur'
        }
    }
    onChangeHandle= (event)=>{
        let data = event.target.value
        this.setState({selected:data, auto:data})

    }
    render() {
        return (
            <div className='col-md-5 mx-auto my-5'>
                <div className="card bg-secondary">
                    <div className="card-header">
                        <h3 className='card-title text-center text-light'>Select Option in React</h3>
                    </div>
                    <div className="card-body text-dark">
                    <form>
                        <p className='lead'>Selected Value: {this.state.selected}</p>
                        <select onChange={this.onChangeHandle} className='form-control' value={this.state.auto}>
                            <option>{this.state.city1}</option>
                            <option>{this.state.city2}</option>
                            <option>{this.state.city3}</option>
                            <option>{this.state.city4}</option>
                            <option>{this.state.city5}</option>
                            <option>{this.state.city6}</option>
                            <option>{this.state.city7}</option>
                        </select>
                    </form>
                    </div>
                </div>
            </div>
        );
    }
}

export default SelectOption;

