# Manual QA Assessment: Bug Evidence

Bug evidence from a manual QA technical assessment I completed for a previous job application. 
The app under test was a Spanish-language inventory web app with a login, user management and a product stock screen.

## Acceptance criteria (summary)

Summarized from the original assessment brief. The brief itself is not included in this repo because it contains test credentials.

- **Login:** valid username and password are required; an error message must appear when credentials are invalid or missing; follow the mockup.
- **User and product registration:** all fields are required and visually marked as required; name and last-name fields accept alphabetic values only; an error message appears when data is missing; follow the mockup.
- **Buttons:** every button in the site follows the mockup style: rounded border, blue background, white text.
- **Stock ("Almacén"):** the product table shows Código, Nombre and Cantidad; products display in blocks of 10 with a pagination bar; data can be filtered by Sucursal and Categoría; the search field filters as you type; products are ordered by Código ascending by default; Excel and PDF export buttons are shown and must export the table correctly; follow the mockup.

## What this shows about my approach

- Functional testing of login, user creation and stock screens against written acceptance criteria and mockups.
- Checking input handling with special characters and blank fields.
- Verifying that exports match the data shown on screen.
- Visual and text checks (typos, mockup mismatches and display errors).
- Clear evidence: one issue per capture, annotated, with screen recordings for steps that need motion.

## Evidence

| File | What it shows | Expected per the criteria |
| --- | --- | --- |
| [BUG01.gif](evidence/BUG01.gif) | Login page: a username is entered with the password left empty, then "Entrar" is clicked. The page reloads, clears the username field, and shows no validation or error message. | An error message must appear when credentials are missing or invalid. |
| [BUG02.PNG](evidence/BUG02.PNG) | Users list includes a user whose last name is blank (marked in red). | All registration fields are required; a user cannot be created without a last name. |
| [BUG03.PNG](evidence/BUG03.PNG) | "Registrar usuario" form with a green "Crear" button (marked in red). | The mockup shows a blue "Registrar" button; all buttons must share the mockup style (rounded border, blue, white text). |
| [BUG04.PNG](evidence/BUG04.PNG) | Users list with names and last names containing numbers and special characters, e.g. "123 Tommy @" and "Zabado@23" (marked in red). | Name and last-name fields must accept alphabetic values only; these records should have been rejected at registration. |
| [BUG05.PNG](evidence/BUG05.PNG) | Users page with the left navigation menu marked in red: the active section ("Usuarios") has no color or highlight indicator, so you cannot tell which section you are in. | Reported as a usability issue; not tied to a specific written criterion. |
| [BUG06.PNG](evidence/BUG06.PNG) | Stock page ("Productos en existencia") with the area between the title and the table marked in red: the "Sucursal" and "Categoría" filter dropdowns from the mockup are missing. | Products must be filterable by Sucursal and Categoría, as shown in the mockup. |
| [BUG07.gif](evidence/BUG07.gif) | Stock page: after searching for "girl" and adding 12 units to "Gossip Girl" (the page shows Existencia = 12), the exported Excel report still shows 0 for that product. The export does not reflect the quantity just entered. | Excel and PDF exports must reproduce the table correctly. |
| [BUG08.PNG](evidence/BUG08.PNG) | A product's stock quantity displays as `[object Object]` instead of a number (marked in red). | The table must show each product's quantity as a number. |
| [Typo_1.PNG](evidence/Typo_1.PNG) | The form title reads "Registrar usaurio" (underlined in red). | Correct spelling: "Registrar usuario", as in the mockup. |
| [Typo_2.PNG](evidence/Typo_2.PNG) | The page title reads "Productos en exsitencia" (underlined in red). | Correct spelling: "Productos en existencia", as in the mockup. |
