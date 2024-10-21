# JobTeaser Final Project
Le Wagon - Data Analytics Final Project: A comprehensive data analytics project developed as the final assessment for the Le Wagon Data Analytics bootcamp. The project includes data exploration, preprocessing, modeling, and visualization, applying key concepts learned throughout the course.

## **1. Introduction:**
### **Context:**
**JobTeaser** is a platform that connects students and companies by managing career services for over 750 universities globally. It provides a **matching tool** where companies can shortlist students for job opportunities. Optimizing the job placement funnel is critical to enhancing student employment rates and improving the platform's efficiency.

**Job placement funnel:**
The job placement funnel is:
- opt-in (student activate a toggle "looking for opportunities")
- opt-in qualified (students upload their CV)
- students being shortlisted by the algorithm
- students answered
- students being interested
- companies answered
- companies approved

Analyzing this funnel will help the product team improve the job placement of the users.


### **Project goal:**
The goal of this project is to analyze and optimize the JobTeaser job placement funnel by identifying bottlenecks in the current process and suggesting improvements to increase student engagement and job matches.

### **Data Overview:**
This analysis uses three key datasets:
#### **Opt-in Table (optin):**
 Contains data about students opting in or out of JobTeaser services.

- **user_id**: ID del estudiante.
- **receive_time**: Fecha/hora de opt-in/out.
- **cause**: Razón (manual o automático).
- **active**: `TRUE` si opt-in, `FALSE` si no.
- **school_id**: ID de la escuela.
- **current_sign_in_at**: Última conexión.
- **resume_uploaded**: CV subido.

#### **Candidate Status Update (candidate_status_update):**
Tracks students' status updates within the job application process.

- **user_id**: ID del estudiante.
- **receive_time**: Fecha/hora del evento.
- **shortlist_id**: ID de Shortlist.
- **status_update**: Estado (estudiante: `awaiting`, `interested`, `not interested`; empresa: `approved`, `declined`).
- **cause**: Razón (click o timeout).
- **school_id**: ID de la escuela.
- **current_sign_in_at**: Última conexión.

#### **School Info Table (dim_schools):**
Provides data about the schools participating in JobTeaser's services.

- **school_id**: ID de la escuela.
- **is_cc**: Centro de carreras o sitio público.
- **intranet_school_id**: ID del centro de carreras si aplica.
- **jt_country**: País de la escuela.
- **jt_intranet_status**: Estado "launched" para centro de carreras.
- **jt_school_type**: Tipo de escuela (1: Ingenierías, 2: Negocios, 3: Otras).



