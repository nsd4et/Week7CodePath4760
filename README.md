# Project 7 - WordPress Pentesting

Time spent: **5** hours spent in total

> Objective: Find, analyze, recreate, and document **five vulnerabilities** affecting an old version of WordPress

## Pentesting Report
Due to the impact it had on my computer (as written below) and due to the fact that I did not open up the README.md template until after I had finsihed my GIFs my answers to some of these questions will not be technical or exact as, I really don't want to restart my computer multiple times this morning or have it black screen on me again. I will explain in depth what I did instead and include links/

I included the screenshot from challenge 7 from the lab. It was just a screenshot of the alert that appeared from making a file's name XSS code.

1. My first vulnerability, named vul1 in the gif, was Authenticaed Stored Cross-Site Scripting. It was tested in 4.2. On the wordPress WPScane vulnerability database it said it was fixed in many different versions, I am unsure which one to put. I am assuming I should put the latest, which was 4.2.3.
In my GIF you can see the WPCan vulnerability database that the links sent me too and my wordpress on the right. I just typed the proof of concept into the post and posted it. I went to view the post and it didn't work. That is when I realized I needed it to be in text not visual. When I made that change and went back to the post, a link called link was there and when you clicked/moused over it, a box would appear saying 'test.' All that I did was try different links from the WPscan to see which ones has POC's that I would be able to use and show that this vulnerbaility was still there. I could not find where it affected the source code so I don't think it does.

2. My second vulnerbaility, named vul22 in the gif, was Authenticaed Stored Cross-Site Scripting in youtube urls embeds. It was also tested in 4.2. It was fixed in version 4.7.3.I also got this informatioin from the WPScan Vulnerability database. All my info for this assignment came from there. 
In my GIF you see just the wordpress post with the XSS for the youtube link. I update it and post it, go to view it and the alert box pops up. This was after my computer froze one of the times and I had to restart it. I didn't want it to do it again, so I didn't open up the Kali during it. I wanted very little things running so I could get the GIF. However, the link that I used for proof of concept is below. https://wpvulndb.com/vulnerabilities/8768
The steps in acquiring this was the same as the first one (and spolier alert, will be the same for the last one). I would just take the wpvulndb link from the scan and see if there was a decription and then go through all the reference links for any that had POC. I found githubs that showed where the code was affected but I did not undertsand what was going on. I have it posted below anyways. 
*/
  function wp_embed_handler_youtube( $matches, $attr, $url, $rawattr ) {
  	global $wp_embed;
 -	$embed = $wp_embed->autoembed( "https://youtube.com/watch?v={$matches[2]}" );
 +	$embed = $wp_embed->autoembed( sprintf( "https://youtube.com/watch?v=%s", urlencode( $matches[2] ) ) );
  
  	/**
  	 * Filters the YoutTube embed output.
    *
   * @global string $wp_version
   */
 -$wp_version = '4.8-alpha-40148';
 +$wp_version = '4.8-alpha-40160';
  
  /**
   * Holds the WordPress DB revision, increments when changes are made to the WordPress DB schema.
 
3. My last vulnerability, called vul3 in the gif, was AUthenticated Shortcode Tags (also XSS). It was tested in 4.2 and fixed in 4.3.1. 
In my gif you already see the test in the post, me updating the post and then vieiwng. This then leads to the alert box by hovering over with the mouse. This is the same reason as the second one, my computer froze and had to do all the restarting again. The link used for POC is https://wpvulndb.com/vulnerabilities/8186. I did the same steps as the first two in order to achieve this end result. That is how I would recreate it. I would just simply run the WPscan again and check all the links to see which ones had POC to use. I am also unsure where it affected the course code. That I just still don't understand. I apologize. There was this link given that walks through the code. https://blog.checkpoint.com/2015/09/15/finding-vulnerabilities-in-core-wordpress-a-bug-hunters-trilogy-part-iii-ultimatum/ 

## Assets

List any additional assets, such as scripts or files

## Resources

- [WordPress Source Browser](https://core.trac.wordpress.org/browser/)
- [WordPress Developer Reference](https://developer.wordpress.org/reference/)

GIFs created with [LiceCap](http://www.cockos.com/licecap/).

## Notes

Describe any challenges encountered while doing the work:
Having both VMs up at once really killed my computer. It would get to a certain point where the VMs would catch up to each other and they would freeze. So I would be in the middle of a GIF recording with both VMs up and it would just stop so I would have to take a picture of what I typed and restart my computer to just show the vulnerability. This even caused my computer to black screen. This is the 2nd time because of this class my computer has done this. I don't have room to keep downloading all these VMs and programs and run it all at once. 
I also apologize but I could not figure it out to save my life how to put the GIFs in the readme. This is the first time I am usualy GitHub so I do apologize for making life a little harder and not having everything together. 

## License

    Copyright [yyyy] [name of copyright owner]

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

        http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
