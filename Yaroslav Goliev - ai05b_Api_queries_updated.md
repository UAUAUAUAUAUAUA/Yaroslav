 Task 1: Build 3 USGS Earthquake Queries

Create three different earthquake queries. Each should use **different parameters** to answer a specific question.

**Ideas for queries:**
- All earthquakes above magnitude 7.0 in the past year
- Earthquakes in a specific geographic region (pick coordinates)
- Recent small earthquakes (magnitude 2.0-3.0)
- Earthquakes sorted by time vs. magnitude
- Earthquakes from a specific date range

1st - https://earthquake.usgs.gov/fdsnws/event/1/query?format=geojson&minmagnitude=5.0&limit=10&starttime=2026-01-01
2nd - https://earthquake.usgs.gov/fdsnws/event/1/query?format=geojson&orderby=magnitude&limit=15
3rd- https://earthquake.usgs.gov/fdsnws/event/1/query?format=geojson&starttime=2026-02-01&endtime=2026-02-05&minlatitude=44&maxlatitude=47&minlongitude=32&maxlongitude=37

**Requirements:**
- Use `format=geojson` (makes it readable)
- Each query must use at least 3 different parameters
- Document what each query is looking for

---

### Task 2: Build 3 Open Library Queries

Create two different book search queries.

1st - https://openlibrary.org/search.json?author=taras+shevchenko&language=ukr
2nd - https://openlibrary.org/search.json?q=artificial+intelligence&limit=3

**Ideas for queries:**
- Books about a specific topic (space, cooking, Python, etc.)
- Books by your favorite author
- Books in a specific genre with year filter
- Search limited to specific fields
- Compare results for different search terms

**Requirements:**
- Each query must use at least 2 different parameters
- Document what you're searching for

---

## Part 5: Testing Your Queries

### How to Test:

1. **Copy your URL** (the entire thing!)
2. **Open a new browser tab**
3. **Paste the URL** into the address bar
4. **Press Enter**
5. **Verify you see JSON data** (looks like nested brackets and key-value pairs)

### What Your Responses Should Look Like (sample only):

**✅ Good response (USGS):**
```json
{
  "type": "FeatureCollection",
  "metadata": {
    "generated": 1738363200000,
    "count": 5
  },
  "features": [
    {
      "type": "Feature",
      "properties": {
        "mag": 5.2,
        "place": "Pacific Ocean",
        ...
```

**✅ Good response (Open Library):**
```json
{
  "numFound": 234,
  "docs": [
    {
      "title": "Learning Python",
      "author_name": ["Mark Lutz"],
      ...
```

**❌ Error response:**
```json
{
  "error": "invalid parameter"
}
```

If you get an error:
- Check your spelling
- Verify parameter names match documentation
- Make sure values are in the correct format
- Check for typos in the base URL

---
## Submission Instructions

1. **Submit** your markdown file: `api_queries.md`to AI / ML repository and share link in Google Classroom.
2. **Test all URLs** - make sure your queries work in your browser!

## Resources

- **USGS Full Documentation:** https://earthquake.usgs.gov/fdsnws/event/1/
- **Open Library API Docs:** https://openlibrary.org/dev/docs/api/search


