```html
<html>

<head>
    <!-- https://getbootstrap.com/docs/4.4/getting-started/introduction/ -->
    <!-- https://www.practicalecommerce.com/Create-Responsive-Ecommerce-Product-Pages-with-Bootstrap -->
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.4.1/css/bootstrap.min.css"
        integrity="sha384-Vkoo8x4CGsO3+Hhxv8T/Q5PaXtkKtu6ug5TOeNV6gBiFeWPGFN9MuhOf23Q9Ifjh" crossorigin="anonymous">
    <script src="https://code.jquery.com/jquery-3.4.1.slim.min.js"
        integrity="sha384-J6qa4849blE2+poT4WnyKhv5vZF5SrPo0iEjwBvKU7imGFAV0wwj1yYfoRSJoZ+n"
        crossorigin="anonymous"></script>
    <script src="https://cdn.jsdelivr.net/npm/popper.js@1.16.0/dist/umd/popper.min.js"
        integrity="sha384-Q6E9RHvbIyZFJoft+2mJbHaEWldlvI9IOYy5n3zV9zzTtmI3UksdQRVvoxMfooAo"
        crossorigin="anonymous"></script>
    <script src="https://stackpath.bootstrapcdn.com/bootstrap/4.4.1/js/bootstrap.min.js"
        integrity="sha384-wfSDF2E50Y2D1uUdj0O3uMBJnjuUD4Ih7YwaYd1iqfktj0Uod8GCExl3Og8ifwB6"
        crossorigin="anonymous"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css">
</head>

<body>
    <div class="container">
        <!-- For colors: https://getbootstrap.com/docs/4.5/components/navbar/#color-schemes -->
        <nav class="navbar navbar-light bg-light">
            <a class="navbar-brand" href="#">
                <img src="/image/bootstrap-solid.svg" width="30" height="30" alt="" loading="lazy">
                Book Bazzar
            </a>
            <form class="form-inline">
                <input class="form-control" type="search" placeholder="Search" aria-label="Search">
                <button class="btn btn-outline-success my-2 my-sm-0" type="submit">Search</button>
            </form>
        </nav>
        <nav class="navbar navbar-light bg-light">

        </nav>
    </div>
    <br />
    <br />
    <div class="container">
        <div class="row">
            <!-- <div class="col-md-4 fixed-top one"> -->
            <div class="col-md-4">
                <img src="image/java.jpeg" class="img-fluid" />
            </div>
            <!-- <div class="col-md-6 offset-sm-4 two"> -->
            <div class="col-md-6">
                <div class="row">
                    <div class="col-md-12">
                        <h1>Java Concurrency in Practice</h1>
                    </div>
                </div>
                <div class="row">
                    <div class="col-md-12">
                        <p class="font-weight-bold">
                            How Billionaire Businessman becomes the Head of States
                        </p>
                    </div>
                </div>
                <div class="row">
                    <div class="col-md-12">
                        <span class="badge badge-info">Book</span>
                        <span class="badge">Product No: 194827</span>
                    </div>
                </div>
                <div class="row">
                    <hr />
                </div>
                <div class="row">
                    <div class="col-md-4">
                        <!-- <span class="sr-only sr-only-focusable">Four out of Five Stars</span> -->
                        <i class="fa fa-star" aria-hidden="true"></i>
                        <i class="fa fa-star" aria-hidden="true"></i>
                        <i class="fa fa-star" aria-hidden="true"></i>
                        <i class="fa fa-star" aria-hidden="true"></i>
                        <i class="fa fa-star-o" aria-hidden="true"></i>

                        <span class="badge badge-success">61</span>
                    </div>
                    <div class="col-md-8">
                        <button type="button" class="btn btn-link">26 Ratings & 356 Reviews</button>
                    </div>
                </div>

                <br />
                <div class="row">
                    <div class="col-md-12">
                        <h2 class="product-price">$129.00</h2>
                    </div>
                </div><!-- end row -->

                <br />
                <div class="row">
                    <div class="col-md-1">
                        <span>
                            <button>
                                <i class="fa fa-plus" aria-hidden="true"></i>
                            </button>
                        </span>
                    </div>
                    <div class="col-md-2">
                        <span>
                            <input type="text" class="form-control w-100" value="1" maxlength="2" />
                        </span>
                    </div>
                    <div class="col-md-1">
                        <button>
                            <span>
                                <i class="fa fa-minus" aria-hidden="true"></i>
                            </span>
                        </button>
                    </div>
                    <div class="col-md-4" align="center">
                        <button type="button" class="btn btn-success btn-lg">
                            Buy Now
                        </button>
                    </div>
                    <div class="col-md-4" align="center">
                        <button type="button" class="btn btn-warning btn-lg">
                            Add to Cart
                        </button>
                    </div>
                </div>

                <br />

                <div class="row">
                    <div class="col-md-12 top-10">
                        <p>To order by telephone, <a href="tel:18005551212">please call 1-800-555-1212</a></p>
                    </div>
                </div><!-- end row -->

            </div>
        </div>
    </div>
</body>

</html>
```
