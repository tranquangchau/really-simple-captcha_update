### First 
```sh
Download plugin for wordpress and pass to wp-content/plugin/
Go admin page, plugin, and active by name plugin
```

### Two, create an instance of ReallySimpleCaptcha class: (at file function)

```sh
$captcha_instance = new ReallySimpleCaptcha();
$captcha_instance->bg = array( 0, 0, 0 );
$word = $captcha_instance->generate_random_word();
$prefix="ccc_";
$url_file = $captcha_instance->generate_image( $prefix, $word );
```

```sh 
<img src="<?php echo $url_file;?>"/>
```

### Check the correctness of the answer in ajax function or function basic file
```sh
$captcha_instance = new ReallySimpleCaptcha();
$correct = $captcha_instance->check( $prefix, $the_answer_from_respondent );
$captcha_instance->remove( $prefix );  //remove file
```

That’s all.
https://wordpress.org/plugins/really-simple-captcha/

