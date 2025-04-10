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

<!-- Success Modal -->
<div id="successModal" class="fixed inset-0 bg-black/80 z-50 hidden flex items-center justify-center p-4">
    <div class="bg-[#1e1e1e] rounded-xl max-w-md w-full modal-content relative">
        <!-- Close Button -->
        <button onclick="hideSuccessModal()" class="absolute top-4 right-4 text-gray-400 hover:text-white">
            <i class="bi bi-x-lg"></i>
        </button>
        <div class="p-6 text-center">
            <h2 class="text-2xl font-bold mb-4 text-primary">Resume Downloaded!</h2>
            <p id="successMessage" class="text-gray-300 mb-6">
                Your resume has been successfully downloaded. Thank you for your interest!
            </p>
            <button onclick="hideSuccessModal()" class="bg-primary hover:bg-orange-600 text-white py-2 px-6 rounded-md font-medium transition-all">
                Close
            </button>
        </div>
    </div>
</div>

<script>
function handleResumeDownload() {
    const resumeType = document.getElementById('resume-type').value;

    if (!resumeType) {
        alert('Please select a resume type');
        return;
    }

    let resumeUrl = '';
    let successMessage = '';
    switch (resumeType) {
        case 'blue-team':
            resumeUrl = 'assets/Resume/Glan Loyan Dsouza - Blue Teaming(Defensive Security).pdf';
            successMessage = 'Your Blue Teaming resume is being downloaded!';
            break;
        case 'red-team':
            resumeUrl = 'assets/Resume/Glan Loyan Dsouza - Red Teaming(Offensive Security).pdf';
            successMessage = 'Your Red Teaming resume is being downloaded!';
            break;
        case 'purple-team':
            resumeUrl = 'assets/Resume/Glan Loyan Dsouza - Purple Teaming.pdf';
            successMessage = 'Your Purple Teaming resume is being downloaded!';
            break;
        default:
            alert('Invalid selection');
            return;
    }

    // Show the success modal with a custom message
    showSuccessModal(successMessage);

    // Trigger the download after a short delay
    setTimeout(() => {
        const link = document.createElement('a');
        link.href = resumeUrl;
        link.download = resumeUrl.split('/').pop(); // Extract the file name from the URL
        document.body.appendChild(link);
        link.click();
        document.body.removeChild(link);
    }, 1000); // Delay to allow the modal to appear

    hideResumeModal(); // Close the first modal
}

function showSuccessModal(message) {
    console.log('Showing success modal with message:', message);
    const successModal = document.getElementById('successModal');
    const successMessage = document.getElementById('successMessage');
    successMessage.textContent = message; // Set the custom message
    successModal.classList.remove('hidden'); // Show the modal
    document.body.style.overflow = 'hidden'; // Disable body scroll
}

function hideSuccessModal() {
    const successModal = document.getElementById('successModal');
    successModal.classList.add('hidden');
    document.body.style.overflow = 'auto'; // Re-enable body scroll
}
</script>

<style>
.hidden {
    display: none;
}
</style>

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