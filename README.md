# UD12DiagramasER

<img width="428" alt="image" src="https://user-images.githubusercontent.com/99056015/164973124-1d37b0d0-84e6-4675-94a2-44e5d4413a43.png">
<img width="428" alt="image" src="https://user-images.githubusercontent.com/99056015/164973130-18317d8e-5423-4372-82e9-9f9546bbf7e5.png">
<img width="428" alt="image" src="https://user-images.githubusercontent.com/19403472/164485415-3574c1ba-195f-48d0-833a-3e3999a8588f.png">
<img width="428" alt="image" src="https://user-images.githubusercontent.com/19403472/164485405-f1fb76df-5593-424b-8e8a-1c1105b0e931.png">



<img width="428" alt="image" src="https://user-images.githubusercontent.com/99056015/164973141-ab146c68-2a3d-4d03-9ed6-afbda753e147.png">
<img width="428" alt="image" src="https://user-images.githubusercontent.com/99056015/164996345-dde9afac-3577-4486-a506-4dac78c8dbf4.png">

/*Valores categoria*/</br>
CREATE TABLE categoria(</br>
id_categoria int AUTO_INCREMENT PRIMARY KEY,</br>
nombre varchar(20) NOT NULL,</br>
descripcion mediumtext NULL</br>
);</br>

/*Valores receta*/</br>
CREATE TABLE receta(</br>
id_receta int AUTO_INCREMENT PRIMARY KEY,</br>
nombre varchar(20) NOT NULL,</br>
tiempototal int NOT NULL</br>
);</br>

/*Valores plato*/</br>
CREATE TABLE plato(</br>
id_plato int AUTO_INCREMENT PRIMARY KEY,</br>
descripcion mediumtext NULL,</br>
precio int NULL,</br>
id_categoria  int NOT NULL,</br>
id_receta  int NOT NULL,</br>
CONSTRAINT FK_categoria FOREIGN KEY (id_categoria)</br>
REFERENCES categoria(id_categoria)</br>
ON DELETE CASCADE ON UPDATE CASCADE,</br>
CONSTRAINT FK_plato_receta FOREIGN KEY (id_receta)</br>
REFERENCES receta(id_receta)</br>
ON DELETE CASCADE ON UPDATE CASCADE</br>

);

/*Valores Ingredientes*/</br>
CREATE TABLE ingredientes(</br>
id_ingrediente int AUTO_INCREMENT PRIMARY KEY,</br>
nombre varchar(20) NOT NULL,</br>
descripcion mediumtext NULL,</br>
ummedidad int NULL,</br>
calorias int NULL,</br>
stock int NULL</br>
);</br>

/*Valores Tiene tabla N-N*/</br>
CREATE TABLE tiene(</br>
	id_tiene int NOT NULL AUTO_INCREMENT PRIMARY KEY,</br>
    id_receta int NOT NULL,</br>
	id_ingrediente int NOT NULL,</br>
	CONSTRAINT FK_recetaa FOREIGN KEY (id_receta)</br>
    REFERENCES receta(id_receta)</br>
    ON DELETE CASCADE ON UPDATE CASCADE,</br>
    CONSTRAINT FK_ingredientee FOREIGN KEY (id_ingrediente)</br>
    REFERENCES ingredientes(id_ingrediente)</br>
    ON DELETE CASCADE ON UPDATE CASCADE</br>
);</br>


<img width="428" alt="image" src="https://user-images.githubusercontent.com/99056015/165063806-89f59c15-6498-4cad-be0e-7f160d050736.png">

<img width="428" alt="image" src="https://user-images.githubusercontent.com/99056015/164973148-418a8c3a-0910-449f-83f6-c500deee99f0.png">
<img width="428" alt="image" src="https://user-images.githubusercontent.com/99056015/164995746-a1455d1f-7987-4758-8e1b-15bf6325ba9e.png">


<img width="428" alt="image" src="https://user-images.githubusercontent.com/99056015/164973156-00c6f919-3644-4b08-a09c-a5b718d04904.png">
<img width="428" alt="image" src="https://user-images.githubusercontent.com/99056015/164973169-fce96534-61f1-455a-a917-ff1ee86e7bbe.png">
<img width="428" alt="image" src="https://user-images.githubusercontent.com/99056015/165325710-e3867d59-fe6a-4f67-8150-08079a86d938.png">
<img width="428" alt="image" src="https://user-images.githubusercontent.com/99056015/165325756-afcd487b-d241-4270-8196-9309a912fc1e.png">

<img width="428" alt="image" src="https://user-images.githubusercontent.com/99056015/164973175-322c46eb-d8ed-47e3-a749-7a072fea8042.png">
<img width="428" alt="image" src="https://user-images.githubusercontent.com/99056015/164973181-407b56c9-67ff-4835-a300-b86d5935c5cd.png">
<img width="428" alt="image" src="https://user-images.githubusercontent.com/99056015/164973189-829da80c-85f5-4382-ad08-5d075ff2da81.png">

<img width="428" alt="image" src="https://user-images.githubusercontent.com/99056015/164973455-f4e22ccd-400c-44c1-8140-a4f630fbfef6.jpeg">
<img width="428" alt="image" src="https://user-images.githubusercontent.com/99056015/164974408-234b6364-5299-4eff-be62-8352d43b7799.png">
<img width="428" alt="image" src="https://user-images.githubusercontent.com/99056015/165313372-d92c82a2-a90c-4b73-893c-b7f0469390f3.png">
<img width="428" alt="image" src="https://user-images.githubusercontent.com/99056015/165313403-0e8dcaa3-ada7-48dc-8572-49cf167b5fb7.png">

<img width="428" alt="image" src="https://user-images.githubusercontent.com/99056015/164973197-f0753498-9819-4a90-95b8-6e740347199b.png">
<img width="428" alt="image" src="https://user-images.githubusercontent.com/99056015/164974389-44c7e9ae-e90d-44b1-84b4-ef8f9a30e2b7.jpeg">

<img width="428" alt="image" src="https://user-images.githubusercontent.com/99056015/164973210-82e3503d-534d-469f-a180-4b2604baa198.png">
<img width="428" alt="image" src="https://user-images.githubusercontent.com/99056015/165269478-557a1ea4-a3c1-415f-ad17-99051e8a0ee0.png">
<img width="428" alt="image" src="https://user-images.githubusercontent.com/99056015/165269577-e21c4420-2eeb-4d89-b4e0-820cbe48c654.png">

<img width="428" alt="image" src="https://user-images.githubusercontent.com/99056015/164973219-977a8b3c-1181-470e-a433-0b991ba67719.png">
<img width="428" alt="image" src="https://user-images.githubusercontent.com/99056015/165259360-d74e4e94-a379-4393-92d0-670515fb0695.png">
<img width="428" alt="image" src="https://user-images.githubusercontent.com/99056015/165259548-a47e938f-7680-4a56-a18d-308ab3126503.png">

<img width="428" alt="image" src="https://user-images.githubusercontent.com/99056015/164973232-4351f024-09e4-41e7-a46f-0292f48b153c.png">
<img width="428" alt="image" src="https://user-images.githubusercontent.com/99056015/164973240-87b3c19c-6fcc-490e-ad15-2d30a4ed66f6.png">
<img width="428" alt="image" src="https://user-images.githubusercontent.com/99056015/165389977-c16112d1-d782-44ce-8f75-21797be688e3.png">
<img width="428" alt="image" src="https://user-images.githubusercontent.com/99056015/165390038-025aff0f-6d29-4e9e-bed2-4918f6020c6c.png">

<img width="428" alt="image" src="https://user-images.githubusercontent.com/99056015/164973244-d3e6da94-7985-4e13-9db1-27a37d4a953c.png">


<img width="428" alt="image" src="https://user-images.githubusercontent.com/99056015/164973252-ef9afd67-47c7-47de-922f-3cc097778f07.png">


<img width="428" alt="image" src="https://user-images.githubusercontent.com/99056015/165559889-c098eac6-3652-4739-90ba-96e2a3d9f84c.png">
<img width="428" alt="image" src="https://user-images.githubusercontent.com/99056015/165559941-a43dbfdd-1a83-4aaf-9c15-ad2a9c9e36da.png">

<img width="428" alt="image" src="https://user-images.githubusercontent.com/99056015/164973260-51d1af8a-794d-44a4-bb17-9e7b8848a66f.png">
<img width="428" alt="image" src="https://user-images.githubusercontent.com/99056015/164973265-6349759d-d254-4938-832a-96d1dca0a7d9.png">
<img width="428" alt="image" src="https://user-images.githubusercontent.com/99056015/164973271-bb6667fd-2eba-4d18-bf11-350f573a9597.png">
pillar de aixa
