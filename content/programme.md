---
title: Programme
order: 3
---

## Programme outline

Date: Tuesday 22nd of Octobre

| Time          | Topic                            |
| ------------- |:--------------------------------:|
| 10 min          | Introduction by the Chair        |
| 20 min          | Opening keynote                  |
| 60 min          | Paper session 1                  |
| 60 min         | Break out Session                  |
| 60 min         | Paper Session 2     |

## Accepted papers
<ul>
<%
  papers = @items.find_all{ |i| i.identifier =~ /^\/papers\/.+/ }
  papers.each do |paper|
%>
<li itemscope itemtype="http://schema.org/ScholarlyArticle">
  <a href='<%= paper.identifier %>paper.pdf' itemprop="name"><%= h paper[:title] %></a>
  <%=
    authors = paper[:author]
    authors.to_a.map{ |a| h "#{a.first} #{a.prefix} #{a.last} #{a.suffix}".strip }.
      map{ |a| "<span itemprop='author'>#{a}</span>" }.
      join(authors.length <= 2 ? ' and ' : ', ').
      sub(/, ([^,]+)$/, ', and \1')
  %>
</li>
<%
  end
%>
</ul>

## Target audience
This workshop is mainly focused on a combined audience of the academic research community, the private institutional research community and the industry. Participants should include researchers in the fields of basic research, applied research or industrial research, and company employees active in research and development, system architecture and valorisation. These parties work in various areas represented in the Semantic Web community such as: artificial intelligence, information retrieval, multimedia, and communication technologies, data mining, data science, human-computer interaction, humanities, and web information systems.
We expect representatives from industry (and user institutions) to share knowledge about their business cases, adoption status, developed use cases, and especially the experienced roadblocks, expectations, views on existing best practices, and requirements with using Semantic Web technology in production environments. From academic participants, we expect to present novel tools for integration in information platforms and innovative approaches that formulate best practices for integration of various Semantic Web technologies/tools within existing infrastructures. The workshop provides an informal setting for researchers and practitioners from different related initiatives to meet and benefit from each other's work and requirements.

## Previous editions of this workshop

[WaSABi 2013 @ ISWC2013](http://2013.wasabi-ws.org)
