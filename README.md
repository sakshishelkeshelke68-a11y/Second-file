# Second-file
<!DOCTYPE html>

<html lang="en">

<head>

    <meta charset="UTF-8">

    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <title>Book Acquisition & Cataloging</title>

    

    <style>

        /* Selects the body element (the entire visible page) */

        body {

            background-color: #f0f8ff; /* Light Blue/Alice Blue */

            font-family: Arial, sans-serif;

            margin: 20px;

        }



        /* Basic styling for the header */

        header {

            text-align: center;

            padding: 10px;

            background-color: #007bff; /* A darker blue for contrast */

            color: white;

            border-radius: 5px;

        }



        /* Style for the main content section */

        #add-book-and-purchase-details {

            max-width: 600px;

            margin: 30px auto;

            padding: 20px;

            background-color: white;

            border: 1px solid #ccc;

            border-radius: 8px;

            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);

        }



        /* Style for form elements to make them look cleaner */

        fieldset {

            border: 1px solid #ddd;

            padding: 15px;

            border-radius: 5px;

            margin-bottom: 20px;

        }

        

        label {

            display: inline-block;

            width: 150px;

            margin-bottom: 8px;

            font-weight: bold;

        }

        

        input[type="text"], 

        input[type="number"],

        select {

            width: calc(100% - 160px); /* Adjust width considering label */

            padding: 8px;

            margin-bottom: 10px;

            border: 1px solid #ccc;

            border-radius: 4px;

        }



        button[type="submit"] {

            background-color: #28a745;

            color: white;

            padding: 10px 15px;

            border: none;

            border-radius: 4px;

            cursor: pointer;

            font-size: 16px;

        }



        button[type="submit"]:hover {

            background-color: #218838;

        }

    </style>

</head>

<body>



    <header>

        <h1>📖 Book Acquisition Form</h1>

        <p>Use this form to add new purchased books to the library inventory.</p>

    </header>



    <main>

        <section id="add-book-and-purchase-details">

            <h2>➕ Enter New Book and Payment Details</h2>

            

            <form action="/api/catalog-new-book" method="POST">

                

                <fieldset>

                    <legend>Book Information</legend>

                    

                    <label for="name">Book Title (Name):</label>

                    <input type="text" id="name" name="name" required><br>



                    <label for="author">Author:</label>

                    <input type="text" id="author" name="author" required><br>



                    <label for="isbn">ISBN:</label>

                    <input type="text" id="isbn" name="isbn" placeholder="e.g., 978-1234567890" required><br>

                </fieldset>

                

                <fieldset>

                    <legend>Acquisition Details</legend>

                    

                    <label for="price">Purchase Price:</label>

                    <input type="number" id="price" name="price" step="0.01" min="0" required><br>



                    <label for="payment_method">Payment Method:</label>

                    <select id="payment_method" name="payment_method" required>

                        <option value="" disabled selected>Select Method</option>

                        <option value="credit_card">Credit Card</option>

                        <option value="bank_transfer">Bank Transfer</option>

                        <option value="cash">Cash</option>

                        <option value="invoice">Invoice / Credit</option>

                    </select><br>

                    

                    <label for="vendor">Vendor/Supplier:</label>

                    <input type="text" id="vendor" name="vendor"><br>

                </fieldset>

                

                <button type="submit">Submit and Add to Library</button>

            </form>

        </section>

    </main>



    <footer>

        <p>Note: This form requires a backend server to function.</p>

    </footer>



</body>

</html><!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Book Acquisition & Cataloging</title>
    
    <style>
        /* Selects the body element (the entire visible page) */
        body {
            background-color: #f0f8ff; /* Light Blue/Alice Blue */
            font-family: Arial, sans-serif;
            margin: 20px;
        }

        /* Basic styling for the header */
        header {
            text-align: center;
            padding: 10px;
            background-color: #007bff; /* A darker blue for contrast */
            color: white;
            border-radius: 5px;
        }

        /* Style for the main content section */
        #add-book-and-purchase-details {
            max-width: 600px;
            margin: 30px auto;
            padding: 20px;
            background-color: white;
            border: 1px solid #ccc;
            border-radius: 8px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
        }

        /* Style for form elements to make them look cleaner */
        fieldset {
            border: 1px solid #ddd;
            padding: 15px;
            border-radius: 5px;
            margin-bottom: 20px;
        }
        
        label {
            display: inline-block;
            width: 150px;
            margin-bottom: 8px;
            font-weight: bold;
        }
        
        input[type="text"], 
        input[type="number"],
        select {
            width: calc(100% - 160px); /* Adjust width considering label */
            padding: 8px;
            margin-bottom: 10px;
            border: 1px solid #ccc;
            border-radius: 4px;
        }

        button[type="submit"] {
            background-color: #28a745;
            color: white;
            padding: 10px 15px;
            border: none;
            border-radius: 4px;
            cursor: pointer;
            font-size: 16px;
        }

        button[type="submit"]:hover {
            background-color: #218838;
        }
    </style>
</head>
<body>

    <header>
        <h1>📖 Book Acquisition Form</h1>
        <p>Use this form to add new purchased books to the library inventory.</p>
    </header>

    <main>
        <section id="add-book-and-purchase-details">
            <h2>➕ Enter New Book and Payment Details</h2>
            
            <form action="/api/catalog-new-book" method="POST">
                
                <fieldset>
                    <legend>Book Information</legend>
                    
                    <label for="name">Book Title (Name):</label>
                    <input type="text" id="name" name="name" required><br>

                    <label for="author">Author:</label>
                    <input type="text" id="author" name="author" required><br>

                    <label for="isbn">ISBN:</label>
                    <input type="text" id="isbn" name="isbn" placeholder="e.g., 978-1234567890" required><br>
                </fieldset>
                
                <fieldset>
                    <legend>Acquisition Details</legend>
                    
                    <label for="price">Purchase Price:</label>
                    <input type="number" id="price" name="price" step="0.01" min="0" required><br>

                    <label for="payment_method">Payment Method:</label>
                    <select id="payment_method" name="payment_method" required>
                        <option value="" disabled selected>Select Method</option>
                        <option value="credit_card">Credit Card</option>
                        <option value="bank_transfer">Bank Transfer</option>
                        <option value="cash">Cash</option>
                        <option value="invoice">Invoice / Credit</option>
                    </select><br>
                    
                    <label for="vendor">Vendor/Supplier:</label>
                    <input type="text" id="vendor" name="vendor"><br>
                </fieldset>
                
                <button type="submit">Submit and Add to Library</button>
            </form>
        </section>
    </main>

    <footer>
        <p>Note: This form requires a backend server to function.</p>
    </footer>

</body>
</html><!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Book Acquisition & Cataloging</title>
    
    <style>
        /* Selects the body element (the entire visible page) */
        body {
            background-color: #f0f8ff; /* Light Blue/Alice Blue */
            font-family: Arial, sans-serif;
            margin: 20px;
        }

        /* Basic styling for the header */
        header {
            text-align: center;
            padding: 10px;
            background-color: #007bff; /* A darker blue for contrast */
            color: white;
            border-radius: 5px;
        }

        /* Style for the main content section */
        #add-book-and-purchase-details {
            max-width: 600px;
            margin: 30px auto;
            padding: 20px;
            background-color: white;
            border: 1px solid #ccc;
            border-radius: 8px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
        }

        /* Style for form elements to make them look cleaner */
        fieldset {
            border: 1px solid #ddd;
            padding: 15px;
            border-radius: 5px;
            margin-bottom: 20px;
        }
        
        label {
            display: inline-block;
            width: 150px;
            margin-bottom: 8px;
            font-weight: bold;
        }
        
        input[type="text"], 
        input[type="number"],
        select {
            width: calc(100% - 160px); /* Adjust width considering label */
            padding: 8px;
            margin-bottom: 10px;
            border: 1px solid #ccc;
            border-radius: 4px;
        }

        button[type="submit"] {
            background-color: #28a745;
            color: white;
            padding: 10px 15px;
            border: none;
            border-radius: 4px;
            cursor: pointer;
            font-size: 16px;
        }

        button[type="submit"]:hover {
            background-color: #218838;
        }
    </style>
</head>
<body>

    <header>
        <h1>📖 Book Acquisition Form</h1>
        <p>Use this form to add new purchased books to the library inventory.</p>
    </header>

    <main>
        <section id="add-book-and-purchase-details">
            <h2>➕ Enter New Book and Payment Details</h2>
            
            <form action="/api/catalog-new-book" method="POST">
                
                <fieldset>
                    <legend>Book Information</legend>
                    
                    <label for="name">Book Title (Name):</label>
                    <input type="text" id="name" name="name" required><br>

                    <label for="author">Author:</label>
                    <input type="text" id="author" name="author" required><br>

                    <label for="isbn">ISBN:</label>
                    <input type="text" id="isbn" name="isbn" placeholder="e.g., 978-1234567890" required><br>
                </fieldset>
                
                <fieldset>
                    <legend>Acquisition Details</legend>
                    
                    <label for="price">Purchase Price:</label>
                    <input type="number" id="price" name="price" step="0.01" min="0" required><br>

                    <label for="payment_method">Payment Method:</label>
                    <select id="payment_method" name="payment_method" required>
                        <option value="" disabled selected>Select Method</option>
                        <option value="credit_card">Credit Card</option>
                        <option value="bank_transfer">Bank Transfer</option>
                        <option value="cash">Cash</option>
                        <option value="invoice">Invoice / Credit</option>
                    </select><br>
                    
                    <label for="vendor">Vendor/Supplier:</label>
                    <input type="text" id="vendor" name="vendor"><br>
                </fieldset>
                
                <button type="submit">Submit and Add to Library</button>
            </form>
        </section>
    </main>

    <footer>
        <p>Note: This form requires a backend server to function.</p>
    </footer>

</body>
</html><!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Book Acquisition & Cataloging</title>
    
    <style>
        /* Selects the body element (the entire visible page) */
        body {
            background-color: #f0f8ff; /* Light Blue/Alice Blue */
            font-family: Arial, sans-serif;
            margin: 20px;
        }

        /* Basic styling for the header */
        header {
            text-align: center;
            padding: 10px;
            background-color: #007bff; /* A darker blue for contrast */
            color: white;
            border-radius: 5px;
        }

        /* Style for the main content section */
        #add-book-and-purchase-details {
            max-width: 600px;
            margin: 30px auto;
            padding: 20px;
            background-color: white;
            border: 1px solid #ccc;
            border-radius: 8px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
        }

        /* Style for form elements to make them look cleaner */
        fieldset {
            border: 1px solid #ddd;
            padding: 15px;
            border-radius: 5px;
            margin-bottom: 20px;
        }
        
        label {
            display: inline-block;
            width: 150px;
            margin-bottom: 8px;
            font-weight: bold;
        }
        
        input[type="text"], 
        input[type="number"],
        select {
            width: calc(100% - 160px); /* Adjust width considering label */
            padding: 8px;
            margin-bottom: 10px;
            border: 1px solid #ccc;
            border-radius: 4px;
        }

        button[type="submit"] {
            background-color: #28a745;
            color: white;
            padding: 10px 15px;
            border: none;
            border-radius: 4px;
            cursor: pointer;
            font-size: 16px;
        }

        button[type="submit"]:hover {
            background-color: #218838;
        }
    </style>
</head>
<body>

    <header>
        <h1>📖 Book Acquisition Form</h1>
        <p>Use this form to add new purchased books to the library inventory.</p>
    </header>

    <main>
        <section id="add-book-and-purchase-details">
            <h2>➕ Enter New Book and Payment Details</h2>
            
            <form action="/api/catalog-new-book" method="POST">
                
                <fieldset>
                    <legend>Book Information</legend>
                    
                    <label for="name">Book Title (Name):</label>
                    <input type="text" id="name" name="name" required><br>

                    <label for="author">Author:</label>
                    <input type="text" id="author" name="author" required><br>

                    <label for="isbn">ISBN:</label>
                    <input type="text" id="isbn" name="isbn" placeholder="e.g., 978-1234567890" required><br>
                </fieldset>
                
                <fieldset>
                    <legend>Acquisition Details</legend>
                    
                    <label for="price">Purchase Price:</label>
                    <input type="number" id="price" name="price" step="0.01" min="0" required><br>

                    <label for="payment_method">Payment Method:</label>
                    <select id="payment_method" name="payment_method" required>
                        <option value="" disabled selected>Select Method</option>
                        <option value="credit_card">Credit Card</option>
                        <option value="bank_transfer">Bank Transfer</option>
                        <option value="cash">Cash</option>
                        <option value="invoice">Invoice / Credit</option>
                    </select><br>
                    
                    <label for="vendor">Vendor/Supplier:</label>
                    <input type="text" id="vendor" name="vendor"><br>
                </fieldset>
                
                <button type="submit">Submit and Add to Library</button>
            </form>
        </section>
    </main>

    <footer>
        <p>Note: This form requires a backend server to function.</p>
    </footer>

</body>
</html><!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Book Acquisition & Cataloging</title>
    
    <style>
        /* Selects the body element (the entire visible page) */
        body {
            background-color: #f0f8ff; /* Light Blue/Alice Blue */
            font-family: Arial, sans-serif;
            margin: 20px;
        }

        /* Basic styling for the header */
        header {
            text-align: center;
            padding: 10px;
            background-color: #007bff; /* A darker blue for contrast */
            color: white;
            border-radius: 5px;
        }

        /* Style for the main content section */
        #add-book-and-purchase-details {
            max-width: 600px;
            margin: 30px auto;
            padding: 20px;
            background-color: white;
            border: 1px solid #ccc;
            border-radius: 8px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
        }

        /* Style for form elements to make them look cleaner */
        fieldset {
            border: 1px solid #ddd;
            padding: 15px;
            border-radius: 5px;
            margin-bottom: 20px;
        }
        
        label {
            display: inline-block;
            width: 150px;
            margin-bottom: 8px;
            font-weight: bold;
        }
        
        input[type="text"], 
        input[type="number"],
        select {
            width: calc(100% - 160px); /* Adjust width considering label */
            padding: 8px;
            margin-bottom: 10px;
            border: 1px solid #ccc;
            border-radius: 4px;
        }

        button[type="submit"] {
            background-color: #28a745;
            color: white;
            padding: 10px 15px;
            border: none;
            border-radius: 4px;
            cursor: pointer;
            font-size: 16px;
        }

        button[type="submit"]:hover {
            background-color: #218838;
        }
    </style>
</head>
<body>

    <header>
        <h1>📖 Book Acquisition Form</h1>
        <p>Use this form to add new purchased books to the library inventory.</p>
    </header>

    <main>
        <section id="add-book-and-purchase-details">
            <h2>➕ Enter New Book and Payment Details</h2>
            
            <form action="/api/catalog-new-book" method="POST">
                
                <fieldset>
                    <legend>Book Information</legend>
                    
                    <label for="name">Book Title (Name):</label>

            
