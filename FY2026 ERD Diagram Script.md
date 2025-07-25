
Table "Affiliation" {
  "AffiliationID" "character varying(32)" [pk, not null]
  "ProjectID" "character varying(32)" [not null]
  "ResProjectID" "character varying(32)" [not null]
  "DateCreated" timestamp [not null]
  "DateUpdated" timestamp [not null]
  "UserID" "character varying(32)" [not null]
  "DateDeleted" timestamp
  "ExportID" "character varying(32)" [not null]
}

Table "Assessment" {
  "AssessmentID" "character varying(32)" [pk, not null]
  "EnrollmentID" "character varying(32)" [not null]
  "PersonalID" "character varying(32)" [not null]
  "AssessmentDate" date [not null]
  "AssessmentLocation" "character varying(250)" [not null]
  "AssessmentType" integer [not null]
  "AssessmentLevel" integer [not null]
  "PrioritizationStatus" integer [not null]
  "DateCreated" timestamp [not null]
  "DateUpdated" timestamp [not null]
  "UserID" "character varying(32)" [not null]
  "DateDeleted" timestamp
  "ExportID" "character varying(32)" [not null]
}

Table "AssessmentQuestion" {
  "AssessmentQuestionID" "character varying(32)" [pk, not null]
  "AssessmentID" "character varying(32)" [not null]
  "EnrollmentID" "character varying(32)" [not null]
  "PersonalID" "character varying(32)" [not null]
  "AssessmentQuestionGroup" "character varying(250)"
  "AssessmentQuestionOrder" integer
  "AssessmentQuestion" "character varying(250)" [not null]
  "AssessmentAnswer" "character varying(500)"
  "DateCreated" timestamp [not null]
  "DateUpdated" timestamp [not null]
  "UserID" "character varying(32)" [not null]
  "DateDeleted" timestamp
  "ExportID" "character varying(32)" [not null]
}

Table "AssessmentResults" {
  "AssessmentResultID" "character varying(32)" [pk, not null]
  "AssessmentID" "character varying(32)" [not null]
  "EnrollmentID" "character varying(32)" [not null]
  "PersonalID" "character varying(32)" [not null]
  "AssessmentResultType" "character varying(250)" [not null]
  "AssessmentResult" "character varying(250)"
  "DateCreated" timestamp [not null]
  "DateUpdated" timestamp [not null]
  "UserID" "character varying(32)" [not null]
  "DateDeleted" timestamp
  "ExportID" "character varying(32)" [not null]
}

Table "CEParticipation" {
  "CEParticipationID" "character varying(32)" [pk, not null]
  "ProjectID" "character varying(32)" [not null]
  "AccessPoint" integer [not null]
  "PreventionAssessment" integer
  "CrisisAssessment" integer
  "HousingAssessment" integer
  "DirectServices" integer
  "ReceivesReferrals" integer [not null]
  "CEParticipationStatusStartDate" date [not null]
  "CEParticipationStatusEndDate" date
  "DateCreated" timestamp [not null]
  "DateUpdated" timestamp [not null]
  "UserID" "character varying(32)" [not null]
  "DateDeleted" timestamp
  "ExportID" "character varying(32)" [not null]
}

Table "Client" {
  "PersonalID" "character varying(32)" [pk, not null]
  "FirstName" "character varying(50)"
  "MiddleName" "character varying(50)"
  "LastName" "character varying(50)"
  "NameSuffix" "character varying(50)"
  "NameDataQuality" integer [not null]
  "SSN" "character varying(9)"
  "SSNDataQuality" integer [not null]
  "Sex" integer
  "DOB" date
  "DOBDataQuality" integer [not null]
  "AmIndAKNative" integer [not null]
  "Asian" integer [not null]
  "BlackAfAmerican" integer [not null]
  "HispanicLatinao" integer [not null]
  "MidEastNAfrican" integer [not null]
  "NativeHIPacific" integer [not null]
  "White" integer [not null]
  "RaceNone" integer
  "AdditionalRaceEthnicity" "character varying(100)"
  "DifferentIdentityText" "character varying(100)"
  "VeteranStatus" integer [not null]
  "DateCreated" timestamp [not null]
  "DateUpdated" timestamp [not null]
  "UserID" "character varying(32)" [not null]
  "DateDeleted" timestamp
  "ExportID" "character varying(32)" [not null]
}

Table "ClientVeteranInfo" {
  "PersonalID" "character varying(32)" [pk, not null]
  "YearEnteredService" integer
  "YearSeparated" integer
  "WorldWarII" integer
  "KoreanWar" integer
  "VietnamWar" integer
  "DesertStorm" integer
  "AfghanistanOEF" integer
  "IraqOIF" integer
  "IraqOND" integer
  "OtherTheater" integer
  "MilitaryBranch" integer
  "DischargeStatus" integer
  "DateCreated" timestamp [not null]
  "DateUpdated" timestamp [not null]
  "UserID" "character varying(32)" [not null]
  "DateDeleted" timestamp
  "ExportID" "character varying(32)" [not null]
}

Table "ConnectedWithSOAR" {
  "IncomeBenefitsID" "character varying(32)" [pk, not null]
  "EnrollmentID" "character varying(32)" [not null]
  "PersonalID" "character varying(32)" [not null]
  "InformationDate" date [not null]
  "ConnectionWithSOAR" integer
  "DateCreated" timestamp [not null]
  "DateUpdated" timestamp [not null]
  "UserID" "character varying(32)" [not null]
  "DateDeleted" timestamp
  "ExportID" "character varying(32)" [not null]
}

Table "CurrentLivingSituation" {
  "CurrentLivingSitID" "character varying(32)" [pk, not null]
  "EnrollmentID" "character varying(32)" [not null]
  "PersonalID" "character varying(32)" [not null]
  "InformationDate" date [not null]
  "CurrentLivingSituation" integer [not null]
  "CLSSubsidyType" integer
  "VerifiedBy" "character varying(100)"
  "LeaveSituation14Days" integer
  "SubsequentResidence" integer
  "ResourcesToObtain" integer
  "LeaseOwn60Day" integer
  "MovedTwoOrMore" integer
  "LocationDetails" "character varying(250)"
  "DateCreated" timestamp [not null]
  "DateUpdated" timestamp [not null]
  "UserID" "character varying(32)" [not null]
  "DateDeleted" timestamp
  "ExportID" "character varying(32)" [not null]
}

Table "DateOfEngagement" {
  "EnrollmentID" "character varying(32)" [pk, not null]
  "DateOfEngagement" date
  "DateCreated" timestamp [not null]
  "DateUpdated" timestamp [not null]
  "UserID" "character varying(32)" [not null]
  "DateDeleted" timestamp
  "ExportID" "character varying(32)" [not null]
}

Table "Disabilities" {
  "DisabilitiesID" "character varying(32)" [pk, not null]
  "EnrollmentID" "character varying(32)" [not null]
  "PersonalID" "character varying(32)" [not null]
  "InformationDate" date [not null]
  "DisabilityType" integer [not null]
  "DisabilityResponse" integer [not null]
  "IndefiniteAndImpairs" integer
  "TCellCountAvailable" integer
  "TCellCount" integer
  "TCellSource" integer
  "ViralLoadAvailable" integer
  "ViralLoad" integer
  "ViralLoadSource" integer
  "AntiRetroviral" integer
  "DataCollectionStage" integer [not null]
  "DateCreated" timestamp [not null]
  "DateUpdated" timestamp [not null]
  "UserID" "character varying(32)" [not null]
  "DateDeleted" timestamp
  "ExportID" "character varying(32)" [not null]
}

Table "DomesticViolence" {
  "HealthAndDVID" "character varying(32)" [pk, not null]
  "EnrollmentID" "character varying(32)" [not null]
  "PersonalID" "character varying(32)" [not null]
  "InformationDate" date [not null]
  "DomesticViolenceSurvivor" integer
  "WhenOccurred" integer
  "CurrentlyFleeing" integer
  "DataCollectionStage" integer [not null]
  "DateCreated" timestamp [not null]
  "DateUpdated" timestamp [not null]
  "UserID" "character varying(32)" [not null]
  "DateDeleted" timestamp
  "ExportID" "character varying(32)" [not null]
}

Table "Education" {
  "EmploymentEducationID" "character varying(32)" [pk, not null]
  "EnrollmentID" "character varying(32)" [not null]
  "PersonalID" "character varying(32)" [not null]
  "InformationDate" date [not null]
  "LastGradeCompleted" integer
  "SchoolStatus" integer
  "DataCollectionStage" integer [not null]
  "DateCreated" timestamp [not null]
  "DateUpdated" timestamp [not null]
  "UserID" "character varying(32)" [not null]
  "DateDeleted" timestamp
  "ExportID" "character varying(32)" [not null]
}

Table "Employment" {
  "EmploymentEducationID" "character varying(32)" [pk, not null]
  "EnrollmentID" "character varying(32)" [not null]
  "PersonalID" "character varying(32)" [not null]
  "InformationDate" date [not null]
  "Employed" integer
  "EmploymentType" integer
  "NotEmployedReason" integer
  "DataCollectionStage" integer [not null]
  "DateCreated" timestamp [not null]
  "DateUpdated" timestamp [not null]
  "UserID" "character varying(32)" [not null]
  "DateDeleted" timestamp
  "ExportID" "character varying(32)" [not null]
}

Table "Enrollment" {
  "EnrollmentID" "character varying(32)" [pk, not null]
  "PersonalID" "character varying(32)" [not null]
  "ProjectID" "character varying(32)" [not null]
  "EntryDate" date [not null]
  "HouseholdID" "character varying(32)" [not null]
  "RelationshipToHoH" integer [not null]
  "EnrollmentCoC" "character varying(6)" [not null]
  "LivingSituation" integer
  "RentalSubsidyType" integer
  "LengthOfStay" integer
  "LOSUnderThreshold" integer
  "PreviousStreetESSH" integer
  "DateToStreetESSH" date
  "TimesHomelessPastThreeYears" integer
  "MonthsHomelessPastThreeYears" integer
  "DisablingCondition" integer [not null]
  "TranslationNeeded" integer
  "PreferredLanguage" integer
  "PreferredLanguageDifferent" "character varying(100)"
  "DateCreated" timestamp [not null]
  "DateUpdated" timestamp [not null]
  "UserID" "character varying(32)" [not null]
  "DateDeleted" timestamp
  "ExportID" "character varying(32)" [not null]
}

Table "EntryRHY" {
  "EnrollmentID" "character varying(32)" [pk, not null]
  "PersonalID" "character varying(32)" [not null]
  "ProjectID" "character varying(32)" [not null]
  "HouseholdID" "character varying(32)" [not null]
  "ReferralSource" integer
  "CountOutreachReferralApproaches" integer
  "FormerWardChildWelfare" integer
  "ChildWelfareYears" integer
  "ChildWelfareMonths" integer
  "FormerWardJuvenileJustice" integer
  "JuvenileJusticeYears" integer
  "JuvenileJusticeMonths" integer
  "UnemploymentFam" integer
  "MentalHealthDisorderFam" integer
  "PhysicalDisabilityFam" integer
  "AlcoholDrugUseDisorderFam" integer
  "InsufficientIncome" integer
  "IncarceratedParent" integer
  "DateCreated" timestamp [not null]
  "DateUpdated" timestamp [not null]
  "UserID" "character varying(32)" [not null]
  "DateDeleted" timestamp
  "ExportID" "character varying(32)" [not null]
}

Table "EntrySSVF" {
  "EnrollmentID" "character varying(32)" [pk, not null]
  "PersonalID" "character varying(32)" [not null]
  "ProjectID" "character varying(32)" [not null]
  "HouseholdID" "character varying(32)" [not null]
  "PercentAMI" integer
  "VAMCStation" "character varying(5)"
  "TargetScreenReqd" integer
  "TimeToHousingLoss" integer
  "AnnualPercentAMI" integer
  "LiteralHomelessHistory" integer
  "ClientLeaseholder" integer
  "HOHLeaseholder" integer
  "SubsidyAtRisk" integer
  "EvictionHistory" integer
  "CriminalRecord" integer
  "IncarceratedAdult" integer
  "PrisonDischarge" integer
  "SexOffender" integer
  "DisabledHoH" integer
  "CurrentPregnant" integer
  "SingleParent" integer
  "DependentUnder6" integer
  "HH5Plus" integer
  "CoCPrioritized" integer
  "HPScreeningScore" integer
  "ThresholdScore" integer
  "MentalHealthConsultation" integer
  "DateCreated" timestamp [not null]
  "DateUpdated" timestamp [not null]
  "UserID" "character varying(32)" [not null]
  "DateDeleted" timestamp
  "ExportID" "character varying(32)" [not null]
}

Table "Event" {
  "EventID" "character varying(32)" [pk, not null]
  "EnrollmentID" "character varying(32)" [not null]
  "PersonalID" "character varying(32)" [not null]
  "EventDate" date [not null]
  "EventType" integer [not null]
  "ProbSolDivRRResult" integer
  "ReferralCaseManageAfter" integer
  "LocationCrisisOrPHHousing" "character varying(250)"
  "ReferralResult" integer
  "ResultDate" date
  "DateCreated" timestamp [not null]
  "DateUpdated" timestamp [not null]
  "UserID" "character varying(32)" [not null]
  "DateDeleted" timestamp
  "ExportID" "character varying(32)" [not null]
}

Table "ExitHousingAssessment" {
  "ExitID" "character varying(32)" [pk, not null]
  "EnrollmentID" "character varying(32)" [not null]
  "PersonalID" "character varying(32)" [not null]
  "HousingAssessment" integer
  "SubsidyInformation" integer
  "DateCreated" timestamp [not null]
  "DateUpdated" timestamp [not null]
  "UserID" "character varying(32)" [not null]
  "DateDeleted" timestamp
  "ExportID" "character varying(32)" [not null]
}

Table "ExitRHY" {
  "ExitID" "character varying(32)" [pk, not null]
  "EnrollmentID" "character varying(32)" [not null]
  "PersonalID" "character varying(32)" [not null]
  "ProjectCompletionStatus" integer
  "EarlyExitReason" integer
  "ExchangeForSex" integer
  "ExchangeForSexPastThreeMonths" integer
  "CountOfExchangeForSex" integer
  "AskedOrForcedToExchangeForSex" integer
  "AskedOrForcedToExchangeForSexPastThreeMonths" integer
  "WorkplaceViolenceThreats" integer
  "WorkplacePromiseDifference" integer
  "CoercedToContinueWork" integer
  "LaborExploitPastThreeMonths" integer
  "CounselingReceived" integer
  "IndividualCounseling" integer
  "FamilyCounseling" integer
  "GroupCounseling" integer
  "SessionCountAtExit" integer
  "PostExitCounselingPlan" integer
  "SessionsInPlan" integer
  "DestinationSafeClient" integer
  "DestinationSafeWorker" integer
  "PosAdultConnections" integer
  "PosPeerConnections" integer
  "PosCommunityConnections" integer
  "DateCreated" timestamp [not null]
  "DateUpdated" timestamp [not null]
  "UserID" "character varying(32)" [not null]
  "DateDeleted" timestamp
  "ExportID" "character varying(32)" [not null]
}

Table "Exits" {
  "ExitID" "character varying(32)" [pk, not null]
  "EnrollmentID" "character varying(32)" [not null]
  "PersonalID" "character varying(32)" [not null]
  "ExitDate" date [not null]
  "Destination" integer [not null]
  "DestinationSubsidyType" integer
  "OtherDestination" "character varying(50)"
  "DateCreated" timestamp [not null]
  "DateUpdated" timestamp [not null]
  "UserID" "character varying(32)" [not null]
  "DateDeleted" timestamp
  "ExportID" "character varying(32)" [not null]
}

Table "Export" {
  "ExportID" "character varying(32)" [pk, not null]
  "SourceType" integer [not null]
  "SourceID" "character varying(32)"
  "SourceName" "character varying(50)"
  "SourceContactFirst" "character varying(50)"
  "SourceContactLast" "character varying(50)"
  "SourceContactPhone" "character varying(10)"
  "SourceContactExtension" "character varying(5)"
  "SourceContactEmail" "character varying(320)"
  "ExportDate" timestamp [not null]
  "ExportStartDate" date [not null]
  "ExportEndDate" date [not null]
  "SoftwareName" "character varying(50)" [not null]
  "SoftwareVersion" "character varying(50)"
  "CSVVersion" "character varying(50)"
  "ExportPeriodType" integer [not null]
  "ExportDirective" integer [not null]
  "HashStatus" integer [not null]
  "ImplementationID" "character varying(200)" [not null]
}

Table "Funder" {
  "FunderID" "character varying(32)" [pk, not null]
  "ProjectID" "character varying(32)" [not null]
  "Funder" integer [not null]
  "OtherFunder" "character varying(100)"
  "GrantID" "character varying(100)" [not null]
  "StartDate" date [not null]
  "EndDate" date
  "DateCreated" timestamp [not null]
  "DateUpdated" timestamp [not null]
  "UserID" "character varying(32)" [not null]
  "DateDeleted" timestamp
  "ExportID" "character varying(32)" [not null]
}

Table "HMISParticipation" {
  "HMISParticipationID" "character varying(32)" [pk, not null]
  "ProjectID" "character varying(32)" [not null]
  "HMISParticipationType" integer [not null]
  "HMISParticipationStatusStartDate" date [not null]
  "HMISParticipationStatusEndDate" date
  "DateCreated" timestamp [not null]
  "DateUpdated" timestamp [not null]
  "UserID" "character varying(32)" [not null]
  "DateDeleted" timestamp
  "ExportID" "character varying(32)" [not null]
}

Table "HealthInsurance" {
  "IncomeBenefitsID" "character varying(32)" [pk, not null]
  "EnrollmentID" "character varying(32)" [not null]
  "PersonalID" "character varying(32)" [not null]
  "InformationDate" date [not null]
  "InsuranceFromAnySource" integer
  "Medicaid" integer
  "NoMedicaidReason" integer
  "Medicare" integer
  "NoMedicareReason" integer
  "SCHIP" integer
  "NoSCHIPReason" integer
  "VHAServices" integer
  "NoVHAReason" integer
  "EmployerProvided" integer
  "NoEmployerProvidedReason" integer
  "COBRA" integer
  "NoCOBRAReason" integer
  "PrivatePay" integer
  "NoPrivatePayReason" integer
  "StateHealthIns" integer
  "NoStateHealthInsReason" integer
  "IndianHealthServices" integer
  "NoIndianHealthServicesReason" integer
  "OtherInsurance" integer
  "OtherInsuranceIdentify" "character varying(50)"
  "DataCollectionStage" integer [not null]
  "DateCreated" timestamp [not null]
  "DateUpdated" timestamp [not null]
  "UserID" "character varying(32)" [not null]
  "DateDeleted" timestamp
  "ExportID" "character varying(32)" [not null]
}

Table "HealthStatus" {
  "HealthAndDVID" "character varying(32)" [pk, not null]
  "EnrollmentID" "character varying(32)" [not null]
  "PersonalID" "character varying(32)" [not null]
  "InformationDate" date [not null]
  "GeneralHealthStatus" integer
  "DentalHealthStatus" integer
  "MentalHealthStatus" integer
  "PregnancyStatus" integer
  "DueDate" date
  "DataCollectionStage" integer [not null]
  "DateCreated" timestamp [not null]
  "DateUpdated" timestamp [not null]
  "UserID" "character varying(32)" [not null]
  "DateDeleted" timestamp
  "ExportID" "character varying(32)" [not null]
}

Table "Household" {
  "HouseholdID" "character varying(32)" [pk, not null]
  "ProjectID" "character varying(32)" [not null]
  "DateCreated" timestamp [not null]
  "DateUpdated" timestamp [not null]
  "UserID" "character varying(32)" [not null]
  "DateDeleted" timestamp
  "ExportID" "character varying(32)" [not null]
}

Table "IncomeAndSources" {
  "IncomeBenefitsID" "character varying(32)" [pk, not null]
  "EnrollmentID" "character varying(32)" [not null]
  "PersonalID" "character varying(32)" [not null]
  "InformationDate" date [not null]
  "IncomeFromAnySource" integer
  "TotalMonthlyIncome" numeric(65,2)
  "Earned" integer
  "EarnedAmount" numeric(65,2)
  "Unemployment" integer
  "UnemploymentAmount" numeric(65,2)
  "SSI" integer
  "SSIAmount" numeric(65,2)
  "SSDI" integer
  "SSDIAmount" numeric(65,2)
  "VADisabilityService" integer
  "VADisabilityServiceAmount" numeric(65,2)
  "VADisabilityNonService" integer
  "VADisabilityNonServiceAmount" numeric(65,2)
  "PrivateDisability" integer
  "PrivateDisabilityAmount" numeric(65,2)
  "WorkersComp" integer
  "WorkersCompAmount" numeric(65,2)
  "TANF" integer
  "TANFAmount" numeric(65,2)
  "GA" integer
  "GAAmount" numeric(65,2)
  "SocSecRetirement" integer
  "SocSecRetirementAmount" numeric(65,2)
  "Pension" integer
  "PensionAmount" numeric(65,2)
  "ChildSupport" integer
  "ChildSupportAmount" numeric(65,2)
  "Alimony" integer
  "AlimonyAmount" numeric(65,2)
  "OtherIncomeSource" integer
  "OtherIncomeAmount" numeric(65,2)
  "OtherIncomeSourceIdentify" "character varying(50)"
  "DataCollectionStage" integer [not null]
  "DateCreated" timestamp [not null]
  "DateUpdated" timestamp [not null]
  "UserID" "character varying(32)" [not null]
  "DateDeleted" timestamp
  "ExportID" "character varying(32)" [not null]
}

Table "Inventory" {
  "InventoryID" "character varying(32)" [pk, not null]
  "ProjectID" "character varying(32)" [not null]
  "CoCCode" "character varying(6)"
  "HouseholdType" integer [not null]
  "Availability" integer
  "UnitInventory" integer [not null]
  "BedInventory" integer [not null]
  "CHVetBedInventory" integer
  "YouthVetBedInventory" integer
  "VetBedInventory" integer
  "CHYouthBedInventory" integer
  "YouthBedInventory" integer
  "CHBedInventory" integer
  "OtherBedInventory" integer
  "ESBedType" integer
  "InventoryStartDate" date [not null]
  "InventoryEndDate" date
  "DateCreated" timestamp [not null]
  "DateUpdated" timestamp [not null]
  "UserID" "character varying(32)" [not null]
  "DateDeleted" timestamp
  "ExportID" "character varying(32)" [not null]
}

Table "MedicalAssistance" {
  "IncomeBenefitsID" "character varying(32)" [pk, not null]
  "EnrollmentID" "character varying(32)" [not null]
  "PersonalID" "character varying(32)" [not null]
  "InformationDate" date [not null]
  "ADAP" integer
  "NoADAPReason" integer
  "RyanWhiteMedDent" integer
  "NoRyanWhiteReason" integer
  "DateCreated" timestamp [not null]
  "DateUpdated" timestamp [not null]
  "UserID" "character varying(32)" [not null]
  "DateDeleted" timestamp
  "ExportID" "character varying(32)" [not null]
}

Table "MoveInDate" {
  "EnrollmentID" "character varying(32)" [pk, not null]
  "PersonalID" "character varying(32)" [not null]
  "ProjectID" "character varying(32)" [not null]
  "HouseholdID" "character varying(32)" [not null]
  "MoveInDate" date
  "oncommonname" "character varying(200)"
  "DateCreated" timestamp [not null]
  "DateUpdated" timestamp [not null]
  "UserID" "character varying(32)" [not null]
  "DateDeleted" timestamp
  "ExportID" "character varying(32)" [not null]
}

Table "NonCashBenefits" {
  "IncomeBenefitsID" "character varying(32)" [pk, not null]
  "EnrollmentID" "character varying(32)" [not null]
  "PersonalID" "character varying(32)" [not null]
  "InformationDate" date [not null]
  "BenefitsFromAnySource" integer
  "SNAP" integer
  "WIC" integer
  "TANFChildCare" integer
  "TANFTransportation" integer
  "OtherTANF" integer
  "OtherBenefitsSource" integer
  "OtherBenefitsSourceIdentify" "character varying(50)"
  "DataCollectionStage" integer [not null]
  "DateCreated" timestamp [not null]
  "DateUpdated" timestamp [not null]
  "UserID" "character varying(32)" [not null]
  "DateDeleted" timestamp
  "ExportID" "character varying(32)" [not null]
}

Table "Organization" {
  "OrganizationID" "character varying(32)" [pk, not null]
  "OrganizationName" "character varying(200)" [not null]
  "VictimServiceProvider" integer [not null]
  "OrganizationCommonName" "character varying(200)"
  "DateCreated" timestamp [not null]
  "DateUpdated" timestamp [not null]
  "UserID" "character varying(32)" [not null]
  "DateDeleted" timestamp
  "ExportID" "character varying(32)" [not null]
}

Table "PATHStatus" {
  "EnrollmentID" "character varying(32)" [pk, not null]
  "PersonalID" "character varying(32)" [not null]
  "ProjectID" "character varying(32)" [not null]
  "HouseholdID" "character varying(32)" [not null]
  "DateOfPATHStatus" date
  "ClientEnrolledInPATH" integer
  "ReasonNotEnrolled" integer
  "DateCreated" timestamp [not null]
  "DateUpdated" timestamp [not null]
  "UserID" "character varying(32)" [not null]
  "DateDeleted" timestamp
  "ExportID" "character varying(32)" [not null]
}

Table "Project" {
  "ProjectID" "character varying(32)" [pk, not null]
  "OrganizationID" "character varying(32)" [not null]
  "ProjectName" "character varying(200)" [not null]
  "ProjectCommonName" "character varying(200)"
  "OperatingStartDate" date [not null]
  "OperatingEndDate" date
  "ContinuumProject" integer [not null]
  "ProjectType" integer
  "HousingType" integer
  "RRHSubType" integer
  "ResidentialAffiliation" integer
  "TargetPopulation" integer
  "HOPWAMedAssistedLivingFac" integer
  "PITCount" integer
  "DateCreated" timestamp [not null]
  "DateUpdated" timestamp [not null]
  "UserID" "character varying(32)" [not null]
  "DateDeleted" timestamp
  "ExportID" "character varying(32)" [not null]
}

Table "ProjectCoC" {
  "ProjectCoCID" "character varying(32)" [pk, not null]
  "ProjectID" "character varying(32)" [not null]
  "CoCCode" "character varying(6)" [not null]
  "Geocode" "character varying(6)" [not null]
  "Address1" "character varying(100)"
  "Address2" "character varying(100)"
  "City" "character varying(50)"
  "State" "character varying(2)"
  "ZIP" "character varying(5)"
  "GeographyType" integer
  "DateCreated" timestamp [not null]
  "DateUpdated" timestamp [not null]
  "UserID" "character varying(32)" [not null]
  "DateDeleted" timestamp
  "ExportID" "character varying(32)" [not null]
}

Table "RHYAftercare" {
  "ExitID" "character varying(32)" [pk, not null]
  "EnrollmentID" "character varying(32)" [not null]
  "PersonalID" "character varying(32)" [not null]
  "AftercareDate" date
  "AftercareProvided" integer
  "EmailSocialMedia" integer
  "Telephone" integer
  "InPersonIndividual" integer
  "InPersonGroup" integer
  "DateCreated" timestamp [not null]
  "DateUpdated" timestamp [not null]
  "UserID" "character varying(32)" [not null]
  "DateDeleted" timestamp
  "ExportID" "character varying(32)" [not null]
}

Table "RHYBCPStatus" {
  "EnrollmentID" "character varying(32)" [pk, not null]
  "PersonalID" "character varying(32)" [not null]
  "ProjectID" "character varying(32)" [not null]
  "HouseholdID" "character varying(32)" [not null]
  "DateOfBCPStatus" date
  "EligibleForRHY" integer
  "ReasonNoServices" integer
  "RunawayYouth" integer
  "DateCreated" timestamp [not null]
  "DateUpdated" timestamp [not null]
  "UserID" "character varying(32)" [not null]
  "DateDeleted" timestamp
  "ExportID" "character varying(32)" [not null]
}

Table "ServiceFAReferral" {
  "ServicesID" "character varying(32)" [pk, not null]
  "EnrollmentID" "character varying(32)" [not null]
  "PersonalID" "character varying(32)" [not null]
  "DateProvided" date [not null]
  "RecordType" integer [not null]
  "TypeProvided" integer [not null]
  "OtherTypeProvided" "character varying(50)"
  "MovingOnOtherType" "character varying(50)"
  "SubTypeProvided" integer
  "FAAmount" numeric(65,2)
  "FAStartDate" date
  "FAEndDate" date
  "ReferralOutcome" integer
  "DateCreated" timestamp [not null]
  "DateUpdated" timestamp [not null]
  "UserID" "character varying(32)" [not null]
  "DateDeleted" timestamp
  "ExportID" "character varying(32)" [not null]
}

Table "User" {
  "UserID" "character varying(32)" [pk, not null]
  "UserFirstName" "character varying(50)"
  "UserLastName" "character varying(50)"
  "UserPhone" "character varying(10)"
  "UserExtension" "character varying(5)"
  "UserEmail" "character varying(320)"
  "DateCreated" timestamp [not null]
  "DateUpdated" timestamp [not null]
  "DateDeleted" timestamp
  "ExportID" "character varying(32)" [not null]
}

Table "VASHExitReason" {
  "ExitID" "character varying(32)" [pk, not null]
  "EnrollmentID" "character varying(32)" [not null]
  "PersonalID" "character varying(32)" [not null]
  "CMExitReason" integer
  "DateCreated" timestamp [not null]
  "DateUpdated" timestamp [not null]
  "UserID" "character varying(32)" [not null]
  "DateDeleted" timestamp
  "ExportID" "character varying(32)" [not null]
}

Table "YouthEducationStatus" {
  "YouthEducationStatusID" "character varying(32)" [pk, not null]
  "EnrollmentID" "character varying(32)" [not null]
  "PersonalID" "character varying(32)" [not null]
  "InformationDate" date [not null]
  "CurrentSchoolAttend" integer
  "MostRecentEdStatus" integer
  "CurrentEdStatus" integer
  "DataCollectionStage" integer [not null]
  "DateCreated" timestamp [not null]
  "DateUpdated" timestamp [not null]
  "UserID" "character varying(32)" [not null]
  "DateDeleted" timestamp
  "ExportID" "character varying(32)" [not null]
}

Ref "fk_assessmentid":"Assessment"."AssessmentID" < "AssessmentQuestion"."AssessmentID"

Ref "fk_assessmentid":"Assessment"."AssessmentID" < "AssessmentResults"."AssessmentID"

Ref "fk_enrollmentid":"Enrollment"."EnrollmentID" < "Assessment"."EnrollmentID"

Ref "fk_enrollmentid":"Enrollment"."EnrollmentID" < "AssessmentQuestion"."EnrollmentID"

Ref "fk_enrollmentid":"Enrollment"."EnrollmentID" < "AssessmentResults"."EnrollmentID"

Ref "fk_enrollmentid":"Enrollment"."EnrollmentID" < "ConnectedWithSOAR"."EnrollmentID"

Ref "fk_enrollmentid":"Enrollment"."EnrollmentID" < "CurrentLivingSituation"."EnrollmentID"

Ref "fk_enrollmentid":"Enrollment"."EnrollmentID" < "Disabilities"."EnrollmentID"

Ref "fk_enrollmentid":"Enrollment"."EnrollmentID" < "DomesticViolence"."EnrollmentID"

Ref "fk_enrollmentid":"Enrollment"."EnrollmentID" < "Education"."EnrollmentID"

Ref "fk_enrollmentid":"Enrollment"."EnrollmentID" < "Employment"."EnrollmentID"

Ref "fk_enrollmentid":"Enrollment"."EnrollmentID" < "Event"."EnrollmentID"

Ref "fk_enrollmentid":"Enrollment"."EnrollmentID" < "ExitHousingAssessment"."EnrollmentID"

Ref "fk_enrollmentid":"Enrollment"."EnrollmentID" < "ExitRHY"."EnrollmentID"

Ref "fk_enrollmentid":"Enrollment"."EnrollmentID" < "Exits"."EnrollmentID"

Ref "fk_enrollmentid":"Enrollment"."EnrollmentID" < "HealthInsurance"."EnrollmentID"

Ref "fk_enrollmentid":"Enrollment"."EnrollmentID" < "HealthStatus"."EnrollmentID"

Ref "fk_enrollmentid":"Enrollment"."EnrollmentID" < "IncomeAndSources"."EnrollmentID"

Ref "fk_enrollmentid":"Enrollment"."EnrollmentID" < "MedicalAssistance"."EnrollmentID"

Ref "fk_enrollmentid":"Enrollment"."EnrollmentID" < "NonCashBenefits"."EnrollmentID"

Ref "fk_enrollmentid":"Enrollment"."EnrollmentID" < "RHYAftercare"."EnrollmentID"

Ref "fk_enrollmentid":"Enrollment"."EnrollmentID" < "ServiceFAReferral"."EnrollmentID"

Ref "fk_enrollmentid":"Enrollment"."EnrollmentID" < "VASHExitReason"."EnrollmentID"

Ref "fk_enrollmentid":"Enrollment"."EnrollmentID" < "YouthEducationStatus"."EnrollmentID"

Ref "fk_exportid":"Export"."ExportID" < "Affiliation"."ExportID"

Ref "fk_exportid":"Export"."ExportID" < "Assessment"."ExportID"

Ref "fk_exportid":"Export"."ExportID" < "AssessmentQuestion"."ExportID"

Ref "fk_exportid":"Export"."ExportID" < "AssessmentResults"."ExportID"

Ref "fk_exportid":"Export"."ExportID" < "CEParticipation"."ExportID"

Ref "fk_exportid":"Export"."ExportID" < "Client"."ExportID"

Ref "fk_exportid":"Export"."ExportID" < "ClientVeteranInfo"."ExportID"

Ref "fk_exportid":"Export"."ExportID" < "ConnectedWithSOAR"."ExportID"

Ref "fk_exportid":"Export"."ExportID" < "CurrentLivingSituation"."ExportID"

Ref "fk_exportid":"Export"."ExportID" < "DateOfEngagement"."ExportID"

Ref "fk_exportid":"Export"."ExportID" < "Disabilities"."ExportID"

Ref "fk_exportid":"Export"."ExportID" < "DomesticViolence"."ExportID"

Ref "fk_exportid":"Export"."ExportID" < "Education"."ExportID"

Ref "fk_exportid":"Export"."ExportID" < "Employment"."ExportID"

Ref "fk_exportid":"Export"."ExportID" < "Enrollment"."ExportID"

Ref "fk_exportid":"Export"."ExportID" < "EntryRHY"."ExportID"

Ref "fk_exportid":"Export"."ExportID" < "EntrySSVF"."ExportID"

Ref "fk_exportid":"Export"."ExportID" < "Event"."ExportID"

Ref "fk_exportid":"Export"."ExportID" < "ExitHousingAssessment"."ExportID"

Ref "fk_exportid":"Export"."ExportID" < "ExitRHY"."ExportID"

Ref "fk_exportid":"Export"."ExportID" < "Exits"."ExportID"

Ref "fk_exportid":"Export"."ExportID" < "Funder"."ExportID"

Ref "fk_exportid":"Export"."ExportID" < "HealthInsurance"."ExportID"

Ref "fk_exportid":"Export"."ExportID" < "HealthStatus"."ExportID"

Ref "fk_exportid":"Export"."ExportID" < "HMISParticipation"."ExportID"

Ref "fk_exportid":"Export"."ExportID" < "Household"."ExportID"

Ref "fk_exportid":"Export"."ExportID" < "IncomeAndSources"."ExportID"

Ref "fk_exportid":"Export"."ExportID" < "Inventory"."ExportID"

Ref "fk_exportid":"Export"."ExportID" < "MedicalAssistance"."ExportID"

Ref "fk_exportid":"Export"."ExportID" < "MoveInDate"."ExportID"

Ref "fk_exportid":"Export"."ExportID" < "NonCashBenefits"."ExportID"

Ref "fk_exportid":"Export"."ExportID" < "Organization"."ExportID"

Ref "fk_exportid":"Export"."ExportID" < "PATHStatus"."ExportID"

Ref "fk_exportid":"Export"."ExportID" < "Project"."ExportID"

Ref "fk_exportid":"Export"."ExportID" < "ProjectCoC"."ExportID"

Ref "fk_exportid":"Export"."ExportID" < "RHYAftercare"."ExportID"

Ref "fk_exportid":"Export"."ExportID" < "RHYBCPStatus"."ExportID"

Ref "fk_exportid":"Export"."ExportID" < "ServiceFAReferral"."ExportID"

Ref "fk_exportid":"Export"."ExportID" < "User"."ExportID"

Ref "fk_exportid":"Export"."ExportID" < "VASHExitReason"."ExportID"

Ref "fk_exportid":"Export"."ExportID" < "YouthEducationStatus"."ExportID"

Ref "fk_householdid":"Household"."HouseholdID" < "Enrollment"."HouseholdID"

Ref "fk_householdid":"Household"."HouseholdID" < "EntryRHY"."HouseholdID"

Ref "fk_householdid":"Household"."HouseholdID" < "EntrySSVF"."HouseholdID"

Ref "fk_householdid":"Household"."HouseholdID" < "MoveInDate"."HouseholdID"

Ref "fk_householdid":"Household"."HouseholdID" < "PATHStatus"."HouseholdID"

Ref "fk_householdid":"Household"."HouseholdID" < "RHYBCPStatus"."HouseholdID"

Ref "fk_organizationid":"Organization"."OrganizationID" < "Project"."OrganizationID"

Ref "fk_personalid":"Client"."PersonalID" < "Assessment"."PersonalID"

Ref "fk_personalid":"Client"."PersonalID" < "AssessmentQuestion"."PersonalID"

Ref "fk_personalid":"Client"."PersonalID" < "AssessmentResults"."PersonalID"

Ref "fk_personalid":"Client"."PersonalID" < "ConnectedWithSOAR"."PersonalID"

Ref "fk_personalid":"Client"."PersonalID" < "CurrentLivingSituation"."PersonalID"

Ref "fk_personalid":"Client"."PersonalID" < "Disabilities"."PersonalID"

Ref "fk_personalid":"Client"."PersonalID" < "DomesticViolence"."PersonalID"

Ref "fk_personalid":"Client"."PersonalID" < "Education"."PersonalID"

Ref "fk_personalid":"Client"."PersonalID" < "Employment"."PersonalID"

Ref "fk_personalid":"Client"."PersonalID" < "Enrollment"."PersonalID"

Ref "fk_personalid":"Client"."PersonalID" < "EntryRHY"."PersonalID"

Ref "fk_personalid":"Client"."PersonalID" < "EntrySSVF"."PersonalID"

Ref "fk_personalid":"Client"."PersonalID" < "Event"."PersonalID"

Ref "fk_personalid":"Client"."PersonalID" < "ExitHousingAssessment"."PersonalID"

Ref "fk_personalid":"Client"."PersonalID" < "ExitRHY"."PersonalID"

Ref "fk_personalid":"Client"."PersonalID" < "Exits"."PersonalID"

Ref "fk_personalid":"Client"."PersonalID" < "HealthInsurance"."PersonalID"

Ref "fk_personalid":"Client"."PersonalID" < "HealthStatus"."PersonalID"

Ref "fk_personalid":"Client"."PersonalID" < "IncomeAndSources"."PersonalID"

Ref "fk_personalid":"Client"."PersonalID" < "MedicalAssistance"."PersonalID"

Ref "fk_personalid":"Client"."PersonalID" < "MoveInDate"."PersonalID"

Ref "fk_personalid":"Client"."PersonalID" < "NonCashBenefits"."PersonalID"

Ref "fk_personalid":"Client"."PersonalID" < "PATHStatus"."PersonalID"

Ref "fk_personalid":"Client"."PersonalID" < "RHYAftercare"."PersonalID"

Ref "fk_personalid":"Client"."PersonalID" < "RHYBCPStatus"."PersonalID"

Ref "fk_personalid":"Client"."PersonalID" < "ServiceFAReferral"."PersonalID"

Ref "fk_personalid":"Client"."PersonalID" < "VASHExitReason"."PersonalID"

Ref "fk_personalid":"Client"."PersonalID" < "YouthEducationStatus"."PersonalID"

Ref "fk_projectid":"Project"."ProjectID" < "Affiliation"."ProjectID"

Ref "fk_projectid":"Project"."ProjectID" < "CEParticipation"."ProjectID"

Ref "fk_projectid":"Project"."ProjectID" < "Enrollment"."ProjectID"

Ref "fk_projectid":"Project"."ProjectID" < "EntryRHY"."ProjectID"

Ref "fk_projectid":"Project"."ProjectID" < "EntrySSVF"."ProjectID"

Ref "fk_projectid":"Project"."ProjectID" < "Funder"."ProjectID"

Ref "fk_projectid":"Project"."ProjectID" < "HMISParticipation"."ProjectID"

Ref "fk_projectid":"Project"."ProjectID" < "Household"."ProjectID"

Ref "fk_projectid":"Project"."ProjectID" < "Inventory"."ProjectID"

Ref "fk_projectid":"Project"."ProjectID" < "MoveInDate"."ProjectID"

Ref "fk_projectid":"Project"."ProjectID" < "PATHStatus"."ProjectID"

Ref "fk_projectid":"Project"."ProjectID" < "ProjectCoC"."ProjectID"

Ref "fk_projectid":"Project"."ProjectID" < "RHYBCPStatus"."ProjectID"

Ref "fk_resprojectid":"Project"."ProjectID" < "Affiliation"."ResProjectID"

Ref "fk_userid":"User"."UserID" < "Affiliation"."UserID"

Ref "fk_userid":"User"."UserID" < "Assessment"."UserID"

Ref "fk_userid":"User"."UserID" < "AssessmentQuestion"."UserID"

Ref "fk_userid":"User"."UserID" < "AssessmentResults"."UserID"

Ref "fk_userid":"User"."UserID" < "CEParticipation"."UserID"

Ref "fk_userid":"User"."UserID" < "Client"."UserID"

Ref "fk_userid":"User"."UserID" < "ClientVeteranInfo"."UserID"

Ref "fk_userid":"User"."UserID" < "ConnectedWithSOAR"."UserID"

Ref "fk_userid":"User"."UserID" < "CurrentLivingSituation"."UserID"

Ref "fk_userid":"User"."UserID" < "DateOfEngagement"."UserID"

Ref "fk_userid":"User"."UserID" < "Disabilities"."UserID"

Ref "fk_userid":"User"."UserID" < "DomesticViolence"."UserID"

Ref "fk_userid":"User"."UserID" < "Education"."UserID"

Ref "fk_userid":"User"."UserID" < "Employment"."UserID"

Ref "fk_userid":"User"."UserID" < "Enrollment"."UserID"

Ref "fk_userid":"User"."UserID" < "EntryRHY"."UserID"

Ref "fk_userid":"User"."UserID" < "EntrySSVF"."UserID"

Ref "fk_userid":"User"."UserID" < "Event"."UserID"

Ref "fk_userid":"User"."UserID" < "ExitHousingAssessment"."UserID"

Ref "fk_userid":"User"."UserID" < "ExitRHY"."UserID"

Ref "fk_userid":"User"."UserID" < "Exits"."UserID"

Ref "fk_userid":"User"."UserID" < "Funder"."UserID"

Ref "fk_userid":"User"."UserID" < "HealthInsurance"."UserID"

Ref "fk_userid":"User"."UserID" < "HealthStatus"."UserID"

Ref "fk_userid":"User"."UserID" < "HMISParticipation"."UserID"

Ref "fk_userid":"User"."UserID" < "Household"."UserID"

Ref "fk_userid":"User"."UserID" < "IncomeAndSources"."UserID"

Ref "fk_userid":"User"."UserID" < "Inventory"."UserID"

Ref "fk_userid":"User"."UserID" < "MedicalAssistance"."UserID"

Ref "fk_userid":"User"."UserID" < "MoveInDate"."UserID"

Ref "fk_userid":"User"."UserID" < "NonCashBenefits"."UserID"

Ref "fk_userid":"User"."UserID" < "Organization"."UserID"

Ref "fk_userid":"User"."UserID" < "PATHStatus"."UserID"

Ref "fk_userid":"User"."UserID" < "Project"."UserID"

Ref "fk_userid":"User"."UserID" < "ProjectCoC"."UserID"

Ref "fk_userid":"User"."UserID" < "RHYAftercare"."UserID"

Ref "fk_userid":"User"."UserID" < "RHYBCPStatus"."UserID"

Ref "fk_userid":"User"."UserID" < "ServiceFAReferral"."UserID"

Ref "fk_userid":"User"."UserID" < "VASHExitReason"."UserID"

Ref "fk_userid":"User"."UserID" < "YouthEducationStatus"."UserID"


Ref: "ClientVeteranInfo"."PersonalID" - "Client"."PersonalID"

Ref: "Disabilities"."DisabilitiesID" < "Disabilities"."AntiRetroviral"

Ref: "Exits"."ExitID" < "Exits"."ExitDate"