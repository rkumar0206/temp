| Food | Quantity | Quantity Measure | Protein (g) | Energy / Calorie | Carbohydrates (g) | Fats (g) | Sugar (g) | Calcium (mg) | Fiber (g) |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Egg | 1 | pc | 6 | 70-80 | 0.6 | 5 | 0.6 | 28.5 | 0 |
| Poha | 100 | g | 2 | 120 | 24 | 0.1 | 0 | 0 | 0.5 |
| Yogurt | 100 | g | 3.6 | 60 | 5 | 3 | 4.52 | 149.5 | 0 |
| Chicken Biryani | 100 | g | 10 | 200-300 | 35-40 | 15-20 | 0 | 0 | 1 |
| White rice | 100 | g | 2.6 | 130 | 28 | 0.3 | 0 | 10 | 0.4 |
| Milk | 100 | g | 3.4 | 42 | 5 | 1 | 5 | 125 | 0 |
| Butter | 10 | g | 0.1 | 80 | 0 | 9 | 0 | 0 | 0 |
| Whey Protein | 1 | scoop | 24 | Varies | 2 | 1 | 1 | Varies | Varies |
| Banana | 1 | pc | 1.3 | 105 | 27 | 0.4 | 14 | 6 | 3.1 |
| Peanut Butter | 100 | g | 25 | 588 | 20 | 50 | 10 | 50 | 6 |
| Paneer | 100 | g | 18 | 265 | 2.6 | 21 | 2.6 | 481 | 0 |
| Almonds | 7 | pc | 4 | 49 | 2 | 4 | 0.7 | 35 | 1.5 |
| Roasted Channa | 100 | g | 8 | 160-180 | 27-30 | 2-3 | 6-8 | 0 | 7 |



![image](https://github.com/rkumar0206/temp/assets/63965898/80242041-eb01-48c7-9c6c-13269c5a0f18)


import javax.xml.bind.JAXBContext;
import javax.xml.bind.JAXBException;
import javax.xml.bind.Unmarshaller;
import java.io.StringReader;

public class XmlToJavaConverter {
    public static Person convertXmlToJava(String xml) throws JAXBException {
        JAXBContext context = JAXBContext.newInstance(Person.class);
        Unmarshaller unmarshaller = context.createUnmarshaller();
        return (Person) unmarshaller.unmarshal(new StringReader(xml));
    }
}

