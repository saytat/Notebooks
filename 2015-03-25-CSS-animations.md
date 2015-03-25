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
					animation-direction: normal;                    
            }

Enter text in [Markdown](http://daringfireball.net/projects/markdown/). Use the toolbar above, or click the **?** button for formatting help.
