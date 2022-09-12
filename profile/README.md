<div id="header" align="center">
   <img src="https://raw.githubusercontent.com/KawaiiTeaCup/.github/main/profile/Chilling%20Tea%20-%20Copy%401-1280x544%20(1).jpg" width="max"/>
   <div id="badges">
      <a href="https://twitter.com/TeaLover1M">
      <img src="https://img.shields.io/badge/TheKawaiiTee-%231DA1F2.svg?style=for-the-badge&logo=Twitter&logoColor=white" alt="Twitter Badge" />
      </a>
      <a href="https://discord.gg/NB9vMf9P8N">
      <img src="https://img.shields.io/badge/KawaiiTeeKlub-%235865F2.svg?style=for-the-badge&logo=discord&logoColor=white" alt="Discord Badge" />
      </a>
      <a href="https://github.com/WithPeko/">
      <img src="https://img.shields.io/badge/WithPeko-%23121011.svg?style=for-the-badge&logo=github&logoColor=white" alt="Github Badge" />
      </a>
   </div>
</div>

# [WithPeko](https://github.com/WithPeko/) builds open source software <3

```ts
// imports :)
import * as interestingText from "./interestingStuff.js";
import * as gitFunctions from "./helpers/gitFunctions.js";

// psst, super secret credentials
gitFunctions.creds(process.env);

// get the file from the repo
const file = await gitFunctions.repos(".github").dir("profile").file("README.md");

// now edit the file
const response = await file.edit({
  text: interestingText,
  encoding: "utf-8",
  commitMessage: "add interesting stuff to the README",
});

// run if the process fails
if (response.fail) {
  console.log("Could not add interesitng stuff to the README @_@");
  console.log(response.error.toString());
}

/**
 * Output:
 * Could not add interesitng stuff to the README @_@
 * File `interestingStuff.js` does not exist
 */
```
