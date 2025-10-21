# TikTok Web Scraper

A Python-based web scraper for extracting data from TikTok profiles, videos, and hashtags.

## Description

This tool allows you to scrape public TikTok data including user profiles, video metadata, comments, and hashtag information. Built with Python, it provides an easy-to-use interface for gathering TikTok data for analysis, research, or content monitoring purposes.

## Features

- Scrape user profile information
- Extract video metadata (likes, comments, shares, views)
- Collect comments from videos
- Search and scrape hashtag content
- Export data to CSV/JSON formats
- Rate limiting to respect platform guidelines

## Installation

1. Clone the repository:
```bash
git clone https://github.com/themiyakasun/tiktok-webscrapper.git
cd tiktok-webscrapper
```

2. Create a virtual environment (recommended):
```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

3. Install required dependencies:
```bash
pip install -r requirements.txt
```

## Dependencies

- Python 3.8+
- requests
- beautifulsoup4
- selenium
- pandas
- python-dotenv

## Usage

### Basic Example

```python
from tiktok_scraper import TikTokScraper

# Initialize the scraper
scraper = TikTokScraper()

# Scrape a user profile
user_data = scraper.get_user_profile('username')

# Scrape videos from a hashtag
videos = scraper.get_hashtag_videos('trending', limit=50)

# Export data
scraper.export_to_csv(videos, 'output.csv')
```

### Command Line Usage

```bash
# Scrape user profile
python scraper.py --user username --output user_data.json

# Scrape hashtag
python scraper.py --hashtag trending --limit 100 --output trending.csv
```

## Configuration

Create a `.env` file in the root directory:

```
RATE_LIMIT=10
TIMEOUT=30
OUTPUT_FORMAT=json
```

## Legal and Ethical Considerations

⚠️ **Important**: This tool is for educational purposes only. Please ensure you:
- Comply with TikTok's Terms of Service
- Respect user privacy and data protection laws (GDPR, CCPA, etc.)
- Only scrape publicly available data
- Implement appropriate rate limiting
- Use scraped data responsibly and ethically

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Disclaimer

This tool is provided as-is for educational and research purposes. The authors are not responsible for any misuse or violations of TikTok's terms of service. Users are solely responsible for ensuring their use complies with all applicable laws and platform policies.

## Contact

Project Link: [https://github.com/themiyakasun/tiktok-webscrapper](https://github.com/themiyakasun/tiktok-webscrapper)

## Acknowledgments

- Thanks to the open-source community
- Inspired by various web scraping projects
