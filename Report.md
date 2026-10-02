# 0) Name and ID

- **Name:** Sharna Barua Srity
- **ID:** 0112310286


# A) Test Case List

# Test Case Table

| TC ID | Test Class | Test Case | Expected Result |
|---|---|---|---|
| T-001 | BookingTest | `constructorSetsAllFields()` | All booking fields are initialized with the supplied values. |
| T-002 | BookingTest | `newBookingStartsAsActive()` | A new booking has `ACTIVE` status. |
| T-003 | BookingTest | `completeBookingSetsStatusToCompleted()` | Completing a booking changes status to `COMPLETED`. |
| T-004 | BookingTest | `completeBookingDoesNotChangeOtherFields()` | Completing a booking does not change booking ID, vehicle, or amount. |
| T-005 | BookingTest | `cancelBookingSetsStatusToCancelled()` | Cancelling a booking changes status to `CANCELLED`. |
| T-006 | BookingTest | `cancelAfterCompleteOverridesStatus()` | Cancelling a completed booking changes status to `CANCELLED`. |
| T-007 | BookingTest | `completeAfterCancelOverridesStatus()` | Completing a cancelled booking changes status to `COMPLETED`. |
| T-008 | BookingTest | `toStringContainsBookingId()` | `toString()` contains the booking ID. |
| T-009 | ParkingSlotTest | `testConstructor()` | Slot fields are initialized correctly; slot is active, balance is zero, wallet exists, and bookings are empty. |
| T-010 | ParkingSlotTest | `testDeactivateSlot()` | Deactivating a slot makes it inactive. |
| T-011 | ParkingSlotTest | `testActivateSlot()` | An inactive slot can be activated. |
| T-012 | ParkingSlotTest | `testSlotIsAvailableWhenNoBookings()` | A slot with no bookings is available. |
| T-013 | ParkingSlotTest | `testSlotIsAvailableForNonOverlappingBooking()` | A new booking that starts when an existing booking ends is allowed. |
| T-014 | ParkingSlotTest | `testSlotIsUnavailableForOverlappingBooking()` | An overlapping booking is rejected as unavailable. |
| T-015 | ParkingSlotTest | `testSlotIsUnavailableWhenNewBookingStartsDuringExistingBooking()` | A booking starting during an existing booking is unavailable. |
| T-016 | ParkingSlotTest | `testSlotIsUnavailableWhenNewBookingEndsDuringExistingBooking()` | A booking ending during an existing booking is unavailable. |
| T-017 | ParkingSlotTest | `testInactiveSlotIsNotCompatible()` | An inactive slot is not compatible with a vehicle. |
| T-018 | ParkingSlotTest | `testMotorcycleCompatibleWithCompactSlot()` | Motorcycle is compatible with a compact slot. |
| T-019 | ParkingSlotTest | `testMotorcycleCompatibleWithRegularSlot()` | Motorcycle is compatible with a regular slot. |
| T-020 | ParkingSlotTest | `testMotorcycleNotCompatibleWithHandicappedSlot()` | Motorcycle is not compatible with a handicapped slot. |
| T-021 | ParkingSlotTest | `testCarCompatibleWithRegularSlot()` | Car is compatible with a regular slot. |
| T-022 | ParkingSlotTest | `testCarCompatibleWithLargeSlot()` | Car is compatible with a large slot. |
| T-023 | ParkingSlotTest | `testCarNotCompatibleWithCompactSlot()` | Car is not compatible with a compact slot. |
| T-024 | ParkingSlotTest | `testBusCompatibleWithLargeSlot()` | Bus is compatible with a large slot. |
| T-025 | ParkingSlotTest | `testBusNotCompatibleWithRegularSlot()` | Bus is not compatible with a regular slot. |
| T-026 | ParkingSlotTest | `testBicycleCompatibleWithHandicappedSlot()` | Bicycle is compatible with a handicapped slot. |
| T-027 | ParkingSlotTest | `testMicrocarCompatibleWithCompactSlot()` | Microcar is compatible with a compact slot. |
| T-028 | ParkingSlotTest | `testMicrocarNotCompatibleWithLargeSlot()` | Microcar is not compatible with a large slot. |
| T-029 | ParkingSlotTest | `testInitialBalanceIsZero()` | A new parking slot has zero balance. |
| T-030 | ParkingSlotTest | `testGetWallet()` | Slot wallet exists and has zero initial balance. |
| T-031 | ParkingSlotTest | `testGetBookings()` | Slot bookings collection exists and is initially empty. |
| T-032 | ParkingSystemTest | `testSingletonReturnsSameInstance()` | `getInstance()` returns the same `ParkingSystem` instance. |
| T-033 | ParkingSystemTest | `testInitialVehiclesListIsEmpty()` | Vehicle list is initially empty. |
| T-034 | ParkingSystemTest | `testInitialParkingSlotsListIsEmpty()` | Parking-slot list is initially empty. |
| T-035 | ParkingSystemTest | `testInitialBookingsListIsEmpty()` | Booking list is initially empty. |
| T-036 | ParkingSystemTest | `testInitialParkingRate()` | Initial parking rate is `10.0` per hour. |
| T-037 | ParkingSystemTest | `testInitialSystemBalance()` | Initial system balance is `0.0`. |
| T-038 | ParkingSystemTest | `testAddVehicle()` | A vehicle can be added and appears in the vehicle list. |
| T-039 | ParkingSystemTest | `testAddMultipleVehicles()` | Multiple vehicles can be added successfully. |
| T-040 | ParkingSystemTest | `testAddParkingSlot()` | A parking slot can be added and appears in the slot list. |
| T-041 | ParkingSystemTest | `testAddMultipleParkingSlots()` | Multiple parking slots can be added successfully. |
| T-042 | ParkingSystemTest | `testGetAvailableParkingSlotsForCar()` | For a car, compatible available regular and large slots are returned; compact is excluded. |
| T-043 | ParkingSystemTest | `testGetAvailableParkingSlotsForBus()` | For a bus, only the compatible large slot is returned. |
| T-044 | ParkingSystemTest | `testGetAvailableParkingSlotsForBicycle()` | For a bicycle, all four tested slot types are available. |
| T-045 | ParkingSystemTest | `testGetAvailableParkingSlotsExcludesInactiveSlot()` | Inactive slots are excluded from available slots. |
| T-046 | ParkingSystemTest | `testGetAvailableParkingSlotsWhenNoSlotsExist()` | An empty list is returned when no slots exist. |
| T-047 | ParkingSystemTest | `testBookingWithEndTimeBeforeStartTime()` | Booking throws `IllegalBookingTimeException`. |
| T-048 | ParkingSystemTest | `testBookingWithEqualStartAndEndTime()` | Booking throws `IllegalBookingTimeException`. |
| T-049 | ParkingSystemTest | `testBookingIncompatibleSlot()` | Booking an incompatible slot throws `IllegalArgumentException`. |
| T-050 | ParkingSystemTest | `testBookingInactiveSlot()` | Booking an inactive slot throws `IllegalArgumentException`. |
| T-051 | ParkingSystemTest | `testSuccessfulBooking()` | A valid booking is created and added to system and slot booking lists. |
| T-052 | ParkingSystemTest | `testBookingHasCorrectVehicle()` | Created booking contains the supplied vehicle. |
| T-053 | ParkingSystemTest | `testBookingHasCorrectParkingSlot()` | Created booking contains the supplied parking slot. |
| T-054 | ParkingSystemTest | `testCarRegularTwoHourBookingAmount()` | Two-hour car booking on a regular slot costs `20.0`. |
| T-055 | ParkingSystemTest | `testMotorcycleRegularBookingAmount()` | Two-hour motorcycle booking on a regular slot costs `10.0`. |
| T-056 | ParkingSystemTest | `testBicycleCompactBookingAmount()` | Two-hour bicycle booking on a compact slot costs `3.2`. |
| T-057 | ParkingSystemTest | `testBusLargeBookingAmount()` | Two-hour bus booking on a large slot costs `60.0`. |
| T-058 | ParkingSystemTest | `testSetVehicles()` | Vehicle list setter replaces the system vehicle list. |
| T-059 | ParkingSystemTest | `testSetParkingSlots()` | Parking-slot list setter replaces the system slot list. |
| T-060 | ParkingSystemTest | `testSetBookings()` | Booking list setter replaces the system booking list. |
| T-061 | ParkingSystemTest | `testSetParkingRate()` | Parking rate can be changed to the supplied value. |
| T-062 | ParkingSystemTest | `testSystemWalletExists()` | System wallet exists. |
| T-063 | ParkingSystemTest | `testSetSystemWallet()` | System wallet can be replaced with the supplied wallet. |
| T-064 | ParkingSystemTest | `testResetForTesting()` | Reset clears vehicles, slots, and bookings and restores rate and balance defaults. |
| T-065 | VehicleTest | `constructor_withWallet_setsAllFieldsCorrectly()` | Vehicle ID, type, wallet, and balance are initialized correctly. |
| T-066 | VehicleTest | `constructor_withInitialBalance_createsWallet()` | Vehicle creates a wallet with the supplied initial balance. |
| T-067 | VehicleTest | `getVehicleId_returnsCorrectId()` | Vehicle ID getter returns the correct ID. |
| T-068 | VehicleTest | `getVehicleType_returnsCorrectType()` | Vehicle type getter returns the correct type. |
| T-069 | VehicleTest | `getWallet_returnsCorrectWallet()` | Wallet getter returns the same wallet instance. |
| T-070 | VehicleTest | `getBalance_returnsWalletBalance()` | Vehicle balance matches its wallet balance. |
| T-071 | VehicleTest | `toString_containsVehicleInformation()` | `toString()` contains vehicle ID, type, and balance. |
| T-072 | WalletTest | `testDefaultConstructor()` | Default wallet balance is `0.0`. |
| T-073 | WalletTest | `testInitialBalance()` | Wallet is initialized with the supplied balance. |
| T-074 | WalletTest | `testAddFunds()` | Adding valid funds increases the wallet balance. |
| T-075 | WalletTest | `testAddZeroFunds()` | Adding zero funds throws `InvalidAmountException` and balance remains unchanged. |
| T-076 | WalletTest | `testAddNegativeFunds()` | Adding negative funds throws `InvalidAmountException` and balance remains unchanged. |
| T-077 | WalletTest | `testDeductFunds()` | Deducting valid funds decreases the wallet balance. |
| T-078 | WalletTest | `testDeductExactBalance()` | Deducting the exact balance results in zero balance. |
| T-079 | WalletTest | `testDeductInsufficientFunds()` | Deducting more than the balance throws `InsufficientFundsException` and balance remains unchanged. |
| T-080 | WalletTest | `testDeductZeroFunds()` | Deducting zero funds throws `InvalidAmountException`. |
| T-081 | WalletTest | `testDeductNegativeFunds()` | Deducting negative funds throws `InvalidAmountException`. |
| T-082 | WalletTest | `testTransferFunds()` | Valid transfer decreases source balance and increases destination balance. |
| T-083 | WalletTest | `testTransferExactBalance()` | Transferring the exact source balance leaves source at zero and adds it to destination. |
| T-084 | WalletTest | `testTransferInsufficientFunds()` | Insufficient transfer throws `InsufficientFundsException` and both balances remain unchanged. |
| T-085 | WalletTest | `testTransferZeroFunds()` | Transferring zero funds throws `InvalidAmountException`. |
| T-086 | WalletTest | `testTransferNegativeFunds()` | Transferring negative funds throws `InvalidAmountException`. |





# B) Defects List

##Booking

Defect id:T-003
Description: Invalid state transitions are allowed (the tests lock in the bug).

Defect id:T-005
Description:COMPLETED -> CANCELLED, no error.

Defect id:T-002
Description:End time before start time is accepted.

Defect id:T-001
Description:Negative or invalid amount is accepted.

Defect id:T-001
Description:Null values are accepted.




##ParkingSlot

Defect id:T-012
Description:Cancelled booking still block the slot.

Defect id:T-018
Description:Invalid or null time ranges are not checked.

Defect id:T-010
Description:An inactive slot reports itself as available.

Defect id:T-009
Description:The constructor accepts invalid values.

Defect id:T-019
Description:Missing break in the MICROCAR case.


 
##ParkingSystem

Defect id:T-047
Description:partial hours are not charged.

Defect id:T-049
Description:Trucks can never park.

Defect id:T-051
Description:complete have no state guard.

Defect id:T-050
Description:cancel,have no state guard.

Defect id:T-061
Description:An invalid parking rate is accepted.



##Vehicle

Defect ID: T-069
Description:Null wallet is accepted.

Defect ID: T-068
Description:Null vehicle type is accepted.

Defect ID: T-071
Description:Zero or negative vehicle ID is accepted.

Defect ID: T-066
Description:Invalid initial balance is not checked

Defect ID: T-065
Description:No equals() and hashCode(), so duplicate vehicles are not detected




##Wallet

Defect ID: T-076
Description:This is a real bug depends on specification.If the requirements say initial balance must be non-negative ,then this is definitely a bug.

Defect ID: T-074
Description:Infinite amounts and overflow are accepted.

Defect ID: T-082
Description:transferFunds(null, amount) destroys money.

Defect ID: T-078
Description:Here the deduction actually works fine (since 0.30000000000000004 >= 0.3 is true), but getBalance() afterward won't be exactly 0.0 — it'll be a tiny residual like 4.44E-17.

Defect ID: T-079
Description: 0.1 + 0.2 in double arithmetic equals 0.30000000000000004, not 0.3.


# C) Mutant Analysis

## Summary

The `parking` package contains **5 classes**.

- **Line Coverage:** 95% (`161/170`)
- **Mutation Coverage:** 81% (`81/100`)
- **Test Strength:** 89% (`81/91`)

### Class-wise Coverage

- **Booking.java:** 100% line coverage, 100% mutation coverage, and 100% test strength.
- **ParkingSlot.java:** 100% line coverage, 84% mutation coverage, and 84% test strength.
- **ParkingSystem.java:** 88% line coverage, 66% mutation coverage, and 88% test strength.
- **Vehicle.java:** 100% line coverage, 100% mutation coverage, and 100% test strength.
- **Wallet.java:** 100% line coverage, 93% mutation coverage, and 93% test strength.

# D) Individual Contribution

I contributed to the testing phase by preparing and executing test cases, identifying functional and usability issues, verifying system outputs against expected results, and documenting the observed errors. I also assisted in debugging and retesting the corrected modules to ensure that the system performed reliably and met the specified requirements.
