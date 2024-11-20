#Getting started
------------

### Install dependencies:
- `npm install`
- `npm install --prefix server`

### Run for development
 - Run client
 `npm run start // for run client, in port 3001`
 - Open browser and open http://{ip}:3001

### Run for zahir 7
 - Run client
 `npm run start:zahir7 // for run client, in port 3002`
 - Open browser and open http://{ip}:3002

### Run for production
 - Build
 `npm run build`
 - Run
 `npm run prod`
 - Open browser and open http://{ip}:3001

 ### Packaging onpremise
 - Install library pkg
 `npm install -g pkg`
 - Build
 `npm run build:onpremise`
 - Package
 `npm run build:pkg // output file in pkg/`
 - Execute
 `double click file exe or etc`
 - Open browser and open http://{ip}:3001
 *Note: untuk menjalankan file .exe atau extensi yang lainnya, harus ada `.env`*

<!-- documetasi redundant field
  <RedundantField
    propsFormik={this.props.propsFormik}
    component={FormikTextField} // di panggil dari folder componentFormik
    tuning={{
        debounce_time: 800, // sekarang tidak ngefek jika angkanya dibawah 600
        // deps_value jangan langsung dicopy jika tidak butuh
        deps_value: [this.props.propsFormik.values.line_items[index].product == null ? "0" : this.props.propsFormik.values.line_items[index].product.id]
      }}
    // getValue optional
    getValue={(values) => {
        return values == null ? "0" : values.line_items[index].quantity;
      }}
    onChangeValue={(value, propsF) => {
        this.props.handleChangeValue('line_items.quantity', index)(value, propsF);
      }}
    validate={(v) => {
      kondisi di buat function supaya tidak bikin lag dan terender berkali kali
      const f = this.props.validateQuantity(index) ? this.props.validateNegativeStock(index) ? stockNegative : requiredQuantity : null
      if (f != null) {
        // console.log("LineItemsFormTransaction, validate, f not null", f(v));
        return f(v);
      } else {
        // console.log("LineItemsFormTransaction, validate, f is null", v);
        return null;
      }
    }}
    onFocusMapValue={(value) => {
        // onFocusMap ini awalnya bernama onFocusInput
        // kenapa berubah karena kegunaan nya yang mapping
        // value ketika focus
        if (value == '-' || value == '- 0') {
          return "0";
        } else {
          return value;
        }
      }}
      yang biasanya props di luar sekarang dimasukan kedalam inputProps property, kecuali property validate
    inputProps={{
      disabled: createPending || patchPending || !connection,
      name: `line_items[${index}].quantity`,
      type: "text",
      noLabel: true,
      lite: true,
      right: true,
      loginClass: true,
      formatValue: 'price',
    }}
  /> -->