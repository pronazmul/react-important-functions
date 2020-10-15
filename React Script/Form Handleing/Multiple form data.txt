import React, { Component } from 'react';

class FormMultiple extends Component {

    constructor(){
        super()

        this.state ={
            name:" ",
            email:" ",
            mobile:" ",
            address:" "
        }
    }

   onChangeHandle = (event) =>{
    let name = event.target.name
    let value = event.target.value
    this.setState({[name]:value})
   }

//    onSubmitHandle = () =>{
//        alert(this.state.username)
//    }


    render() {
        return (
            <div className='col-md-5 mx-auto mt-5'>
                <div className="card bg-secondary">
                    <div className="card-header">
                        <h3 className='card-title text-center text-light'>Multiple Form Data</h3>
                    </div>
                    <div className="card-body">
                        <p className='lead'>Your Name: {this.state.name}</p>
                        <p className='lead'>Your Email: {this.state.email}</p>
                        <p className='lead'>Your Phone No: {this.state.mobile}</p>
                        <p className='lead'>Your Address: {this.state.address}</p>
                    <form>
                        <input name='name' placeholder='Enter Name' onChange={this.onChangeHandle} className='form-control mt-1' type="text"/>
                        <input name='email' placeholder='Enter email' onChange={this.onChangeHandle} className='form-control mt-1' type="text"/>
                        <input name='mobile' placeholder='Enter mobile no' onChange={this.onChangeHandle} className='form-control mt-1' type="text"/>
                        <input name='address' placeholder='Enter address' onChange={this.onChangeHandle} className='form-control mt-1' type="text"/>
                        <input className = 'btn btn-info btn-block mt-4' type='submit' value='Submit'></input>
                    </form>
                    </div>
                </div>
            </div>
        );
    }
}

export default FormMultiple;