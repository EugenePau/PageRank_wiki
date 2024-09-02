# PageRank Mini-Project

## Overview

This mini-project implements a simplified version of the PageRank algorithm. It consists of three main scripts:

1. **`spider.py`**: Parses the desired webpage and stores the data in a SQLite database (`cat.sqlite`).
2. **`sprank.py`**: Implements the PageRank algorithm to rank the pages, updating the rankings in the SQLite database.
3. **`spdump.py`**: Outputs the new rankings of every link stored in the database.

This example parses the wikipedia page of 'Cat'.

## Project Structure

```
pagerank-mini-project/
├── spider.py
├── sprank.py
├── spdump.py
└── cat.sqlite
```

## Requirements

- Python 3.x
- SQLite
- Requests library (`pip install requests`)
- BeautifulSoup library (`pip install beautifulsoup4`)

## Usage

### Step 1: Parse the Webpage

Run `spider.py` to parse a webpage and store the links and their content in `cat.sqlite`.

```bash
python spider.py <URL>
```

Replace `<URL>` with the desired webpage URL.

### Step 2: Calculate PageRank

After parsing, run `sprank.py` to calculate the PageRank of the pages stored in `cat.sqlite`.

```bash
python sprank.py
```

### Step 3: Output Rankings

Finally, run `spdump.py` to output the new rankings of all the links stored in the database.

```bash
python spdump.py
```

## Database Structure

The `cat.sqlite` database contains the following tables:

- **pages**: Stores the URLs and their content.
- **rankings**: Stores the PageRank values associated with each URL.

## Example Commands

1. To parse a webpage:
   ```bash
   python spider.py https://example.com
   ```

2. To calculate PageRank:
   ```bash
   python sprank.py
   ```

3. To dump the rankings:
   ```bash
   python spdump.py
   ```

## Notes

- Ensure that you have permission to crawl the webpages you target.
- This is a simplified implementation for educational purposes and may not handle all edge cases found in real-world applications.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.