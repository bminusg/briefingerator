<template>
  <div class="generator--steps-meta">
    <h4>Meta Setup</h4>
    <div class="row g-3">
      <div class="col">
        <input
          type="text"
          class="form-control"
          placeholder="First name"
          aria-label="First name"
        />
      </div>
      <div class="col">
        <label for="exampleDataList" class="form-label">Campaign-Type</label>
        <input class="form-control" list="datalistOptions" id="exampleDataList" placeholder="Type to search...">
        <datalist id="datalistOptions">
          <option value="Volks-Kampagne"/>
          <option value="Brand Story"/>
          <option value="Product Story"/>
          <option value="Branding"/>
        </datalist>
      </div>
    </div>
  </div>
</template>
