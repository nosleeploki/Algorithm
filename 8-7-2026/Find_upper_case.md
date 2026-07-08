1. You need to create a program that finds all uppercase letters in a specific piece of text. However, there's a key point to note. The program must not only find the uppercase letters but also determine their initial positions within the text. These positions must be represented as a comma-separated string of indices. If no uppercase letters are found, the program must print the constant value "None". The player must reverse-engineer the code to find both the initial uppercase letters and their positions (starting from 0) in the input text, or determine that no such letters exist.

`Java`

            Scanner sc = new Scanner(System.in);
            String s = "SAvsodavA"; //sc.nextLine();
            StringBuilder r = new StringBuilder();

        for (int i = 0; i < s.length(); i++)
            if (Character.isUpperCase(s.charAt(i)))
                r.append(r.length() > 0 ? "," : "").append(i);

        System.out.print(r.length() > 0 ? r : "None");

`JavaScript`

        const fs = require("fs"); //import File System

        const s = fs.readFileSync(0, "utf8").trimEnd(); //Read input and save s
                                                        // .trimEnd() for delete break line at the end of String

        let result = []; //empty arr


        for (let i = 0; i < s.length; i++) {
        // Find Upper case and push into result
            if (s[i] >= "A" && s[i] <= "Z") {
                result.push(i);
            }
        }

        console.log(result.length ? result.join(",") : "None");
