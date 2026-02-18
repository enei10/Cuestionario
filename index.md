```mermaid
flowchart TD
    ADP_01["ADP_01<br/>Durante el 2025, en su entidad, ¿existió..."]
    ADP_01 -- in [0, 2] --> TEC_02
    ADP_01 -- =1 --> ADP_02
    ADP_02["ADP_02<br/>Durante el 2025, según su conocimiento, ..."]
    ADP_02 --> ADP_03
    ADP_03["ADP_03<br/>Durante el 2025, ¿usted participó direct..."]
    ADP_03 -- =0 --> ADP_04
    ADP_03 -- in [1, 2] --> ADP_05
    ADP_04["ADP_04<br/>De la solución de IA en la etapa más ava..."]
    ADP_04 --> ADP_06
    ADP_05["ADP_05<br/>De la solución de IA en la etapa más ava..."]
    ADP_05 --> ADP_07
    ADP_06["ADP_06<br/>Según su conocimiento, de esa misma solu..."]
    ADP_06 --> ADP_09
    ADP_07["ADP_07<br/>Según su conocimiento, de esa misma solu..."]
    ADP_07 --> ADP_08
    ADP_08["ADP_08<br/>Pensando en esa solución, indique en qué..."]
    ADP_08 --> ADP_09
    ADP_09["ADP_09<br/>Durante el 2025, según su conocimiento, ..."]
    ADP_09 -- =1 --> ADP_10
    ADP_09 -- in [0, 2] --> ADP_11
    ADP_10["ADP_10<br/>¿Podría indicar aproximadamente cuántos ..."]
    ADP_10 --> ADP_11
    ADP_11["ADP_11<br/>Durante el 2025, según su conocimiento, ..."]
    ADP_11 -- =1 --> ADP_12
    ADP_11 -- in [0, 2] --> TEC_02
    ADP_12["ADP_12<br/>¿Podría indicar aproximadamente cuántos ..."]
    ADP_12 --> TEC_02
    CAR_01["CAR_01<br/>P1. Entidad Pública Recursos"]
    CAR_01 --> CAR_02
    CAR_02["CAR_02<br/>P2. Ubicación Departamento"]
    CAR_02 --> CAR_03
    CAR_03["CAR_03<br/>P3. ¿Cuál es su nivel educativo más alto..."]
    CAR_03 --> CAR_04
    CAR_04["CAR_04<br/>P4. ¿Qué edad tiene en años cumplidos?"]
    CAR_04 --> CAR_05
    CAR_05["CAR_05<br/>P5. Sexo"]
    CAR_05 --> CAR_06
    CAR_06["CAR_06<br/>P6. ¿Qué rol tiene en la toma de decisio..."]
    CAR_06 --> CAR_07
    CAR_07["CAR_07<br/>P7. ¿En qué área labora actualmente?"]
    CAR_07 --> CAR_08
    CAR_08["CAR_08<br/>P8. ¿Cuánto tiempo lleva trabajando en l..."]
    CAR_08 --> CAR_09
    CAR_09["CAR_09<br/>P9. ¿Bajo qué tipo de contrato trabaja e..."]
    CAR_09 --> EXP_01
    CIB_01["CIB_01<br/>Durante el 2025, ¿su entidad contaba con..."]
    CIB_01 --> CIB_02
    CIB_02["CIB_02<br/>Durante el 2025, ¿considera que en su en..."]
    CIB_02 --> CIB_03
    CIB_03["CIB_03<br/>Durante el 2025, ¿cómo evaluaría la prep..."]
    CIB_03 --> CIB_04
    CIB_04["CIB_04<br/>Durante el 2025, ¿su área o entidad ha s..."]
    CON_01["CON_01<br/>¿Cómo calificaría usted su nivel de cono..."]
    CON_01 -- =1 --> CON_03
    CON_01 -- in [2, 3, 4, 5] --> CON_02
    CON_02["CON_02<br/>A continuación se presentan algunas afir..."]
    CON_02 --> CON_03
    CON_03["CON_03<br/>¿Has recibido capacitación sobre intelig..."]
    CON_03 -- =1 --> CON_05
    CON_03 -- in [2, 3, 4] --> CON_04
    CON_04["CON_04<br/>¿Qué factores le dificultarían aprender ..."]
    CON_04 --> CON_05
    CON_05["CON_05<br/>¿Qué tanto interés tiene usted en aprend..."]
    CON_05 -- in [3, 4, 5] --> CON_06
    CON_05 -- in [1, 2] --> CON_07
    CON_06["CON_06<br/>¿Por qué medio preferiría aprender o seg..."]
    CON_06 --> GEN_01
    CON_07["CON_07<br/>¿Cuáles son las razones por las que uste..."]
    CON_07 --> GEN_01
    DAT_01["DAT_01<br/>Durante 2025, en su entidad, indique en ..."]
    DAT_01 --> CIB_01
    DEC_01{"DEC_01<br/>¿Usó IA Laboral en GEN_01 o TRA_01?"}
    DEC_01 -- SÍ --> MEJ_01
    DEC_01 -- NO --> ADP_01
    EXP_01["EXP_01<br/>Antes de esta encuesta, ¿habías escuchad..."]
    EXP_01 --> EXP_02
    EXP_02["EXP_02<br/>¿Habías escuchado o leído sobre estos us..."]
    EXP_02 --> CON_01
    GEN_01["GEN_01<br/>Durante el 2025, ¿ha utilizado herramien..."]
    GEN_01 -- =0 --> GEN_14
    GEN_01 -- in [2, 3] --> GEN_03
    GEN_01 -- =1 --> GEN_02
    GEN_02["GEN_02<br/>Durante el 2025, ¿con qué frecuencia ha ..."]
    GEN_02 --> GEN_05
    GEN_03["GEN_03<br/>Durante el 2025, ¿con qué frecuencia ha ..."]
    GEN_03 --> GEN_04
    GEN_04["GEN_04<br/>Durante el 2025, ¿qué herramientas utili..."]
    GEN_04 --> GEN_07
    GEN_05["GEN_05<br/>Durante el 2025, ¿qué herramientas de IA..."]
    GEN_05 --> GEN_06
    GEN_06["GEN_06<br/>Durante el 2025, cuando utilizó herramie..."]
    GEN_06 -- in [1, 5] --> GEN_13
    GEN_06 -- in [2, 3, 4] --> GEN_08
    GEN_07["GEN_07<br/>Durante el 2025, cuando utilizó herramie..."]
    GEN_07 -- in [1, 5] --> GEN_12
    GEN_07 -- in [2, 3, 4] --> GEN_09
    GEN_08["GEN_08<br/>Durante el 2025, ¿cuáles de las herramie..."]
    GEN_08 --> GEN_11
    GEN_09["GEN_09<br/>Durante el 2025, ¿cuáles de las herramie..."]
    GEN_09 --> GEN_10
    GEN_10["GEN_10<br/>Durante el 2025, para las herramientas q..."]
    GEN_10 --> GEN_12
    GEN_11["GEN_11<br/>Durante el 2025, para las herramientas q..."]
    GEN_11 --> GEN_13
    GEN_12["GEN_12<br/>Durante el 2025, ¿para cuáles de las sig..."]
    GEN_12 --> IGEN_01
    GEN_13["GEN_13<br/>Durante el 2025, ¿para cuáles de las sig..."]
    GEN_13 --> GEN_14
    GEN_14["GEN_14<br/>Durante el 2025, ¿cuáles fueron las razo..."]
    GEN_14 --> TRA_01
    IGEN_01["IGEN_01<br/>Pensando en cómo usted usó IA generativa..."]
    IGEN_01 --> TRA_01
    ITRA_01["ITRA_01<br/>Pensando en cómo usted usó IA tradiciona..."]
    ITRA_01 --> DEC_01
    MAR_01["MAR_01<br/>Durante 2025, ¿usted oyó hablar sobre lo..."]
    MAR_01 -- in [0, 2] --> MAR_03
    MAR_01 -- =1 --> MAR_02
    MAR_02["MAR_02<br/>¿Qué tan familiarizadoa estaba usted con..."]
    MAR_02 --> MAR_03
    MAR_03["MAR_03<br/>Durante 2025, ¿existía en su entidad alg..."]
    MAR_03 --> DAT_01
    MAR_03 -- =1 --> MAR_04
    MAR_04["MAR_04<br/>Durante 2025, ¿qué tan alineadas conside..."]
    MAR_04 --> DAT_01
    MEJ_01["MEJ_01<br/>Pensando en su uso de IA en general dura..."]
    MEJ_01 --> RIE_01
    ORG_01["ORG_01<br/>Durante el 2025, ¿en qué medida los sigu..."]
    ORG_01 --> TEC_01
    ORG_02["ORG_02<br/>Durante el 2025, ¿en qué medida consider..."]
    ORG_02 --> MAR_01
    RIE_01["RIE_01<br/>¿En qué medida considera usted que el us..."]
    RIE_01 --> ADP_01
    TEC_01["TEC_01<br/>Durante el 2025, ¿cuáles fueron las limi..."]
    TEC_01 --> ORG_02
    TEC_02["TEC_02<br/>Durante el 2025, ¿en qué medida los sigu..."]
    TEC_02 --> ORG_01
    TRA_01["TRA_01<br/>Durante el 2025, ¿ha utilizado herramien..."]
    TRA_01 -- in [2, 3] --> TRA_02
    TRA_01 -- =0 --> TRA_06
    TRA_01 -- =1 --> TRA_03
    TRA_02["TRA_02<br/>Durante el 2025, ¿para cuáles de las sig..."]
    TRA_02 --> TRA_04
    TRA_03["TRA_03<br/>Durante el 2025, ¿para cuáles de las sig..."]
    TRA_03 --> TRA_05
    TRA_04["TRA_04<br/>Durante el 2025, ¿con qué frecuencia ha ..."]
    TRA_04 --> ITRA_01
    TRA_05["TRA_05<br/>Durante el 2025, ¿con qué frecuencia ha ..."]
    TRA_05 --> TRA_06
    TRA_06["TRA_06<br/>Durante el 2025, ¿cuáles fueron las razo..."]
    TRA_06 --> DEC_01
    classDef title fill:#f9f,stroke:#333,stroke-width:2px;
