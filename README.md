# GHOST EC2 PI 🧠💨

A self-protecting EC2 instance that escapes when root access is detected, leaving behind a trail of Pi triplets as breadcrumb identifiers.

## 🔥 Concept

Inspired by Person of Interest, Fringe aesthetics. When root access is detected from an unauthorized user, the EC2 instance:

- Snapshots itself
- Terminates the current instance
- Launches a new one in another Availability Zone
- Changes its identity using the next 3 digits of Pi in its hostname
- Logs the event for "hunters" who know what to look for

## 💡 Example hostnames

- `ghost-ec2-pi314-euw1-x8f3`
- `ghost-ec2-pi159-euw2-y9t7`
- `ghost-ec2-pi265-euw3-dz4p`

## 📦 Structure

- `infrastructure/` - Terraform scripts to deploy IAM, EC2, Lambda, etc.
- `lambda/` - Lambda function to handle escape & redeploy
- `instance/` - Scripts to monitor access to root and trigger Lambda
- `utils/` - Pi logic, helpers
- `dashboard/` - (Optional) Flask app to visualize fugitive trails

## 🚀 Roadmap

- [ ] Deploy EC2 with minimal permissions
- [ ] Script access monitor
- [ ] Lambda for migration
- [ ] Pi-based naming
- [ ] Dashboard (bonus)

## 📜 License

MIT
