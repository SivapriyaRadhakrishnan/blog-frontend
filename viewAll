import axios from 'axios'
import React, { useEffect, useState } from 'react'
import Navbar from './Navbar'

const Viewall = () => {
    const [data,setData] = useState([

    ])

    const fetchData=()=>{
        axios.post("http://localhost:3030/viewall",{},{headers:{"token":sessionStorage.getItem("token"),"Content-Type":"application/json"}}).then(
            (response)=>{
                setData(response.data)
            }
        ).catch(
            (error)=>{
                console.log(error)
            }
        )
    }
    useEffect(()=>{fetchData()},[])
    return (
        <div>
            <Navbar/>
            <div className="container row">
                <div className="col col-12 col-sm-12 col-md-12 col-lg-12 col-xl-12 cl-xxl-12">
                    <div className="row g-3">
                        {data.map(
                            (value,index)=>{
                                return <div className="col col-12 col-sm-12 col-md-12 col-lg-12 col-xl-12 col-xxl-12">
                                    <div class="card" >
                                        <img src="..." class="card-img-top" alt="..." />
                                            <div class="card-body">
                                                <p class="card-text">{value.Message}</p>
                                                <p class="card-text">Posted on{value.postedDate}</p>
                                            </div>
                                    </div>
                                </div>
                            }
                        )}
                    </div>
                </div>
            </div>
        </div>
    )
}

export default Viewall
