# College Admission Form - Bootstrap Practice Project

This project is a replica of a college admission form, created as a practice project while learning Bootstrap. The form includes a carousel of images, a detailed admission enquiry form, and various Bootstrap components and utilities for styling and layout.

## Table of Contents

- [Demo](#demo)
- [Features](#features)
- [Technologies Used](#technologies-used)
- [Setup](#setup)
- [File Structure](#file-structure)
- [Details](#details)
  - [HTML Structure](#html-structure)
  - [CSS Customization](#css-customization)
- [License](#license)

## Demo

You can view the live project [here](https://admission-form-bootstrap.vercel.app/).

## Features

- Responsive design using Bootstrap
- Image carousel for visual interest
- Detailed admission form with various input types
- Custom CSS for additional styling

## Technologies Used

- HTML5
- CSS3
- Bootstrap 5.1.3
- JavaScript

## Setup

1. Clone the repository:
    ```sh
    git clone https://github.com/N0AH-14/Bootstrap-Practice-Project
    ```
2. Open `index.html` in your preferred web browser.

## File Structure

```plaintext
.
├── index.html
├── style.css
└── README.md
```

## Details

### HTML Structure

The HTML file is structured with Bootstrap's grid system to ensure responsiveness. Here are the main components:

#### Head Section
- Bootstrap CSS CDN
- Custom CSS link
- Meta tags for responsive design

#### Body Section
- **Carousel**: Uses Bootstrap's carousel component to cycle through images.
- **Admission Form**: Includes various form controls such as text inputs, email input, telephone input, dropdowns for state and city, and more.

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Python Assignment 1</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.1.3/dist/css/bootstrap.min.css" rel="stylesheet">
    <link href="style.css" rel="stylesheet">
</head>
<body>
    <div class="container-fluid">
        <div class="row">
            <!-- Carousel Section -->
            <div class="col shadow-lg p-3 mb-5 bg-body-tertiary rounded ms-5 my-5 me-2">
                <div id="carouselExampleInterval" class="carousel slide" data-bs-ride="carousel">
                    <div class="carousel-inner">
                        <div class="carousel-item active" data-bs-interval="1000">
                            <img src="https://static.npfs.co/accounts/338/documents/2024/2/26/Admission%20open%20.jpg" class="d-block w-100" alt="Slide 1">
                        </div>
                        <div class="carousel-item" data-bs-interval="2000">
                            <img src="https://cdn.npfs.co/uploads/template/338/896/publish/images/4.png" class="d-block w-100" alt="Slide 2">
                        </div>
                        <div class="carousel-item">
                            <img src="https://static.npfs.co/accounts/338/documents/2024/2/26/Official%20Partner.jpg" class="d-block w-100" alt="Slide 3">
                        </div>
                    </div>
                    <button class="carousel-control-prev" type="button" data-bs-target="#carouselExampleInterval" data-bs-slide="prev">
                        <span class="carousel-control-prev-icon" aria-hidden="true"></span>
                        <span class="visually-hidden">Previous</span>
                    </button>
                    <button class="carousel-control-next" type="button" data-bs-target="#carouselExampleInterval" data-bs-slide="next">
                        <span class="carousel-control-next-icon" aria-hidden="true"></span>
                        <span class="visually-hidden">Next</span>
                    </button>
                </div>
            </div>
            <!-- Form Section -->
            <form class="col shadow-lg p-3 mb-5 bg-body-tertiary rounded me-5 my-5 ms-2 border">
                <h3>Admission Enquiry 2024 - 25</h3>
                <div class="container-fluid">
                    <!-- User Buttons -->
                    <div class="row mb-3">
                        <button type="button" class="btn btn-outline-light col">New User</button>
                        <button type="button" class="btn btn-outline-light col">Existing User</button>
                    </div>
                    <!-- Form Fields -->
                    <div class="row mb-3">
                        <input type="text" class="form-control" placeholder="Enter Name*" required>
                    </div>
                    <div class="row mb-3">
                        <input type="email" class="form-control" placeholder="Enter Email Address*" required>
                    </div>
                    <div class="row mb-3">
                        <select class="form-select col-2" id="countrycode" required>
                            <option value="+91" selected>+91</option>
                            <option value="+91">India(+91)</option>
                        </select>
                        <input type="tel" class="form-control col-10" placeholder="Preferably Whatsapp Number" required>
                    </div>
                    <div class="row mb-3">
                        <input type="text" class="form-control" placeholder="Enter OTP" required>
                    </div>
                    <div class="row mb-3">
                        <select class="form-select col" required>
                            <option value="" selected>Select State *</option>
                            <!-- Add other state options here -->
                        </select>
                        <select class="form-select col" name="State" required>
                            <option value="select city" selected>Select City</option>
                            <!-- Add city options here -->
                        </select>
                    </div>
                    <div class="row mb-3">
                        <select class="form-select" name="university_id" required>
                            <option value="" selected>Applying For *</option>
                            <option value="1500557">Transfer - UG</option>
                            <option value="1500431">Under Graduate</option>
                            <option value="1500432">Lateral - UG</option>
                            <option value="1500433">Post Graduate</option>
                            <option value="1500435">Certification</option>
                            <option value="1500436">Doctoral</option>
                        </select>
                    </div>
                    <div class="row mb-3">
                        <select class="form-select col" name="course_id" required>
                            <option value="" selected>Select Program *</option>
                            <!-- Add program options here -->
                        </select>
                        <select class="form-select col" name="specialization_id" required>
                            <option value="" selected>Select Specialization *</option>
                            <!-- Add specialization options here -->
                        </select>
                    </div>
                    <div class="row mb-3">
                        <img src="https://admission.poornima.edu.in/captcha" class="col" alt="captcha">
                        <input type="text" class="form-control col" placeholder="Enter text as shown" required>
                    </div>
                    <div class="row mb-3">
                        <input class="form-check-input col-1" type="checkbox" id="flexCheckDefault" required>
                        <label class="form-check-label col-11" for="flexCheckDefault">
                            I authorize Poornima University Jaipur to contact me with updates & notifications via Email, SMS, WhatsApp & voice call. This will override the registry on DND / NDNC. *
                        </label>
                    </div>
                    <div class="row mb-3">
                        <button type="submit" class="btn btn-primary col">Register</button>
                    </div>
                </div>
            </form>
        </div>
    </div>
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js"></script>
</body>
</html>
```

### CSS Customization

The CSS file (`style.css`) includes custom styles to enhance the form's appearance, such as border styling and background images.

```css
/* Custom border styles */
.border {
    border: 1px solid black;
    border-radius: 5px;
    background-color: rgb(255, 210, 21);
}

/* Background image styling */
.bgimg {
    background-image: url('https://cdn.npfs.co/uploads/template/338/896/publish/images/4.png');
    background-size: cover;
    background-repeat: no-repeat;
    background-position: center;
}
```

## License

This project is open-source and available under the [MIT License](LICENSE).
