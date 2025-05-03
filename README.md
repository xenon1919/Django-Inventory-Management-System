
# Django Inventory Management System

A web-based **Inventory Management System** built with **Django** to manage products efficiently. Features a modern, responsive UI with CRUD operations (Create, Read, Update, Delete) for product management. Uses Python 3.11, Django, Bootstrap 4, and crispy forms for a seamless user experience.

## Features
- **Add Products**: Create new products with details like name, SKU, price, quantity, and supplier.
- **View Products**: Display all products in a styled, responsive table.
- **Update Products**: Edit existing product details.
- **Delete Products**: Confirm and delete products securely.
- **Modern UI**: Large, bold elements, flexbox layouts, and a consistent product-themed SVG icon.
- **Responsive Design**: Adapts to mobile and desktop screens.
- **Form Styling**: Enhanced with `django-crispy-forms` and Bootstrap for clean input fields.
- **Tech Stack**: Django, Python 3.11, SQLite, Bootstrap 4.5.2, `crispy-bootstrap5`.


## Prerequisites
- **Python 3.11**
- **Pipenv** (for managing dependencies)
- **Git** (to clone the repository)

## Installation
1. **Clone the Repository**:
   ```bash
   git clone https://github.com/xenon1919/Django-Inventory-Management-System.git
   cd Django-Inventory-Management-System
   ```

2. **Set Up Virtual Environment**:
   ```bash
   pipenv install
   pipenv shell
   ```

3. **Apply Migrations**:
   ```bash
   python manage.py makemigrations
   python manage.py migrate
   ```

4. **Create a Superuser** (optional, for admin access):
   ```bash
   python manage.py createsuperuser
   ```

5. **Run the Development Server**:
   ```bash
   python manage.py runserver
   ```
   Open `http://127.0.0.1:8000` in your browser.

## Dependencies
Specified in `Pipfile`:
- `django`: Core framework.
- `django-crispy-forms`: Enhanced form rendering.
- `crispy-bootstrap5`: Bootstrap 5 template pack for crispy forms.

Install dependencies using:
```bash
pipenv install
```

## Project Structure
- **`invApp/`**: Django app containing models, views, and templates.
- **`templates/invApp/`**:
  - `layout.html`: Base template with navbar and Bootstrap 4.5.2.
  - `home.html`: Homepage with welcome message.
  - `product_form.html`: Form for adding products.
  - `product_list.html`: Table displaying all products.
  - `product_delete.html`: Confirmation for deleting products.
  - `product_update.html` (assumed): Form for updating products.
- **`static/`**: (Optional) CSS/JS files for custom styling.
- **`Pipfile`**: Dependency configuration.

## Usage
1. **Access the App**: Visit `http://127.0.0.1:8000` after starting the server.
2. **Navigate**: Use the navbar to:
   - Add a new product (`Add Product`).
   - View all products (`Show Products`).
   - Update or delete products from the product list.
3. **Admin Panel**: Access `/admin` with superuser credentials to manage products or users.

## Notes
- **Bootstrap Version Mismatch**:
  - The project uses **Bootstrap 4.5.2** in `layout.html` but includes `crispy-bootstrap5` for Bootstrap 5 form styling. This may cause minor styling inconsistencies (e.g., `form-control` or `btn` classes).
  - **Recommendation**: Either:
    - Upgrade to Bootstrap 5 in `layout.html`:
      ```html
      <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet">
      <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js"></script>
      ```
    - Or, switch to `crispy-bootstrap4` in `Pipfile`:
      ```toml
      crispy-bootstrap4 = "*"
      ```
      Then run `pipenv install`.
  - Current UI enhancements are styled to work with Bootstrap 4, ensuring compatibility.

- **Database**: Uses SQLite by default (Django’s default). For production, consider PostgreSQL or MySQL.
- **Static Files**: If you move inline CSS to `static/css/`, run `python manage.py collectstatic` and add `{% load static %}` to templates.

## Contributing
1. Fork the repository.
2. Create a feature branch (`git checkout -b feature/your-feature`).
3. Commit changes (`git commit -m 'Add your feature'`).
4. Push to the branch (`git push origin feature/your-feature`).
5. Open a Pull Request.

## License
MIT License. See `LICENSE` for details.

## Contact
For questions or suggestions, open an issue or contact [xenon1919] on GitHub.
