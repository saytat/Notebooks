## A New Post

Enter text in [Markdown](http://daringfireball.net/projects/markdown/). Use the toolbar above, or click the **?** button for formatting help.
HTML:

      <section>
        <div id='red'>
        </div>
        <div id='blue'>
        </div>
        <div id='grey'>
        </div>
      </section>

CSS:

    #red {
      display: inline-block;
      position: relative; //first block is positioned relative w.r.t. container
      background-color: red;
      width: 40%;
      height: 30%;
     /* top: 0; 
      left: 1%;
      bottom: 50%;
      right: 70%;*/
    }
    #blue {
      display: inline-block;
      position: absolute; //since display type is inline-block, the blue box is starting after red box ends, even though the red box is not visible. Why is the red box not visible???
      background-color: blue;
      width: 40%;
      height: 30%;
      left: 10%;
      /*bottom: 50%;
      right: 70%;*/
      }
 