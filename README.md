import 'package:flutter/material.dart';

class FAQItem {
  final String question;
  final String answer;
  final String image;

  FAQItem({required this.question, required this.answer, required this.image});
}

List<FAQItem> faqList = [
  FAQItem(
  question: "Hamburguesa",
  answer: 'S/.8.99',
  image: "https://s3.abcstatics.com/media/gurmesevilla/2012/01/comida-rapida-casera.jpg"
),
  FAQItem(
  question: "Pizza",
  answer: "S/.10.99",
  image: "https://s3.abcstatics.com/media/gurmesevilla/2012/01/comida-rapida-casera.jpg"
),
  FAQItem(
  question: "Ensalada Cesar",
  answer: "S/.6.99",
  image: "https://s3.abcstatics.com/media/gurmesevilla/2012/01/comida-rapida-casera.jpg"
),
  FAQItem(
  question: "Pasta Alfredo",
  answer: "S/.12.99",
  image: "https://s3.abcstatics.com/media/gurmesevilla/2012/01/comida-rapida-casera.jpg"
),
  FAQItem(
  question: "Sandwich de Pollo",
  answer: "S/.7.99",
  image: "https://s3.abcstatics.com/media/gurmesevilla/2012/01/comida-rapida-casera.jpg"
),
  FAQItem(
  question: "Sopa Del Dia",
  answer: "S/.4.99",
  image: "https://s3.abcstatics.com/media/gurmesevilla/2012/01/comida-rapida-casera.jpg"
),
];

class MyApp extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      title: 'FAQ',
      home: Scaffold(
        appBar: AppBar(
          title: Text('FAQ'),
        ),
        body: ListView.builder(
          itemCount: faqList.length,
          itemBuilder: (context, index) {
            return ExpansionTile(
              title: Text(faqList[index].question),
              children: [
                Padding(
                  padding: EdgeInsets.symmetric(horizontal: 16.0),
                  child: Text(
                    faqList[index].answer,
                    style: TextStyle(fontSize: 16.0),
                  ),
                ),
              ],
            );
          },
        ),
      ),
    );
  }
}
