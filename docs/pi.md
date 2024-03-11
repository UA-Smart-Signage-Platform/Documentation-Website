# Requirements

## Inception Phase

## Elaboration Phase


### Functional Requirements
    Content Management:
        Ability to upload, manage and organize content.
        Support for various media formats (images, videos, audio, text).
        Content scheduling for specific times or events.

    Display Management:
        Control over which screens display specific content.
        Grouping of screens.
        Support for remote display management and configuration.

    Integration:
        Integration with external data sources (RSS feeds, social media, APIs) for      dynamic content.
        Compatibility with various screen types.

    User Interface:
        Intuitive user interface for content management.
        Role-based access control for different users (administrators, content managers, etc.).
        Reporting and analytics features to track content performance and screen status. (idk about this one).


### Non-Functional Requirements
	Performance:
    	Fast response times for content uploads and updates.
    	Smooth playback without buffering or lag.
    	Scalability to support a growing number of screens and users.

	Reliability:
    	High availability to ensure screens are always operational.
    	Fault tolerance to handle hardware failures or network issues.
    	Disaster recovery capabilities to recover from system failures (backups).

	Security:
    	User authentication and authorization mechanisms.
    	Encryption of data during transmission and storage.
    	Protection against unauthorized access and tampering of content (jwt + smth).

	Scalability:
    		Ability to scale the system as the number of screens or content volume increases.

	Usability:
    	Support for multiple languages (pt + en?).
    	Responsive design for user interfaces across different devices (maybe).

	Compatibility:
    	Compatibility with various operating systems and web browsers (raspi by construction should be always the same, react should be universal).
    	Compliance with industry standards and protocols (HTML5 + RESTful APIs).

## Personas