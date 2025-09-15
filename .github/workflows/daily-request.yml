name: Daily API Request

on:
  schedule:
    - cron: "0 13 * * 1-5" # lunes a viernes a las 13:00 UTC (~09:00 Chile)
  workflow_dispatch: {}

jobs:
  request:
    runs-on: ubuntu-latest
    concurrency:
      group: daily-request
      cancel-in-progress: true

    steps:
      - name: Build JSON (Chile TZ)
        run: |
          YEAR=$(TZ="America/Santiago" date +"%Y")
          PREV_MONTH=$(TZ="America/Santiago" date -d "-1 month" +"%-m")
          PREV_DAY=$(TZ="America/Santiago" date -d "-1 day" +"%-d")

          cat > payload_base.json <<EOF
          [
            [
              {
                  "idUsuario": "DNI_PLACEHOLDER",
                  "day": 0,
                  "month": $PREV_MONTH,
                  "year": $YEAR,
                  "horaEntrada": "08:00",
                  "horaSalida": "18:00",
                  "dayClass": "imputacionNormal",
                  "editable": true
              },
              {
                  "idUsuario": "DNI_PLACEHOLDER",
                  "day": 1,
                  "month": $PREV_MONTH,
                  "year": $YEAR,
                  "horaEntrada": "08:00",
                  "horaSalida": "18:00",
                  "dayClass": "imputacionNormal",
                  "editable": true
              },
              {
                  "idUsuario": "DNI_PLACEHOLDER",
                  "day": 2,
                  "month": $PREV_MONTH,
                  "year": $YEAR,
                  "horaEntrada": "08:00",
                  "horaSalida": "18:00",
                  "dayClass": "imputacionNormal",
                  "editable": true
              },
              {
                  "idUsuario": "DNI_PLACEHOLDER",
                  "day": 3,
                  "month": $PREV_MONTH,
                  "year": $YEAR,
                  "horaEntrada": "08:00",
                  "horaSalida": "18:00",
                  "dayClass": "imputacionNormal",
                  "editable": true
              },
              {
                  "idUsuario": "DNI_PLACEHOLDER",
                  "day": 4,
                  "month": $PREV_MONTH,
                  "year": $YEAR,
                  "horaEntrada": "08:00",
                  "horaSalida": "18:30",
                  "dayClass": "imputacionNormal",
                  "editable": true,
                  "diferencia": "10:30"
              },
              {
                  "idUsuario": "DNI_PLACEHOLDER",
                  "day": 5,
                  "month": $PREV_MONTH,
                  "year": $YEAR,
                  "horaEntrada": "08:00",
                  "horaSalida": "18:00",
                  "dayClass": "imputacionFestivo",
                  "editable": true
              },
              {
                  "idUsuario": "DNI_PLACEHOLDER",
                  "day": 6,
                  "month": $PREV_MONTH,
                  "year": $YEAR,
                  "horaEntrada": "08:00",
                  "horaSalida": "18:00",
                  "dayClass": "imputacionFestivo",
                  "editable": true
              },
              {
                  "idUsuario": "DNI_PLACEHOLDER",
                  "day": 7,
                  "month": $PREV_MONTH,
                  "year": $YEAR,
                  "horaEntrada": "08:00",
                  "horaSalida": "18:00",
                  "dayClass": "imputacionNormal",
                  "editable": true,
                  "horaEntradaDefault": "08:00",
                  "horaSalidaDefault": "17:30"
              },
              {
                  "idUsuario": "DNI_PLACEHOLDER",
                  "day": 8,
                  "month": $PREV_MONTH,
                  "year": $YEAR,
                  "horaEntrada": "08:00",
                  "horaSalida": "18:00",
                  "dayClass": "imputacionNormal",
                  "editable": true
              },
              {
                  "idUsuario": "DNI_PLACEHOLDER",
                  "day": 9,
                  "month": $PREV_MONTH,
                  "year": $YEAR,
                  "horaEntrada": "08:00",
                  "horaSalida": "18:00",
                  "dayClass": "imputacionNormal",
                  "editable": true
              },
              {
                  "idUsuario": "DNI_PLACEHOLDER",
                  "day": 10,
                  "month": $PREV_MONTH,
                  "year": $YEAR,
                  "horaEntrada": "08:00",
                  "horaSalida": "18:00",
                  "dayClass": "imputacionNormal",
                  "editable": true
              },
              {
                  "idUsuario": "DNI_PLACEHOLDER",
                  "day": 11,
                  "month": $PREV_MONTH,
                  "year": $YEAR,
                  "horaEntrada": "08:00",
                  "horaSalida": "18:00",
                  "dayClass": "imputacionNormal",
                  "editable": true
              },
              {
                  "idUsuario": "DNI_PLACEHOLDER",
                  "day": 12,
                  "month": $PREV_MONTH,
                  "year": $YEAR,
                  "horaEntrada": "08:00",
                  "horaSalida": "18:00",
                  "dayClass": "imputacionFestivo",
                  "editable": true
              },
              {
                  "idUsuario": "DNI_PLACEHOLDER",
                  "day": 13,
                  "month": $PREV_MONTH,
                  "year": $YEAR,
                  "horaEntrada": "08:00",
                  "horaSalida": "18:00",
                  "dayClass": "imputacionFestivo",
                  "editable": true
              },
              {
                  "idUsuario": "DNI_PLACEHOLDER",
                  "day": 14,
                  "month": $PREV_MONTH,
                  "year": $YEAR,
                  "horaEntrada": "08:00",
                  "horaSalida": "18:00",
                  "dayClass": "imputacionNormal",
                  "editable": true
              },
              {
                  "idUsuario": "DNI_PLACEHOLDER",
                  "day": 15,
                  "month": $PREV_MONTH,
                  "year": $YEAR,
                  "horaEntrada": "08:00",
                  "horaSalida": "18:00",
                  "dayClass": "imputacionNormal",
                  "editable": true
              },
              {
                  "idUsuario": "DNI_PLACEHOLDER",
                  "day": 16,
                  "month": $PREV_MONTH,
                  "year": $YEAR,
                  "horaEntrada": "08:00",
                  "horaSalida": "18:00",
                  "dayClass": "imputacionNormal",
                  "editable": true
              },
              {
                  "idUsuario": "DNI_PLACEHOLDER",
                  "day": 17,
                  "month": $PREV_MONTH,
                  "year": $YEAR,
                  "horaEntrada": "08:00",
                  "horaSalida": "18:00",
                  "dayClass": "imputacionNormal",
                  "editable": true
              },
              {
                  "idUsuario": "DNI_PLACEHOLDER",
                  "day": 18,
                  "month": $PREV_MONTH,
                  "year": $YEAR,
                  "horaEntrada": "08:00",
                  "horaSalida": "18:00",
                  "dayClass": "imputacionNormal",
                  "editable": true
              },
              {
                  "idUsuario": "DNI_PLACEHOLDER",
                  "day": 19,
                  "month": $PREV_MONTH,
                  "year": $YEAR,
                  "horaEntrada": "08:00",
                  "horaSalida": "18:00",
                  "dayClass": "imputacionFestivo",
                  "editable": true
              },
              {
                  "idUsuario": "DNI_PLACEHOLDER",
                  "day": 20,
                  "month": $PREV_MONTH,
                  "year": $YEAR,
                  "horaEntrada": "08:00",
                  "horaSalida": "18:00",
                  "dayClass": "imputacionFestivo",
                  "editable": true
              },
              {
                  "idUsuario": "DNI_PLACEHOLDER",
                  "day": 21,
                  "month": $PREV_MONTH,
                  "year": $YEAR,
                  "horaEntrada": "08:00",
                  "horaSalida": "18:00",
                  "dayClass": "imputacionNormal",
                  "editable": true
              },
              {
                  "idUsuario": "DNI_PLACEHOLDER",
                  "day": 22,
                  "month": $PREV_MONTH,
                  "year": $YEAR,
                  "horaEntrada": "08:00",
                  "horaSalida": "18:00",
                  "dayClass": "imputacionNormal",
                  "editable": true
              },
              {
                  "idUsuario": "DNI_PLACEHOLDER",
                  "day": 23,
                  "month": $PREV_MONTH,
                  "year": $YEAR,
                  "horaEntrada": "08:00",
                  "horaSalida": "18:00",
                  "dayClass": "imputacionNormal",
                  "editable": true
              },
              {
                  "idUsuario": "DNI_PLACEHOLDER",
                  "day": 24,
                  "month": $PREV_MONTH,
                  "year": $YEAR,
                  "horaEntrada": "08:00",
                  "horaSalida": "18:00",
                  "dayClass": "imputacionNormal",
                  "editable": true
              },
              {
                  "idUsuario": "DNI_PLACEHOLDER",
                  "day": 25,
                  "month": $PREV_MONTH,
                  "year": $YEAR,
                  "horaEntrada": "08:00",
                  "horaSalida": "18:00",
                  "dayClass": "imputacionNormal",
                  "editable": true
              },
              {
                  "idUsuario": "DNI_PLACEHOLDER",
                  "day": 26,
                  "month": $PREV_MONTH,
                  "year": $YEAR,
                  "horaEntrada": "08:00",
                  "horaSalida": "18:00",
                  "dayClass": "imputacionFestivo",
                  "editable": true
              },
              {
                  "idUsuario": "DNI_PLACEHOLDER",
                  "day": 27,
                  "month": $PREV_MONTH,
                  "year": $YEAR,
                  "horaEntrada": "08:00",
                  "horaSalida": "18:00",
                  "dayClass": "imputacionFestivo",
                  "editable": true
              },
              {
                  "idUsuario": "DNI_PLACEHOLDER",
                  "day": 28,
                  "month": $PREV_MONTH,
                  "year": $YEAR,
                  "horaEntrada": "08:00",
                  "horaSalida": "18:00",
                  "dayClass": "imputacionNormal",
                  "editable": true
              },
              {
                  "idUsuario": "DNI_PLACEHOLDER",
                  "day": 29,
                  "month": $PREV_MONTH,
                  "year": $YEAR,
                  "horaEntrada": "08:00",
                  "horaSalida": "18:00",
                  "dayClass": "imputacionNormal",
                  "editable": true
              }
            ],
            []
          ]
          EOF

          echo "✅ JSON generado:"
          cat payload_base.json

      - name: Call API for each user
        run: |
          USERS_JSON='${{ secrets.USERS_JSON }}'
      
          echo "Iterando sobre usuarios..."
          echo "$USERS_JSON" | jq -c '.[]' | while read user; do
            DNI=$(echo $user | jq -r '.dni')
            MATRICULA=$(echo $user | jq -r '.matricula')
            USER_HASH=$(echo -n "$DNI" | sha256sum | cut -c1-8)
      
            echo "➡️ Enviando request para usuario hash=$USER_HASH"
      
            # Crear payload específico con el DNI
            jq --arg dni "$DNI" '.[][] |= (.idUsuario = $dni)' payload_base.json > payload.json
      
            RESPONSE=$(curl -s -o response.json -w "%{http_code}" \
              -X POST "${{ secrets.API_URL }}" \
              -H "Accept: application/json, text/plain, */*" \
              -H "Content-Type: application/json" \
              -H "Matricula: $MATRICULA" \
              -H "dni: $DNI" \
              -b "cookiesession1=${{ secrets.COOKIE }}" \
              --data-binary @payload.json)
      
            if [ "$RESPONSE" -lt 200 ] || [ "$RESPONSE" -ge 300 ]; then
              echo "❌ Falló request para usuario hash=$USER_HASH (HTTP $RESPONSE)"
              if [ -s response.json ]; then
                jq '.status?, .message?' response.json || echo "ℹ️ Respuesta no es JSON válida"
              else
                echo "ℹ️ Respuesta vacía del servidor"
              fi
              exit 1
            fi
      
            echo "✅ Request exitoso para usuario hash=$USER_HASH"
            if [ -s response.json ]; then
              jq '.status?, .message?' response.json || echo "ℹ️ Respuesta no es JSON válida"
            else
              echo "ℹ️ Respuesta vacía del servidor"
            fi
          done
