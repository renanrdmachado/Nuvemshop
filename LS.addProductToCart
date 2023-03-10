LS.addProductToCart = function( product, cb_success, cb_error ){

    if( typeof product != "object" )
        return;

    var form = document.createElement('form');
    form.method = "POST";
    form.action = "/comprar/";

    console.log('form',form);

    if( product.id ) {
        // ID
        var input_id = document.createElement('input');
        input_id.name = "add_to_cart";
        input_id.value = product.id;
        console.log('input_id',input_id);
        form.append( input_id );
    }

    if( product.quantity ) {
        // QUANTITY
        var input_qty = document.createElement('input');
        input_qty.name ="quantity";
        input_qty.value = product.quantity;
        console.log('input_qty',input_qty);
        form.append( input_qty );
    }
    if( product.custom ) {
        // CUSTOM
        var input_custom = document.createElement('input');
        input_custom.name = "properties["+product.custom.name+"]";
        input_custom.value = product.custom.value;
        form.append( input_custom );
    }

    // ADICIONA AO CARRINHO
    LS.addToCartEnhanced(
        $( form ),
        'Adicionar ao carrinho',
        'Adicionando',
        'Sem estoque',
        true,
            cb_success,
            cb_error
    );
}

// LS.addProductToCart( 
//     {
//         id: 101689414,
//         quantity: 2,
//         custom: {
//             name: "Modelo",
//             value: "Teste 123"
//         }
//     },
//     function(){
//         console.log('SUCESSO');
//         $('#ajax-cart>a')[0].click();
//     },
//     function(){
//         console.log('ERRO')
//     }
// );
