```csharp
namespace MyBio
{
  class Bio
  {
    private string name, country, email, website;
    private string[] skills, interests;

    public Bio()
    {
      this.name = "João Gustavo";
      this.country = "Brazil";
      this.email = "jgbispo20@gmail.com";
      this.website = "https://bispolink.vercel.app/";
      this.skills = new string[] { "Node.js", "CSharp", "C++", "Java" };
      this.interests = new string[] { "Game Development", "Back-end Development" };
    }

    public void PrintBio()
    {
      Console.WriteLine("Name: " + name);
      Console.WriteLine("Country: " + country);
      Console.WriteLine("Email: " + email);
      Console.WriteLine("Website: " + website);

      Console.WriteLine("Skills: ");
      foreach (string skill in skills)
      {
        Console.WriteLine(" - " + skill);
      }
      Console.WriteLine("Interests: ");
      foreach (string interest in interests)
      {
        Console.WriteLine(interest);
      }
    }
  }
}
```