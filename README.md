## BORA – Better Opportunities, Routes and Accessibility
## 1. Project Overview

BORA – Better Opportunities, Routes and Accessibility is a proposed system designed to address difficulties in accessing reliable, affordable and suitable transport in Sierra Leone.

The system provides a logical approach for passengers to submit transport requests, view available transport providers and fare information, and confirm a journey. It also directs urgent medical requests towards appropriate emergency assistance.

This project is developed as part of the PROG101: Principles of Programming Logic and Design assignment at Limkokwing University of Creative Technology, Sierra Leone.

## 2. Problem Statement

Limited transport availability, unclear fares, poor road access and long waiting times are major challenges in many communities in Sierra Leone. These problems make it difficult for people to reach hospitals, schools, workplaces and markets, and they particularly affect rural communities, older people, persons with disabilities, low-income households, students and patients.

The proposed system aims to improve how transport requests are submitted, recorded and matched with available providers.

## 3. Project Objectives

The main objectives are to:

Provide a simple way for passengers to submit transport requests.
Validate information submitted by passengers.
Generate a unique identification number for every request.
Identify urgent medical requests and display emergency guidance.
Show available providers and fare information before a journey is confirmed.
Offer a waiting-list option when no suitable transport is available.
Improve the organisation and tracking of transport requests.

## 4. Main System Features

Passenger transport request submission.
Request information validation.
Medical emergency identification and guidance.
Unique Request ID generation.
Provider search and fare information display.
Journey confirmation, editing and cancellation.
Waiting-list option.
Request status tracking.
Passenger feedback collection.

## 5. Journey Purpose Categories

The system will recognise the following journey purposes:

Healthcare.
Education.
Work.
Market.
Other.

## 6. Request Status

Each request will have one of the following statuses:

Pending: The request has been received.
Waiting: No suitable provider is available and the request is on the waiting list.
Confirmed: The passenger has confirmed a provider and the journey is arranged.
Cancelled: The request has been cancelled.

## 7. Computational Thinking Concepts

The project applies the following computational thinking concepts:

Decomposition
Pattern Recognition
Abstraction
Algorithm Design

## 8. Technologies and Tools

The project uses the following tools for its logical design and documentation:

GitHub – Project storage and version control.
Microsoft Word – Assignment documentation.
Flowcharts – Visual representation of system processes.
Pseudocode – Description of the system's logical steps.

## 9. Repository Structure

The repository contains the following project materials:

Documentation – Project report and explanations.
Algorithms – Algorithm designs.
Pseudocode – Logical instructions for the system.
Flowcharts – Visual diagrams of the system processes.
Screenshots – Evidence of project development and GitHub activities.

## 10. Expected Outputs

The expected system outputs include:

Request submission confirmation.
Unique Request Identification Number.
Error and validation messages.
Emergency guidance message for urgent requests.
List of available providers and fare estimates.
Waiting-list message when no provider is available.
Request status display (confirmed, waiting or cancelled).

## 11. Project Limitations

The project focuses on logical system design and documentation. It does not represent a fully developed application. It is not an ambulance or emergency dispatch service, does not replace emergency services or government transport authorities, and does not provide vehicles, repair roads or guarantee transport.

## 12. Sustainable Development Goals

The project supports:

SDG 3: Good Health and Well-being.
SDG 9: Industry, Innovation and Infrastructure.
SDG 10: Reduced Inequalities.
SDG 11: Sustainable Cities and Communities.
## 13. Conclusion

BORA – Better Opportunities, Routes and Accessibility is proposed as a logical solution to improve how transport requests are submitted, matched and monitored in Sierra Leone. It demonstrates how programming logic and computational thinking can be applied to address real-life community challenges.# PROG101_ASSIGNMENT1_MARIAN_SIA_MARAH_905006533

## ALGORITHM DESIGN
The following step-by-step algorithm describes the main process of BORA.
1.	Start the system.
2.	Display the transport request form.
3.	Receive the passenger's starting location, destination, journey purpose, preferred time and assistance requirements.
4.	Check whether all required information has been entered.
5.	If information is missing, ask the user to correct the request and repeat the validation step.
6.	Save the complete request and generate a request identification number.
7.	Check whether the passenger has identified the journey as a medical emergency.
8.	If it is an emergency, display a clear instruction to contact the appropriate emergency service or nearest health facility immediately. Mark the request as urgent, but do not treat the platform as an ambulance service.
9.	Search the provider list for transport that matches the route, time and accessibility requirements.
10.	If no suitable provider is available, inform the passenger and offer a waiting-list or community assistance option.
11.	If providers are available, display the provider details, estimated fare and relevant journey information.
12.	Ask the passenger to confirm one option.
13.	If the passenger confirms, record the match and send the journey details to the passenger and provider.
14.	If the passenger does not confirm, allow the passenger to edit or cancel the request.
15.	After the journey, invite the passenger to provide feedback and update the request status.
16.	End the process.

## PSEUDOCODE
BEGIN
    DISPLAY "Welcome to BORA"

    INPUT passenger Name
    INPUT origin
    INPUT destination
    INPUT journey Purpose
    INPUT preferred Time
    INPUT assistance Needed
    INPUT is Medical Emergency

    WHILE origin is empty OR destination is empty OR preferred Time is empty
        DISPLAY "Please complete all required journey details"
        INPUT origin
        INPUT destination
        INPUT preferred Time
    END WHILE

    requestID= GENERATE_REQUEST_ID()
    SAVE_REQUEST(requestID, origin, destination,
                 journey Purpose, preferred Time,
                 assistance Needed, is Medical Emergency)

    IF is Medical Emergency = TRUE THEN
        DISPLAY "URGENT: Contact the appropriate emergency service
                 or nearest health facility immediately."
        SET request Priority = "URGENT"
    ELSE
        SET request Priority = "NORMAL"
    END IF

    providers = FIND_AVAILABLE_PROVIDERS(
                    origin, destination, preferred Time,
                    assistance Needed)

    IF providers is empty THEN
        DISPLAY "No suitable provider is currently available"
        OFFER_WAITING_LIST()
        SET request Status = "WAITING"
    ELSE
        DISPLAY providers and available fare information
        INPUT user Choice

        IF user Choice is valid THEN
            DISPLAY selected provider and journey details
            INPUT confirmation

            IF confirmation = "YES" THEN
                CONFIRM_MATCH(requestID, user Choice)
                SET request Status = "CONFIRMED"
                DISPLAY "Your transport request is confirmed"
            ELSE
                DISPLAY "You may edit or cancel your request"
                SET request Status = "NOT_CONFIRMED"
            END IF
        ELSE
            DISPLAY "Please select a valid provider"
            SET request Status = "PENDING"
        END IF
    END IF

    UPDATE_REQUEST_STATUS(requestID, request Status)
    DISPLAY "Thank you for using BORA"
END

## FLOW CHART

<img width="2159" height="8192" alt="Untitled diagram-2026-11-04-144136" src="https://github.com/user-attachments/assets/bac34301-825d-4d02-bc9c-416dd5e7b508" />


## AUTHOR
-MARIAN SIA MARAH-905006533


