<!DOCTYPE html>
<html>
<head>
	<meta charset="utf-8">
	<meta name="viewport" content="width=device-width, initial-scale=1">
	<title></title>
	<script type="text/javascript" src="https://cdnjs.cloudflare.com/ajax/libs/html2canvas/1.4.1/html2canvas.min.js"></script>
</head>
<body>
	<iframe src="https://www.brainwareuniversity.ac.in/studentselfservice/" frameborder="0" width="100%" height="500"></iframe>
	<button onclick="takeScreenshot()">Take Screenshot</button>
</body>
<script type="text/javascript">
	function takeScreenshot() {
		html2canvas(document.querySelector("body")).then(canvas => {
			const link = document.createElement("a");
			link.download = "screenshot.png";
			link.href = canvas.toDataURL('image/png');
			link.click();
		});
	}
</script>
</html>


