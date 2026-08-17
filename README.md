# My-CV-Tools

## Description

My-CV-Tools is a simple Bash and GitHub Actions exercise. It demonstrates basic Git workflow, feature branches, CI/CD, version tagging, and release management.

## Project Structure

```text
My-CV-Tools/
├── cv.sh
└── .github/
    └── workflows/
        └── ci-cd.yml
```

## Bash Script

The `cv.sh` script prints basic CV information: name, address, experience, and education.

Run it with:

```bash
chmod +x cv.sh
./cv.sh
```

## Branching Workflow

Main branches:
- `dev` - development
- `uat` - testing / user acceptance
- `main` - final stable version

Feature branches:
- `feature/tambah-alamat`
- `feature/tambah-pengalaman`
- `feature/tambah-pendidikan`

The features are developed and merged into `dev` sequentially.

## CI/CD

GitHub Actions is used instead of GitLab CI/CD. The workflow is stored in `.github/workflows/ci-cd.yml`.

It contains three jobs:
1. **Test** - prints the test process.
2. **Build** - prints the build process.
3. **Deploy** - prints the deploy process.

The jobs run sequentially:

```text
Test → Build → Deploy
```

## Version and Release

After the completed project is merged through `dev` and `uat` into `main`, the initial project version is tagged:

```text
v1.0.0
```

A GitHub Release is then created for team and business documentation.

## Feature Change Types

- `feature/tambah-alamat` - minor change
- `feature/tambah-pengalaman` - major change
- `feature/tambah-pendidikan` - patch change

## Exercise Flow

```text
Feature Branch
      ↓
     dev
      ↓
     uat
      ↓
    main
      ↓
   v1.0.0
      ↓
GitHub Release
```
