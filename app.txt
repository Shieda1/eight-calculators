// https://calculator.swiftutors.com/fluid-density-calculator.html

const v1 =  document.getElementById('v1');
const v2 = document.getElementById('v2');
const v3 = document.getElementById('v3');
const v4 = document.getElementById('v4');
const v5 = document.getElementById('v5');
const v6 = document.getElementById('v6');
const v7 = document.getElementById('v7');
const btn = document.getElementById('btn');
const result = document.getElementById('result');

// radio buttons
const finalDensityRadio = document.getElementById('finalDensityRadio');
const initialDensityRadio = document.getElementById('initialDensityRadio');
const coefficientofVolumetricTemperatureExpansionRadio = document.getElementById('coefficientofVolumetricTemperatureExpansionRadio');
const initialTemperatureRadio = document.getElementById('initialTemperatureRadio');
const finalTemperatureRadio = document.getElementById('finalTemperatureRadio');
const initialPressureRadio = document.getElementById('initialPressureRadio');
const finalPressureRadio = document.getElementById('finalPressureRadio');
const bulkModulusFluidElasticityRadio = document.getElementById('bulkModulusFluidElasticityRadio');

let finalDensity;
let initialDensity = v1;
let coefficientofVolumetricTemperatureExpansion = v2;
let initialTemperature = v3;
let finalTemperature = v4;
let initialPressure = v5;
let finalPressure = v6;
let bulkModulusFluidElasticity = v7;

// labels of the inpust
const variable1 = document.getElementById('variable1');
const variable2 = document.getElementById('variable2');
const variable3 = document.getElementById('variable3');
const variable4 = document.getElementById('variable4');
const variable5 = document.getElementById('variable5');
const variable6 = document.getElementById('variable6');
const variable7 = document.getElementById('variable7');

finalDensityRadio.addEventListener('click', function() {
  variable1.textContent = '(ρ0) Initial Density (kg/m³)';
  variable2.textContent = '(β) Coefficient of Volumetric Temperature Expansion (m³/m³°C)';
  variable3.textContent = '(t0) Initial Temperature (°C)';
  variable4.textContent = '(t1) Final Temperature (°C)';
  variable5.textContent = '(p0) Initial Pressure (N/m²)';
  variable6.textContent = '(p1) Final Pressure (N/m²)';
  variable7.textContent = '(E) Bulk Modulus Fluid Elasticity (N/m²)';
  initialDensity = v1;
  coefficientofVolumetricTemperatureExpansion = v2;
  initialTemperature = v3;
  finalTemperature = v4;
  initialPressure = v5;
  finalPressure = v6;
  bulkModulusFluidElasticity = v7;
  result.textContent = '';
});

initialDensityRadio.addEventListener('click', function() {
  variable1.textContent = '(ρ1) Final Density (kg/m³)';
  variable2.textContent = '(β) Coefficient of Volumetric Temperature Expansion (m³/m³°C)';
  variable3.textContent = '(t0) Initial Temperature (°C)';
  variable4.textContent = '(t1) Final Temperature (°C)';
  variable5.textContent = '(p0) Initial Pressure (N/m²)';
  variable6.textContent = '(p1) Final Pressure (N/m²)';
  variable7.textContent = '(E) Bulk Modulus Fluid Elasticity (N/m²)';
  finalDensity = v1;
  coefficientofVolumetricTemperatureExpansion = v2;
  initialTemperature = v3;
  finalTemperature = v4;
  initialPressure = v5;
  finalPressure = v6;
  bulkModulusFluidElasticity = v7;
  result.textContent = '';
});

coefficientofVolumetricTemperatureExpansionRadio.addEventListener('click', function() {
  variable1.textContent = '(ρ1) Final Density (kg/m³)';
  variable2.textContent = '(ρ0) Initial Density (kg/m³)';
  variable3.textContent = '(t0) Initial Temperature (°C)';
  variable4.textContent = '(t1) Final Temperature (°C)';
  variable5.textContent = '(p0) Initial Pressure (N/m²)';
  variable6.textContent = '(p1) Final Pressure (N/m²)';
  variable7.textContent = '(E) Bulk Modulus Fluid Elasticity (N/m²)';
  finalDensity = v1;
  initialDensity = v2;
  initialTemperature = v3;
  finalTemperature = v4;
  initialPressure = v5;
  finalPressure = v6;
  bulkModulusFluidElasticity = v7;
  result.textContent = '';
});

initialTemperatureRadio.addEventListener('click', function() {
  variable1.textContent = '(ρ1) Final Density (kg/m³)';
  variable2.textContent = '(ρ0) Initial Density (kg/m³)';
  variable3.textContent = '(β) Coefficient of Volumetric Temperature Expansion (m³/m³°C)';
  variable4.textContent = '(t1) Final Temperature (°C)';
  variable5.textContent = '(p0) Initial Pressure (N/m²)';
  variable6.textContent = '(p1) Final Pressure (N/m²)';
  variable7.textContent = '(E) Bulk Modulus Fluid Elasticity (N/m²)';
  finalDensity = v1;
  initialDensity = v2;
  coefficientofVolumetricTemperatureExpansion = v3;
  finalTemperature = v4;
  initialPressure = v5;
  finalPressure = v6;
  bulkModulusFluidElasticity = v7;
  result.textContent = '';
});

finalTemperatureRadio.addEventListener('click', function() {
  variable1.textContent = '(ρ1) Final Density (kg/m³)';
  variable2.textContent = '(ρ0) Initial Density (kg/m³)';
  variable3.textContent = '(β) Coefficient of Volumetric Temperature Expansion (m³/m³°C)';
  variable4.textContent = '(t0) Initial Temperature (°C)';
  variable5.textContent = '(p0) Initial Pressure (N/m²)';
  variable6.textContent = '(p1) Final Pressure (N/m²)';
  variable7.textContent = '(E) Bulk Modulus Fluid Elasticity (N/m²)';
  finalDensity = v1;
  initialDensity = v2;
  coefficientofVolumetricTemperatureExpansion = v3;
  initialTemperature = v4;
  initialPressure = v5;
  finalPressure = v6;
  bulkModulusFluidElasticity = v7;
  result.textContent = '';
});

initialPressureRadio.addEventListener('click', function() {
  variable1.textContent = '(ρ1) Final Density (kg/m³)';
  variable2.textContent = '(ρ0) Initial Density (kg/m³)';
  variable3.textContent = '(β) Coefficient of Volumetric Temperature Expansion (m³/m³°C)';
  variable4.textContent = '(t0) Initial Temperature (°C)';
  variable5.textContent = '(t1) Final Temperature (°C)';
  variable6.textContent = '(p1) Final Pressure (N/m²)';
  variable7.textContent = '(E) Bulk Modulus Fluid Elasticity (N/m²)';
  finalDensity = v1;
  initialDensity = v2;
  coefficientofVolumetricTemperatureExpansion = v3;
  initialTemperature = v4;
  finalTemperature = v5;
  finalPressure = v6;
  bulkModulusFluidElasticity = v7;
  result.textContent = '';
});

finalPressureRadio.addEventListener('click', function() {
  variable1.textContent = '(ρ1) Final Density (kg/m³)';
  variable2.textContent = '(ρ0) Initial Density (kg/m³)';
  variable3.textContent = '(β) Coefficient of Volumetric Temperature Expansion (m³/m³°C)';
  variable4.textContent = '(t0) Initial Temperature (°C)';
  variable5.textContent = '(p0) Initial Pressure (N/m²)';
  variable6.textContent = '(p1) Final Pressure (N/m²)';
  variable7.textContent = '(E) Bulk Modulus Fluid Elasticity (N/m²)';
  finalDensity = v1;
  initialDensity = v2;
  coefficientofVolumetricTemperatureExpansion = v3;
  initialTemperature = v4;
  initialPressure = v5;
  finalTemperature = v6;
  bulkModulusFluidElasticity = v7;
  result.textContent = '';
});

bulkModulusFluidElasticityRadio.addEventListener('click', function() {
  variable1.textContent = '(ρ1) Final Density (kg/m³)';
  variable2.textContent = '(ρ0) Initial Density (kg/m³)';
  variable3.textContent = '(β) Coefficient of Volumetric Temperature Expansion (m³/m³°C)';
  variable4.textContent = '(t0) Initial Temperature (°C)';
  variable5.textContent = '(t1) Final Temperature (°C)';
  variable6.textContent = '(p1) Final Pressure (N/m²)';
  variable7.textContent = '(E) Bulk Modulus Fluid Elasticity (N/m²)';
  finalDensity = v1;
  initialDensity = v2;
  coefficientofVolumetricTemperatureExpansion = v3;
  initialTemperature = v4;
  initialPressure = v5;
  finalTemperature = v6;
  finalPressure = v7;
  result.textContent = '';
});

btn.addEventListener('click', function() {
  
  if(finalDensityRadio.checked)
    result.textContent = `Final Density = ${computeFinalDensity().toFixed(2)} kg/m³`;

  else if(initialDensityRadio.checked)
    result.textContent = `Initial Density = ${computeInitialDensity().toFixed(2)} kg/m³`;

  else if(coefficientofVolumetricTemperatureExpansionRadio.checked)
    result.textContent = `Coefficient of Volumetric Temperature Expansion = ${computeCoefficientofVolumetricTemperatureExpansion().toFixed(2)} m³/m³°C`;

  else if(initialTemperatureRadio.checked)
    result.textContent = `Initial Temperature = ${computeInitialTemperature().toFixed(2)} °C`;

  else if(finalTemperatureRadio.checked)
    result.textContent = `Final Temperature = ${computeFinalTemperature().toFixed(2)} °C`;

  else if(initialPressureRadio.checked)
    result.textContent = `Initial Pressure = ${computeInitialPressure().toFixed(2)} N/m²`;

  else if(finalPressureRadio.checked)
    result.textContent = `Final Pressure = ${computeFinalPressure().toFixed(2)} N/m²`;

  else if(bulkModulusFluidElasticityRadio.checked)
    result.textContent = `Bulk Modulus Fluid Elasticity = ${computeBulkModulusFluidElasticity().toFixed(2)} N/m²`;
})

// calculation

function computeFinalDensity() {
  return Number(initialDensity.value) / (1 + Number(coefficientofVolumetricTemperatureExpansion.value) * (Number(finalTemperature.value) - Number(initialTemperature.value))) / (1 - (Number(finalPressure.value) - Number(initialPressure.value)) / Number(bulkModulusFluidElasticity.value));
}

function computeInitialDensity() {
  return Number(costofGoodsManufactured.value) - Number(directLaborCost.value) - Number(factoryOverheadCost.value) - Number(openingWorkinProcessInventory.value) + Number(endingWorkinProcessInventory.value);
}

function computeCoefficientofVolumetricTemperatureExpansion() {
  return Number(costofGoodsManufactured.value) - Number(directMaterialsCost.value) - Number(factoryOverheadCost.value) - Number(openingWorkinProcessInventory.value) + Number(endingWorkinProcessInventory.value);
}

function computeInitialTemperature() {
  return Number(costofGoodsManufactured.value) - Number(directMaterialsCost.value) - Number(directLaborCost.value) - Number(openingWorkinProcessInventory.value) + Number(endingWorkinProcessInventory.value);
}

function computeFinalTemperature() {
  return Number(costofGoodsManufactured.value) - Number(directMaterialsCost.value) - Number(directLaborCost.value) - Number(factoryOverheadCost.value) + Number(endingWorkinProcessInventory.value);
}

function computeInitialPressure() {
  return Number(directMaterialsCost.value) + Number(directLaborCost.value) + Number(factoryOverheadCost.value) + Number(openingWorkinProcessInventory.value) - Number(costofGoodsManufactured.value);
}

function computeFinalPressure() {
  return Number(costofGoodsManufactured.value) - Number(directMaterialsCost.value) - Number(directLaborCost.value) - Number(factoryOverheadCost.value) + Number(endingWorkinProcessInventory.value);
}

function computeBulkModulusFluidElasticity() {
  return Number(directMaterialsCost.value) + Number(directLaborCost.value) + Number(factoryOverheadCost.value) + Number(openingWorkinProcessInventory.value) - Number(costofGoodsManufactured.value);
}