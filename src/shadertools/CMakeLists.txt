# Generated from shadertools.pro.

#####################################################################
## ShaderTools Module:
#####################################################################

qt_internal_add_module(ShaderTools
    EXCEPTIONS
    SOURCES
        qshaderbaker.cpp qshaderbaker_p.h
        qshaderbatchablerewriter.cpp qshaderbatchablerewriter_p.h
        qspirvcompiler.cpp qspirvcompiler_p.h
        qspirvshader.cpp qspirvshader_p.h
        qspirvshaderremap.cpp qspirvshaderremap_p.h
        qtshadertoolsglobal.h
    DEFINES
        QT_BUILD_SHADERTOOLS_LIB
    INCLUDE_DIRECTORIES
        ../3rdparty/SPIRV-Cross
        ../3rdparty/glslang
    LIBRARIES
        Qt::GuiPrivate
# special case begin
        Qt::BundledSpirv_Cross
        Qt::BundledGlslang_Glslang
        Qt::BundledGlslang_Spirv
        Qt::BundledGlslang_Osdependent
        Qt::BundledGlslang_Oglcompiler
# special case end
    PUBLIC_LIBRARIES
        Qt::Core
        Qt::Gui
    PRIVATE_MODULE_INTERFACE
        Qt::GuiPrivate
    GENERATE_CPP_EXPORTS
    GENERATE_PRIVATE_CPP_EXPORTS
)

## Scopes:
#####################################################################

#### Keys ignored in scope 2:.:.:shadertools.pro:NOT EXISTS _ss_[QT_HOST_DATA]/.qmake.cache:
# LIBLOC = "$$shadowed($$dirname _QMAKE_CONF_)" "/lib"

#### Keys ignored in scope 3:.:.:shadertools.pro:else:
# LIBLOC = "$$[QT_HOST_LIBS]"
qt_internal_add_docs(ShaderTools
    doc/qtshadertools.qdocconf
)

