# bootstrap5-togglepassword

Toggle Password v1.0.0

Description:
Toggle password visibility by simply adding $('[type="password"]).togglepassword(); to your javascript

Works with the following dependencies:
* Bootstrap v5.3 (https://getbootstrap.com/docs/5.3/)
* Bootstrap Icons v1.11.1 (https://icons.getbootstrap.com/)
* jQuery v3.7.1 (https://jquery.com/)
  
How to use:
1. Add Bootstrap CSS and Bootstrap Icons CSS files to your <head> tag
2. Add jQuery JS file to your <body> tag, preferable at the end of the body
3. Add the bootstrap5-togglepassword JS file after the jQuery script
4. Include the line on your Document Load event:
   $('[type="password"]).togglepassword();

Sample code:

<!doctype html>
<html lang="en" data-bs-theme="light">

<head>
    <meta charset="utf-8">
    <title>Sample</title>
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="assets/css/bootstrap.min.css">
    <link rel="stylesheet" href="assets/css/bootstrap-icons.css">
</head>

<body>

    <main>
        <div class="bg-body-secondary d-flex align-items-center justify-content-center vh-100 p-3">
            <div class="card w-100" style="max-width: 20rem;">
                <div class="card-body">
                    <form data-role="form" data-action="action/login" autocomplete="off">
                        <fieldset>
                            <div class="mb-3">
                                <label class="form-label" for="username">Username</label>
                                <input type="text" class="form-control" id="username" name="username" required autofocus>
                            </div>
                            <div class="mb-3">
                                <label class="form-label" for="password">Password</label>
                                <input type="password" class="form-control" id="password" name="password" required>
                            </div>
                            <button class="btn btn-primary w-100">Login</button>
                        </fieldset>
                    </form>
                </div>
            </div>
        </div>

    </main>

    <script src="assets/js/bootstrap.bundle.min.js"></script>
    <script src="assets/js/jquery-3.7.1.min.js"></script>
    <script src="assets/js/togglepassword.js"></script>
    <script>
        $(() => {

            $('[type="password"]').togglepassword('btn');

        });
    </script>
</body>

</html>
