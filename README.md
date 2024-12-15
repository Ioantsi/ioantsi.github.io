<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Contact Information</title>
</head>
<body>
    <h1>Download Contact Information</h1>
    <p>Click the button below to download my contact details:</p>
    <button id="downloadBtn">Download vCard</button>

    <script>
        document.getElementById('downloadBtn').addEventListener('click', () => {
            const vCardContent = `BEGIN:VCARD
VERSION:3.0
FN:John Doe
TEL:+1234567890
EMAIL:john.doe@example.com
ORG:Your Organization
END:VCARD`;

            const blob = new Blob([vCardContent], { type: 'text/vcard' });
            const link = document.createElement('a');
            link.href = URL.createObjectURL(blob);
            link.download = 'contact.vcf';
            link.click();
        });
    </script>
</body>
</html>
