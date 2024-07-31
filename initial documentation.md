Initial documentation test test

  ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  **Workflow**                                                                                             **LOENA**                     **Data     **Transformation Rules**
                                                                                                                                         Format**   
  -------------------------------------------------------------------------------------------------------- ----------------------------- ---------- --------------------------------------------------------------------------------------------------------------
  Response Body -- Get Customer Order Details                                                              Request -- UPP Callback                  

  transaction/transaction_id                                                                               transaction_id                String     No transformation required

  transaction/channel                                                                                      channel                       String     No transformation required

  order/order_receiver_id                                                                                  customer_details/cust_phone   String     No transformation required

  order/order_line_items\[fulfilment_type="LoanPayment"\]/fulfilment/attributes\[key=loan_amount\]/value   additional_info               String     Pass value {\\\"amount\\\":{
                                                                                                                                                    **order/order_line_items\[fulfilment_type="LoanPayment"\]/fulfilment/attributes\[key=loan_amount\]/value**},
                                                                                                                                                    \\\"payment_provider\\\":\\\"**order/payment_method**\\\"}\",

  order/payment_method                                                                                                                              

  N/A                                                                                                      status_code                   String     Pass static value "00"

  N/A                                                                                                      status_desc                   String     Pass static value "Success"
  ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
