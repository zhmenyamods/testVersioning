---
title: Guide 4
deprecated: false
hidden: false
metadata:
  robots: index
---
<Table align={["left","left","left"]}>
  <thead>
    <tr>
      <th style={{ textAlign: "left" }}>
        Decline Response Codes
      </th>

      <th style={{ textAlign: "left" }}>
        Issuer Requirements
      </th>

      <th style={{ textAlign: "left" }}>
        Merchant Reattempts
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td style={{ textAlign: "left" }}>
        Category 1: Issuer will never approve

        04 (Pick up card \[no fraud])

        <br />

        07 (Pick up card, special condition \[fraud account])12 (Invalid Transaction)
        14 (Invalid account number \[no such number])
        15 (No such issuer \[first 8 digits of account number do not relate to an issuing identifier])
        41 (Lost card, pick up)
        43 (Stolen card, pick up)
        46 (Closed account)
        57 (Transaction not permitted to cardholder)
        R0 (Stop payment order)
        R1 (Revocation of authorization order)
        R3 (Revocation of all authorizations order)
      </td>

      <td style={{ textAlign: "left" }}>
        Limit use to transactions that will never be approved
      </td>

      <td style={{ textAlign: "left" }}>
        Reattempt not permitted
      </td>
    </tr>

    <tr>
      <td style={{ textAlign: "left" }}>
        Category 2: Issuer cannot approve at this time

        03 (Invalid merchant)\
        19 (Re-enter transaction)
        39 (No credit account)
        51 (Not sufficient funds)
        52 (No checking account)
        53 (No savings account)
        59 (Suspected fraud)
        61 (Exceeds approval amount limit)
        62 (Restricted card \[card invalid in region or country])
        65 (Exceeds withdrawal frequency limit)
        75 (Allowable number of PIN-entry tries exceeded)
        78 (Blocked, first used or special condition \[account is temporarily blocked])
        86 (Cannot verify PIN)
        91 (Issuer or switch inoperative)
        93 (Transaction cannot be completed – violation of law)
        96 (System malfunction)
        5C (Transaction not supported / blocked by issuer)
        9G (Blocked by cardholder / contact cardholder)
        N3 (Cash service not available)
        N4 (Cash request exceeds issuer or approved limit)
        Z5 (valid account but amount not supported)
      </td>

      <td style={{ textAlign: "left" }}>
        Use to indicate the decline condition
      </td>

      <td style={{ textAlign: "left" }}>
        Reattempt permitted up to 20 attempts in 30 days
      </td>
    </tr>

    <tr>
      <td style={{ textAlign: "left" }}>
        Category 3: Data quality (Revalidate payment information before reattempt)

        54 (Expired card or expiration date missing)\
        55 (PIN incorrect or missing)
        70 (PIN data required \[Europe Region only])
        82 (Negative Online CAM, dCVV, iCVV, or CVV results)
        1A (Additional customer authentication required \[Europe Region only])
        6P (Verification Failed \[Cardholder Identification does not match issuer records])
        N7 (Decline for CVV2 failure)
      </td>

      <td style={{ textAlign: "left" }}>
        Use to indicate the decline condition/ data element in need of correction
      </td>

      <td style={{ textAlign: "left" }}>
        Revalidate payment information\
        before reattempt.

        Reattempt permitted up to 20 attempts in 30 days
      </td>
    </tr>

    <tr>
      <td style={{ textAlign: "left" }}>
        Category 4: Generic response codes

        All other Decline Response codes
      </td>

      <td style={{ textAlign: "left" }}>
        Limit use to transactions where no other value applies
      </td>

      <td style={{ textAlign: "left" }}>
        Reattempt permitted up to 20 attempts in 30 days
      </td>
    </tr>
  </tbody>
</Table>