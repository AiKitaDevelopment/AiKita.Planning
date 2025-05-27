# 🛠️ Quality Assurance Principle Statement

**Quality Assurance (QA)** is a foundational principle of our development process. 
We embed quality into every stage of our development lifecycle — from design to deployment. 
The following QA practices and goals define our standard:  

## General QA Guidelines

1. **Test Coverage**
   - A minimum of **80% unit test coverage** must be achieved and maintained throughout the codebase.
   - All features and bug fixes must be covered by **automated tests** before merging.

2. **Performance Standards**
   - The app must support **100 concurrent users** with response times **under 2 seconds** for all major actions.
   - Performance tests will be conducted for each major release.

3. **Usability Testing**
   - **Hallway usability testing** (quick tests with random users) will be applied as soon as individual features are functional.
   - **Field testing** will be conducted as user stories reach integration status — to test end-to-end flow with target user groups.
   - Usability feedback will be looped directly back into product iterations.

4. **Constant QA Integration**
   - Continuous Integration (CI) pipelines will automatically run unit and performance tests.
   - Code reviews will include QA checks for logic correctness, edge cases, and test presence.

5. **QA Culture**
   - QA is not a phase, it is a **mindset**. Every team member is responsible for upholding the quality standard.
   - We actively seek **qualitative feedback** from users, developers, and testers, and apply it continuously.

---

# 🎯QA Milestones

| Milestone | Description | Target Date | 
|-----------|-------------|-------------|
| **M1 – QA Infrastructure Setup** | CI/CD with automated test runner + code coverage reporting | Month 2 | 
| **M2 – Core Unit Tests (>50%)** | Unit tests for all core modules, 50% coverage | Mont 4  | 
| **M3 – Usability Testing Phase 1 (Hallway)** | Hallway testing of UI flow, 5 test users | Month 4 | 
| **M4 – Core Performance Test** | Load test with 100 simulated users | Month 6 | 
| **M5 – Field Testing Phase** | Field test with 10 users of full feature set | Month 7 | 
| **M6 – Final QA Audit & Sign-off** | Regression testing, usability feedback integrated | Month 8 -10 |

# :chart_with_upwards_trend: Documentation

| Date | Task | Status | Details | 
|------|-----------|-------------|-------------|
| 01.05.2025 | Entity Unit Tests | 80% completed | Implemented for all entities (backend) and their local validation excluding fulldata. | 
| 07.05.2025 | Entity Unit Tests | 30% completed | Implemented for all entities (backend) and their global validation uncluding fulldata. | 
| 20.05.2025 | API Backend Testing | 100% completed | Validated backend endpoints via Postman | 
| 27.05.2025 | Validated end-to-end data integrity | 100% completed | Cross-checking backend database entries (via SQL Manager) with frontend output | 


