**Web**

1. **Trifecta’s Trail**

**Difficulty:** Easy/ 100 points

**Description:**  
hey guys check out this cool website i just found the author must be quite the writer he explained vulnerabilities like a true gentlement iykyk buttt i think they might be something fishy going on they check it out\!\!\! here ya go user : [https://balakumaran1507.github.io/Trifecta\_CTF/](https://balakumaran1507.github.io/Trifecta_CTF/)

**Solution:**  
The challenge name “Trifecta” was basically screaming *three stages, bro*. So I popped open the page source and, yep, there were three sneaky Base64 strings chilling in different corners of the files.

* **Layer 1** – Hiding in the CSS like it owned the place, tucked inside a `content:` property.

* **Layer 2** – Sitting in the HTML under the XSS section, trying to act like a command line snippet. Nice try.

* **Layer 3** – Just vibing in the linked JavaScript file.

Decoded each of them one by one, slapped the pieces together like digital LEGO, and boom the full flag popped out.

Flag: **NOCT{im\_just\_wasting\_ur\_time}**


2. **Dumb Bots**

**Difficulty:** Easy/ 100 points

**Description:**

ayoooo its me again ofc im again with a super cool website well sooner or later this author gonna blow up like litterally.... may god bless his soul here ya go bud : [https://balakumaran1507.github.io/fck\_bots\_CTF/](https://balakumaran1507.github.io/fck_bots_CTF/)

**Solution:**

First stop — robots.txt. Always worth a peek to see what the site doesn’t want you snooping around in. Sure enough, it had a `/unlisted/` path sitting there like a neon “come check me out” sign.

![unlisted](https://github.com/user-attachments/assets/cc34185f-c1df-4503-96ca-71d3934cafcb)

Rolled over to that directory, and there it was `flag.txt` just chilling. Opened it up, and boom… flag secured.

![dumbbots](https://github.com/user-attachments/assets/7b785ee7-8be2-473b-93c4-2e6430336811)

Flag: **NOCT{bots\_reveal\_too\_much}**


3. **Lost In Your Eyes💗**

**Difficulty:** Easy/ 200 points

**Description:**

its me again you guessed it right im back with another super cool website ofc same as the great author himself this time he into some shady stuff help me uncover whats he is hiding despite knowing they is nothing? where do you look? they is something in something that never existed? well thats for you to figure it out : [https://balakumaran1507.github.io/lost\_in\_ur\_eyes\_CTF/](https://balakumaran1507.github.io/lost_in_ur_eyes_CTF/)

**Solution:**

Checked the page source and spotted a `console.log` near the bottom that screamed “look at the JS file.”

\<ADD IMAGE\>

\<ADD IMAGE\>

Popped open the JS in the site’s resources and saw a `parts` array loaded with Base64 chunks. Decoded them, stitched them together, and boom  full flag unlocked.

Flag: **NOCT{not\_found\_but\_achieved}**


4. **One Last Time 🥂**

**Difficulty:** Easy/ 200 points

**Description:** 

hear me out okay?\! i just have one last super dexule cool website to show you just one more and i promise this is the last of the great authors website well its pretty sad our journey ends here but it was a good one player here ya go ur last target take him down: [https://balakumaran1507.github.io/LSB\_shapes\_CTF/](https://balakumaran1507.github.io/LSB_shapes_CTF/) all he wanted was to make websites for her and u distoryed every single on of em.... i hope u feel good with those points...

**Solution:**

Hit the GitHub Pages URL, poked around the source and assets, and spotted a weirdly named `smaple.svg` (yep, typo).

![sample](https://github.com/user-attachments/assets/05d82314-7c3a-440e-b780-01ffdb51deaf)

Cracked it open and found a `<metadata>` tag holding an `EncodedFlag` value, while the `<desc>` was just there to throw me off.

![meta](https://github.com/user-attachments/assets/b2dec508-fa3a-4fa0-8de0-b16ce206e042)

Grabbed the Base64 string from the metadata, decoded it, and boom flag in hand.

Flag: **NOCT{svg\_svg\_svg}**

