# What are the Coding Challenges Like?
### Our principles

- Demonstrate applied problem solving
- Reflect real-life software engineering
- Concrete milestones and progression
- No brain-teasers
- No theoretical algorithm questions

Most candidates who have done software engineering professionally, in class, in
 boot-camps or as a hobby should feel comfortable with the code challenges we
 present.

We do not care for abstract algorithm or exotic data structures, and you do not
 need to go through textbooks to prepare for our code challenges.

We focus on applied problem solving and progression. Our questions are
 structured with achievable milestones.

### Sample Question

#### Instruction

```
Build a simple Yelp-like system: Given a set of restaurant and metadata (coordinates, ratings, opening hours), design and implement the following functionalities without using a database.

1. Find restaurants within specified radius, given a coordinate
2. Improve the above function by only returning restaurants that are open given desired dining hour
3. Improve the above function by sorting the results by average ratings
```

#### Skeleton Code

```c++
using namespace std;

struct Restaurant {
  double latitude;
  double longitude;
  int id;
  string name;
  int open_hour;   /* in [0-23] */
  int close_hour;  /* in [0-23] */

  Restaurant(...) { ... }  /* Omitted */
};

struct Rating {
  int id;
  int rating;      /* in [1-5] */

  Rating(...) { ... }      /* Omitted */
};

class Yelp {
 public:
  Yelp(vector<Restaurant> restaurants, vector<Rating> ratings) : restaurants_(restaurants), ratings_(ratings) { }
  ~Yelp() { }

  /*
   * Returns list of Restaurant within radius.
   *
   *  latitude: double
   *  longitude: double
   *  radius: kilometer in int
   *  dining_hour: If null, find any restaurant in radius.
   *               Otherwise return list of open restaurants at specified hour.
   *  sort_by_rating: If true, sort result in descending order,
   *                  highest rated first.
   */
  vector<Restaurant> find(double latitude, double longitude, int radius,
      int dining_hour, boolean sort_by_rating) {
    cout << "please implement" << endl;
    vector<Restaurant> output;
    return output;
  }

 private:
  vector<Restaurant> restaurants_;
  vector<Rating> ratings_;
};

int main(int argc, char* argv[]) {
  vector<Restaurant> restaurants = ...;  /* Omitted */
  vector<Rating> ratings = ...;          /* Omitted */

  Yelp y = Yelp(restaurants, ratings);
  y.find(-37.7, -122.6, 5, null, false);
}
```

If you still feel a bit rusty, no worries. Here are some pointers to help you brush up:

- [Elements of Programming Interviews: The Insiders' Guide](http://www.amazon.com/Elements-Programming-Interviews-Insiders-Guide/dp/1479274836/)
- [Cracking the Coding Interview](http://www.amazon.com/Cracking-Coding-Interview-Programming-Questions/dp/098478280X/)

Feel free to [reach out to us](support@oneinterview.io) if you have questions or concerns.