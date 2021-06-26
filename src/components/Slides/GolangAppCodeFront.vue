<template>
    <section>
        <h2 v-html="translations[lang].title"></h2>
        <!-- eslint-disable -->
        <pre style="box-shadow:none">
            <highlight-code lang="javascript">
                // We use async/await because Go functions are asynchronous
                // go bindings have to be in this index.html
                async function goUpdateItems(qty_values, lvl_values) {
                    // Call Go function to update item count values
                    return await updateItems(qty_values, lvl_values);
                }

                // update items
                goUpdateItems(JSON.stringify(int_qty_array), JSON.stringify(int_lvl_array)).then(()=>{
                    // update power
                    var power_selection = document.getElementById( "power-selection" );
                    goUpdatePower(power_selection.options[power_selection.selectedIndex].value).then( () => {
                        // then save data
                        goSaveData().then(()=>{
                            alert('Saved Data!');
                            loadItems();
                        });
                    });  
                });
            </highlight-code>
        </pre>
        <!-- eslint-enable -->
    </section>
</template>

<script>
export default {
    props: {
        lang: String,
    },
    data() {
        return {
        translations: {
            en: {
                title: `JS Code Example`,
            },
            pt: {
                title: `Exemplo de Código JS`,
            }
        }
        }
    },
    }
</script>



