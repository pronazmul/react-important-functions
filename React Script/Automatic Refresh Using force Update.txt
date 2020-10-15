import React, { Component } from 'react';

class RefreshNow extends Component {
    constructor(){
        super()
        this.autoRefresh= this.autoRefresh.bind(this)
    }
    autoRefresh(){
        this.forceUpdate()
    }
    render() {
        return (
            <div>
                <button onClick={this.autoRefresh} className='btn btn-success d-block mx-auto mt-5'>Refresh Now</button>
                <h1 className='text-center'>{Math.random()}</h1>
            </div>
        );
    }
}

export default RefreshNow;