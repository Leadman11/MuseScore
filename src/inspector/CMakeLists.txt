# SPDX-License-Identifier: GPL-3.0-only
# MuseScore-Studio-CLA-applies
#
# MuseScore Studio
# Music Composition & Notation
#
# Copyright (C) 2021 MuseScore Limited
#
# This program is free software: you can redistribute it and/or modify
# it under the terms of the GNU General Public License version 3 as
# published by the Free Software Foundation.
#
# This program is distributed in the hope that it will be useful,
# but WITHOUT ANY WARRANTY; without even the implied warranty of
# MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
# GNU General Public License for more details.
#
# You should have received a copy of the GNU General Public License
# along with this program.  If not, see <https://www.gnu.org/licenses/>.
declare_module("inspector")

set(MODULE_QRC ${CMAKE_CURRENT_LIST_DIR}/view/inspector_resources.qrc )

set(MODULE_QML_IMPORT ${CMAKE_CURRENT_LIST_DIR}/view/qml)

set(MODULE_SRC
    ${CMAKE_CURRENT_LIST_DIR}/inspectormodule.cpp
    ${CMAKE_CURRENT_LIST_DIR}/inspectormodule.h

    ${CMAKE_CURRENT_LIST_DIR}/types/accidentaltypes.h
    ${CMAKE_CURRENT_LIST_DIR}/types/ambitustypes.h
    ${CMAKE_CURRENT_LIST_DIR}/types/articulationtypes.h
    ${CMAKE_CURRENT_LIST_DIR}/types/barlinetypes.h
    ${CMAKE_CURRENT_LIST_DIR}/types/beamtypes.h
    ${CMAKE_CURRENT_LIST_DIR}/types/bendtypes.h
    ${CMAKE_CURRENT_LIST_DIR}/types/chordsymboltypes.h
    ${CMAKE_CURRENT_LIST_DIR}/types/dynamictypes.h
    ${CMAKE_CURRENT_LIST_DIR}/types/fretdiagramtypes.h
    ${CMAKE_CURRENT_LIST_DIR}/types/glissandotypes.h
    ${CMAKE_CURRENT_LIST_DIR}/types/hairpintypes.h
    ${CMAKE_CURRENT_LIST_DIR}/types/keysignaturetypes.h
    ${CMAKE_CURRENT_LIST_DIR}/types/markertypes.h
    ${CMAKE_CURRENT_LIST_DIR}/types/noteheadtypes.h
    ${CMAKE_CURRENT_LIST_DIR}/types/ornamenttypes.h
    ${CMAKE_CURRENT_LIST_DIR}/types/linetypes.h
    ${CMAKE_CURRENT_LIST_DIR}/types/directiontypes.h
    ${CMAKE_CURRENT_LIST_DIR}/types/slurtietypes.h
    ${CMAKE_CURRENT_LIST_DIR}/types/texttypes.h
    ${CMAKE_CURRENT_LIST_DIR}/types/commontypes.h
    ${CMAKE_CURRENT_LIST_DIR}/types/tremolobartypes.h
    ${CMAKE_CURRENT_LIST_DIR}/types/tremolotypes.h
    ${CMAKE_CURRENT_LIST_DIR}/types/voicetypes.h

    ${CMAKE_CURRENT_LIST_DIR}/models/iinspectormodelcreator.h
    ${CMAKE_CURRENT_LIST_DIR}/models/inspectormodelcreator.cpp
    ${CMAKE_CURRENT_LIST_DIR}/models/inspectormodelcreator.h
    ${CMAKE_CURRENT_LIST_DIR}/models/abstractinspectormodel.cpp
    ${CMAKE_CURRENT_LIST_DIR}/models/abstractinspectormodel.h
    ${CMAKE_CURRENT_LIST_DIR}/models/abstractinspectorproxymodel.cpp
    ${CMAKE_CURRENT_LIST_DIR}/models/abstractinspectorproxymodel.h
    ${CMAKE_CURRENT_LIST_DIR}/models/inspectorlistmodel.cpp
    ${CMAKE_CURRENT_LIST_DIR}/models/inspectorlistmodel.h
    ${CMAKE_CURRENT_LIST_DIR}/models/propertyitem.cpp
    ${CMAKE_CURRENT_LIST_DIR}/models/propertyitem.h
    ${CMAKE_CURRENT_LIST_DIR}/models/pointfpropertyitem.cpp
    ${CMAKE_CURRENT_LIST_DIR}/models/pointfpropertyitem.h
    ${CMAKE_CURRENT_LIST_DIR}/models/inspectormodelwithvoiceandpositionoptions.cpp
    ${CMAKE_CURRENT_LIST_DIR}/models/inspectormodelwithvoiceandpositionoptions.h
    ${CMAKE_CURRENT_LIST_DIR}/models/general/generalsettingsmodel.cpp
    ${CMAKE_CURRENT_LIST_DIR}/models/general/generalsettingsmodel.h
    ${CMAKE_CURRENT_LIST_DIR}/models/general/appearance/appearancesettingsmodel.cpp
    ${CMAKE_CURRENT_LIST_DIR}/models/general/appearance/appearancesettingsmodel.h
    ${CMAKE_CURRENT_LIST_DIR}/models/general/playback/playbackproxymodel.cpp
    ${CMAKE_CURRENT_LIST_DIR}/models/general/playback/playbackproxymodel.h
    ${CMAKE_CURRENT_LIST_DIR}/models/general/playback/internal_models/arpeggioplaybackmodel.cpp
    ${CMAKE_CURRENT_LIST_DIR}/models/general/playback/internal_models/arpeggioplaybackmodel.h
    ${CMAKE_CURRENT_LIST_DIR}/models/general/playback/internal_models/breathplaybackmodel.cpp
    ${CMAKE_CURRENT_LIST_DIR}/models/general/playback/internal_models/breathplaybackmodel.h
    ${CMAKE_CURRENT_LIST_DIR}/models/general/playback/internal_models/fermataplaybackmodel.cpp
    ${CMAKE_CURRENT_LIST_DIR}/models/general/playback/internal_models/fermataplaybackmodel.h
    ${CMAKE_CURRENT_LIST_DIR}/models/general/playback/internal_models/glissandoplaybackmodel.cpp
    ${CMAKE_CURRENT_LIST_DIR}/models/general/playback/internal_models/glissandoplaybackmodel.h
    ${CMAKE_CURRENT_LIST_DIR}/models/general/playback/internal_models/noteplaybackmodel.cpp
    ${CMAKE_CURRENT_LIST_DIR}/models/general/playback/internal_models/noteplaybackmodel.h
    ${CMAKE_CURRENT_LIST_DIR}/models/general/playback/internal_models/gradualtempochangeplaybackmodel.cpp
    ${CMAKE_CURRENT_LIST_DIR}/models/general/playback/internal_models/gradualtempochangeplaybackmodel.h
    ${CMAKE_CURRENT_LIST_DIR}/models/measures/measuressettingsmodel.cpp
    ${CMAKE_CURRENT_LIST_DIR}/models/measures/measuressettingsmodel.h
    ${CMAKE_CURRENT_LIST_DIR}/models/emptystaves/emptystavesvisiblitysettingsmodel.cpp
    ${CMAKE_CURRENT_LIST_DIR}/models/emptystaves/emptystavesvisiblitysettingsmodel.h
    ${CMAKE_CURRENT_LIST_DIR}/models/score/scoreappearancesettingsmodel.cpp
    ${CMAKE_CURRENT_LIST_DIR}/models/score/scoreappearancesettingsmodel.h
    ${CMAKE_CURRENT_LIST_DIR}/models/score/scoredisplaysettingsmodel.cpp
    ${CMAKE_CURRENT_LIST_DIR}/models/score/scoredisplaysettingsmodel.h
    ${CMAKE_CURRENT_LIST_DIR}/models/score/internal/pagetypelistmodel.cpp
    ${CMAKE_CURRENT_LIST_DIR}/models/score/internal/pagetypelistmodel.h
    ${CMAKE_CURRENT_LIST_DIR}/models/parts/partssettingsmodel.cpp
    ${CMAKE_CURRENT_LIST_DIR}/models/parts/partssettingsmodel.h
    ${CMAKE_CURRENT_LIST_DIR}/models/text/textsettingsmodel.cpp
    ${CMAKE_CURRENT_LIST_DIR}/models/text/textsettingsmodel.h
    ${CMAKE_CURRENT_LIST_DIR}/models/text/textstylepopupmodel.cpp
    ${CMAKE_CURRENT_LIST_DIR}/models/text/textstylepopupmodel.h
    ${CMAKE_CURRENT_LIST_DIR}/view/widgets/fretcanvas.cpp
    ${CMAKE_CURRENT_LIST_DIR}/view/widgets/fretcanvas.h
    ${CMAKE_CURRENT_LIST_DIR}/view/widgets/bendgridcanvas.cpp
    ${CMAKE_CURRENT_LIST_DIR}/view/widgets/bendgridcanvas.h
    ${CMAKE_CURRENT_LIST_DIR}/view/widgets/gridcanvas.cpp
    ${CMAKE_CURRENT_LIST_DIR}/view/widgets/gridcanvas.h
    ${CMAKE_CURRENT_LIST_DIR}/models/notation/notationsettingsproxymodel.cpp
    ${CMAKE_CURRENT_LIST_DIR}/models/notation/notationsettingsproxymodel.h
    ${CMAKE_CURRENT_LIST_DIR}/models/notation/accidentals/accidentalsettingsmodel.cpp
    ${CMAKE_CURRENT_LIST_DIR}/models/notation/accidentals/accidentalsettingsmodel.h
    ${CMAKE_CURRENT_LIST_DIR}/models/notation/ambituses/ambitussettingsmodel.cpp
    ${CMAKE_CURRENT_LIST_DIR}/models/notation/ambituses/ambitussettingsmodel.h
    ${CMAKE_CURRENT_LIST_DIR}/models/notation/articulations/articulationsettingsmodel.cpp
    ${CMAKE_CURRENT_LIST_DIR}/models/notation/articulations/articulationsettingsmodel.h
    ${CMAKE_CURRENT_LIST_DIR}/models/notation/barlines/barlinesettingsmodel.cpp
    ${CMAKE_CURRENT_LIST_DIR}/models/notation/barlines/barlinesettingsmodel.h
    ${CMAKE_CURRENT_LIST_DIR}/models/notation/barlines/barlinesettingsproxymodel.cpp
    ${CMAKE_CURRENT_LIST_DIR}/models/notation/barlines/barlinesettingsproxymodel.h
    ${CMAKE_CURRENT_LIST_DIR}/models/notation/beams/beammodesmodel.cpp
    ${CMAKE_CURRENT_LIST_DIR}/models/notation/beams/beammodesmodel.h
    ${CMAKE_CURRENT_LIST_DIR}/models/notation/bends/bendsettingsmodel.cpp
    ${CMAKE_CURRENT_LIST_DIR}/models/notation/bends/bendsettingsmodel.h
    ${CMAKE_CURRENT_LIST_DIR}/models/notation/brackets/bracketsettingsmodel.cpp
    ${CMAKE_CURRENT_LIST_DIR}/models/notation/brackets/bracketsettingsmodel.h
    ${CMAKE_CURRENT_LIST_DIR}/models/notation/chordsymbols/chordsymbolsettingsmodel.cpp
    ${CMAKE_CURRENT_LIST_DIR}/models/notation/chordsymbols/chordsymbolsettingsmodel.h
    ${CMAKE_CURRENT_LIST_DIR}/models/notation/clefs/clefsettingsmodel.cpp
    ${CMAKE_CURRENT_LIST_DIR}/models/notation/clefs/clefsettingsmodel.h
    ${CMAKE_CURRENT_LIST_DIR}/models/notation/lines/hairpinlinesettingsmodel.cpp
    ${CMAKE_CURRENT_LIST_DIR}/models/notation/lines/hairpinlinesettingsmodel.h
    ${CMAKE_CURRENT_LIST_DIR}/models/notation/lines/slurandtiesettingsmodel.cpp
    ${CMAKE_CURRENT_LIST_DIR}/models/notation/lines/slurandtiesettingsmodel.h
    ${CMAKE_CURRENT_LIST_DIR}/models/notation/fermatas/fermatasettingsmodel.cpp
    ${CMAKE_CURRENT_LIST_DIR}/models/notation/fermatas/fermatasettingsmodel.h
    ${CMAKE_CURRENT_LIST_DIR}/models/notation/frames/horizontalframesettingsmodel.cpp
    ${CMAKE_CURRENT_LIST_DIR}/models/notation/frames/horizontalframesettingsmodel.h
    ${CMAKE_CURRENT_LIST_DIR}/models/notation/frames/textframesettingsmodel.cpp
    ${CMAKE_CURRENT_LIST_DIR}/models/notation/frames/textframesettingsmodel.h
    ${CMAKE_CURRENT_LIST_DIR}/models/notation/frames/verticalframesettingsmodel.cpp
    ${CMAKE_CURRENT_LIST_DIR}/models/notation/frames/verticalframesettingsmodel.h
    ${CMAKE_CURRENT_LIST_DIR}/models/notation/frames/fretframesettingsproxymodel.cpp
    ${CMAKE_CURRENT_LIST_DIR}/models/notation/frames/fretframesettingsproxymodel.h
    ${CMAKE_CURRENT_LIST_DIR}/models/notation/frames/fretframe/fretframesettingsmodel.cpp
    ${CMAKE_CURRENT_LIST_DIR}/models/notation/frames/fretframe/fretframesettingsmodel.h
    ${CMAKE_CURRENT_LIST_DIR}/models/notation/frames/fretframe/fretframechordssettingsmodel.cpp
    ${CMAKE_CURRENT_LIST_DIR}/models/notation/frames/fretframe/fretframechordssettingsmodel.h
    ${CMAKE_CURRENT_LIST_DIR}/models/notation/frames/fretframe/fretframechordlistmodel.cpp
    ${CMAKE_CURRENT_LIST_DIR}/models/notation/frames/fretframe/fretframechordlistmodel.h
    ${CMAKE_CURRENT_LIST_DIR}/models/notation/frames/fretframe/fretframechorditem.cpp
    ${CMAKE_CURRENT_LIST_DIR}/models/notation/frames/fretframe/fretframechorditem.h
    ${CMAKE_CURRENT_LIST_DIR}/models/notation/fretdiagrams/fretdiagramsettingsmodel.cpp
    ${CMAKE_CURRENT_LIST_DIR}/models/notation/fretdiagrams/fretdiagramsettingsmodel.h
    ${CMAKE_CURRENT_LIST_DIR}/models/notation/lines/glissandosettingsmodel.cpp
    ${CMAKE_CURRENT_LIST_DIR}/models/notation/lines/glissandosettingsmodel.h
    ${CMAKE_CURRENT_LIST_DIR}/models/notation/lines/vibratosettingsmodel.cpp
    ${CMAKE_CURRENT_LIST_DIR}/models/notation/lines/vibratosettingsmodel.h
    ${CMAKE_CURRENT_LIST_DIR}/models/notation/lines/hairpinsettingsmodel.cpp
    ${CMAKE_CURRENT_LIST_DIR}/models/notation/lines/hairpinsettingsmodel.h
    ${CMAKE_CURRENT_LIST_DIR}/models/notation/lines/ottavasettingsmodel.cpp
    ${CMAKE_CURRENT_LIST_DIR}/models/notation/lines/ottavasettingsmodel.h
    ${CMAKE_CURRENT_LIST_DIR}/models/notation/lines/voltasettingsmodel.cpp
    ${CMAKE_CURRENT_LIST_DIR}/models/notation/lines/voltasettingsmodel.h
    ${CMAKE_CURRENT_LIST_DIR}/models/notation/lines/letringsettingsmodel.cpp
    ${CMAKE_CURRENT_LIST_DIR}/models/notation/lines/letringsettingsmodel.h
    ${CMAKE_CURRENT_LIST_DIR}/models/notation/lines/palmmutesettingsmodel.cpp
    ${CMAKE_CURRENT_LIST_DIR}/models/notation/lines/palmmutesettingsmodel.h
    ${CMAKE_CURRENT_LIST_DIR}/models/notation/lines/textlinesettingsmodel.cpp
    ${CMAKE_CURRENT_LIST_DIR}/models/notation/lines/textlinesettingsmodel.h
    ${CMAKE_CURRENT_LIST_DIR}/models/notation/lines/gradualtempochangesettingsmodel.cpp
    ${CMAKE_CURRENT_LIST_DIR}/models/notation/lines/gradualtempochangesettingsmodel.h
    ${CMAKE_CURRENT_LIST_DIR}/models/notation/lines/notelinesettingsmodel.cpp
    ${CMAKE_CURRENT_LIST_DIR}/models/notation/lines/notelinesettingsmodel.h
    ${CMAKE_CURRENT_LIST_DIR}/models/notation/images/imagesettingsmodel.cpp
    ${CMAKE_CURRENT_LIST_DIR}/models/notation/images/imagesettingsmodel.h
    ${CMAKE_CURRENT_LIST_DIR}/models/notation/jumps/jumpsettingsmodel.cpp
    ${CMAKE_CURRENT_LIST_DIR}/models/notation/jumps/jumpsettingsmodel.h
    ${CMAKE_CURRENT_LIST_DIR}/models/notation/keysignatures/keysignaturesettingsmodel.cpp
    ${CMAKE_CURRENT_LIST_DIR}/models/notation/keysignatures/keysignaturesettingsmodel.h
    ${CMAKE_CURRENT_LIST_DIR}/models/notation/markers/markersettingsmodel.cpp
    ${CMAKE_CURRENT_LIST_DIR}/models/notation/markers/markersettingsmodel.h
    ${CMAKE_CURRENT_LIST_DIR}/models/notation/ornaments/ornamentsettingsmodel.cpp
    ${CMAKE_CURRENT_LIST_DIR}/models/notation/ornaments/ornamentsettingsmodel.h
    ${CMAKE_CURRENT_LIST_DIR}/models/notation/lines/pedalsettingsmodel.cpp
    ${CMAKE_CURRENT_LIST_DIR}/models/notation/lines/pedalsettingsmodel.h
    ${CMAKE_CURRENT_LIST_DIR}/models/notation/lyrics/lyricssettingsmodel.cpp
    ${CMAKE_CURRENT_LIST_DIR}/models/notation/lyrics/lyricssettingsmodel.h
    ${CMAKE_CURRENT_LIST_DIR}/models/notation/sectionbreaks/sectionbreaksettingsmodel.cpp
    ${CMAKE_CURRENT_LIST_DIR}/models/notation/sectionbreaks/sectionbreaksettingsmodel.h
    ${CMAKE_CURRENT_LIST_DIR}/models/notation/spacers/spacersettingsmodel.cpp
    ${CMAKE_CURRENT_LIST_DIR}/models/notation/spacers/spacersettingsmodel.h
    ${CMAKE_CURRENT_LIST_DIR}/models/notation/staffs/staffsettingsmodel.cpp
    ${CMAKE_CURRENT_LIST_DIR}/models/notation/staffs/staffsettingsmodel.h
    ${CMAKE_CURRENT_LIST_DIR}/models/notation/stafftype/stafftypesettingsmodel.cpp
    ${CMAKE_CURRENT_LIST_DIR}/models/notation/stafftype/stafftypesettingsmodel.h
    ${CMAKE_CURRENT_LIST_DIR}/models/notation/symbols/symbolsettingsmodel.cpp
    ${CMAKE_CURRENT_LIST_DIR}/models/notation/symbols/symbolsettingsmodel.h
    ${CMAKE_CURRENT_LIST_DIR}/models/notation/tempos/temposettingsmodel.cpp
    ${CMAKE_CURRENT_LIST_DIR}/models/notation/tempos/temposettingsmodel.h
    ${CMAKE_CURRENT_LIST_DIR}/models/notation/timesignatures/timesignaturesettingsmodel.cpp
    ${CMAKE_CURRENT_LIST_DIR}/models/notation/timesignatures/timesignaturesettingsmodel.h
    ${CMAKE_CURRENT_LIST_DIR}/models/notation/tremolobars/tremolobarsettingsmodel.cpp
    ${CMAKE_CURRENT_LIST_DIR}/models/notation/tremolobars/tremolobarsettingsmodel.h
    ${CMAKE_CURRENT_LIST_DIR}/models/notation/tremolos/tremolosettingsmodel.cpp
    ${CMAKE_CURRENT_LIST_DIR}/models/notation/tremolos/tremolosettingsmodel.h
    ${CMAKE_CURRENT_LIST_DIR}/models/notation/notes/notesettingsproxymodel.cpp
    ${CMAKE_CURRENT_LIST_DIR}/models/notation/notes/notesettingsproxymodel.h
    ${CMAKE_CURRENT_LIST_DIR}/models/notation/notes/beams/beamsettingsmodel.cpp
    ${CMAKE_CURRENT_LIST_DIR}/models/notation/notes/beams/beamsettingsmodel.h
    ${CMAKE_CURRENT_LIST_DIR}/models/notation/notes/chords/chordsettingsmodel.cpp
    ${CMAKE_CURRENT_LIST_DIR}/models/notation/notes/chords/chordsettingsmodel.h
    ${CMAKE_CURRENT_LIST_DIR}/models/notation/notes/hooks/hooksettingsmodel.cpp
    ${CMAKE_CURRENT_LIST_DIR}/models/notation/notes/hooks/hooksettingsmodel.h
    ${CMAKE_CURRENT_LIST_DIR}/models/notation/notes/noteheads/noteheadsettingsmodel.cpp
    ${CMAKE_CURRENT_LIST_DIR}/models/notation/notes/noteheads/noteheadsettingsmodel.h
    ${CMAKE_CURRENT_LIST_DIR}/models/notation/notes/noteheads/noteheadgroupsmodel.cpp
    ${CMAKE_CURRENT_LIST_DIR}/models/notation/notes/noteheads/noteheadgroupsmodel.h
    ${CMAKE_CURRENT_LIST_DIR}/models/notation/notes/stems/stemsettingsmodel.cpp
    ${CMAKE_CURRENT_LIST_DIR}/models/notation/notes/stems/stemsettingsmodel.h
    ${CMAKE_CURRENT_LIST_DIR}/models/notation/mmrests/mmrestsettingsmodel.cpp
    ${CMAKE_CURRENT_LIST_DIR}/models/notation/mmrests/mmrestsettingsmodel.h
    ${CMAKE_CURRENT_LIST_DIR}/models/notation/measurerepeats/measurerepeatsettingsmodel.cpp
    ${CMAKE_CURRENT_LIST_DIR}/models/notation/measurerepeats/measurerepeatsettingsmodel.h
    ${CMAKE_CURRENT_LIST_DIR}/models/notation/tuplets/tupletsettingsmodel.cpp
    ${CMAKE_CURRENT_LIST_DIR}/models/notation/tuplets/tupletsettingsmodel.h
    ${CMAKE_CURRENT_LIST_DIR}/models/notation/instrumentname/instrumentnamesettingsmodel.cpp
    ${CMAKE_CURRENT_LIST_DIR}/models/notation/instrumentname/instrumentnamesettingsmodel.h
    ${CMAKE_CURRENT_LIST_DIR}/models/notation/rests/beams/restbeamsettingsmodel.cpp
    ${CMAKE_CURRENT_LIST_DIR}/models/notation/rests/beams/restbeamsettingsmodel.h
    ${CMAKE_CURRENT_LIST_DIR}/models/notation/rests/restsettingsproxymodel.cpp
    ${CMAKE_CURRENT_LIST_DIR}/models/notation/rests/restsettingsproxymodel.h
    ${CMAKE_CURRENT_LIST_DIR}/models/notation/dynamics/dynamicsettingsmodel.cpp
    ${CMAKE_CURRENT_LIST_DIR}/models/notation/dynamics/dynamicsettingsmodel.h
    ${CMAKE_CURRENT_LIST_DIR}/models/notation/expressions/expressionsettingsmodel.h
    ${CMAKE_CURRENT_LIST_DIR}/models/notation/expressions/expressionsettingsmodel.cpp
    ${CMAKE_CURRENT_LIST_DIR}/models/notation/stringtunings/stringtuningssettingsmodel.cpp
    ${CMAKE_CURRENT_LIST_DIR}/models/notation/stringtunings/stringtuningssettingsmodel.h
    ${CMAKE_CURRENT_LIST_DIR}/models/inspectorpopupcontroller.cpp
    ${CMAKE_CURRENT_LIST_DIR}/models/inspectorpopupcontroller.h
    ${CMAKE_CURRENT_LIST_DIR}/internal/services/elementrepositoryservice.cpp
    ${CMAKE_CURRENT_LIST_DIR}/internal/services/elementrepositoryservice.h
    ${CMAKE_CURRENT_LIST_DIR}/internal/interfaces/ielementrepositoryservice.h
    )

set(MODULE_LINK
    muse::uicomponents
    engraving
    Qt::Quick
    )

setup_module()
