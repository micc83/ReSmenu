jQuery ReSmenu
=======

**jQuery ReSmenu** is a very simple and lightweight (~1Kb) jQuery plugin that collapse ul menus into selects on responsive layouts. You can find some examples in the included demo or [here](http://codeb.it/resmenu/).

To use it you just have to include jQuery and a copy of the plugin in your head or footer:

    <script type="text/javascript" src="http://code.jquery.com/jquery-latest.js"></script>
    <script type="text/javascript" src="jquery.resmenu.min.js"></script>
    
Let's say this is your menu:

    <div class="menu_container">
        <ul class="toresponsive">
            <li><a href="/">Home</a></li>
            <li class="current-menu-item"><a href="test.htm">Link</a></li>
            <li><a href="test.htm">Link 2</a></li>
            <li><a href="test.htm">Link 3</a></li>
            <li><a href="test.htm">Link 4</a></li>
        </ul>
    </div>

Now the only thing to do is to trigger the menu with:

    $(window).ready(function () {
        $('.toresponsive').ReSmenu();
    });

If you need more control here's the plugin settings:

    $('.toresponsive').ReSmenu({
        menuClass:    'responsive_menu',   // Responsive menu class
        selectId:     'resmenu',          // select ID
        textBefore:   false,               // Text to add before the mobile menu
        selectOption: false,               // First select option
        activeClass:  'current-menu-item', // Active menu li class
        maxWidth:     480                  // Size to which the menu is responsive
    });
    
## Let's style your select

**ReSmenu** runs out of the box but if you want to style your select to better fit the container you can take advantage of the short css style taken from [twitter bootstrap](http://getbootstrap.com/):

    .responsive_menu select {
        display: block;
        width: 100%;
        height: 36px;
        padding: 6px 12px;
        font-size: 14px;
        line-height: 1.42857;
        color: rgb(85, 85, 85);
        vertical-align: middle;
        background-color: rgb(255, 255, 255);
        background-image: none;
        border: none;
    }
    
## Credits and contacts

ReSmenu has been made by [me](http://codeb.it). You can contact me at micc83@gmail.com or [twitter](https://twitter.com/Micc1983) for any issue or feauture request.
