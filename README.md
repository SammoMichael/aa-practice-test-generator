# a/A Practice Test Generator

This is a practice test generator to prepare for A01, your first assessment at App Academy. This repo is forked from the Github of Mallory Bulkley, an App Academy alum who created this when she was a student. The purpose of this tool is to allow you to get comfortable with the types of problems that could pop up on an assessment. Note that the purpose is **NOT TO MEMORIZE SOLUTIONS** - the problems included in this generator are _not_ an exhaustive list of what could show up on the assessment. Choosing to memorize solutions without understanding them may get you by in the short-term, but will never be worth it in the long run. Practice thinking and struggling through these problems so that you are agile and prepared for anything come assessment day.

## How to use this repo

1. Clone this repo onto your local machine.

2. Navigate to your local repo directory in terminal and run one of the following generators (detailed in below section):

   - `ruby random_test_generator.rb` - Generates a practice test in a folder called `practice_assessment`
   - `ruby generator.rb` - Generates a test by category, based on how many problems of each category you want in a folder called `category_assessment` (requires following a prompt)

3. Navigate to the directory that was generated from running one of the above commands. Run `bundle exec rspec spec.rb` to test your answers against the spec as you work through `practice_test.rb`.

4. Check your solutions against those in `solutions.rb`.

## Generators

All of the practice problems are listed and categorized in `list.csv`. Categories include: recursion, sorting, enumerable, array, string, and bonus. Bonus problems will not appear on the assessment but are good to practice and can help you gain a deeper understanding of some of the more complex problems, especially with regards to recursion. There are two different generators included in this repo - they are detailed below.

### Practice Assessment Generator

**Command**: `ruby random_test_generator.rb`

Generates a random practice assessment including problems across all categories (except for bonus). Test files will be generated inside of a directory called `practice_assessment`.

- `practice_test.rb` contains the problems to be solved

- `spec.rb` combines the specs for the chosen problems into one file for easy testing

- `solutions.rb` combines the solutions for each problem

### Problems by Category Generator

**Command**: `ruby generator.rb` (must follow prompt after)

Prompts you for your desired number of questions from each category, and uses your input and the CSV file to generate a test of randomly selected practice problems from each category specified. Test files will be generated inside of a directory called `practice_assessment`.

The most problems in any category is 12, so if you would like to generate a file with all of the problems, you can put 12 for each category (duplicates will not be created if there are less than 12 problems in a category).

For both generators, 3 files will be created inside the generated folder as follows:

- `practice_test.rb` contains the problems to be solved

- `spec.rb` combines the specs for the chosen problems into one file for easy testing

- `solutions.rb` combines the solutions for each problem

**Warning**: If you run the generator again, it will re-write the previously generated files and erase your previous work. If you wish to save your previous work, you will need to rename the files. This applies to both generators.
