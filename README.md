<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>نموذج اختبار تجميعات أنظمة التشغيل (133 سؤال)</title>
  <style>
    :root {
      --bg: #f3f0f8;
      --card: #ffffff;
      --primary: #5b21b6;
      --primary-hover: #4c1d95;
      --primary-soft: #ede9fe;
      --text: #1f2937;
      --muted: #6b7280;
      --border: #e5e7eb;
      --success-bg: #ecfdf5;
      --success-border: #10b981;
      --success-text: #065f46;
      --error-bg: #fef2f2;
      --error-border: #ef4444;
      --error-text: #991b1b;
    }

    * { box-sizing: border-box; }

    body {
      margin: 0;
      font-family: system-ui, -apple-system, "Segoe UI", Tahoma, Arial, sans-serif;
      background: var(--bg);
      color: var(--text);
      line-height: 1.6;
    }

    .container {
      max-width: 860px;
      margin: 0 auto;
      padding: 20px 14px 64px;
    }

    .banner-card {
      background: var(--card);
      border-radius: 14px;
      border-top: 10px solid var(--primary);
      box-shadow: 0 2px 10px rgba(0, 0, 0, 0.06);
      padding: 22px;
      margin-bottom: 16px;
    }

    .banner-card h1 {
      margin: 0 0 8px;
      font-size: 1.5rem;
      color: var(--text);
    }

    .banner-card p {
      margin: 0;
      color: var(--muted);
      font-size: 0.95rem;
    }

    .controls-card {
      background: var(--card);
      border-radius: 12px;
      box-shadow: 0 2px 8px rgba(0, 0, 0, 0.05);
      padding: 16px;
      margin-bottom: 18px;
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(190px, 1fr));
      gap: 12px;
      align-items: end;
    }

    .field label {
      display: block;
      font-size: 0.85rem;
      font-weight: 700;
      margin-bottom: 6px;
      color: var(--text);
    }

    .field select {
      width: 100%;
      padding: 9px 10px;
      border-radius: 8px;
      border: 1px solid var(--border);
      background: #fff;
      color: var(--text);
      font-size: 0.9rem;
    }

    .stats-bar {
      background: var(--card);
      border-radius: 12px;
      padding: 12px 16px;
      margin-bottom: 18px;
      box-shadow: 0 2px 8px rgba(0, 0, 0, 0.05);
      display: flex;
      flex-wrap: wrap;
      justify-content: space-between;
      align-items: center;
      gap: 10px;
      font-size: 0.9rem;
      position: sticky;
      top: 8px;
      z-index: 20;
    }

    .stat-pill {
      background: var(--primary-soft);
      color: var(--primary);
      font-weight: 700;
      padding: 4px 10px;
      border-radius: 999px;
      font-size: 0.84rem;
    }

    .btn {
      border: none;
      border-radius: 8px;
      padding: 10px 16px;
      font-size: 0.92rem;
      font-weight: 700;
      cursor: pointer;
      transition: 0.15s ease;
    }

    .btn-primary {
      background: var(--primary);
      color: #fff;
    }

    .btn-primary:hover {
      background: var(--primary-hover);
    }

    .btn-secondary {
      background: #f3f4f6;
      color: var(--text);
      border: 1px solid #d1d5db;
    }

    .btn-secondary:hover {
      background: #e5e7eb;
    }

    .question-card {
      background: var(--card);
      border-radius: 12px;
      padding: 20px;
      margin-bottom: 14px;
      box-shadow: 0 2px 8px rgba(0, 0, 0, 0.05);
      border: 1px solid transparent;
    }

    .question-card.is-correct {
      border-color: var(--success-border);
      background: #fcfffe;
    }

    .question-card.is-wrong {
      border-color: var(--error-border);
      background: #fffdfd;
    }

    .q-header {
      display: flex;
      justify-content: space-between;
      align-items: center;
      gap: 8px;
      margin-bottom: 10px;
      font-size: 0.82rem;
      color: var(--muted);
    }

    .q-badge {
      background: #f3f4f6;
      padding: 2px 8px;
      border-radius: 6px;
      font-weight: 600;
    }

    .q-text {
      direction: ltr;
      text-align: left;
      font-size: 1.02rem;
      font-weight: 600;
      margin-bottom: 14px;
      white-space: pre-line;
      color: #111827;
    }

    .options-list {
      display: flex;
      flex-direction: column;
      gap: 8px;
    }

    .option-item {
      direction: ltr;
      text-align: left;
      display: flex;
      align-items: flex-start;
      gap: 10px;
      padding: 10px 12px;
      border: 1px solid var(--border);
      border-radius: 8px;
      cursor: pointer;
      transition: 0.12s ease;
      background: #fff;
    }

    .option-item:hover {
      border-color: var(--primary);
      background: #faf5ff;
    }

    .option-item input {
      margin-top: 3px;
      accent-color: var(--primary);
      width: 16px;
      height: 16px;
      flex-shrink: 0;
    }

    .option-item.correct-opt {
      background: var(--success-bg);
      border-color: var(--success-border);
      color: var(--success-text);
      font-weight: 600;
    }

    .option-item.wrong-opt {
      background: var(--error-bg);
      border-color: var(--error-border);
      color: var(--error-text);
    }

    .feedback-line {
      margin-top: 10px;
      font-size: 0.88rem;
      font-weight: 700;
    }

    .feedback-ok { color: var(--success-text); }
    .feedback-bad { color: var(--error-text); }

    .result-card {
      background: var(--card);
      border-radius: 14px;
      padding: 22px;
      margin-bottom: 18px;
      box-shadow: 0 3px 12px rgba(0, 0, 0, 0.08);
      border: 2px solid var(--primary);
      display: none;
    }

    .filter-row {
      display: flex;
      flex-wrap: wrap;
      gap: 8px;
      margin-top: 14px;
    }

    .footer-actions {
      display: flex;
      flex-wrap: wrap;
      gap: 10px;
      justify-content: space-between;
      align-items: center;
      margin-top: 20px;
    }
  </style>
</head>
<body>
  <div class="container">
    <div class="banner-card">
      <h1>تجميعات أنظمة التشغيل (Linux)</h1>
      <p>نموذج اختبار تفاعلي يضم 133 سؤالاً من التجميعات — يدعم التكرار، وتحديد النطاق، والتصحيح الفوري والنهائي.</p>
    </div>

    <div class="controls-card">
      <div class="field">
        <label for="modeSelect">وضع الاختبار</label>
        <select id="modeSelect">
          <option value="instant">تدريب فوري (إظهار النتيجة بعد كل سؤال)</option>
          <option value="exam">اختبار نهائي (تصحيح بعد التسليم)</option>
        </select>
      </div>

      <div class="field">
        <label for="rangeSelect">نطاق الأسئلة</label>
        <select id="rangeSelect">
          <option value="all">جميع الأسئلة (1 - 133)</option>
          <option value="1-45">الأسئلة (1 - 45)</option>
          <option value="46-90">الأسئلة (46 - 90)</option>
          <option value="91-133">الأسئلة (91 - 133)</option>
        </select>
      </div>

      <div class="field">
        <label for="shuffleSelect">ترتيب الأسئلة</label>
        <select id="shuffleSelect">
          <option value="order">الترتيب الأصلي للتجميعات</option>
          <option value="shuffle">خلط عشوائي للأسئلة</option>
        </select>
      </div>
    </div>

    <div class="stats-bar">
      <div>
        <span class="stat-pill" id="attemptPill">المحاولة #1</span>
        <span class="stat-pill" id="progressPill">تمت الإجابة: 0 / 133</span>
        <span class="stat-pill" id="timerPill">الوقت: 00:00</span>
      </div>
      <div style="display:flex; gap:8px; flex-wrap:wrap;">
        <button class="btn btn-secondary" type="button" id="restartTopBtn">إعادة الاختبار</button>
        <button class="btn btn-primary" type="button" id="submitTopBtn">تسليم النتيجة</button>
      </div>
    </div>

    <div class="result-card" id="resultCard">
      <h2 style="margin:0 0 8px;">نتيجة الاختبار</h2>
      <div id="scoreSummary" style="font-size:1.1rem; font-weight:700;"></div>
      <div class="filter-row">
        <button class="btn btn-secondary" type="button" data-filter="all">عرض الكل</button>
        <button class="btn btn-secondary" type="button" data-filter="wrong">الإجابات الخاطئة فقط</button>
        <button class="btn btn-secondary" type="button" data-filter="correct">الإجابات الصحيحة فقط</button>
      </div>
    </div>

    <div id="questionsContainer"></div>

    <div class="footer-actions">
      <button class="btn btn-secondary" type="button" id="restartBottomBtn">إعادة الاختبار من جديد</button>
      <button class="btn btn-primary" type="button" id="submitBottomBtn">تسليم الاختبار وعرض النتيجة</button>
    </div>
  </div>

  <script>
    const QUESTIONS = [
      { id: 1, page: 1, q: "1) A license where you have access to the source code is called:", opts: ["A. Open source", "B. Closed source", "C. Beta source", "D. None of the above"], ans: ["A. Open source"], multi: 1 },
      { id: 2, page: 1, q: "2) Alias create shortcuts to longer commands", opts: ["True", "False"], ans: ["True"], multi: 1 },
      { id: 3, page: 1, q: "3) Any software update could be minor or major", opts: ["True", "False"], ans: ["True"], multi: 1 },
      { id: 4, page: 1, q: "4) Open source licenses differ, but generally agree that: (choose two)", opts: ["You must redistribute your changes", "You should be able modify the software as you wish", "You should have access to the source code of software", "You are not allowed to sell the software"], ans: ["You should be able modify the software as you wish", "You should have access to the source code of software"], multi: 2 },
      { id: 5, page: 1, q: "5) Linux is the central controller", opts: ["True", "False"], ans: ["False"], multi: 1 },
      { id: 6, page: 1, q: "6) Either software or operating systems had some updates", opts: ["True", "False"], ans: ["True"], multi: 1 },
      { id: 7, page: 2, q: "7) After the beta period, the software is promoted to stable", opts: ["True", "False"], ans: ["True"], multi: 1 },
      { id: 8, page: 2, q: "8) UNIX was originally invented at:", opts: ["AT&T Bell Labs", "Bangalore University", "Stanford University", "Berkeley University"], ans: ["AT&T Bell Labs"], multi: 1 },
      { id: 9, page: 2, q: "9) Linux is the kernel", opts: ["True", "False"], ans: ["True"], multi: 1 },
      { id: 10, page: 2, q: "10) Backward compatibility means it still works with older versions", opts: ["True", "False"], ans: ["True"], multi: 1 },
      { id: 11, page: 2, q: "11) Source code refers to:", opts: ["A human readable version of computer software", "The interface that software uses to talk to the kernel", "The version of a program that the computer runs on the CPU", "The license that dictates how you may use and share the software"], ans: ["A human readable version of computer software"], multi: 1 },
      { id: 12, page: 2, q: "12) In writing commands, Arguments change the behavior of the command", opts: ["False", "True"], ans: ["False"], multi: 1 },
      { id: 13, page: 3, q: "13) Linux translates source-to-machine code", opts: ["False", "True"], ans: ["False"], multi: 1 },
      { id: 14, page: 3, q: "14) Unix is (choose two)", opts: ["A text editor", "A trademark", "An operating system", "A type of hardware"], ans: ["A trademark", "An operating system"], multi: 2 },
      { id: 15, page: 3, q: "15) A longer maintenance cycle means you will be supported at current software levels longer, needing less frequent upgrades.", opts: ["True", "False"], ans: ["True"], multi: 1 },
      { id: 16, page: 3, q: "16) Globbing characters is used to match sets of files in a directory", opts: ["True", "False"], ans: ["True"], multi: 1 },
      { id: 17, page: 3, q: "17) Linux is not Unix because:", opts: ["It hasn't undergone certification", "It's free", "There are too many distributions", "It's not made by the Open Group"], ans: ["It hasn't undergone certification"], multi: 1 },
      { id: 18, page: 4, q: "18) To execute the same command as previously executed five commands ago, you would type:", opts: ["!-5", "!5", "@-5", "&5"], ans: ["!-5"], multi: 1 },
      { id: 19, page: 4, q: "19) The main purpose of using glob characters is to be able to provide a command a list of filenames. True or False?", opts: ["True", "False"], ans: ["True"], multi: 1 },
      { id: 20, page: 4, q: "20) What one character treats the character that follows it as if it was surrounded by single quotes?", opts: ["%", "/", "\\", "#"], ans: ["\\"], multi: 1 },
      { id: 21, page: 4, q: "21) Select all the applications that provide access to the Command Line Interface (CLI)? (choose two)", opts: ["Terminal window", "firefox", "opera", "Virtual Terminal"], ans: ["Terminal window", "Virtual Terminal"], multi: 2 },
      { id: 22, page: 4, q: "22) Linux is written in:", opts: ["C", "C++", "Java", "Perl"], ans: ["C"], multi: 1 },
      { id: 23, page: 5, q: "23) Which distributions are made by or clones of Red Hat? (choose two)", opts: ["Debian", "Fedora", "CentOS", "Slackware"], ans: ["Fedora", "CentOS"], multi: 2 },
      { id: 24, page: 5, q: "24) A pair of single quotes (') will prevent the shell from interpreting any metacharacter. True or False?", opts: ["True", "False"], ans: ["True"], multi: 1 },
      { id: 25, page: 5, q: "25) To start searching a man page, the first key you press is:", opts: ["f", "S", "!", "/"], ans: ["/"], multi: 1 },
      { id: 26, page: 5, q: "26) Which of the following are glob characters? (choose three)", opts: ["The question mark \"?\"", "The square brackets \"[\" and \"]\"", "The asterisk \"*\"", "The dash character \"-\""], ans: ["The question mark \"?\"", "The square brackets \"[\" and \"]\"", "The asterisk \"*\""], multi: 3 },
      { id: 27, page: 5, q: "27) One of the jobs of the kernel is to:", opts: ["Load the operating system after the computer is turned on.", "Manage the system's resources.", "Transfer mail from one machine to another.", "Turn source code into machine code."], ans: ["Manage the system's resources."], multi: 1 },
      { id: 28, page: 6, q: "28) Open source means: (choose two)", opts: ["You can modify the software's source code.", "You must share your changes.", "You can view the software's source code.", "You must support the software you share."], ans: ["You can modify the software's source code.", "You can view the software's source code."], multi: 2 },
      { id: 29, page: 6, q: "29) A license where you don't have access to the source code is called:", opts: ["Closed source", "Impaired source.", "Sourceless.", "Open source."], ans: ["Closed source"], multi: 1 },
      { id: 30, page: 6, q: "30) Apple's OS X is: (choose two)", opts: ["Able to natively run Windows binaries.", "Only compatible with Apple hardware.", "Certified as UNIX compatible.", "Derived from Linux"], ans: ["Only compatible with Apple hardware.", "Certified as UNIX compatible."], multi: 2 },
      { id: 31, page: 6, q: "31) The double ampersand characters (&&) are used to separate commands to be executed conditionally, where if the command to the left of the ampersands fails, then the command to the right of the ampersands will be executed.", opts: ["True", "False"], ans: ["False"], multi: 1 },
      { id: 32, page: 6, q: "32) Ubuntu is derived from which distribution?", opts: ["Debian", "Slackware", "Fedora", "Red Hat Enterprise Linux"], ans: ["Debian"], multi: 1 },
      { id: 33, page: 7, q: "33) Software is backward compatible if :", opts: ["It still supports old file formats or applications", "People still use old versions.", "It can be upgraded without downtime.", "It works across Linux/Mac/Windows."], ans: ["It still supports old file formats or applications"], multi: 1 },
      { id: 34, page: 7, q: "34) The ____ command will print a list of the commands that you've previously executed.", opts: ["History", "exec", "eval", "list"], ans: ["History"], multi: 1 },
      { id: 35, page: 7, q: "35) The acronym CLI stands for:", opts: ["Computer Line Interface", "Command Line Interpreter", "Command Line Interface", "Computer Link Interpreter"], ans: ["Command Line Interface"], multi: 1 },
      { id: 36, page: 7, q: "36) The shell program interprets the commands you type into the terminal, into instructions that the Linux operating system can execute. True or False?", opts: ["True", "False"], ans: ["True"], multi: 1 },
      { id: 37, page: 7, q: "37) Select the command that can report the location of a command:", opts: ["Which", "where", "what"], ans: ["Which"], multi: 1 },
      { id: 38, page: 8, q: "38) Which environment variable contains a list of directories that is searched for commands to execute?", opts: ["PATH", "EXEC", "PS2", "SP1"], ans: ["PATH"], multi: 1 },
      { id: 39, page: 8, q: "39) In order to search an info page, the first key to press is (choose one)", opts: ["S", "/", "t", "f"], ans: ["/"], multi: 1 },
      { id: 40, page: 8, q: "40) The statement that describes the difference between a man page and an info page is:", opts: ["The info page is like a guide; a man page is a more concise reference.", "The man page is like a guide; the info page is a more concise reference.", "There is very little difference between them.", "The man page is a long detailed reference; the info page is very terse."], ans: ["The info page is like a guide; a man page is a more concise reference."], multi: 1 },
      { id: 41, page: 8, q: "41) To get help while using the info command, press:", opts: ["G", "h", "Z", "a"], ans: ["h"], multi: 1 },
      { id: 42, page: 9, q: "42) What is the standard option to provide a command line program to view its documentation?", opts: ["-h", "--info", "--doc", "--help"], ans: ["--help"], multi: 1 },
      { id: 43, page: 9, q: "43) In order to exit viewing a man page, press:", opts: ["Y", "Z", "q", "X"], ans: ["q"], multi: 1 },
      { id: 44, page: 9, q: "44) To search the man page sections for the keyword example, which of the following command lines could you execute? (choose two)", opts: ["man -f example", "man -k example", "whatis example", "apropos example"], ans: ["man -k example", "apropos example"], multi: 2 },
      { id: 45, page: 9, q: "45) The whatis command is the same as man -w.", opts: ["True", "False"], ans: ["False"], multi: 1 },
      { id: 46, page: 10, q: "46) Commands typically executed by a user are covered in what section of the manual?", opts: ["1", "2", "3", "5"], ans: ["1"], multi: 1 },
      { id: 47, page: 10, q: "47) The following sections commonly appear on a man page (choose three)", opts: ["LICENSE", "SYNOPSIS", "NAME", "DESCRIPTION"], ans: ["SYNOPSIS", "NAME", "DESCRIPTION"], multi: 3 },
      { id: 48, page: 10, q: "48) The command man -k is the same as the command apropos.", opts: ["True", "False"], ans: ["True"], multi: 1 },
      { id: 49, page: 10, q: "49) If you are reading the synopsis of a command from a man page, then items in square brackets are:", opts: ["Optional", "Required arguments", "Comments", "Required options"], ans: ["Optional"], multi: 1 },
      { id: 50, page: 10, q: "50) To get help on using the info command, execute (choose two)", opts: ["Info -q", "info info", "man info", "help info"], ans: ["info info", "man info"], multi: 2 },
      { id: 51, page: 11, q: "51) The directory where additional documentation for software packages most likely can be found is:", opts: ["/usr/share/doc", "/var/lib/doc", "/var/share/doc", "/usr/software/doc"], ans: ["/usr/share/doc"], multi: 1 },
      { id: 52, page: 11, q: "52) The tilde (~) is used to represent:", opts: ["A user's home directory", "Nothing; it has no special meaning.", "The directory above the current working directory.", "Any two single characters."], ans: ["A user's home directory"], multi: 1 },
      { id: 53, page: 11, q: "53) Hidden files are files that begin with what character?", opts: ["A period (.)", "A plus (+).", "An asterisk (*)", "A dash (-)"], ans: ["A period (.)"], multi: 1 },
      { id: 54, page: 11, q: "54) The cd command by itself will take you to what directory?", opts: ["Your home directory", "The system root directory.", "None; it is not a valid command.", "The directory above the current working directory."], ans: ["Your home directory"], multi: 1 },
      { id: 55, page: 11, q: "55) The ls command color codes results by default. True or False?", opts: ["True", "False"], ans: ["False"], multi: 1 },
      { id: 56, page: 12, q: "56) The command rm -r will...", opts: ["remove a directory along with any files or subdirectories", "prompt for each confirmation before deleting each file in a directory.", "generate an error; -r isn't a valid option.", "remove only empty directories."], ans: ["remove a directory along with any files or subdirectories"], multi: 1 },
      { id: 57, page: 12, q: "57) The rm command can delete multiple files at once. True or False?", opts: ["True", "False"], ans: ["True"], multi: 1 },
      { id: 58, page: 12, q: "58) The double dot (..) can be used with the cd command to represent:", opts: ["The directory above the current working directory", "Nothing; it has no special meaning.", "Any two single characters.", "A user's home directory."], ans: ["The directory above the current working directory"], multi: 1 },
      { id: 59, page: 12, q: "59) The double dot (..) can be used to represent the directory...", opts: ["...above the current directory", "...with any two single numbers.", "...above the current directory only when using the cd command.", "...below the current directory."], ans: ["...above the current directory"], multi: 1 },
      { id: 60, page: 12, q: "60) What command will allow you to change your current working directory?", opts: ["List", "ls", "cd", "chdir"], ans: ["cd"], multi: 1 },
      { id: 61, page: 13, q: "61) The ls command without options or arguments...", opts: ["...lists the contents of the current directory", "...prompts for a directory to list.", "...generates an error as this command requires arguments.", "...lists the contents of a user's home directory."], ans: ["...lists the contents of the current directory"], multi: 1 },
      { id: 62, page: 13, q: "62) The top-level directory on a Linux system is represented as:", opts: ["/root", "/home", ":", "/"], ans: ["/"], multi: 1 },
      { id: 63, page: 13, q: "63) The command ls -S will sort files:", opts: ["By size, largest to smallest", "By size, smallest to largest.", "By modification date, newest to oldest.", "By number of symlinks, largest to smallest."], ans: ["By size, largest to smallest"], multi: 1 },
      { id: 64, page: 13, q: "64) The find command can search for files based on the size of the file.", opts: ["True", "False"], ans: ["True"], multi: 1 },
      { id: 65, page: 13, q: "65) Which option for the cut command is used to specify a delimiter?", opts: ["-d", "-D", "-f", "#"], ans: ["-d"], multi: 1 },
      { id: 66, page: 14, q: "66) The command echo \"text\" > file.txt will create file.txt if it does not already exist?", opts: ["True", "False"], ans: ["True"], multi: 1 },
      { id: 67, page: 14, q: "67) Which option for the cut command is used to specify the field?", opts: ["-D", "-d", "-f", "#"], ans: ["-f"], multi: 1 },
      { id: 68, page: 14, q: "68) Which of the following commands scans the file to determine file locations?", opts: ["Where", "find", "search", "locate"], ans: ["find"], multi: 1 },
      { id: 69, page: 14, q: "69) The command echo \"text\" > file.txt will not overwrite file.txt if it already exists?", opts: ["True", "False"], ans: ["False"], multi: 1 },
      { id: 70, page: 14, q: "70) Which of the following commands can be used to scroll through a text file? (choose two)", opts: ["Less", "More", "Cat", "Some"], ans: ["Less", "More"], multi: 2 },
      { id: 71, page: 15, q: "71) A pipe allows you to...", opts: ["...send the output of one command to another", "...type multiple commands at one prompt.", "...send the same input to multiple commands.", "...send the output of a command to a file."], ans: ["...send the output of one command to another"], multi: 1 },
      { id: 72, page: 15, q: "72) Which command(s) can be used to sort the lines of list.file alphabetically and display it on the screen? (choose two)", opts: ["cat list.file | sort", "sort < list.file", "echo list.file > sort", "cat list.file >> sort"], ans: ["cat list.file | sort", "sort < list.file"], multi: 2 },
      { id: 73, page: 15, q: "73) A successful command will print output to STDOUT?", opts: ["True", "False"], ans: ["True"], multi: 1 },
      { id: 74, page: 15, q: "74) Error messages generated by commands are sent where by default?", opts: ["STDERR", "STDIN", "Log files", "STDOUT"], ans: ["STDERR"], multi: 1 },
      { id: 75, page: 15, q: "75) Which of the following commands will append its output to output.file?", opts: ["echo Testing >> output.file.", "echo Testing > output.file.", "output.file < echo Testing.", "echo Testing 1> output.file."], ans: ["echo Testing >> output.file."], multi: 1 },
      { id: 76, page: 16, q: "76) What is the correct way to assign the word \"Hello\" to a variable?", opts: ["A=\"Hello\"", "echo $A \"Hello\"", "$A=\"Hello\"", "echo \"Hello\" > A"], ans: ["A=\"Hello\""], multi: 1 },
      { id: 77, page: 16, q: "77) Which shell command accepts input from the user's keyboard?", opts: ["read", "echo", "gets", "input"], ans: ["read"], multi: 1 },
      { id: 78, page: 16, q: "78) The if command looks for what exit code to consider a condition to be true?", opts: ["0", "10", "255", "1"], ans: ["0"], multi: 1 },
      { id: 79, page: 16, q: "79) Which are appropriate editors for writing shell scripts?", opts: ["vi", "LibreOffice Writer", "/bin/bash", "Firefox"], ans: ["vi"], multi: 1 },
      { id: 80, page: 16, q: "80) A file begins with #!/bin/csh. This means:", opts: ["Running the script will invoke /bin/csh to interpret the rest of the file", "The operator should not be using /bin/csh", "Nothing, this is a comment", "C Shell compatibility mode is enabled"], ans: ["Running the script will invoke /bin/csh to interpret the rest of the file"], multi: 1 },
      { id: 81, page: 17, q: "81) What is the correct way to save the current directory to a variable?", opts: ["A=`pwd`", "pwd $A", "$A=$cwd", "pwd | $A"], ans: ["A=`pwd`"], multi: 1 },
      { id: 82, page: 17, q: "82) What information is held inside $? ?", opts: ["The previous command's exit code", "The name of the command run", "The current user ID", "The current process id"], ans: ["The previous command's exit code"], multi: 1 },
      { id: 83, page: 17, q: "83) A conditional that lets you make multiple comparisons with a pattern is called:", opts: ["case", "if", "branch", "test"], ans: ["case"], multi: 1 },
      { id: 84, page: 17, q: "84) Which user can view the /etc/shadow file?", opts: ["The root user", "All users", "No user"], ans: ["The root user"], multi: 1 },
      { id: 85, page: 17, q: "85) The /etc/shadow file contains plain-text passwords.", opts: ["True", "False"], ans: ["False"], multi: 1 },
      { id: 86, page: 18, q: "86) Which of the following commands will display how long the system has been running since the last boot?", opts: ["id", "uptime", "who", "what"], ans: ["uptime"], multi: 1 },
      { id: 87, page: 18, q: "87) Each user belongs to at least one group", opts: ["True", "False"], ans: ["True"], multi: 1 },
      { id: 88, page: 18, q: "88) Which of the following commands will display the groups that the user bob belongs to?", opts: ["all bob", "group bob", "id bob", "groups -a"], ans: ["id bob"], multi: 1 },
      { id: 89, page: 18, q: "89) Which command would allow a user to execute commands as root?", opts: ["grep", "sudo", "about", "who"], ans: ["sudo"], multi: 1 },
      { id: 90, page: 18, q: "90) A GID is associated with a group name.", opts: ["True", "False"], ans: ["True"], multi: 1 },
      { id: 91, page: 19, q: "91) Which command will display the users that are currently logged in to the system?", opts: ["Whoami", "Id", "About", "Who"], ans: ["Who"], multi: 1 },
      { id: 92, page: 19, q: "92) Sudo privileges can be used to specify which user can use the sudo command to execute commands as other users.", opts: ["True", "False"], ans: ["True"], multi: 1 },
      { id: 93, page: 19, q: "93) Which of the following options for the useradd command allows root to specify the UID to be associated with the account?", opts: ["-G", "-g", "-u", "-M"], ans: ["-u"], multi: 1 },
      { id: 94, page: 19, q: "94) Which command can be used to determine a user's most recent log in?", opts: ["Shell", "History", "Last", "login"], ans: ["Last"], multi: 1 },
      { id: 95, page: 19, q: "95) For non-root users, the passwd command can only be used to change the password of the user running the command.", opts: ["True", "False"], ans: ["True"], multi: 1 },
      { id: 96, page: 20, q: "96) If a user is deleted, the files and directories that the user owned...", opts: ["will have no user owner", "will have no UID owner.", "are deleted as well.", "will show a UID as the owner, but not user name"], ans: ["will show a UID as the owner, but not user name"], multi: 1 },
      { id: 97, page: 20, q: "97) Which of the following commands set \"other\" permissions on file to r-x?", opts: ["chmod o=r+x file", "chmod o=rx file", "chmod o-r-w file", "chmod o+rx file"], ans: ["chmod o=rx file"], multi: 1 },
      { id: 98, page: 20, q: "98) Which of the following commands sets \"other\" permissions on file to r-x?", opts: ["chmod 777 file", "chmod 776 file", "chmod 775 file", "chmod 774 file"], ans: ["chmod 775 file"], multi: 1 },
      { id: 99, page: 20, q: "99) The groupmod command can be used to add users to a group.", opts: ["True", "False"], ans: ["False"], multi: 1 },
      { id: 100, page: 20, q: "100) The user sysadmin will be able to change the permissions of a file because they own it.", opts: ["True", "False"], ans: ["True"], multi: 1 },
      { id: 101, page: 21, q: "101) The chown command can be used to change the owner and group of a file.", opts: ["True", "False"], ans: ["True"], multi: 1 },
      { id: 102, page: 21, q: "102) The chgrp command can be used on a file by:", opts: ["A user that belongs to the files current group", "Only root", "The file owner and root", "Only the file owner"], ans: ["The file owner and root"], multi: 1 },
      { id: 103, page: 21, q: "103) The chgrp command can be used to change the owner and group of a file?", opts: ["True", "False"], ans: ["False"], multi: 1 },
      { id: 104, page: 21, q: "104) Only one set (user, group, other) of permission can be changed at once using the symbolic method.", opts: ["True", "False"], ans: ["False"], multi: 1 },
      { id: 105, page: 21, q: "105) The groupmod command can be used to change a group name.", opts: ["True", "False"], ans: ["True"], multi: 1 },
      { id: 106, page: 21, q: "106) The groupmod command can be used to change a group GID.", opts: ["True", "False"], ans: ["True"], multi: 1 },
      { id: 107, page: 22, q: "107) UIDs 1-499 are usually reserved for what kind of users?", opts: ["Are not used for user accounts, but for group accounts", "Remote log-in accounts", "System accounts, such as server processes", "Log-in (human) users"], ans: ["System accounts, such as server processes"], multi: 1 },
      { id: 108, page: 22, q: "108) Which of the following commands can be used to modify a group?", opts: ["modgroup", "groupadd", "addgroup", "groupmod"], ans: ["groupmod"], multi: 1 },
      { id: 109, page: 22, q: "109) Which of the following options for the useradd command allows the root to specify supplementary groups the user will be a member of.", opts: ["-u", "-G", "-U", "-g"], ans: ["-G"], multi: 1 },
      { id: 110, page: 22, q: "110) Which of the following permissions would allow all users to add, view, and delete files in a directory?", opts: ["777", "750", "775", "666"], ans: ["777"], multi: 1 },
      { id: 111, page: 22, q: "111) The user sysadmin will be able to read the file because they own it. ---r--r-- 1 sysadmin group 38270 Sep 2 18:49 file True or False?", opts: ["True", "False"], ans: ["False"], multi: 1 },
      { id: 112, page: 23, q: "112) Octal notation uses the following values for the permissions granted:", opts: ["r=4, w=2, x=1", "r=7, w=5, x=0", "r=3, w=2, x=1", "r=4, w=2, x=0"], ans: ["r=4, w=2, x=1"], multi: 1 },
      { id: 113, page: 23, q: "113) A user cannot delete a file if they do not own it. True or False?", opts: ["True", "False"], ans: ["False"], multi: 1 },
      { id: 114, page: 23, q: "114) The \"execute\" permission on a directory allows you to: (choose three)", opts: ["Change to that directory or use it as part of a path", "Along with write permission to successfully delete the directory", "Along with read permission to successfully perform ls -l", "Along with write permission to successfully create new files"], ans: ["Change to that directory or use it as part of a path", "Along with read permission to successfully perform ls -l", "Along with write permission to successfully create new files"], multi: 3 },
      { id: 115, page: 23, q: "115) The \"execute\" permission on a file allows you to:", opts: ["Run the file as a script", "This permission isn't meaningful for text files.", "Delete the file", "Move the file to a new directory"], ans: ["Run the file as a script"], multi: 1 },
      { id: 116, page: 23, q: "116) The chown command can be used to change the user owner on a file by:", opts: ["Only root", "A user that belongs to the files current group", "The file owner and root", "The file owner"], ans: ["Only root"], multi: 1 },
      { id: 117, page: 24, q: "117) The chmod command can be used on a file by:", opts: ["The file owner and root", "Only root", "A user that belongs to the files current group", "The file owner"], ans: ["The file owner and root"], multi: 1 },
      { id: 118, page: 24, q: "118) Which option for the chown command can be used to change the owner of a directory and all the files and directories below it?", opts: ["-r", "-R", "-f", "-a"], ans: ["-R"], multi: 1 },
      { id: 119, page: 24, q: "119) The chown command will only accept one file at a time as an argument?", opts: ["True", "False"], ans: ["False"], multi: 1 },
      { id: 120, page: 24, q: "120) The \"execute\" permission is never set on files by default. True or False?", opts: ["True", "False"], ans: ["True"], multi: 1 },
      { id: 121, page: 24, q: "121) The user owner of a file will always have the same or higher permissions as \"other\". True or False?", opts: ["True", "False"], ans: ["False"], multi: 1 },
      { id: 122, page: 25, q: "122) UIDs 1-500 are usually reserved for what kind of users?", opts: ["System accounts, such as server processes", "Are not used for user accounts, but for group accounts", "Log-in (human) users", "Remote log-in accounts"], ans: ["System accounts, such as server processes"], multi: 1 },
      { id: 123, page: 25, q: "123) On a system that does not use UPG, the useradd command will also create a user group. For example, user bob, group bob. True or False?", opts: ["True", "False"], ans: ["False"], multi: 1 },
      { id: 124, page: 25, q: "124) The useradd command will create a home directory by default for a user.?", opts: ["True", "False"], ans: ["False"], multi: 1 },
      { id: 125, page: 25, q: "125) The usermod command can be used to do all of the following except...", opts: ["...add a user to a supplementary group.", "...change the user's MAX and MIN password settings.", "...change the user's home directory.", "...change the user's UID and GID."], ans: ["...change the user's MAX and MIN password settings."], multi: 1 },
      { id: 126, page: 25, q: "126) Which of the following commands will add the group extra to the user bob's secondary groups in addition to bob's current secondary groups?", opts: ["usermod -G extra bob", "usermod -a extra bob", "usermod -aG extra bob", "usermod -ag bob extra"], ans: ["usermod -aG extra bob"], multi: 1 },
      { id: 127, page: 26, q: "127) Which option for the usermod command can be used to specify a user's group ID (either primary or secondary)? (choose two)", opts: ["-g", "-G", "-s", "-S"], ans: ["-g", "-G"], multi: 2 },
      { id: 128, page: 26, q: "128) The userdel command will...", opts: ["...delete the user account, but leave the user's files by default.", "...will prompt before deleting each file owned by a user.", "...automatically delete a user and the user's home directory and its contents.", "...automatically delete a user and all the files owned by that user."], ans: ["...delete the user account, but leave the user's files by default."], multi: 1 },
      { id: 129, page: 26, q: "129) Which of the following files contains encrypted user password information?", opts: ["/etc/usr", "/etc/shadow", "/etc/passwd", "/etc/group"], ans: ["/etc/shadow"], multi: 1 },
      { id: 130, page: 26, q: "130) Which of the following files contains user IDs?", opts: ["/etc/group", "/etc/shadow", "/etc/usr", "/etc/passwd"], ans: ["/etc/passwd"], multi: 1 },
      { id: 131, page: 27, q: "131) Which of the following files does the groupadd command use to determine the new GID when a GID isn't specified?", opts: ["/etc/shadow", "/etc/group", "/etc/passwd", "/etc/usr"], ans: ["/etc/group"], multi: 1 },
      { id: 132, page: 27, q: "132) Which of the following commands, run as root, will prevent the user bob from logging in?", opts: ["usermod -d bob", "usermod -l bob", "usermod -D bob", "usermod -L bob"], ans: ["usermod -L bob"], multi: 1 },
      { id: 133, page: 27, q: "133) What directory contains user's home directories?", opts: ["/", "/home", "/rootfs", "/user"], ans: ["/home"], multi: 1 }
    ];

    let activeQuestions = [];
    let userAnswers = {};
    let attemptNumber = 1;
    let secondsElapsed = 0;
    let isSubmitted = false;
    let currentFilter = "all";

    const container = document.getElementById("questionsContainer");
    const modeSelect = document.getElementById("modeSelect");
    const rangeSelect = document.getElementById("rangeSelect");
    const shuffleSelect = document.getElementById("shuffleSelect");
    const attemptPill = document.getElementById("attemptPill");
    const progressPill = document.getElementById("progressPill");
    const timerPill = document.getElementById("timerPill");
    const resultCard = document.getElementById("resultCard");
    const scoreSummary = document.getElementById("scoreSummary");

    setInterval(() => {
      if (!isSubmitted) {
        secondsElapsed++;
        const mins = String(Math.floor(secondsElapsed / 60)).padStart(2, "0");
        const secs = String(secondsElapsed % 60).padStart(2, "0");
        timerPill.textContent = `الوقت: ${mins}:${secs}`;
      }
    }, 1000);

    function getFilteredList() {
      let list = [...QUESTIONS];
      const rangeVal = rangeSelect.value;
      if (rangeVal !== "all") {
        const [start, end] = rangeVal.split("-").map(Number);
        list = list.filter(item => item.id >= start && item.id <= end);
      }
      if (shuffleSelect.value === "shuffle") {
        for (let i = list.length - 1; i > 0; i--) {
          const j = Math.floor(Math.random() * (i + 1));
          [list[i], list[j]] = [list[j], list[i]];
        }
      }
      return list;
    }

    function isQuestionCorrect(qObj) {
      const chosen = userAnswers[qObj.id] || [];
      if (chosen.length !== qObj.ans.length) return false;
      return qObj.ans.every(a => chosen.includes(a)) && chosen.every(c => qObj.ans.includes(c));
    }

    function getMultiLabel(count) {
      if (count === 2) return "اختيار متعدد (اختر إجابتين)";
      if (count === 3) return "اختيار متعدد (اختر 3 إجابات)";
      return "اختيار من متعدد";
    }

    function renderQuestions() {
      container.innerHTML = "";
      activeQuestions.forEach((qObj, idx) => {
        const chosen = userAnswers[qObj.id] || [];
        const hasAnswered = chosen.length > 0;
        const showEval = modeSelect.value === "instant" ? hasAnswered : isSubmitted;
        const correct = isQuestionCorrect(qObj);

        if (isSubmitted && currentFilter === "wrong" && correct) return;
        if (isSubmitted && currentFilter === "correct" && !correct) return;

        const card = document.createElement("div");
        card.className = "question-card";
        if (showEval) {
          card.classList.add(correct ? "is-correct" : "is-wrong");
        }

        const header = document.createElement("div");
        header.className = "q-header";
        header.innerHTML = `
          <span>بطاقة #${idx + 1} • صفحة ${qObj.page}</span>
          <span class="q-badge">${getMultiLabel(qObj.multi)}</span>
        `;
        card.appendChild(header);

        const qText = document.createElement("div");
        qText.className = "q-text";
        qText.textContent = qObj.q;
        card.appendChild(qText);

        const optList = document.createElement("div");
        optList.className = "options-list";

        qObj.opts.forEach(opt => {
          const label = document.createElement("label");
          label.className = "option-item";

          const isChecked = chosen.includes(opt);
          const isRightAnswer = qObj.ans.includes(opt);

          if (showEval) {
            if (isRightAnswer) label.classList.add("correct-opt");
            else if (isChecked && !isRightAnswer) label.classList.add("wrong-opt");
          }

          const input = document.createElement("input");
          input.type = qObj.multi > 1 ? "checkbox" : "radio";
          input.name = `q_${qObj.id}`;
          input.value = opt;
          input.checked = isChecked;

          input.addEventListener("change", () => {
            if (qObj.multi > 1) {
              let curr = [...(userAnswers[qObj.id] || [])];
              if (input.checked) {
                if (!curr.includes(opt)) curr.push(opt);
              } else {
                curr = curr.filter(x => x !== opt);
              }
              userAnswers[qObj.id] = curr;
            } else {
              userAnswers[qObj.id] = [opt];
            }
            updateStats();
            if (modeSelect.value === "instant" || isSubmitted) {
              renderQuestions();
            }
          });

          const span = document.createElement("span");
          span.textContent = opt;

          label.appendChild(input);
          label.appendChild(span);
          optList.appendChild(label);
        });

        card.appendChild(optList);

        if (showEval) {
          const fb = document.createElement("div");
          fb.className = `feedback-line ${correct ? "feedback-ok" : "feedback-bad"}`;
          fb.textContent = correct
            ? "✓ إجابة صحيحة"
            : `✗ إجابة غير مكتملة أو خاطئة — الإجابة المعتمدة: ${qObj.ans.join(" ، ")}`;
          card.appendChild(fb);
        }

        container.appendChild(card);
      });
    }

    function updateStats() {
      const answeredCount = activeQuestions.filter(q => (userAnswers[q.id] || []).length > 0).length;
      progressPill.textContent = `تمت الإجابة: ${answeredCount} / ${activeQuestions.length}`;
      attemptPill.textContent = `المحاولة #${attemptNumber}`;
    }

    function startNewAttempt(incrementAttempt) {
      if (incrementAttempt) attemptNumber++;
      userAnswers = {};
      secondsElapsed = 0;
      isSubmitted = false;
      currentFilter = "all";
      resultCard.style.display = "none";
      activeQuestions = getFilteredList();
      updateStats();
      renderQuestions();
      window.scrollTo({ top: 0, behavior: "smooth" });
    }

    function submitExam() {
      isSubmitted = true;
      currentFilter = "all";
      let correctCount = 0;
      activeQuestions.forEach(q => {
        if (isQuestionCorrect(q)) correctCount++;
      });
      const total = activeQuestions.length;
      const pct = total ? Math.round((correctCount / total) * 100) : 0;
      scoreSummary.textContent = `درجتك: ${correctCount} من ${total} (${pct}%)`;
      resultCard.style.display = "block";
      renderQuestions();
      resultCard.scrollIntoView({ behavior: "smooth" });
    }

    document.getElementById("restartTopBtn").addEventListener("click", () => startNewAttempt(true));
    document.getElementById("restartBottomBtn").addEventListener("click", () => startNewAttempt(true));
    document.getElementById("submitTopBtn").addEventListener("click", submitExam);
    document.getElementById("submitBottomBtn").addEventListener("click", submitExam);

    modeSelect.addEventListener("change", renderQuestions);
    rangeSelect.addEventListener("change", () => startNewAttempt(false));
    shuffleSelect.addEventListener("change", () => startNewAttempt(false));

    document.querySelectorAll("[data-filter]").forEach(btn => {
      btn.addEventListener("click", () => {
        currentFilter = btn.getAttribute("data-filter");
        renderQuestions();
      });
    });

    activeQuestions = getFilteredList();
    updateStats();
    renderQuestions();
  </script>
</body>
</html>
