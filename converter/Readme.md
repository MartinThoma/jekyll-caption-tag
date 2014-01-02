You can adjust the Python code in this folder to convert WordPress
style caption tags

    [caption id="attachment_69281" align="aligncenter" width="229"]
        <a href="http://martin-thoma.com/wp-content/uploads/2013/06/amazon-double-domination.jpg">
            <img src="http://martin-thoma.com/wp-content/uploads/2013/06/amazon-double-domination-229x300.jpg" 
                 alt="Amazon doesn&#039;t like band no. 4 of &quot;The Dresden Files&quot;" 
                 width="229" height="300" class="size-medium wp-image-69281" />
        </a> Amazon doesn't like band no. 4 of "The Dresden Files"
    [/caption]

to my caption tags

    {% caption align="aligncenter" width="229" 
        caption="Amazon doesn't like band no. 4 of 'The Dresden Files'" 
        url="../images/2013/06/amazon-double-domination.jpg" 
        alt="Amazon doesn&#039;t like band no. 4 of &quot;The Dresden Files&quot;" 
        height="300" 
        class="size-medium wp-image-69281" 
        title="Amazon doesn't like band no. 4 of 'The Dresden Files'" %}

This is not necessary for my plugin, but it "could come in handy some 
day" :-)
