```php
<?php

class DeveloperProfile {
    // Developer properties
    public $name;
    public $bio;
    public $education;
    public $stack;
    public $currentProject;
    public $socialLinks;
    public $learning; // New property for topics i'm currently learning
    #TODO: Create work
    #TODO: Get a job

    public function __construct() {
        $this->name = "Miguel Alejandro";
        $this->bio = "Passionate programmer with a love for problems and backend development.\n
	I enjoy building projects from scratch, breaking my head over challenges,\n
	and I never want to stop learning.";

        $this->education = "I have an advanced degree in Web Development, and I'm currently\n
	pursuing a master's specialization in AI and Big Data.";

        $this->stack = [
            "Backend"  => ["Laravel", "Node.js", "MySQL", "SQLite"],
            "Frontend" => ["React", "TailwindCSS"]
        ];

        $this->currentProject = ["Queater" => "https://queater.com/"];
        $this->socialLinks = [
            "LinkedIn" => "https://www.linkedin.com/in/miguel-alejandro-santiesteban-aguiar/",
            "X"        => "https://x.com/MiguelAguiarDev"
        ];

        $this->learning = []; // Initialize as empty array
    }

    // Method to add new learning topics
    public function addKnowledge($topic) {
        if (!in_array($topic, $this->learning)) {
            $this->learning[] = $topic;
        }
    }
}

$profile = new DeveloperProfile();
$profile->addKnowledge("Algorithms and Data Structures");

?>

```
