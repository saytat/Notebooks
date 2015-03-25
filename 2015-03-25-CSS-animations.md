## CSS Animations

1. select the element to be animated: 
        html_element {
     			animation-name: flip;
                animation-duration: 2s;
                animation-timing-function: ease;
        }

2. define the animation:
		@keyframes flip {
        		start {
                }
                
                stop {
                }
        }
   OR
       
       @keyframes flip {
                    0% {
                    }
                    
                    33% {
                    }
                    
                    66% {
                    }
                    
                    100% {
                    }
            }

3. Set animation parameters:
			html_element {
            		animation-name: ;
                    animation-duration: ; //10ms, 1s etc. in seconds and ms only.
                    animation-timing-function: ; //ease, ease-in,ease-out,ease-in-out,linear, step-start,step-end, cubic-bezier(0.1, 0.7, 1.0, 0.1), steps(4,end)
                    animation-iteration-count:1 ;//numbers or __infinite__
					animation-direction: normal;// keywords available: normal, reverse, alternate, alternate-reverse, initial, inherit.
                    animation-delay: 4s; //delays the animation start time, can have negative value.
                    animation-fill-mode: forwards;//forwards, backwards. If forwards then the value of the first keyframe is set before animation starts. If backwards then the value of the last keyframe is set after animation stops.
            }

##Example 1

**html**

    <ul>
      <li><p>learn <span id="first">coding</span></p></li>
      <li><p>make <span>things</span></p></li>
    </ul>
    
**css**

      ul {
              list-style: none;
              font-family: sans-serif;
              font-size: 3em;
      }
      
      #first {
              color: blue;
      }
      
      #first {
                animation-name: flip;
                animation-duration: 4s;
                animation-iteration-count: infinite;
                animation-timing-function: linear;
                animation-direction: alternate;
                animation-delay: 2s;
                animation-fill-mode: forwards;
                }
      
      @keyframes flip {
                33.3% {
                  color: black;
                  background: red;
                }
                
                66.6% {
                  color: red;
                  background: black;
                }
      
                86% {
                  color: white;
                  background: blue;
                }
      }

**html**: same

**css**: 

          ul {
            list-style: none;
            font-family: sans-serif;
            font-size: 3em;
          }
          
          #first {
            display: inline-block;
            color: blue;
          }
          
          a {
            text-decoration: none;
          }
          
          #first::before {
            content: "design";
            position: absolute;
            display: inline-block;
            background: transparent;
            color:white;
            opacity: 0.01;
          }
          
          #first:hover {
                          animation-name: loop;
                    animation-duration: 100ms;
                    animation-iteration-count: infinite;
                    animation-timing-function: step-in-out;
                    animation-direction: alternate;
                    animation-fill-mode: forwards;
                    }
          
          @keyframes loop {
                  33.3% {
                    color: black;
                    background: red;
                  }
                  66.6% {
                    color: red;
                    background: black;
                  }
            
                  86% {
                    color: white;
                    background: blue;
                  }
          }
          
          #first:before {
                    animation-name: flip;
                    animation-duration: 3s;
                    animation-iteration-count: infinite;
                    animation-timing-function: step-start;
          }
          
          /*#first:hover:before {
                          animation-name: loop;
                    animation-duration: 100ms;
                    animation-iteration-count: 1;
                    animation-timing-function: step-in-out;
                    animation-direction: alternate;
                    animation-fill-mode: forwards;
                    }  not working */
          
          
          
          
          
          @keyframes flip {
            
                  50% {
                    color: red;
                    background: white;
                    opacity: 1;
                  }
          }

