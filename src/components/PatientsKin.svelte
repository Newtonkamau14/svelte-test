<script>
</script>

<main>
    <h4 class="text-primary mt-3">Next of kin</h4>
    <div class="mb-3">
      <label for="kinsName" class="form-label">Name</label>
      <input
        type="text"
        class="form-control"
        id="kinsName"
        name="kinsName"
      />
    </div>

    <div class="row">
     <div class="mb-3 col w-50">
        <label for="kinsDateOfBirth" class="form-label"
          >Date of Birth</label
        >
        <input type="date" name="kinsDateOfBirth" id="kinsDateOfBirth" class="form-control">
      </div>

      <div class="mb-3 col w-50">
        <label for="kinsIdNumber" class="form-label">ID Number</label>
        <input
          type="text"
          class="form-control"
          id="kinsIdNumber"
          name="kinsIdNumber"
          maxlength="8"
        />
      </div>
    </div>

    <div class="row">
      <label for="kinsGender" class="form-label">Gender</label>
      <select
        class="form-select m-3 col w-50"
        aria-label="Default select example"
        id="kinsGender"
        name="kinsGender"
      >
        <option value="Male">Male</option>
        <option value="Female">Female</option>
        <option value="Other">Other</option>
        <option value="Rather not say">Rather not say</option>
      </select>
      <label for="kinsRelationship" class="form-label">Relationship</label>
      <select
        class="form-select m-3 col w-50"
        aria-label="Default select example"
        id="kinsRelationship"
        name="kinsRelationship"
      >
        <option value="Father">Father</option>
        <option value="Mother">Mother</option>
        <option value="Sibling">Sibling</option>
        <option value="Guardian">Guardian</option>
        <option value="Cousin">Cousin</option>
        <option value="Uncle">Uncle</option>
        <option value="Aunt">Aunt</option>
      </select>
    </div>

    <div class="mb-3">
      <label for="kinsTelephone" class="form-label"
        >Telephone<input
          type="tel"
          name="kinsTelephone"
          id="kinsTelephone"
          class="form-control"
      /></label>
    </div>
</main>

<style>
</style>
