# RealSec Labs - Cybersecurity Solutions

RealSec Labs is a modern cybersecurity solutions platform designed to provide cutting-edge tools, services, and resources to protect digital assets and infrastructure. This project showcases a responsive website with features like a tools section, blog, contact form, and resume download functionality.

---

## Features

- **Responsive Design**: Fully responsive layout optimized for all devices.
- **Interactive Navbar**: Smooth scrolling and mobile-friendly navigation.
- **Hero Section**: Highlights the mission and vision of RealSec Labs.
- **Tools Section**: Showcases cybersecurity tools like Intruscan and IAM Real.
- **Open Source Projects**: Dynamically fetches and displays GitHub repositories.
- **Blog Section**: Displays the latest articles on cybersecurity trends and techniques.
- **Contact Form**: Allows users to send inquiries with validation.
- **Resume Modal**: HRs can download resumes for different domains (Blue Teaming, Red Teaming, Purple Teaming).

<div class="relative mb-6">
    <label for="resume-type" class="block text-sm font-medium mb-2 text-gray-300">Domain Hiring For</label>
    <div class="relative">
        <select id="resume-type" class="w-full bg-[#232323] border border-gray-700 rounded-md py-3 px-4 text-gray-300 focus:outline-none focus:ring-2 focus:ring-primary appearance-none">
            <option value="" disabled selected>Select a domain</option>
            <option value="blue-team">Blue Teaming (Defensive Security)</option>
            <option value="red-team">Red Teaming (Offensive Security)</option>
            <option value="purple-team">Purple Teaming (Offensive + Defensive Security)</option>
        </select>
        <!-- Custom Dropdown Arrow -->
        <div class="absolute inset-y-0 right-0 flex items-center pr-3 pointer-events-none">
            <i class="bi bi-chevron-down text-gray-400"></i>
        </div>
    </div>
</div>

---

## Technologies Used

- **HTML5**: For semantic structure.
- **CSS3**: For styling and animations.
- **Tailwind CSS**: For utility-first styling.
- **JavaScript**: For interactivity and dynamic content.
- **Bootstrap Icons**: For icons.
- **GitHub API**: To fetch and display repositories dynamically.

---

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/realsec-labs.git