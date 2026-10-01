function goToSell() {

    document
        .getElementById("sell")
        .scrollIntoView({
            behavior: "smooth"
        });

}


function goToPrices() {

    document
        .getElementById("prices")
        .scrollIntoView({
            behavior: "smooth"
        });

}


function postListing() {

    let crop =
        document.getElementById("crop").value;

    let quantity =
        document.getElementById("quantity").value;

    let price =
        document.getElementById("expectedPrice").value;

    let location =
        document.getElementById("location").value;


    if (
        crop === "" ||
        quantity === "" ||
        price === "" ||
        location === ""
    ) {

        alert(
            "Please fill all the details."
        );

        return;

    }


    alert(
        "✅ Produce listing posted successfully!\n\n" +

        "Crop: " + crop +

        "\nQuantity: " + quantity + " Kg" +

        "\nExpected Price: ₹" + price + "/Kg" +

        "\nLocation: " + location
    );


    document
        .getElementById("quantity")
        .value = "";

    document
        .getElementById("expectedPrice")
        .value = "";

    document
        .getElementById("location")
        .value = "";

}


function acceptOrder(button) {

    button.innerText =
        "Accepted ✓";

    button.style.background =
        "#555";

    alert(
        "✅ Buyer request accepted successfully!"
    );

}
