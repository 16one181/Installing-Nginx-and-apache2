---
- name: Install and Configure Apache2
  hosts: K-m
  become: yes
  tasks:
    - name: Update apt cache
      apt:
        update_cache: yes
      when: ansible_os_family == "Debian"

    - name: Install Apache2
      apt:
        name: apache2
        state: present

    - name: Start and enable Apache2
      service:
        name: apache2
        state: started
        enabled: yes

    - name: Configure Apache2 default page
      copy:
        content: |
          <html>
            <head>
              <title>Apache2 Server</title>
            </head>
            <body>
              <h1>Welcome to Apache2 Server</h1>
              <p>This server is managed by Shashank</p>
            </body>
          </html>
        dest: /var/www/html/index.html
- name: Install and Configure Nginx
  hosts: K-s
  become: yes
  tasks:
    - name: Update apt cache
      apt:
        update_cache: yes
      when: ansible_os_family == "Debian"

    - name: Install Nginx
      apt:
        name: nginx
        state: present

    - name: Start and enable Nginx
      service:
        name: nginx
        state: started
        enabled: yes

    - name: Configure Nginx default page
      copy:
        content: |
          <html>
            <head>
              <title>Nginx Server</title>
            </head>
            <body>
              <h1>Welcome to Nginx</h1>
              <p>This server is managed by Shashank</p>
            </body>
          </html>
        dest: /var/www/html/index.html
