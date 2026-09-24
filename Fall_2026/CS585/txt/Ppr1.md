# End-To-End Arguments in System Design 

"End-to-End Arguments in System Design." Jerome H. Saltzer, David P. Reed & 
David D. Clark. ACM Transactions on Computer Systems (TOCS), 1984.

[[https://dl.acm.org/doi/pdf/10.1145/357401.357402|Text]]

## Definitions

- Firmware: 'Computer programs and data stored in hardware - typically in read-
  only memory'--https://csrc.nist.gov/glossary/term/firmware

## Quotes and Comments

> "The principle, called the end-to-end argument, suggests that functions placed at low levels of a system may be redundant or of little value when compared with the cost of providing them at that low level."
- Why is this the case? Is it common that most functionality is not left to the
  hardware? I.e. is this why there is all those layers above the physical?
  
### 1. Inroduction

> " In a broader context, the argument seems to apply to many other functions of a computer operating system, including its file system."
- To my knowledge it is true that the file system is laregley maintained by 
  software (the kernel), but I wonder how you know where to draw those lines? 
  How can you tell that you're putting to much burden on the hardware?

### 2. Careful File Transfer

#### 2.1 End-to-End Cartaking

> "Unfortunately, systematic countering of threat (2) requires writing correct programs, which is quite difficult."
- I feel like I've heard this many times over. Why is this so difficult? 
  Is it a lack of robust/routine testing? Is it a lack of CS standards? 
  
> "Then, as a final additional step, the part of the file transfer application residing in host B reads the transferred file copy back from its disk storage system into its own memory, recalculates the checksum, and sends this value back to host A, where it is compared with the checksum of the original."
- Nyo ho ho, they clearly don't know about the one's compliment approach. No 
  but seriously, it is cool to see how these methods have adapted over time.
  
> "Now let us consider the usefulness of a common proposal, namely, that the communication system provide, internally, a guarantee of reliable data transmis- sion...  but the careful file transfer application must still counter the remaining threats; so it should still provide its own retries based on an end-to-end checksum of the file"
- TLDR: applications will always need to provide safety measures, why then 
  put the burden on the hardware? 
  
### 2.2 A Too-Real Example

> "Application programmers, aware of this checksum, assumed that the network 
  was providing relaible transmission... Some of these source files were 
  corrupted by byte exchanges, and their owners were forced to the ultimate 
  end-to-end error check: manual comparison with and correction from old 
  lsitings."
- Cool example, demonstraates not only why moving this error checking off the 
  hardware is useful, but also an example of how things tend to break before 
  being fixed, as oposed to the other way around.
  
### 2.3 Performance Aspects

> "However, it would be too simplistic to conclude that the lower levels should play no part in obtaining reliability... The simple strategy outlined above, transmitting the file and then checking to see that the file has arrived correctly, would perform more poorly as the length of the file increased. The probability that all packets of a file arrive correctly decreases exponentially with the file length, and thus the expected time to transmit the file grows exponentially with file length."
- Call me out king! So it is not an either or, it must be a both and, 
  implementing safegaurds on both with performance and reliability being the 
  ultimate goal.

> "There is little reason to push in this direction very far, when it is considered that the end- to-end check of the file transfer application must still be implemented no matter how reliable the communication system becomes... It is probably not important to strive for a negligble error rate at any point below the application level."
- Cool, very cool!

> "Performing the function at the lower level may cost more--for two reasons. First, since the lower level subsystem is common to many applications, those applications that do not need the function will pay for it anyway."   
- Fuck, are they about to talk about the necessity to have more than one 
  transfer protocol in a precursor to what would become TCP and UDP? Fuck 
  *bites lip*. Nah but for real, why do we only have two protocols? Wouldn't 
  more variance allow for more specific needs to be met? Could this be a way 
  of moving things such as TLS out of the App layer?
  
  ## 3. Other Examples of the End-To-End Argument
  
  ### 3.1 Delivery Guarantees
  
  > 'The acknowledgment that is really desired is an end-to-end one, which can be originated only by the target application--"I did it," or "I didn't."'
  - The precursor to PACK and NACK, Wicked B)

## 4. Idenftifying the Ends
