# 0) Name and ID

- **Name:** Sharna Barua Srity
- **ID:** 0112310286

---

# A) Test Case List

# Test Case Table

| TC ID | Test Class | Test Case | Expected Result |
|---|---|---|---|
| TC-001 | BookingTest | `constructorSetsAllFields()` | All booking fields are initialized with the supplied values. |
| TC-002 | BookingTest | `newBookingStartsAsActive()` | A new booking has `ACTIVE` status. |
| TC-003 | BookingTest | `completeBookingSetsStatusToCompleted()` | Completing a booking changes status to `COMPLETED`. |
| TC-004 | BookingTest | `completeBookingDoesNotChangeOtherFields()` | Completing a booking does not change booking ID, vehicle, or amount. |
| TC-005 | BookingTest | `cancelBookingSetsStatusToCancelled()` | Cancelling a booking changes status to `CANCELLED`. |
| TC-006 | BookingTest | `cancelAfterCompleteOverridesStatus()` | Cancelling a completed booking changes status to `CANCELLED`. |
| TC-007 | BookingTest | `completeAfterCancelOverridesStatus()` | Completing a cancelled booking changes status to `COMPLETED`. |
| TC-008 | BookingTest | `toStringContainsBookingId()` | `toString()` contains the booking ID. |
| TC-009 | ParkingSlotTest | `testConstructor()` | Slot fields are initialized correctly; slot is active, balance is zero, wallet exists, and bookings are empty. |
| TC-010 | ParkingSlotTest | `testDeactivateSlot()` | Deactivating a slot makes it inactive. |
| TC-011 | ParkingSlotTest | `testActivateSlot()` | An inactive slot can be activated. |
| TC-012 | ParkingSlotTest | `testSlotIsAvailableWhenNoBookings()` | A slot with no bookings is available. |
| TC-013 | ParkingSlotTest | `testSlotIsAvailableForNonOverlappingBooking()` | A new booking that starts when an existing booking ends is allowed. |
| TC-014 | ParkingSlotTest | `testSlotIsUnavailableForOverlappingBooking()` | An overlapping booking is rejected as unavailable. |
| TC-015 | ParkingSlotTest | `testSlotIsUnavailableWhenNewBookingStartsDuringExistingBooking()` | A booking starting during an existing booking is unavailable. |
| TC-016 | ParkingSlotTest | `testSlotIsUnavailableWhenNewBookingEndsDuringExistingBooking()` | A booking ending during an existing booking is unavailable. |
| TC-017 | ParkingSlotTest | `testInactiveSlotIsNotCompatible()` | An inactive slot is not compatible with a vehicle. |
| TC-018 | ParkingSlotTest | `testMotorcycleCompatibleWithCompactSlot()` | Motorcycle is compatible with a compact slot. |
| TC-019 | ParkingSlotTest | `testMotorcycleCompatibleWithRegularSlot()` | Motorcycle is compatible with a regular slot. |
| TC-020 | ParkingSlotTest | `testMotorcycleNotCompatibleWithHandicappedSlot()` | Motorcycle is not compatible with a handicapped slot. |
| TC-021 | ParkingSlotTest | `testCarCompatibleWithRegularSlot()` | Car is compatible with a regular slot. |
| TC-022 | ParkingSlotTest | `testCarCompatibleWithLargeSlot()` | Car is compatible with a large slot. |
| TC-023 | ParkingSlotTest | `testCarNotCompatibleWithCompactSlot()` | Car is not compatible with a compact slot. |
| TC-024 | ParkingSlotTest | `testBusCompatibleWithLargeSlot()` | Bus is compatible with a large slot. |
| TC-025 | ParkingSlotTest | `testBusNotCompatibleWithRegularSlot()` | Bus is not compatible with a regular slot. |
| TC-026 | ParkingSlotTest | `testBicycleCompatibleWithHandicappedSlot()` | Bicycle is compatible with a handicapped slot. |
| TC-027 | ParkingSlotTest | `testMicrocarCompatibleWithCompactSlot()` | Microcar is compatible with a compact slot. |
| TC-028 | ParkingSlotTest | `testMicrocarNotCompatibleWithLargeSlot()` | Microcar is not compatible with a large slot. |
| TC-029 | ParkingSlotTest | `testInitialBalanceIsZero()` | A new parking slot has zero balance. |
| TC-030 | ParkingSlotTest | `testGetWallet()` | Slot wallet exists and has zero initial balance. |
| TC-031 | ParkingSlotTest | `testGetBookings()` | Slot bookings collection exists and is initially empty. |
| TC-032 | ParkingSystemTest | `testSingletonReturnsSameInstance()` | `getInstance()` returns the same `ParkingSystem` instance. |
| TC-033 | ParkingSystemTest | `testInitialVehiclesListIsEmpty()` | Vehicle list is initially empty. |
| TC-034 | ParkingSystemTest | `testInitialParkingSlotsListIsEmpty()` | Parking-slot list is initially empty. |
| TC-035 | ParkingSystemTest | `testInitialBookingsListIsEmpty()` | Booking list is initially empty. |
| TC-036 | ParkingSystemTest | `testInitialParkingRate()` | Initial parking rate is `10.0` per hour. |
| TC-037 | ParkingSystemTest | `testInitialSystemBalance()` | Initial system balance is `0.0`. |
| TC-038 | ParkingSystemTest | `testAddVehicle()` | A vehicle can be added and appears in the vehicle list. |
| TC-039 | ParkingSystemTest | `testAddMultipleVehicles()` | Multiple vehicles can be added successfully. |
| TC-040 | ParkingSystemTest | `testAddParkingSlot()` | A parking slot can be added and appears in the slot list. |
| TC-041 | ParkingSystemTest | `testAddMultipleParkingSlots()` | Multiple parking slots can be added successfully. |
| TC-042 | ParkingSystemTest | `testGetAvailableParkingSlotsForCar()` | For a car, compatible available regular and large slots are returned; compact is excluded. |
| TC-043 | ParkingSystemTest | `testGetAvailableParkingSlotsForBus()` | For a bus, only the compatible large slot is returned. |
| TC-044 | ParkingSystemTest | `testGetAvailableParkingSlotsForBicycle()` | For a bicycle, all four tested slot types are available. |
| TC-045 | ParkingSystemTest | `testGetAvailableParkingSlotsExcludesInactiveSlot()` | Inactive slots are excluded from available slots. |
| TC-046 | ParkingSystemTest | `testGetAvailableParkingSlotsWhenNoSlotsExist()` | An empty list is returned when no slots exist. |
| TC-047 | ParkingSystemTest | `testBookingWithEndTimeBeforeStartTime()` | Booking throws `IllegalBookingTimeException`. |
| TC-048 | ParkingSystemTest | `testBookingWithEqualStartAndEndTime()` | Booking throws `IllegalBookingTimeException`. |
| TC-049 | ParkingSystemTest | `testBookingIncompatibleSlot()` | Booking an incompatible slot throws `IllegalArgumentException`. |
| TC-050 | ParkingSystemTest | `testBookingInactiveSlot()` | Booking an inactive slot throws `IllegalArgumentException`. |
| TC-051 | ParkingSystemTest | `testSuccessfulBooking()` | A valid booking is created and added to system and slot booking lists. |
| TC-052 | ParkingSystemTest | `testBookingHasCorrectVehicle()` | Created booking contains the supplied vehicle. |
| TC-053 | ParkingSystemTest | `testBookingHasCorrectParkingSlot()` | Created booking contains the supplied parking slot. |
| TC-054 | ParkingSystemTest | `testCarRegularTwoHourBookingAmount()` | Two-hour car booking on a regular slot costs `20.0`. |
| TC-055 | ParkingSystemTest | `testMotorcycleRegularBookingAmount()` | Two-hour motorcycle booking on a regular slot costs `10.0`. |
| TC-056 | ParkingSystemTest | `testBicycleCompactBookingAmount()` | Two-hour bicycle booking on a compact slot costs `3.2`. |
| TC-057 | ParkingSystemTest | `testBusLargeBookingAmount()` | Two-hour bus booking on a large slot costs `60.0`. |
| TC-058 | ParkingSystemTest | `testSetVehicles()` | Vehicle list setter replaces the system vehicle list. |
| TC-059 | ParkingSystemTest | `testSetParkingSlots()` | Parking-slot list setter replaces the system slot list. |
| TC-060 | ParkingSystemTest | `testSetBookings()` | Booking list setter replaces the system booking list. |
| TC-061 | ParkingSystemTest | `testSetParkingRate()` | Parking rate can be changed to the supplied value. |
| TC-062 | ParkingSystemTest | `testSystemWalletExists()` | System wallet exists. |
| TC-063 | ParkingSystemTest | `testSetSystemWallet()` | System wallet can be replaced with the supplied wallet. |
| TC-064 | ParkingSystemTest | `testResetForTesting()` | Reset clears vehicles, slots, and bookings and restores rate and balance defaults. |
| TC-065 | VehicleTest | `constructor_withWallet_setsAllFieldsCorrectly()` | Vehicle ID, type, wallet, and balance are initialized correctly. |
| TC-066 | VehicleTest | `constructor_withInitialBalance_createsWallet()` | Vehicle creates a wallet with the supplied initial balance. |
| TC-067 | VehicleTest | `getVehicleId_returnsCorrectId()` | Vehicle ID getter returns the correct ID. |
| TC-068 | VehicleTest | `getVehicleType_returnsCorrectType()` | Vehicle type getter returns the correct type. |
| TC-069 | VehicleTest | `getWallet_returnsCorrectWallet()` | Wallet getter returns the same wallet instance. |
| TC-070 | VehicleTest | `getBalance_returnsWalletBalance()` | Vehicle balance matches its wallet balance. |
| TC-071 | VehicleTest | `toString_containsVehicleInformation()` | `toString()` contains vehicle ID, type, and balance. |
| TC-072 | WalletTest | `testDefaultConstructor()` | Default wallet balance is `0.0`. |
| TC-073 | WalletTest | `testInitialBalance()` | Wallet is initialized with the supplied balance. |
| TC-074 | WalletTest | `testAddFunds()` | Adding valid funds increases the wallet balance. |
| TC-075 | WalletTest | `testAddZeroFunds()` | Adding zero funds throws `InvalidAmountException` and balance remains unchanged. |
| TC-076 | WalletTest | `testAddNegativeFunds()` | Adding negative funds throws `InvalidAmountException` and balance remains unchanged. |
| TC-077 | WalletTest | `testDeductFunds()` | Deducting valid funds decreases the wallet balance. |
| TC-078 | WalletTest | `testDeductExactBalance()` | Deducting the exact balance results in zero balance. |
| TC-079 | WalletTest | `testDeductInsufficientFunds()` | Deducting more than the balance throws `InsufficientFundsException` and balance remains unchanged. |
| TC-080 | WalletTest | `testDeductZeroFunds()` | Deducting zero funds throws `InvalidAmountException`. |
| TC-081 | WalletTest | `testDeductNegativeFunds()` | Deducting negative funds throws `InvalidAmountException`. |
| TC-082 | WalletTest | `testTransferFunds()` | Valid transfer decreases source balance and increases destination balance. |
| TC-083 | WalletTest | `testTransferExactBalance()` | Transferring the exact source balance leaves source at zero and adds it to destination. |
| TC-084 | WalletTest | `testTransferInsufficientFunds()` | Insufficient transfer throws `InsufficientFundsException` and both balances remain unchanged. |
| TC-085 | WalletTest | `testTransferZeroFunds()` | Transferring zero funds throws `InvalidAmountException`. |
| TC-086 | WalletTest | `testTransferNegativeFunds()` | Transferring negative funds throws `InvalidAmountException`. |







# B) Defects List

Defect id:TC-003
Description: Invalid state transitions are allowed (the tests lock in the bug)

Defect id:TC-005
Description:COMPLETED -> CANCELLED, no error

Defect id:TC-002
Description:End time before start time is accepted

Defect id:TC-001
Description:Negative or invalid amount is accepted

Defect id:TC-001
Description:Null values are accepted
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
