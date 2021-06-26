<template>
    <section>
        <h2 v-html="translations[lang].title"></h2>
            <!-- eslint-disable -->
            <pre style="box-shadow:none">
                <highlight-code lang="go">
                    -------------------------------------------------
                    file: main.go------------------------------------
                    -------------------------------------------------
                    ... 
                    ui, err := lorca.New("", "", 1200, 900, customArgs...)
                    if err != nil {
                        log.Fatal("lorca error:", err)
                    }
                    defer ui.Close()

                    // A simple way to know when UI is ready (uses body.onload event in JS)
                    ui.Bind("start", func() {
                        log.Println("UI is ready")
                    })

                    // Create and bind Go object to the UI
                    u := &gui.UiData{
                        Items: []gui.UiItem{},
                    }
                    ui.Bind("updateItems", u.UpdateItems)
                    ...

                    -------------------------------------------------
                    file: gui.go-------------------------------------
                    -------------------------------------------------
                    ... 
                    // Go types that are bound to the UI must be thread-safe, because each binding
                    // is executed in its own goroutine. In this simple case we may use atomic
                    // operations, but for more complex cases one should use proper synchronization.
                    type UiData struct {
                        sync.Mutex
                        Items     []UiItem
                        FileData  []byte
                        Character string
                        CharData  parser.CharData
                    }
                    func (u *UiData) UpdateItems(qty_str string, lvl_str string) {
                        u.Lock()
                        defer u.Unlock()

                        qty_ints := parseIntSlice(qty_str)
                        lvl_ints := parseIntSlice(lvl_str)

                        for i, v := range qty_ints {
                            u.Items[i].FileItem.ModifiedCount = v
                            u.Items[i].FileItem.ModifiedLvl = lvl_ints[i]
                        }
                        log.Println("Items updated.")

                        var items []parser.Item
                        for _, item := range u.Items {
                            items = append(items, item.FileItem)
                        }

                        u.FileData = parser.ModifyItemData(u.FileData, items)
                    }
                    ... 
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
                title: `GO Code Example`,
            },
            pt: {
                title: `Exemplo de Código GO`,
            }
        }
        }
    },
    }
</script>



