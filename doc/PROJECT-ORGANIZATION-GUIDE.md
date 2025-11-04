# LDAP Infrastructure Suite - Project Organization Guide

**Project**: #3 - LDAP Infrastructure Suite - Feature Release Tracker  
**URL**: https://github.com/orgs/infrastructure-alexson/projects/3  
**Last Updated**: 2025-11-04

---

## Overview

This guide provides step-by-step instructions for organizing the GitHub Project for the LDAP Infrastructure Suite. It covers custom fields, views, iterations, and issue organization.

---

## Custom Fields Setup

Navigate to: **Project Settings → Fields**

### 1. Version (Single Select)

**Field Name**: `Version`  
**Type**: Single select  
**Description**: Target release version for the feature

**Options**:
- `v1.0.0` (Foundation)
- `v1.1.0` (Production Ready)
- `v1.2.0` (Enterprise Features)
- `v2.0.0` (Cloud Native)
- `v2.1.0` (Advanced Automation)

**Color Scheme**:
- v1.0.0: Blue (#0366d6)
- v1.1.0: Blue-green (#1d76db)
- v1.2.0: Green (#2ea44f)
- v2.0.0: Yellow (#fbca04)
- v2.1.0: Purple (#d4c5f9)

---

### 2. Priority (Single Select)

**Field Name**: `Priority`  
**Type**: Single select  
**Description**: Feature priority level

**Options**:
- `Critical` - Must complete, blocks other work
- `High` - Important for release
- `Medium` - Standard priority
- `Low` - Nice to have

**Color Scheme**:
- Critical: Red (#d73a4a)
- High: Orange (#d93f0b)
- Medium: Yellow (#fbca04)
- Low: Gray (#6a737d)

---

### 3. Component (Single Select)

**Field Name**: `Component`  
**Type**: Single select  
**Description**: Primary component or service affected

**Options**:
- `389 DS` - 389 Directory Service / LDAP
- `Kea DHCP` - Kea DHCP server
- `BIND 9` - BIND 9 DNS server
- `Web Manager` - LDAP Web Manager
- `PostgreSQL` - PostgreSQL database
- `Redis` - Redis cache
- `Infrastructure` - Docker Compose, Kubernetes, deployment
- `Documentation` - Documentation and guides

**Color Scheme**:
- 389 DS: Blue (#2196F3)
- Kea DHCP: Orange (#FF9800)
- BIND 9: Purple (#9C27B0)
- Web Manager: Green (#4CAF50)
- PostgreSQL: Cyan (#00BCD4)
- Redis: Red (#F44336)
- Infrastructure: Teal (#009688)
- Documentation: Gray (#607D8B)

---

### 4. Estimated Effort (Number)

**Field Name**: `Estimated Effort`  
**Type**: Number  
**Description**: Estimated development effort in days  
**Unit**: Days

**Guidelines**:
- Small tasks: 1-2 days
- Medium tasks: 3-5 days
- Large tasks: 6-8 days
- Very large tasks: 9+ days

---

### 5. Iteration (Iteration Field)

**Field Name**: `Iteration`  
**Type**: Iteration  
**Description**: Sprint or iteration assignment

**Iterations to Create**:

#### Iteration 1: Container Images
- **Start Date**: 2026-04-01
- **End Date**: 2026-04-15
- **Duration**: 2 weeks
- **Focus**: Build custom container images
- **Issues**: #3, #4, #5

#### Iteration 2: Integration
- **Start Date**: 2026-04-16
- **End Date**: 2026-04-30
- **Duration**: 2 weeks
- **Focus**: Docker Compose and service integration
- **Issues**: #1, #2, #6

#### Iteration 3: Operations
- **Start Date**: 2026-05-01
- **End Date**: 2026-05-15
- **Duration**: 2 weeks
- **Focus**: Monitoring and operational tools
- **Issues**: #7, #9

#### Iteration 4: Release
- **Start Date**: 2026-05-16
- **End Date**: 2026-05-31
- **Duration**: 2 weeks
- **Focus**: Documentation and release preparation
- **Issues**: #8, #10

---

## Project Views

Navigate to: **Project → View dropdown → New view**

### View 1: By Version (Board View)

**Name**: `By Version`  
**Type**: Board  
**Purpose**: Visualize issues grouped by target version

**Configuration**:
- **Group by**: Version
- **Sort by**: Priority (High to Low), then Issue number
- **Show**: All items
- **Layout**: Cards

**Use Case**: Track features across different releases, see version progress

---

### View 2: By Priority (Table View)

**Name**: `By Priority`  
**Type**: Table  
**Purpose**: Focus on high-priority work

**Configuration**:
- **Group by**: Priority
- **Sort by**: Priority (Critical to Low), then Version, then Issue number
- **Columns**: Issue, Status, Version, Component, Estimated Effort, Assignees
- **Show**: All items

**Use Case**: Identify critical and high-priority items that need immediate attention

---

### View 3: By Component (Board View)

**Name**: `By Component`  
**Type**: Board  
**Purpose**: Organize work by service/component

**Configuration**:
- **Group by**: Component
- **Sort by**: Priority (High to Low), then Issue number
- **Show**: All items
- **Layout**: Cards

**Use Case**: See all work related to specific components (e.g., all BIND 9 tasks)

---

### View 4: v1.0.0 Sprint (Table View)

**Name**: `v1.0.0 Sprint`  
**Type**: Table  
**Purpose**: Current sprint/iteration focus

**Configuration**:
- **Filter**: `version:v1.0.0`
- **Sort by**: Priority (High to Low), then Estimated Effort (High to Low)
- **Columns**: Issue, Status, Priority, Component, Estimated Effort, Iteration, Assignees
- **Show**: Filtered items only

**Use Case**: Daily standup view, sprint planning, tracking current work

---

### View 5: Roadmap (Roadmap View)

**Name**: `Release Roadmap`  
**Type**: Roadmap  
**Purpose**: Timeline visualization

**Configuration**:
- **Group by**: Iteration
- **Date field**: Iteration (start/end dates)
- **Sort by**: Iteration date
- **Show**: All items

**Use Case**: High-level release timeline, stakeholder communication, planning

---

## Issue Field Values

### Current v1.0.0 Issues

| Issue | Title | Version | Priority | Component | Effort (days) |
|-------|-------|---------|----------|-----------|---------------|
| #1 | Docker Compose Deployment | v1.0.0 | High | Infrastructure | 8 |
| #2 | Service Discovery | v1.0.0 | High | Infrastructure | 5 |
| #3 | 389 DS Container Images | v1.0.0 | Medium | 389 DS | 6 |
| #4 | Kea DHCP Container Images | v1.0.0 | Medium | Kea DHCP | 6 |
| #5 | BIND 9 Container Images | v1.0.0 | Medium | BIND 9 | 6 |
| #6 | Web Manager Integration | v1.0.0 | Medium | Web Manager | 4 |
| #7 | Monitoring & Health Checks | v1.0.0 | Medium | Infrastructure | 5 |
| #8 | Documentation | v1.0.0 | High | Documentation | 8 |
| #9 | Backup & Restore | v1.0.0 | Medium | Infrastructure | 5 |
| #10 | Container Registry | v1.0.0 | Medium | Infrastructure | 4 |

**Total Estimated Effort**: 57 days  
**Average per Issue**: 5.7 days

---

## Work Organization

### Recommended Implementation Order

#### Phase 1: Container Images (18 days, 2 weeks)
1. **Issue #3** - 389 DS Container Images (6 days)
   - Base image customization
   - Schema installation
   - Replication setup

2. **Issue #4** - Kea DHCP Container Images (6 days)
   - LDAP backend integration
   - HA configuration
   - Control Agent setup

3. **Issue #5** - BIND 9 Container Images (6 days)
   - DLZ LDAP compilation
   - Zone configuration
   - Primary/secondary setup

**Iteration**: 1 (Apr 1-15, 2026)  
**Why First**: Foundation - must have container images before integration

---

#### Phase 2: Integration (17 days, 2 weeks)
4. **Issue #1** - Docker Compose Deployment (8 days)
   - Complete docker-compose.yml
   - Service orchestration
   - Network and volume configuration

5. **Issue #2** - Service Discovery (5 days)
   - Automatic configuration
   - Service account creation
   - Integration testing

6. **Issue #6** - Web Manager Integration (4 days)
   - Connect to all services
   - DHCP API integration
   - Dashboard updates

**Iteration**: 2 (Apr 16-30, 2026)  
**Why Second**: Brings all components together

---

#### Phase 3: Operations (10 days, 2 weeks)
7. **Issue #7** - Monitoring & Health Checks (5 days)
   - Health check endpoints
   - Prometheus metrics
   - Dashboard creation

8. **Issue #9** - Backup & Restore (5 days)
   - Backup scripts
   - Restore procedures
   - Automation

**Iteration**: 3 (May 1-15, 2026)  
**Why Third**: Operational readiness

---

#### Phase 4: Release (12 days, 2 weeks)
9. **Issue #8** - Documentation (8 days)
   - Installation guides
   - Configuration reference
   - Troubleshooting

10. **Issue #10** - Container Registry (4 days)
    - CI/CD pipeline
    - Multi-arch builds
    - Publication

**Iteration**: 4 (May 16-31, 2026)  
**Why Last**: Release preparation

---

## Metrics & Tracking

### Velocity Tracking

**Total Work**: 57 days  
**Iterations**: 4 (8 weeks)  
**Average per Iteration**: 14.25 days  
**Target Team Size**: 2-3 developers

**Expected Velocity**:
- 2 developers: ~12-15 days/iteration (realistic with testing)
- 3 developers: ~18-21 days/iteration (with coordination overhead)

### Burndown Tracking

**Iteration 1**: 18 days → Remaining: 39 days  
**Iteration 2**: 17 days → Remaining: 22 days  
**Iteration 3**: 10 days → Remaining: 12 days  
**Iteration 4**: 12 days → Remaining: 0 days (Release!)

### Issue Status Transitions

**Workflow**:
1. **Todo** - Not started
2. **In Progress** - Actively being worked on
3. **In Review** - PR open, awaiting review
4. **Done** - Merged and closed

**Status Updates**:
- Update status daily
- Move to "In Progress" when starting
- Move to "In Review" when PR is created
- Move to "Done" when merged

---

## Manual Setup Steps

### Step 1: Access the Project

1. Navigate to: https://github.com/orgs/infrastructure-alexson/projects/3
2. Ensure you have admin access

### Step 2: Add Custom Fields

1. Click the **Settings** icon (gear) in top-right
2. Click **Fields** in the left sidebar
3. For each field listed above:
   - Click **+ New field**
   - Enter **Field name**
   - Select **Field type**
   - Add **Options** (for select fields)
   - Click **Save**

### Step 3: Create Iterations

1. In Settings → Fields
2. Find the **Iteration** field
3. Click **Manage iterations**
4. Create 4 iterations with the dates listed above
5. Save each iteration

### Step 4: Create Views

1. Go back to the main project view
2. Click **View** dropdown (next to the current view name)
3. Click **+ New view**
4. For each view listed above:
   - Select view type (Board, Table, or Roadmap)
   - Enter view name
   - Configure grouping, sorting, and filters
   - Customize columns (for Table views)
   - Save the view

### Step 5: Update Issue Fields

For each issue (#1 through #10):
1. Open the issue in the project
2. Click the issue to open the side panel
3. Set the following fields:
   - **Version**: v1.0.0
   - **Priority**: As listed in table above
   - **Component**: As listed in table above
   - **Estimated Effort**: As listed in table above
   - **Iteration**: As listed in phases above
4. Close the side panel

### Step 6: Verify Setup

1. Switch between different views
2. Verify all issues appear correctly
3. Check that grouping and sorting work
4. Confirm roadmap view shows timeline

---

## Best Practices

### Issue Management

**Create Issues**:
- Use descriptive titles
- Add detailed description
- Set all custom fields
- Add labels
- Link related issues

**Update Progress**:
- Update status regularly
- Add comments for major updates
- Link pull requests
- Update estimates if needed

**Close Issues**:
- Verify acceptance criteria met
- Link to merged PRs
- Add final comments
- Mark as Done

### Sprint Planning

**Before Sprint**:
- Review and estimate all issues
- Assign issues to iteration
- Set priorities
- Assign team members

**During Sprint**:
- Daily status updates
- Move issues through workflow
- Update estimates if needed
- Communicate blockers

**After Sprint**:
- Sprint review/demo
- Retrospective
- Update velocity metrics
- Plan next sprint

### Communication

**Stand-ups**:
- Use "v1.0.0 Sprint" view
- Review In Progress items
- Identify blockers
- Update statuses

**Planning**:
- Use "By Version" view
- Review upcoming work
- Estimate new issues
- Assign priorities

**Stakeholder Updates**:
- Use "Roadmap" view
- Show timeline progress
- Highlight milestones
- Report metrics

---

## Troubleshooting

### Issue Not Appearing in View

**Problem**: Issue is missing from a view  
**Solutions**:
- Check view filters match issue fields
- Verify issue is added to project
- Refresh the page
- Check if issue is archived

### Fields Not Saving

**Problem**: Custom field values don't persist  
**Solutions**:
- Ensure field is created in project settings
- Check permissions (need write access)
- Try refreshing and setting again
- Clear browser cache

### Roadmap Not Showing Issues

**Problem**: Roadmap view is empty  
**Solutions**:
- Verify Iteration field is set on issues
- Check iteration dates are configured
- Ensure date field is set to "Iteration"
- Refresh the view

---

## Additional Resources

- **GitHub Projects Documentation**: https://docs.github.com/en/issues/planning-and-tracking-with-projects
- **Custom Fields Guide**: https://docs.github.com/en/issues/planning-and-tracking-with-projects/understanding-fields
- **Iteration Planning**: https://docs.github.com/en/issues/planning-and-tracking-with-projects/customizing-views-in-your-project/customizing-the-roadmap-layout

---

## Quick Reference

| Action | Location | Steps |
|--------|----------|-------|
| Add custom field | Project Settings → Fields | Click "+ New field" |
| Create view | View dropdown | Click "+ New view" |
| Update issue field | Issue side panel | Click issue, set fields |
| Assign to iteration | Issue side panel | Set Iteration field |
| Group by field | View settings | Configure → Group by |
| Filter view | View toolbar | Click filter icon |

---

**Project Organization Guide**  
**Version**: 1.0  
**Last Updated**: 2025-11-04  
**Repository**: https://github.com/infrastructure-alexson/ldap-infrastructure-suite

