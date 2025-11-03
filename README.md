# Hi there 👋, I'm Harshi
**Data Scientist | ML Engineer | Edtech Builder**

💻 I work on ML, MLOps, and NLP  
📚 Currently building an SAT/ACT edtech platform  
🌱 Exploring transformers, RAG, and chatbot systems  

---

## 🚀 Languages & Tools
![Python](https://img.shields.io/badge/Python-3776AB?logo=python&logoColor=white)
![AWS](https://img.shields.io/badge/AWS-FF9900?logo=amazon-aws&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?logo=docker&logoColor=white)

---

## 📊 GitHub Stats
![Your GitHub stats](https://github-readme-stats.vercel.app/api?username=HarshiPaliwal&show_icons=true&theme=tokyonight)
![Top Languages](https://github-readme-stats.vercel.app/api/top-langs/?username=HarshiPaliwal&layout=compact&theme=tokyonight)

---

## 📫 Connect with me
[LinkedIn](https://linkedin.com/in/YOUR-LINK) • [Twitter](https://twitter.com/YOUR-LINK) • [Portfolio](YOUR-SITE)
# harshika-paliwal
0:00 Hello. In this video series, we're going to walk through how to parameterize your SQL statements in Omni with templated filters and parameters.
0:07 Omni allows for parametrization of SQL using the Mustache template engine. This can be used in both views and fields. Templated filters are going to allow users to inherit SQL conditions from the front end filters directly in their SQL in Omni.
0:22 And parameters can allow you to inject raw values into your SQL from either filter values, user attributes, or if something is in query or in a filter.
0:32 Use cases we're going to cover in the following videos are going to be how to parameterize your WHERE clause within a SQL statement, how to create dynamic timeframe selectors, dynamic conversion rates, how to also apply user attributes to mask underlying dimension values, or even dynamically swap field
0:48 values in those dimensions as well. Before we dive into those use cases, let's cover what is the difference between templative filters and filters dynamically inject text into a SQL query, often a dimension or a fact table.
1:03 They have an opening and closing statement. So the opening statement is going to be a double curly bracket with a pound sign.
1:09 And the closing statement is going to be a double curly bracket with a back sign. In between these, these curly brackets, you'll reference the filter like this, the viewName, filterFieldName, and filter. And in between each of those opening and closing statements, that's where you'll reference the lookup
1:23 value, the viewName.fieldName. In practice, this looks something more like this, where we're going to have a viewName, filterName, and then filter, the dimension or column we're referencing or looking up, and then the same thing in the closing statement.
1:45 no value set in the filter, this would not be injected into the WHERE clause, but if you did want to include a default value, you can add a second template, uhm, right here, but instead of the pound sign in the first statement, it is a caret, and that's where you'll be able to inject the actual SQL, 
2:02 SQL statement that you want to inject within that WHERE clause. Now, parameters inject exact values into SQL queries to, or determine if a field is in a query or a filter, often in dimensions or fact tables, just like templated filters.
2:20 Unlike templated filters, though, it is going to be just one statement wrapped in curly brackets that look like this. This is very similar to Jinja or Liquid if you're familiar with those.
2:32 So there's going to be a couple of ways we can inject values into SQL statements and examples are injecting just a straight value from a field or filter where we say filters dot field name dot value.
2:44 We can leverage time frames and take the range start or range end. So if we were doing a between filter, we can actually grab the start date and the end date for that between filter.
2:57 Um, we can also create Booleans for if something is within a query. So if I have selected a field, in the query, we can actually create a Boolean for that, or if it was filtered.
3:10 And then the last one is a user attribute. So a value for a user attribute. Maybe something along the lines of, can this user see PII?
3:19 Um, and if they can, they would get a name for it. If they couldn't, they would be a mask of that name field or something along those lines.
3:28 So, in the following videos, we're going to cover how we can use templated filters and parameters. Looking forward to it.
