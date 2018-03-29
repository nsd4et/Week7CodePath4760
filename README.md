# Project 7 - WordPress Pentesting

Time spent: **5** hours spent in total

> Objective: Find, analyze, recreate, and document **five vulnerabilities** affecting an old version of WordPress

## Pentesting Report
Due to the impact it had on my computer (as written below) and due to the fact that I did not open up the README.md template until after I had finsihed my GIFs my answers to some of these questions will not be technical or exact as, I really don't want to restart my computer multiple times this morning or have it black screen on me again. I will explain in depth what I did instead.

I included the screenshot from challenge 7 from the lab. It was just a screenshot of the alert that appeared from making a file's name XSS code.

1. My first vulnerability, named vul1 in the gif, was Authenticaed Stored Cross-Site Scripting. It was tested in 4.2. On the wordPress WPScane vulnerability database it said it was fixed in many different versions, I am unsure which one to put. I am assuming I should put the latest, which was 4.2.3.
In my GIF you can see the WPCan vulnerability database that the links sent me too and my wordpress on the right. I just typed the proof of concept into the post and posted it. I went to view the post and it didn't work. That is when I realized I needed it to be in text not visual. When I made that change and went back to the post, a link called link was there and when you clicked/moused over a box would appear saying 'test.' All that I did was try different links from the WPscan to see which ones has POC's that I would be able to use and show that this vulnerbaility was still there. I could not find where it affected the source code so I don't think it does.

2. My second vulnerbaility, named vul2 in the gif, 
 
1. (Optional) Vulnerability Name or ID
  - [ ] Summary: 
    - Vulnerability types:
    - Tested in version:
    - Fixed in version: 
  - [ ] GIF Walkthrough: 
  - [ ] Steps to recreate: 
  - [ ] Affected source code:
    - [Link 1](https://core.trac.wordpress.org/browser/tags/version/src/source_file.php) 

## Assets

List any additional assets, such as scripts or files

## Resources

- [WordPress Source Browser](https://core.trac.wordpress.org/browser/)
- [WordPress Developer Reference](https://developer.wordpress.org/reference/)

GIFs created with [LiceCap](http://www.cockos.com/licecap/).

## Notes

Describe any challenges encountered while doing the work:
Having both VMs up at once really killed my computer. It would get to a certain point where the VMs would catch up to each other and they would freeze. So I would be in the middle of a GIF recording with both VMs up and it would just stop so I would have to take a picture of what I typed and restart my computer to just show the vulnerability. This even caused my computer to black screen. This is the 2nd time because of this class my computer has done this. I don't have room to keep downloading all these VMs and programs and run it all at once. 

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
