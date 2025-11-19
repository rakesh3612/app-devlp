 <!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Web App with Menu Items</title>

    <!-- Bootstrap CSS -->
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet">

    <style>
        .navbar-brand {
            color: #308d46 !important;
            font-weight: bold;
        }
    </style>
</head>

<body>

    <!-- Navbar -->
    <nav class="navbar navbar-expand-lg navbar-light bg-light">
        <div class="container-fluid">

            <a class="navbar-brand" href="#">CMR Institute of Technology</a>

            <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarDropdownMenu">
                <span class="navbar-toggler-icon"></span>
            </button>

            <div class="collapse navbar-collapse" id="navbarDropdownMenu">
                <ul class="navbar-nav ms-auto">

                    <!-- Tutorials Dropdown -->
                    <li class="nav-item dropdown">
                        <a class="nav-link dropdown-toggle" href="#" id="tutorialsDropdown" role="button"
                           data-bs-toggle="dropdown" aria-expanded="false">
                            Tutorials
                        </a>

                        <ul class="dropdown-menu" aria-labelledby="tutorialsDropdown">
                            <li><a class="dropdown-item" href="#">HTML</a></li>
                            <li><a class="dropdown-item" href="#">CSS</a></li>
                            <li><a class="dropdown-item" href="#">JavaScript</a></li>
                        </ul>
                    </li>

                    <!-- Students Menu -->
                    <li class="nav-item">
                        <a class="nav-link" href="#">Students</a>
                    </li>

                    <!-- Jobs -->
                    <li class="nav-item">
                        <a class="nav-link" href="#">Jobs</a>
                    </li>

                    <!-- Courses -->
                    <li class="nav-item">
                        <a class="nav-link" href="#">Courses</a>
                    </li>

                </ul>
            </div>
        </div>
    </nav>

    <!-- Content -->
    <div class="container mt-4">
        <h2>Welcome to Web App</h2>
        <p>Select any menu item from the navbar.</p>
    </div>

    <!-- Bootstrap JS -->
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js"></script>

</body>
</html>
