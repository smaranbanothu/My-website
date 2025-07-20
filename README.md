<!DOCTYPE html>
<html>
<head>
  <title>Typewriter</title>
</head>
<body>

  <h2 id="type"></h2>
  <p id="paragraph"></p>

  <script>
    // For heading
    let headingText = "Smaran's Website";
    let i = 0;

    function typewriterHeading() {
      if (i < headingText.length) {
        document.getElementById("type").innerHTML += headingText.charAt(i);
        i++;
        setTimeout(typewriterHeading, 100);
      }
    }

    // For paragraph
    let paraText = "Welcome to Smaran website.i am smaran ,this is my website. for more details email to banothusmaran@gmail.com.";
    let j = 0;

    function typewriterParagraph() {
      if (j < paraText.length) {
        document.getElementById("paragraph").innerHTML += paraText.charAt(j);
        j++;
        setTimeout(typewriterParagraph, 100);
      }
    }

    // Start both typewriters
    typewriterHeading();      // Start heading first
    setTimeout(typewriterParagraph, headingText.length * 100 + 500); // Start paragraph after heading finishes
  </script>

</body>
</html>
