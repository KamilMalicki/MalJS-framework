Mal.js
Copyright ® Kamil Malicki 2023/2024
framework version {1.0.0}

Mal JS to framework napisany w języku
JavaScript, który ułatwia oraz dodaje
wiele nowych funkcji. Możesz go użyć
do aplikacji konsolowych oraz do szybkiego
napisania strony internetowej.

Wywołanie funkcji z obiektu Console:

Console.output("To jest komunikat wyświetlany w konsoli.");
Console.error("To jest komunikat błędu.");
Console.warn("To jest komunikat ostrzeżenia.");
Wywołanie funkcji z obiektu Page:

Page.output("To jest wyświetlany tekst na stronie.");
Page.head("Tytuł nagłówka");
Page.text("To jest przykładowy tekst na stronie.");
Wywołanie funkcji z obiektu MathFun:

var sum = MathFun.add(5, 3);
var squareRoot = MathFun.squareRoot(25);
Wywołanie funkcji z obiektu Graphics (jeśli korzystasz z przeglądarki, możesz umieścić te funkcje w skrypcie HTML):

Graphics.rectangle(10, 10, 50, "blue");
Graphics.circle(100, 100, 30, "red");
Wywołanie funkcji z obiektu DOM (dla interakcji z elementami DOM na stronie internetowej):

var myElement = DOM.getid("elementId");
DOM.setStyle(myElement, "color", "red");
Wywołanie funkcji z obiektu Root (na przykład do autoryzacji):

Root.log("admin", "password123", "secured-page.html");
Pamiętaj, że musisz umieścić te wywołania funkcji w odpowiednich miejscach w swoim kodzie, w zależności od potrzeb aplikacji.


Console:

output(text): Wyświetla tekst w konsoli.
error(text): Wyświetla błąd w konsoli.
warn(text): Wyświetla ostrzeżenie w konsoli.
info(text): Wyświetla informację w konsoli.
table(data): Wyświetla dane w postaci tabeli w konsoli.
clear(): Czyści konsolę.
group(groupName): Rozpoczyna grupę w konsoli.
groupEnd(): Kończy grupę w konsoli.
time(timerName): Rozpoczyna pomiar czasu.
timeEnd(timerName): Kończy pomiar czasu.
assert(condition, message): Sprawdza warunek i wyświetla wiadomość w przypadku niepowodzenia.

Page:

output(text): Wyświetla tekst na stronie.
input(variable, value): Przypisuje wartość zmiennej.
inputNow(format): Wyświetla okno dialogowe do wprowadzenia danych.
head(value): Tworzy nagłówek na stronie.
headextra(value): Tworzy dodatkowy nagłówek z animacją.
articleopen(): Rozpoczyna sekcję artykułu.
mail(value): Tworzy link do wysłania e-maila.
text(value): Wyświetla tekst na stronie.
colorpicker(): Dodaje wybór koloru.
calendar(): Dodaje kalendarz.
video(value): Wyświetla wideo.
audio(value): Odtwarza audio.
foto(value): wyświetla zdjęcie
articleclose(): Zamyka sekcję artykułu.
info(value): Wyświetla informację na stronie.
css(selector, styles): Dodaje reguły CSS do dokumentu.

Root:

log(a, b, c): Prosi użytkownika o login i hasło i przekierowuje do URL.
fullscreen(): Sprawdza, czy przeglądarka jest w trybie pełnoekranowym.
open(url): Otwiera nowe okno przeglądarki.
close(): Zamyka okno przeglądarki.
window(text): Wyświetla alert na stronie.
prompt(message, defaultValue): Wyświetla okno dialogowe z komunikatem i wartością domyślną.

MathFun:

add(a, b): Dodaje dwie liczby a i b.
subtract(a, b): Odejmuje liczbę b od liczby a.
multiply(a, b): Mnoży dwie liczby a i b.
divide(a, b): Dzieli liczbę a przez b, zabezpieczając się przed dzieleniem przez zero.
power(base, exponent): Podnosi podstawę base do potęgi exponent.
squareRoot(number): Oblicza pierwiastek kwadratowy liczby number.
absoluteValue(number): Zwraca wartość bezwzględną liczby number.
round(number): Zaokrągla liczbę do najbliższej liczby całkowitej.
floor(number): Zaokrągla liczbę w dół do najbliższej liczby całkowitej.
ceiling(number): Zaokrągla liczbę w górę do najbliższej liczby całkowitej.
getRandomInt(min, max): Generuje losową liczbę całkowitą w zakresie od min do max.
Operacje logiczne:
andGate(input1, input2): Wykonuje operację "i" logicznego między input1 i input2.
orGate(input1, input2): Wykonuje operację "lub" logicznego między input1 i input2.
notGate(input): Wykonuje operację "nie" logicznego na input.
norGate(input1, input2): Wykonuje operację "nor" logicznego między input1 i input2.
nandGate(input1, input2): Wykonuje operację "nand" logicznego między input1 i input2.
xorGate(input1, input2): Wykonuje operację "xor" logicznego między input1 i input2.
xnorGate(input1, input2): Wykonuje operację "xnor" logicznego między input1 i input2.
Funkcje matematyczne trygonometryczne:
sin(angle): Oblicza sinus kąta angle.
cos(angle): Oblicza cosinus kąta angle.
tan(angle): Oblicza tangens kąta angle.
Pozostałe operacje matematyczne:
log(number): Oblicza logarytm naturalny liczby number.
max(numbers): Znajduje maksymalną wartość wśród podanych liczb.
min(numbers): Znajduje minimalną wartość wśród podanych liczb.

Graphics:

rectangle(x, y, size, color): Tworzy prostokąt o określonym rozmiarze i kolorze na stronie.
circle(x, y, radius, color): Tworzy okrąg o określonym promieniu i kolorze na stronie.
triangle(x, y, size, color): Tworzy trójkąt o określonym rozmiarze i kolorze na stronie.
createButton(x, y, label, clickHandler): Tworzy przycisk z etykietą i obsługą zdarzenia kliknięcia.
createTextField(x, y, placeholder): Tworzy pole tekstowe z podanym tekstem zastępczym.
createFrame(x, y, width, height, color): Tworzy ramkę o określonych wymiarach i kolorze.
addText(x, y, text, color): Dodaje tekst na stronie w określonej pozycji i kolorze.

DOM:

Funkcje do manipulacji elementami w modelu DOM:
getid(id): Pobiera element o określonym identyfikatorze (ID).
getclass(className): Pobiera elementy o określonej klasie.
getname(tagName): Pobiera elementy o określonym tagu.
createElement(tagName): Tworzy nowy element o określonym tagu.
addEvent(element, event, callback): Dodaje obsługę zdarzenia do elementu.
removeEvent(element, event, callback): Usuwa obsługę zdarzenia z elementu.
setAttribute(element, attribute, value): Ustawia atrybut elementu na określoną wartość.
getAttribute(element, attribute): Pobiera wartość określonego atrybutu elementu.
removeAttribute(element, attribute): Usuwa atrybut z elementu.
getStyle(element, property): Pobiera styl określonego właściwości elementu.
setStyle(element, property, value): Ustawia określoną właściwość CSS elementu.
addClass(elementId, className): Dodaje klasę do elementu.
removeClass(elementId, className): Usuwa klasę z elementu.
toggleClass(elementId, className): Przełącza klasę w elemencie.
hide(elementId): Ukrywa element.
show(elementId): Wyświetla element.
fadeOut(elementId): Powoduje wygaszenie elementu poprzez zmianę jego przezroczystości.
