<script>

</script>


<main>
    <h4 class="text-primary">Patients Registration Form</h4>
        <div class="mb-3 col w-50">
          <label for="patientsTelephone" class="form-label">Telephone</label>
          <input
            type="tel"
            class="form-control"
            id="patientsTelephone"
            name="patientsTelephone"
          />
        </div>
        <div class="mb-3 col w-50">
          <label for="patientsName" class="form-label">Name</label>
          <input
            type="text"
            class="form-control"
            id="patientsName"
            name="patientsName"
          />
        </div>

        <div class="row">
          <div class="mb-3 col w-50">
            <label for="patientsDateOfBirth" class="form-label"
              >Date of Birth</label
            >
            <input
              type="date"
              name="patientsDateOfBirth"
              id="patientsDateOfBirth"
              class="form-control"
            />
          </div>

          <div class="mb-3 col w-50">
            <label for="patientsIdNumber" class="form-label">ID Number</label>
            <input
              type="text"
              class="form-control"
              id="patientsIdNumber"
              name="patientsIdNumber"
              minlength="4"
              maxlength="8"
              required
            />
          </div>
        </div>

        <div class="mb-3 col w-50">
          <label for="patientsAddress" class="form-label">Address</label>
          <input
            type="text"
            class="form-control"
            id="patientsAddress"
            name="patientsAddress"
          />
        </div>

        <div class="row">
          <div class="mb-3 col w-50">
            <label for="patientsCounty" class="form-label">County</label>
            <input
              type="text"
              class="form-control"
              id="patientsCounty"
              name="patientsCounty"
            />
          </div>
          <div class="mb-3 col w-50">
            <label for="patientsSubCounty" class="form-label">Sub County</label
            ><input
              type="text"
              class="form-control"
              id="patientsSubCounty"
              name="patientsSubCounty"
            />
          </div>
        </div>

        <div class="mb-3 w-50">
          <label for="patientsEmail" class="form-label">Email</label>
          <input
            type="email"
            class="form-control"
            name="patientsEmail"
            id="patientsEmail"
            required
          />
        </div>

        <div class="row">
          <label for="patientsGender" class="form-label">Gender</label>
          <select
            class="form-select m-3 col w-50"
            aria-label="Default select example"
            id="patientsGender"
            name="patientsGender"
          >
            <option value="Male">Male</option>
            <option value="Female">Female</option>
            <option value="Other">Other</option>
            <option value="Rather not say">Rather not say</option>
          </select>
          <label for="patientsMaritalStatus" class="form-label"
            >Marital Status</label
          >
          <select
            class="form-select m-3 col w-50"
            aria-label="Default select example"
            id="patientsMaritalStatus"
            name="patientsMaritalStatus"
          >
            <option value="Single">Single</option>
            <option value="Married">Married</option>
            <option value="Divorced">Divorced</option>
          </select>
        </div>

</main>

<style>

</style>