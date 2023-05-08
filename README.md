Download Link: https://assignmentchef.com/product/solved-ve475-introduction-to-cryptography-homework-3
<br>
<strong>Ex. 1 –</strong><em> Finite fields</em>

<ol>

 <li>Show that X<sup>2</sup> + 1 is irreducible in F3[X].</li>

 <li>Why does the multiplicative inverse of 1 + 2X mod X<sup>2</sup> + 1 exist in F3[X]</li>

 <li>Find the multiplicative inverse of 1 + 2X mod X<sup>2</sup> + 1, in F3[X].</li>

</ol>

<strong>Ex. 2 –</strong><em> AES</em>

The goal of this exercise is to reshape the decryption of AES such that it has the same structure as encryption.

<ol>

 <li>First we determine the inverse of each layer.</li>

 <li>Describe<em> InvShiftRows</em> the inverse operation of ShiftRows.</li>

 <li>What is the inverse of the layer AddRoundKey?</li>

 <li>Explain why the transformation<em> InvMixColumns</em> is given by the multiplication by the matrix</li>

</ol>

⎛00001110 00001011 00001101 00001001⎜ ⎜ <sub>⎜</sub>00001001 00001110 00001011 00001101

<table>

 <tbody>

  <tr>

   <td>⎜</td>

  </tr>

 </tbody>

</table>

⎜ ⎝00001101 00001001 00001110 00001011

00001011 00001101 00001001 00001110

We call<em> InvSubBytes</em> the lookup table inverse of SubBytes.

<ol start="2">

 <li>Describe the decryption process using the previous transformations.</li>

 <li>Why can lnvShiftRows and lnvSubBytes be applied on reverse order?</li>

 <li>Similarly we want to inverse the order of application of AddRoundKey and lnvMixColumns.</li>

 <li>Why is it not possible to reverse the order of application of AddRoundKey and lnvMix­Columns?</li>

 <li>Calling the initial matrix<sub> (</sub><sub>ai,j</sub><sub>),</sub> the MixColumns matrix<sub> (</sub><sub>mi,j</sub><sub>),</sub> and the AddRoundKey matrix (ki,j), what is the result of applying first MixColumns and then AddRoundKey?</li>

 <li>Show that the inverse operation is given by</li>

</ol>

(ei,j) —* (mi,j)<sup>−</sup><sup>1</sup>(ei,j)<em> ED </em>(mi,j)<sup>−</sup><sup>1</sup>(ki,j).

<ol>

 <li>Define a new operations<em> InvAddRoundKey</em> such that “AddRounKey then lnvMixColumns” can be replaced by “lnvMixColumns then lnvAddRoundKey”.</li>

 <li>Conclude on how to process the decryption.</li>

 <li>What are the advantages of this strategy over simply reversing the order of application of the transformations?</li>

</ol>




<strong>Ex. 3 –</strong><em> DES</em>

<ol>

 <li>Research and explain how the DES cryptosystem works.</li>

 <li>Quickly explain linear and differential cryptanalysis.</li>

 <li>What is triple DES and why was it used instead of double DES?</li>

 <li>Explain how passwords are stored on Unix systems ? Is it a problem <em>Hint:</em> check man passwd and then follow the suggested man pages</li>

</ol>

<strong>Ex. 4 –</strong><em> Programming</em>

In the AES, choose two layers to implement in C. The 128 bits should be looked at as an unsigned char pointer. 0perations should be implemented using logical operators (and, or, and xor).

A bonus will be given for each extra layer implemented, and the generation of the S-Box. A big bonus will reward a complete implementation of the AES.