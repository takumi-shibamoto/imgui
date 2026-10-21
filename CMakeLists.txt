# Create a library.
add_library(ImGui STATIC

    "imconfig.h"
    "imgui_demo.cpp"
    "imgui_draw.cpp"
    "imgui_internal.h"
    "imgui_tables.cpp"
    "imgui_widgets.cpp"
    "imgui.cpp"
    "imgui.h"
    "imstb_rectpack.h"
    "imstb_textedit.h"
    "imstb_truetype.h"
    "backends/imgui_impl_glfw.cpp"
    "backends/imgui_impl_glfw.h"
    "backends/imgui_impl_opengl3.cpp"
    "backends/imgui_impl_opengl3.h"

)

# Set the include directory.
target_include_directories(ImGui PUBLIC ".")
target_include_directories(ImGui PUBLIC "backends")

# link the glfw3 library.
target_link_libraries(ImGui PRIVATE glfw)